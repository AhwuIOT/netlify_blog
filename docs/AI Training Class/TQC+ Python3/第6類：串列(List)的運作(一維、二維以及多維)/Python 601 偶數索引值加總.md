#Python #TQC 
#### 題目說明：

請撰寫一程式，利用一維串列存放使用者輸入的12個正整數（範圍1~99）。顯示這些數字，接著將串列索引為偶數的數字相加並輸出結果。

> [!hint]
> 輸出每一個數字欄寬設定為3，每3個一列，靠右對齊。

#### 範例輸入

```
56
45
43
22
3
1
39
20
93
18
44
83
```

#### 範例輸出

```
 56 45 43
 22  3  1
 39 20 93
 18 44 83
278
```

---
```python linenums="1"
l = []
SUM = 0
for i in range(12):
	a = eval(input())
	l.append(a)
	if(i % 2 == 0):
		SUM += a
for i in range(12):
	print("{:>3d}".format(l[i]), end = "")
	if(i % 3 == 2):
		print("\n")
print(SUM)
```
- Reference
	- [TQC+ 程式語言Python 601 偶數索引值加總 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-601-%e5%81%b6%e6%95%b8%e7%b4%a2%e5%bc%95%e5%80%bc%e5%8a%a0%e7%b8%bd/)