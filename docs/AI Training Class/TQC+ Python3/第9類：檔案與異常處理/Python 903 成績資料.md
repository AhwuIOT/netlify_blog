#Python #TQC #file 
#### 題目說明：

請撰寫一程式，要求使用者輸入五個人的名字並加入到data.txt的尾端。之後再顯示此檔案的內容。

#### 範例輸入

```
Daisy
Kelvin
Tom
Joyce
Sarah
```

#### 範例輸出

```
Append completed!
Content of "data.txt":
Ben
Cathy
Tony
Daisy
Kelvin
Tom
Joyce
Sarah
```

---
#### Solution
```python linenums="1"
f = open("data.txt", 'a+')

for i in range(5):

  a = input()

  f.write('\n'+a)

  

print("Append completed!")

print('Content of "data.txt":')

  

f.seek(0)

print(f.read())

  

f.close()
```
---
#### 重要語法
```python linenums="1"
"""
open file中a+代表持續往下寫入，不會覆蓋過去的檔案
"""
file.seek(0)
"""
由於寫完檔案已經跳到檔案最後一行，因此必須使用seek()回到最開頭
"""
```
---

- Reference
	- [TQC+ 程式語言Python 903 成績資料 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-903-%e6%88%90%e7%b8%be%e8%b3%87%e6%96%99/)
-  Link
	- [[檔案讀寫參數]]