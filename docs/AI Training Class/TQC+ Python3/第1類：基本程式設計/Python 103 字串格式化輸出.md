#Python #String #TQC 
#### 題目說明：

請撰寫一程式，輸入四個單字，然後將這四個單字以欄寬為10、欄與欄間隔一個空白字元、每列印兩個的方式，先列印向右靠齊，再列印向左靠齊，左右皆以直線 |（Vertical bar）作為邊界。

#### 範例輸入

```
I
enjoy
learning
Python
```

#### 範例輸出

```
|         I      enjoy|
|  learning     Python|
|I          enjoy     |
|learning   Python    |
```

---
#### Solution
```python linenums="1"
a = input()
b = input()
c = input()
d = input()
print("|{:>10s} {:>10s}|".format(a, b))
print("|{:>10s} {:>10s}|".format(c, d))
print("|{:<10s} {:<10s}|".format(a, b))
print("|{:<10s} {:<10s}|".format(c, d))
```
- Reference
	- [TQC+ 程式語言Python 103 字串格式化輸出 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-103-%e5%ad%97%e4%b8%b2%e6%a0%bc%e5%bc%8f%e5%8c%96%e8%bc%b8%e5%87%ba/)

