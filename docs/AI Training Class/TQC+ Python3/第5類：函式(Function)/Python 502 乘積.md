#Python #TQC 
#### 題目說明：

請撰寫一程式，將使用者輸入的兩個整數作為參數傳遞給一個名為compute(x, y)的函式，此函式將回傳x和y的乘積。

#### 範例輸入

```
56
11
```

#### 範例輸出

```
616
```

---
#### Solution
```python linenums="1"
def compute(x, y):
	return x*y
print(compute(eval(input()), eval(input())))
```
- Reference
	- [TQC+ 程式語言Python 502 乘積 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-502-%e4%b9%98%e7%a9%8d/)