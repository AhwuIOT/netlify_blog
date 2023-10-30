#Python #TQC 
#### 題目說明：

請撰寫一程式，依照使用者輸入的n，畫出對應的等腰三角形。

#### 範例輸入

```
7
```

#### 範例輸出

```
      *
     ***
    *****
   *******
  *********
 ***********
*************
```

---
#### Solution
```python linenums="1" linenums="1"
a = eval(input())
for i in range(a, 0, -1):
	print(" "*i+"*"*(1+2*(a-i)))
```

> [!attention]
> 記得一定要從a 數回0，用-1步數
> 另外還有print的內容1+2*(a-i)

- Reference
	- [TQC+ 程式語言Python 410 繪製等腰三角形 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-410-%e7%b9%aa%e8%a3%bd%e7%ad%89%e8%85%b0%e4%b8%89%e8%a7%92%e5%bd%a2/)