### Reference
1. [中文官網-簡單的應用程式狀態管理](https://flutter.cn/docs/development/data-and-backend/state-mgmt/simple)
2. [第一個 state 管理 - Provider 的使用與深入](https://www.writershelf.com/article/%E7%AC%AC%E4%B8%80%E5%80%8B-state-%E7%AE%A1%E7%90%86-provider-%E7%9A%84%E4%BD%BF%E7%94%A8%E8%88%87%E6%B7%B1%E5%85%A5?locale=zh-TW&prne=roa)
3. [Day22 Flutter 的狀態管理 Provider (一)](https://ithelp.ithome.com.tw/articles/10250504)
---
### Provider概念
1. Provider是繼承自InheritedWidget
2. InheritedWidget目的是為了將資源傳下去
3. InheritedWidget在使用上有缺陷
4. InheritedWiget結合StatefulWidget與ChangeNotifier結合後成為Provider
5. Provider使用方式分為

> 1. Consumer
> 2. Provider.of(context)

---
### 實作
- [ChatGPT製作Todo-Provider](https://chat.openai.com/share/b3dd5006-141d-415a-a56a-ce2bde3a76ab)

#### 實作程式碼
```dart linenums="1"
//main.dart
import 'package:flutter/material.dart';
import 'package:provider/provider.dart';
import 'todo_provider.dart';
import 'todo_model.dart';
import 'todo_listview.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return ChangeNotifierProvider(
      create: (context) => TodoProvider(),
      child: const MaterialApp(
        title: 'Todo List',
        home: TodoListPage(),
        debugShowCheckedModeBanner: false,
      ),
    );
  }
}

class TodoListPage extends StatefulWidget {
  const TodoListPage({super.key});

  @override
  State<TodoListPage> createState() => _TodoListPageState();
}

class _TodoListPageState extends State<TodoListPage> {
  int _currentIndex = 0;

  @override
  Widget build(BuildContext context) {
    return DefaultTabController(
      length: 2,
      child: Scaffold(
        appBar: AppBar(
          title: Text('Todo List'),
          bottom: TabBar(
            onTap: (index) {
              setState(() {
                _currentIndex = index;
              });
            },
            tabs: const [
              Tab(icon: Icon(Icons.list), text: 'Todos'),
              Tab(icon: Icon(Icons.done_all), text: 'Completed'),
            ],
          ),
        ),
        body: TabBarView(
          children: [
            TodoListView(false),
            TodoListView(true),
          ],
        ),
        floatingActionButton: _currentIndex == 0
            ? FloatingActionButton(
                onPressed: () => _showAddTodoDialog(context),
                child: Icon(Icons.add),
              )
            : null,
      ),
    );
  }

  void _showAddTodoDialog(BuildContext context) {
    showDialog(
      context: context,
      builder: (context) {
        String title = '';
        return AlertDialog(
          title: const Text('Add Todo'),
          content: TextField(
            onChanged: (value) => title = value,
            decoration: const InputDecoration(hintText: 'Todo title'),
          ),
          actions: [
            ElevatedButton(
              onPressed: () {
                if (title.isNotEmpty) {
                  Provider.of<TodoProvider>(context, listen: false)
                      .addTodo(Todo(title: title));
                }
                Navigator.of(context).pop();
              },
              child: Text('Add'),
            ),
          ],
        );
      },
    );
  }
}
```

```dart linenums="1"
//todo_model.dart
class Todo {
  String title;
  bool isDone;

  Todo({required this.title, this.isDone = false});

  Map<String, dynamic> toJson() => {
        'title': title,
        'isDone': isDone,
      };

  static Todo fromJson(Map<String, dynamic> json) => Todo(
        title: json['title'],
        isDone: json['isDone'],
      );
}
```

```dart linenums="1"
//todo_provider.dart
import 'package:flutter/material.dart';
import 'todo_model.dart';
import 'package:shared_preferences/shared_preferences.dart';
import 'dart:convert';

class TodoProvider extends ChangeNotifier {
  List<Todo> _todos = [];

  TodoProvider() {
    loadTodos();
  }

  List<Todo> get todos => _todos;
  List<Todo> get completedTodos => _todos.where((todo) => todo.isDone).toList();

  void addTodo(Todo todo) {
    _todos.add(todo);
    saveTodos();
    notifyListeners();
  }

  void toggleTodoStatus(Todo todo) {
    todo.isDone = !todo.isDone;
    saveTodos();
    notifyListeners();
  }

  void saveTodos() async {
    final prefs = await SharedPreferences.getInstance();
    final String encodedData = json.encode(
      _todos.map((todo) => todo.toJson()).toList(),
    );
    await prefs.setString('todos', encodedData);
  }

  void loadTodos() async {
    final prefs = await SharedPreferences.getInstance();
    final String? encodedData = prefs.getString('todos');
    if (encodedData != null) {
      final List<dynamic> decodedData = json.decode(encodedData);
      _todos = decodedData.map((item) => Todo.fromJson(item)).toList();
      notifyListeners();
    }
  }
}

```

```dart linenums="1"
//todo_listview.dart
import 'package:flutter/material.dart';
import 'package:provider/provider.dart';
import 'todo_provider.dart';

class TodoListView extends StatelessWidget {
  final bool showCompleted;

  TodoListView(this.showCompleted);

  @override
  Widget build(BuildContext context) {
    final provider = Provider.of<TodoProvider>(context);
    final todos = showCompleted
        ? provider.completedTodos
        : provider.todos.where((todo) => !todo.isDone).toList();

    return ListView.builder(
      itemCount: todos.length,
      itemBuilder: (context, index) {
        final todo = todos[index];
        return ListTile(
          title: Text(todo.title),
          leading: Checkbox(
            value: todo.isDone,
            onChanged: (_) {
              provider.toggleTodoStatus(todo);
            },
          ),
        );
      },
    );
  }
}
```