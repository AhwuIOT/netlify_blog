#Python #TQC 
題目說明：

請撰寫一程式，要求使用者輸入一字串，顯示該字串每個字元的索引。

#### 範例輸入

```
Sandwich
```

#### 範例輸出

```
Index of 'S': 0
Index of 'a': 1
Index of 'n': 2
Index of 'd': 3
Index of 'w': 4
Index of 'i': 5
Index of 'c': 6
Index of 'h': 7
```

---
#### Solution
```python linenums="1"
n = input()
for i in range(len(n)):
	print("Index of {}: {}".format(n[i], i))
```
- Reference
	- [TQC+ 程式語言Python 801 字串索引](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-801-%e5%ad%97%e4%b8%b2%e7%b4%a2%e5%bc%95/)