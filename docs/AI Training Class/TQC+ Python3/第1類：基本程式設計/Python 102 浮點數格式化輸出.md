#Python #String #TQC 
#### 題目說明：

請撰寫一程式，輸入四個分別含有小數1到4位的浮點數，然後將這四個浮點數以欄寬為7、欄與欄間隔一個空白字元、每列印兩個的方式，先列印向右靠齊，再列印向左靠齊，左右皆以直線 |（Vertical bar）作為邊界。

> 提示：輸出浮點數到小數點後第二位。

#### 範例輸入

```
23.12
395.3
100.4617
564.329
```

#### 範例輸出

```
|  23.12  395.30|
| 100.46  564.33|
|23.12   395.30 |
|100.46  564.33 |
```

---
#### Solution
```python linenums="1"
a = eval(input())
b = eval(input())
c = eval(input())
d = eval(input())
print("|{:>7.2f} {:>7.2f} |".format(a, b))
print("|{:>7.2f} {:>7.2f} |".format(c, d))
print("|{:<7.2f} {:<7.2f} |".format(a, b))
print("|{:<7.2f} {:<7.2f} |".format(c, d))
```



- Reference
	- [TQC+ 程式語言Python 102 浮點數格式化輸出](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-102-%e6%b5%ae%e9%bb%9e%e6%95%b8%e6%a0%bc%e5%bc%8f%e5%8c%96%e8%bc%b8%e5%87%ba/)
	