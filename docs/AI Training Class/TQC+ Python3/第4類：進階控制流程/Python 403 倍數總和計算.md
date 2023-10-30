#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入兩個正整數a、b（a<=b），輸出從a到b（包含a和b）之間4或9的倍數（一列輸出十個數字、欄寬為4、靠左對齊）以及倍數之個數、總和。

#### 範例輸入1

```
5
55
```

#### 範例輸出1

```
8   9   12  16  18  20  24  27  28  32  
36  40  44  45  48  52  54  
17
513
```

#### 範例輸入2

```
4
9
```

#### 範例輸出2

```
4   8   9   
3
21
```

---
#### Solution
```python linenums="1" linenums="1"
a = eval(input())
b = eval(input())
SUM = 0
l = []
for i in range(a, b+1):
	if((i % 4 == 0) | (i % 9 ==0)):
		SUM += i
		l.append(i)
for i in range(len(l)):
	print("{:<4d}".format(l[i]), end = "")
print()
print(len(l))
print(SUM)
```
- Reference
	- [TQC+ 程式語言Python 403 倍數總和計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-403-%e5%80%8d%e6%95%b8%e7%b8%bd%e5%92%8c%e8%a8%88%e7%ae%97/)