#Python #TQC 
#### 題目說明：

請撰寫一程式，呼叫函式compute()，該函式功能為讓使用者輸入系別（Department）、學號（Student ID）和姓名（Name）並顯示這些訊息。

#### 範例輸入

```
Information Management
123456789
Tina Chen
```

#### 範例輸出

```
Department: Information Management
Student ID: 123456789
Name: Tina Chen
```

---
#### Solution
```python linenums="1"
def compute():
  a = input()
  b = input()
  c = input()
  print('Department:%s'%a)
  print('Student ID:%s'%b)
  print('Name:%s'%c)

compute()
```
- Reference
	- [TQC+ 程式語言Python 501 訊息顯示 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-501-%e8%a8%8a%e6%81%af%e9%a1%af%e7%a4%ba/)