#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入十個成績，接下來將十個成績中最小和最大值（最小、最大值不重複）以外的成績作加總及平均，並輸出結果。

> 提示：平均值輸出到小數點後第二位。

#### 範例輸入

```
89
78
67
80
75
98
77
89
76
60
```

#### 範例輸出

```
631
78.88
```

---
#### Solution
```python linenums="1"
l = []
for i in range(10):
	a = eval(input())
	l.append(a)
l.sort()
print("{:.2f}".format((sum(l)-(l[0]+l[i]))/8))
```
- Reference
	- [TQC+ 程式語言Python 605 成績計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-605-%e6%88%90%e7%b8%be%e8%a8%88%e7%ae%97/)