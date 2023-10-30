#Python #TQC 
#### 題目說明：

請撰寫一程式，自行輸入兩個詞典（以輸入鍵值”end”作為輸入結束點，詞典中將不包含鍵值”end”），將此兩詞典合併，並根據key值字母由小到大排序輸出，如有重複key值，後輸入的key值將覆蓋前一key值。

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示

**Create dict1:**  
**Key:** a  
**Value:** apple  
**Key:** b  
**Value:** banana  
**Key:** d  
**Value:** durian  
**Key:** end  
**Create dict2:**  
**Key:** c  
**Value:** cat  
**Key:** e  
**Value:** elephant  
**Key:** end  
**a: apple**  
**b: banana**  
**c: cat**  
**d: durian**  
**e: elephant**

---
#### Solution
```python linenums="1"
def compute():
	D = {}
	while True:
		key = input("Key:")
		if(key=='end'):
			return D
		else:
			D[key] = input("Value:")
print("Create dict1:")
d1 = compute()
print("Create dict2:")
d2 = compute()
d1.update(d2)
d3 = dict(sorted(d1.items()))
for i in d3:
	print(i,":",d3[i])
```

>[!attention]
>注意使用dictionary排序時的寫法dict(sorted(d1.items()))

- Reference
	- [TQC+ 程式語言Python 708 詞典合併](https://jbprogramnotes.com/2020/05/tqc-%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80python-708-%E8%A9%9E%E5%85%B8%E5%90%88%E4%BD%B5/)
