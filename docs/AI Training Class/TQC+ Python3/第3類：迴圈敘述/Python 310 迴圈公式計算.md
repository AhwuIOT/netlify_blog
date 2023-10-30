#Python #TQC 
#### 題目說明：

請使用迴圈敘述撰寫一程式，讓使用者輸入正整數n (1 < n)，計算以下公式的總和並顯示結果：  
$$\frac{1}{\sqrt{1}+\sqrt{2}}+\frac{1}{\sqrt{2}+\sqrt{3}}+\frac{1}{\sqrt{3}+\sqrt{4}}+...+\frac{1}{\sqrt{n-1}+\sqrt{n}} $$

> [!hint]
> 輸出結果至小數點後四位。

#### 範例輸入

```
8
```

#### 範例輸出

```
1.8284
```

---
#### Solution
```python linenums="1"
a = eval(input())
SUM = 0
for i in range(1, a):
	SUM += 1/((i**0.5)+(i+1)**0.5)
print("%.4f"%SUM)
```
- Reference
	- [TQC+ 程式語言Python 310 迴圈公式計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-310-%e8%bf%b4%e5%9c%88%e5%85%ac%e5%bc%8f%e8%a8%88%e7%ae%97/)