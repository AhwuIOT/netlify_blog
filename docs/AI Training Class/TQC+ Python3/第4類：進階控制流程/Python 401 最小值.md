#Python #TQC 
#### 題目說明：

請撰寫一程式，由使用者輸入十個數字，然後找出其最小值，最後輸出最小值。

#### 範例輸入

```
23
57
48
2
99
70
9
65
35
88
```

#### 範例輸出

```
2
```

---
#### Solution
```python linenums="1" linenums="1"
l = []
for i in range(10):
	l.append(eval(input()))
print(min(l))
```
- Reference
	- [TQC+ 程式語言Python 401 最小值 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-401-%e6%9c%80%e5%b0%8f%e5%80%bc/)