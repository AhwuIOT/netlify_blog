#Python #TQC #file 
#### 題目說明：

請撰寫一程式，讀取read.txt的內容（內容為數字，以空白分隔）並將這些數字加總後輸出。檔案讀取完成後要關閉。

#### 範例輸出

```
660
```

#### read.txt內容
```
11 22 33 22 33 44 33 44 55 44 55 66 55 66 77
```

---
#### Solution
```python linenums="1"
f = open("read.txt", 'r')

data = f.read()

l = [int(i)for i in data.split()]

print(sum(l))


f.close()
```

- Reference
	- [TQC+ 程式語言Python 902 資料加總 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-902-%e8%b3%87%e6%96%99%e5%8a%a0%e7%b8%bd/)
- Link
	- [[檔案讀寫參數]]