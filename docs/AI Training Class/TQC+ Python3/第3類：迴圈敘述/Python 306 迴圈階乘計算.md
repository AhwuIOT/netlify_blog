#Python #TQC 
#### 題目說明：

請使用迴圈敘述撰寫一程式，讓使用者輸入一個正整數n，利用迴圈計算並輸出n!的值。

#### 範例輸入

```
15
```

#### 範例輸出

```
1307674368000
```

---
#### Solution
```python linenums="1"
a = eval(input())
SUM = 1
for i in range(1, a+1):
	SUM *= i
print(SUM)
```

>[!attention]
>SUM記得從1開始，否則結果值會是0

- Reference
	- [TQC+ 程式語言Python 306 迴圈階乘計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-306-%e8%bf%b4%e5%9c%88%e9%9a%8e%e4%b9%98%e8%a8%88%e7%ae%97/)