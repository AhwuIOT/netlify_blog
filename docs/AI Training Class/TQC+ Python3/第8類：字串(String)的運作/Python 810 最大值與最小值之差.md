#Python #String #TQC 
#### 題目說明：

請撰寫一程式，首先要求使用者輸入正整數k（1 <= k <= 100），代表有k筆測試資料。每一筆測試資料是一串數字，每個數字之間以一空白區隔，請找出此串列數字中最大值和最小值之間的差。

>[!hint]
>差值輸出到小數點後第二位。

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示

4  
94 52.9 3.14 77 46  
**90.86**  
-2 0 1000.34 -14.4 89 50  
**1014.74**  
87.78 33333 29.3  
**33303.70**  
9998 9996 9999  
**3.00**

---
#### Solution

```python linenums="1"
n = eval(input())
if(n <= 100 & n >= 1):
	for i in range(n):
		s = input()
		l = [float(i) for i in s.split()]
		print("{:.2f}".format(max(l)-min(l)))
```

- Reference
	- [TQC+ 程式語言Python 810 最大值與最小值之差](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-810-%e6%9c%80%e5%a4%a7%e5%80%bc%e8%88%87%e6%9c%80%e5%b0%8f%e5%80%bc%e4%b9%8b%e5%b7%ae/)