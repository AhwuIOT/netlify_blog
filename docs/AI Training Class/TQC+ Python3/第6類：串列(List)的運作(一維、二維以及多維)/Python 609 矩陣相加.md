#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者建立兩個2*2的矩陣，其內容為從鍵盤輸入的整數，接著輸出這兩個矩陣的內容以及它們相加的結果。

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示

**Enter matrix 1:**  
**[1, 1]:**3  
**[1, 2]:**5  
**[2, 1]:** 7  
**[2, 2]:** 5  
**Enter matrix 2:**  
**[1, 1]:** 6  
**[1, 2]:** 9  
**[2, 1]:** 8  
**[2, 2]:** 3

**Matrix 1:**  
**3 5 **  
**7 5 **  
**Matrix 2:**  
**6 9 **  
**8 3 **  
**Sum of 2 matrices:**  
**9 14 **  
**15 8 **

---
#### Solution
```python linenums="1"
l = [[[0 for i in range(2)] for j in range(2)]for k in range(2)]
for i in range(2):
	print("Enter matrix %d"%(i+1))
	for j in range(2):
		for k in range(2):
			print("[{},{}]:".format((j+1), (k+1)), end = "")
			a = eval(input())
			l[i][j][k] = a
for i in range(2):
	print("Matrix %d"%(i+1))
	for j in range(2):
		for k in range(2):
			print("{}".format(l[i][j][k]),end = " ")
		print()
print("Sum of 2 matrices:")
for i in range(2):
	for j in range(2):
		print("{}".format(l[0][i][j]+l[1][i][j]), end = " ")
	print()
		
```

> [!attention]
> 如果不用三維陣列那就需要寫比較多程式碼

- Reference
	- [TQC+ 程式語言Python 609 矩陣相加 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-609-%e7%9f%a9%e9%99%a3%e7%9b%b8%e5%8a%a0/)