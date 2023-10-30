#Python #TQC 
#### 題目說明：

請使用迴圈敘述撰寫一程式，讓使用者輸入兩個正整數a、b（a < b），利用迴圈計算從a開始的偶數連加到b的總和。例如：輸入a=1、b=100，則輸出結果為2550（2 + 4 + … + 100 = 2550）。

#### 範例輸入

```
14
1144
```

#### 範例輸出

```
327714
```

---
#### Solution
```python linenums="1"
a = eval(input())
b = eval(input())
SUM = 0
if(a < b):
	for i in range(a, b+1):
		if(i % 2 == 0):
			SUM += i
print(SUM)
```
- Reference
	- [TQC+ 程式語言Python 302 迴圈偶數連加 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-302-%e8%bf%b4%e5%9c%88%e5%81%b6%e6%95%b8%e9%80%a3%e5%8a%a0/)