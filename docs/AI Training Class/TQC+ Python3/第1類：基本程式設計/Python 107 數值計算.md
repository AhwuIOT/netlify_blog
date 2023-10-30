#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入五個數字，計算並輸出這五個數字之數值、總和及平均數。

>[!hint]
>總和與平均數皆輸出到小數點後第1位。

#### 範例輸入1

```
20
40
60
80
100
```

#### 範例輸出1

```
20 40 60 80 100
Sum = 300.0
Average = 60.0
```

#### 範例輸入2

```
88.7
12
56
132.55
3
```

#### 範例輸出2

```
88.7 12 56 132.55 3
Sum = 292.2
Average = 58.5
```

---
#### Solution
```python linenums="1"
l = []
for i in range(5):
	l.append(eval(input()))
for i in range(5):
	print(l[i],end = " ")
print()
print("Sum = %.1f"%sum(l))
print("Average = %.1f"%(sum(l)/5))
```
- Reference
	- [TQC+ 程式語言Python 107 數值計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-107-%e6%95%b8%e5%80%bc%e8%a8%88%e7%ae%97/)
