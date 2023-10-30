#Python #TQC 
#### 題目說明：

請使用迴圈敘述撰寫一程式，要求使用者輸入一個數字，此數字代表後面測試資料的數量。每一筆測試資料是一個正整數（由使用者輸入），將此正整數的每位數全部加總起來。

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示 1
1  
98765  
**Sum of all digits of 98765 is 35**

---
#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示 2
3  
32412  
**Sum of all digits of 32412 is 12**  
0  
**Sum of all digits of 0 is 0**  
769  
**Sum of all digits of 769 is 22**

---
#### Solution
```python linenums="1"
n = eval(input())
for i in range(n):
	l = []
	a = input()
	for j in range(len(a)):
		l.append(int(a[j]))
	print("Sum of all digits of {} is {}".format(a, sum(l)))
```

> [!attention]
> **因為輸入是String格式，所以可以用index方式去將其再轉換為int格式做加總，有些答案會使用一直%的方式，也不失為一種手段。**

- Reference
	- [TQC+ 程式語言Python 308 迴圈位數加總 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-308-%e8%bf%b4%e5%9c%88%e4%bd%8d%e6%95%b8%e5%8a%a0%e7%b8%bd/)