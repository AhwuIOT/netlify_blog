#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入數字，輸入的動作直到輸入值為9999才結束，然後找出其最小值，並輸出最小值。

#### 範例輸入

```
29
100
948
377
-28
0
-388
9999
```

#### 範例輸出

```
-388
```

---
#### Solution
```python linenums="1" linenums="1"
l = []
while True:
	a = eval(input())
	if(a == 9999):break
	else:
		l.append(a)
print(min(l))
```
- Reference
	- [TQC+ 程式語言Python 402 不定數迴圈-最小值 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-402-%e4%b8%8d%e5%ae%9a%e6%95%b8%e8%bf%b4%e5%9c%88-%e6%9c%80%e5%b0%8f%e5%80%bc/)