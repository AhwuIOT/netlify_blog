#Python #TQC 
#### 題目說明：

請使用迴圈敘述撰寫一程式，讓使用者輸入一個正整數a，利用迴圈計算從1到a之間，所有5之倍數數字總和。

#### 範例輸入

```
21
```

#### 範例輸出

```
50
```

---
#### Solution
```python linenums="1"
a = eval(input())
SUM = 0
for i in range(1, a+1):
	if(i % 5 == 0): SUM += i
print(SUM)
```
- Reference
	- [TQC+ 程式語言Python 304 迴圈倍數總和 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-304-%e8%bf%b4%e5%9c%88%e5%80%8d%e6%95%b8%e7%b8%bd%e5%92%8c/)