#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入兩個正整數rows、cols，分別表示二維串列lst 的「第一個維度大小」與「第二個維度大小」。  
串列元素[row][col]所儲存的數字，其規則為：row、col 的交點值 = 第二個維度的索引col – 第一個維度的索引row。  
接著以該串列作為參數呼叫函式compute()輸出串列。

>[!hint]
>欄寬為4。

#### 範例輸入

```
5
10
```

#### 範例輸出

```
   0   1   2   3   4   5   6   7   8   9
  -1   0   1   2   3   4   5   6   7   8
  -2  -1   0   1   2   3   4   5   6   7
  -3  -2  -1   0   1   2   3   4   5   6
  -4  -3  -2  -1   0   1   2   3   4   5
```

---
#### Solution
```python linenums="1"
def compute(rows, cols):
	for i in range(rows):
		for j in range(cols):
			print("{:4d}".format(j-i), end = "")
		print()
compute(eval(input()), eval(input()))
```
- Reference
	- [TQC+ 程式語言Python 606 二維串列行列數 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-606-%e4%ba%8c%e7%b6%ad%e4%b8%b2%e5%88%97%e8%a1%8c%e5%88%97%e6%95%b8/)