#Python #String #TQC 
#### 題目說明：

請撰寫一程式，要求使用者輸入一字串，該字串為五個數字，以空白隔開。請將此五個數字加總（Total）並計算平均（Average）。

#### 範例輸入

```
-2 34 18 29 -56
```

#### 範例輸出

```
Total = 23
Average = 4.6
```

---
#### Solution

```python linenums="1"
n = input()
l = [int(x) for x in n.split()]
print("Total = {}".format(sum(l)))
print("Average = {}".format(sum(l)/5))
```

> [!attention]
> 注意n.split()轉換後會變為list，需要透過迴圈賦值方式將其資料型態從String轉為int

- Reference
	- [TQC+ 程式語言Python 807 字串加總](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-807-%e5%ad%97%e4%b8%b2%e5%8a%a0%e7%b8%bd/)
- Link
	- [[split()用法]]