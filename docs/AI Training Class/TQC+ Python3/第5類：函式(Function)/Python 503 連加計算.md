#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入兩個整數，接著呼叫函式compute()，此函式接收兩個參數a、b，並回傳從a連加到b的和。

#### 範例輸入

```
33
66
```

#### 範例輸出

```
1683
```

---
#### Solution
```python linenums="1"
def compute(a, b):
	SUM = 0
	for i in range(a, b+1):
		SUM += i
	return SUM
print(compute(eval(input()), eval(input())))
```
- Reference
	- [TQC+ 程式語言Python 503 連加計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-503-%e9%80%a3%e5%8a%a0%e8%a8%88%e7%ae%97/)