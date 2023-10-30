#Python #String #TQC 
題目說明：

請撰寫一程式，讓使用者輸入一字串，分別將該字串轉換成全部大寫以及每個字的第一個字母大寫。

#### 範例輸入

```
learning python is funny
```

#### 範例輸出

```
LEARNING PYTHON IS FUNNY
Learning Python Is Funny
```

---
#### Solution

```python linenums="1"
n = input()
print(n.upper())
print(n.title())
```

---
#### upper()與title()使用
在Python 3中，`upper()`和`title()`是字串物件的方法，用於修改字串的大小寫形式。以下是它們的用法：

1. `upper()`: `upper()`方法將字串中的所有字母轉換為大寫形式，並回傳一個新的字串。它不會修改原始字串。

   範例程式碼：
   ```python linenums="1"
   text = "hello, world!"
   uppercase_text = text.upper()
   print(uppercase_text)
   ```

   輸出：
   ```
   HELLO, WORLD!
   ```

2. `title()`: `title()`方法將字串中的每個單字的首字母轉換為大寫形式，並回傳一個新的字串。它不會修改原始字串。

   範例程式碼：
   ```python linenums="1"
   text = "hello, world!"
   title_case_text = text.title()
   print(title_case_text)
   ```

   輸出：
   ```
   Hello, World!
   ```

需要注意的是，`upper()`和`title()`方法回傳的是新的字串物件，而不是直接修改原始字串。如果你想修改原始字串，可以將結果指派給原始字串變數。

例如：

```python linenums="1"
text = "hello, world!"
text = text.upper()
print(text)  # 輸出 "HELLO, WORLD!"

text = "hello, world!"
text = text.title()
print(text)  # 輸出 "Hello, World!"
```

- [TQC+ 程式語言Python 804 大寫轉換](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-804-%e5%a4%a7%e5%af%ab%e8%bd%89%e6%8f%9b/)