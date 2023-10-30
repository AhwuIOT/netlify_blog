# 改編以下Dart Code to Flutter
```Dart linenums="1"
void main(){
  printProgress(callback: (int progress){
    print('列印進度: $progress%');
  });
}
void printProgress({Function(int)? callback}){
	for(int progress = 0; progress <= 10; progress ++){
	  if(callback != null){
		callback(progress);
	  }
	}
}
```

## 第一種（不利用動畫Package只使用StatefulWidget）

![[Kapture 2023-10-18 at 16.05.05.gif]]
### Flutter Code(用按鍵按)
```Dart linenums="1"
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Progress Button',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: ProgressButton(),
    );
  }
}

class ProgressButton extends StatefulWidget {
  @override
  _ProgressButtonState createState() => _ProgressButtonState();
}

class _ProgressButtonState extends State<ProgressButton> {
  int progress = 0;

  void updateProgress() {
    setState(() {
      progress += 10;
      if (progress > 100) {
        progress = 0;
      }
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Progress Button'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text(
              '進度: $progress%',
              style: TextStyle(fontSize: 24),
            ),
            SizedBox(height: 20),
            ElevatedButton(
              onPressed: updateProgress,
              child: Text('更新進度'),
            ),
          ],
        ),
      ),
    );
  }
}
```

### Flutter Code(不用按鍵)
```Dart linenums="1"
import 'package:flutter/material.dart';
import 'dart:async';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Progress Button',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: ProgressButton(),
    );
  }
}

class ProgressButton extends StatefulWidget {
  @override
  _ProgressButtonState createState() => _ProgressButtonState();
}

class _ProgressButtonState extends State<ProgressButton> {
  int progress = 0;
  Timer? timer;

  @override
  void initState() {
    super.initState();
    startTimer();
  }

  @override
  void dispose() {
    timer?.cancel();
    super.dispose();
  }

  void startTimer() {
    timer = Timer.periodic(Duration(seconds: 10), (timer) {
      setState(() {
        progress += 10;
        if (progress > 100) {
          progress = 0;
        }
      });
    });
  }

  void updateProgress() {
    setState(() {
      progress += 10;
      if (progress > 100) {
        progress = 0;
      }
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Progress Button'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text(
              '進度: $progress%',
              style: TextStyle(fontSize: 24),
            ),
            SizedBox(height: 20),
            // ElevatedButton(
            //   onPressed: updateProgress,
            //   child: Text('更新進度'),
            // ),
          ],
        ),
      ),
    );
  }
}
```

---

## 第二種（使用TickerProvider)


![[Kapture 2023-10-18 at 15.44.10.gif]]


### Flutter Code
```Dart linenums="1"
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Print Progress',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: PrintProgressPage(),
    );
  }
}

class PrintProgressPage extends StatefulWidget {
  @override
  _PrintProgressPageState createState() => _PrintProgressPageState();
}

class _PrintProgressPageState extends State<PrintProgressPage>
    with SingleTickerProviderStateMixin {
  AnimationController? _animationController;
  Animation<double>? _animation;
  int _progress = 0;

  @override
  void initState() {
    super.initState();
    _animationController = AnimationController(
      duration: const Duration(seconds: 5),
      vsync: this,
    );
    _animation = Tween<double>(begin: 0, end: 2).animate(_animationController!)
      ..addListener(() {
        setState(() {
          _progress = (_animation!.value * 10).toInt();
        });
      });
    _animationController!.forward();
  }

  @override
  void dispose() {
    _animationController!.dispose();
    super.dispose();
  }

  void resetAnimation() {
    _animationController!.reset();
    _animationController!.forward();
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Print Progress'),
      ),
      body: Center(
          child: Row(
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          Text(
            '列印進度: $_progress%',
            style: TextStyle(fontSize: 24),
          ),
          SizedBox(
            width: 10,
          ),
          ElevatedButton(onPressed: resetAnimation, child: Text('Reset'))
        ],
      )),
    );
  }
}
```