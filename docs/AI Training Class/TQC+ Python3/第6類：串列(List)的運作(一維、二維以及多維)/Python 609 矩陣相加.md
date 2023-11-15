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

這段 Python 程式碼主要進行了三維列表的創建、數據輸入、數據顯示和矩陣求和的操作。以下是對應的 Mermaid 流程圖語法：

```mermaid
graph TD
    A[開始] --> B[創建三維列表 l]
    B --> C[遍歷 i 從 0 到 1]
    C -->|每次迴圈| D[打印提示信息]
    D --> E[遍歷 j 從 0 到 1]
    E -->|每次迴圈| F[遍歷 k 從 0 到 1]
    F -->|每次迴圈| G[輸入 l[i][j][k] 的值]
    G --> H{是否完成所有輸入?}
    H -->|是| I[顯示兩個矩陣]
    H -->|否| E
    I --> J[遍歷 i 和 j 從 0 到 1]
    J -->|每次迴圈| K[計算並打印兩個矩陣的和]
    K --> L{是否完成所有求和?}
    L -->|是| M[結束]
    L -->|否| J
```

這段代碼首先創建一個三維的列表 `l`，然後通過嵌套的迴圈結構從用戶那裡接收數據並填充到這個列表中。之後，代碼遍歷這個列表並打印出兩個矩陣的內容。最後，代碼計算這兩個矩陣的和並將結果輸出到屏幕上。




- Reference
	- [TQC+ 程式語言Python 609 矩陣相加 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-609-%e7%9f%a9%e9%99%a3%e7%9b%b8%e5%8a%a0/)