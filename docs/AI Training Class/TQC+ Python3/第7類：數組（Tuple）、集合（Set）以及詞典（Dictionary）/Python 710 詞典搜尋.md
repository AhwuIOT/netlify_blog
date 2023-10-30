#Python #TQC 
#### 題目說明：

請撰寫一程式，為一詞典輸入資料（以輸入鍵值”end”作為輸入結束點，詞典中將不包含鍵值”end”），再輸入一鍵值並檢視此鍵值是否存在於該詞典中。

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示

**Key:** 123-4567-89  
**Value:** Jennifer  
**Key:** 987-6543-21  
**Value:** Tommy  
**Key:** 246-8246-82  
**Value:** Kay  
**Key:** end  
**Search key:** 246-8246-82  
**True**

---
#### Solution
```python linenums="1"
D = {}
while True:
	key = input("Key:")
	if(key == 'end'):break
	else:
		D[key] = input("Value:")
s = input("Search key:")
print(s in D)
		 
```
- Reference
	- (https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-710-%e8%a9%9e%e5%85%b8%e6%90%9c%e5%b0%8b/)