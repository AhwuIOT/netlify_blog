#Python #TQC 
#### 題目說明：

請使用迴圈敘述撰寫一程式，讓使用者輸入兩個正整數a、b（a < b），利用迴圈計算從a開始連加到b的總和。例如：輸入a=1、b=100，則輸出結果為5050（1 + 2 + … + 100 = 5050）。

#### 範例輸入

```
66
666
```

#### 範例輸出

```
219966
```

---
#### Solution
```python linenums="1"
a = eval(input())
b = eval(input())
SUM = 0
if(a < b):
	for i in range(a, b+1):
		SUM += i
print(SUM)
```
- [TQC+ 程式語言Python 301 迴圈整數連加 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-301-%e8%bf%b4%e5%9c%88%e6%95%b4%e6%95%b8%e9%80%a3%e5%8a%a0/)