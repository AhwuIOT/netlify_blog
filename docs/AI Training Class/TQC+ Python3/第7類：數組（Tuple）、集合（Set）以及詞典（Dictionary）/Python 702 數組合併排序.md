#Python #TQC 
#### 題目說明：

請撰寫一程式，輸入並建立兩組數組，各以-9999為結束點（數組中不包含-9999）。將此兩數組合併並從小到大排序之，顯示排序前的數組和排序後的串列。

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示

**Create tuple1:**  
9  
0  
-1  
3  
8  
-9999  
**Create tuple2:**  
28  
16  
39  
56  
78  
88  
-9999  
**Combined tuple before sorting: (9, 0, -1, 3, 8, 28, 16, 39, 56, 78, 88)**  
**Combined list after sorting: [-1, 0, 3, 8, 9, 16, 28, 39, 56, 78, 88]**

---
#### Solution
```python linenums="1"
l1 = []
print("Create tuple1:")
while True:
  a = eval(input())
  if(a == -9999):break
  else:
    l1.append(a)

l2 = []
print("Create tuple2:")
while True:
  a = eval(input())
  if(a == -9999):break
  else:
    l2.append(a)

l1.extend(l2)
t = tuple(l1)
l1.sort()
print("Combined tuple before sorting: ",t)
print("Combined list after sorting: ",l1)

```
- Reference 
	- [Python3 List extend()方法](https://www.runoob.com/python3/python3-att-list-extend.html)
	- [TQC+ 程式語言Python 702 數組合併排序](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-702-%e6%95%b8%e7%b5%84%e5%90%88%e4%bd%b5%e6%8e%92%e5%ba%8f/)