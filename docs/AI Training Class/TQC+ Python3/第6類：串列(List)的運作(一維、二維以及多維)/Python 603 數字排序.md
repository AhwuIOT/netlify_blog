#Python #TQC 
#### 題目說明：

請撰寫一程式，要求使用者輸入十個數字並存放在串列中。接著由大到小的順序顯示最大的3個數字。

#### 範例輸入1

```
40
32
12
29
20
19
38
48
57
44
```

#### 範例輸出1

```
57 48 44
```

---

#### 範例輸入2

```
139
246
15
38
77
122
42
30
100
1
```

#### 範例輸出2

```
246 139 122
```

---
#### Solution
```python linenums="1"
l = []
for i in range(10):
  l.append(eval(input()))
l.sort()
print(l[-1], l[-2], l[-3])
```
- Reference
	- [TQC+ 程式語言Python 603 數字排序 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-603-%e6%95%b8%e5%ad%97%e6%8e%92%e5%ba%8f/)
- Link
	- [[sort()的用法]]