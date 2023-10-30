#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者建立一個3*3的矩陣，其內容為從鍵盤輸入的整數（不重複），接著輸出矩陣最大值與最小值的索引。

#### 範例輸入

```
6
4
8
39
12
3
-3
49
33
```

#### 範例輸出

```
Index of the largest number 49 is: (2, 1)
Index of the smallest number -3 is: (2, 0)
```
#### Solution
```python linenums="1"
l = []
for i in range(9):
	l.append(eval(input()))
MAX = max(l)
M_row = l.index(MAX) // 3
M_col = l.index(MAX) % 3
MIN = min(l)
m_row = l.index(MIN) // 3
m_col = l.index(MIN) % 3
print("Index of the largest number {} is: ({}, {})".format(MAX, M_row, M_col))
print("Index of the smallest number {} is: ({}, {})".format(MIN, m_row, m_col))
```

>[!attention]
>整除3可以得到該值的row，%3可以得到column

- Reference
	- [TQC+ 程式語言Python 608 最大最小值索引 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-608-%e6%9c%80%e5%a4%a7%e6%9c%80%e5%b0%8f%e5%80%bc%e7%b4%a2%e5%bc%95/)