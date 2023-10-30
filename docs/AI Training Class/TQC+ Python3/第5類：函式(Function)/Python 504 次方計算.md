#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入兩個整數，接著呼叫函式compute()，此函式接收兩個參數a、b，並回傳$$a^b$$的值。

#### 範例輸入

```
14
3
```

#### 範例輸出

```
2744
```

---
#### Solution
```python linenums="1"
def compute(a, b):
	return a**b
print(compute(eval(input()), eval(input())))
```
- Reference
	- [TQC+ 程式語言Python 504 次方計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-504-%e6%ac%a1%e6%96%b9%e8%a8%88%e7%ae%97/)