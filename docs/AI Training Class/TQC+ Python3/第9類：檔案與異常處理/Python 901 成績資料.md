#Python #TQC #file 

#### 題目說明
請撰寫一程式，將使用者輸入的五筆資料寫入到write.txt（若不存在，則讓程式建立它），每一筆資料為一行，包含學生名字和期末總分，以空白隔開。檔案寫入完成後要關閉。
>[!hint ]
>>將輸入的五筆資料寫入檔案中，不另外輸出於頁面。

#### 範例輸入

```
Leon 87
Ben 90
Sam 77
Karen 92
Kelena 92
```



---
#### Solution

```python linenums="1"
file = open("wirte.txt", 'w')

for i in range(5):
	data = input()
	file.write(data + '\n')
file.close()
```


---
- Reference
	- [TQC+ 程式語言Python 901 成績資料 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-901-%e6%88%90%e7%b8%be%e8%b3%87%e6%96%99/)
- Link
	- [[檔案讀寫參數]]