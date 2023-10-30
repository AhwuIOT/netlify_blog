#Python #TQC 
#### 題目說明：

請撰寫一程式，將使用者輸入的三個參數，變數名稱分別為a（代表字元character）、x（代表個數）、y（代表列數），作為參數傳遞給一個名為compute()的函式，該函式功能為：一列印出x個a字元，總共印出y列。


>[!hint]
>輸出的每一個字元後方有一空格。

#### 範例輸入

```
e
5
4
```

#### 範例輸出

```
e e e e e 
e e e e e 
e e e e e 
e e e e e 
```

---
#### Solution
```python linenums="1"
def compute(a, x, y):
	for i in range(y):
		print((a + " ")*x)
compute(input(), eval(input()), eval(input()))		
```
- Reference
	- [TQC+ 程式語言Python 505 依參數格式化輸出 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-505-%e4%be%9d%e5%8f%83%e6%95%b8%e6%a0%bc%e5%bc%8f%e5%8c%96%e8%bc%b8%e5%87%ba/)