#Python #TQC #file 
#### 題目說明：

請撰寫一程式，要求使用者輸入檔案名稱data.txt和一字串s，顯示該檔案的內容。接著刪除檔案中的字串s，顯示刪除後的檔案內容並存檔。

#### 範例輸入1

```plain text
data.txt
Tomato
```

#### 範例輸出1

```plain text
=== Before the deletion
Apple Kiwi Banana
Tomato Pear Durian

=== After the deletion
Apple Kiwi Banana
 Pear Durian
 
```

#### 範例輸入2

```plain text
data.txt
Kiwi
```

#### 範例輸出2

```plain text
=== Before the deletion
Apple Kiwi Banana
Tomato Pear Durian

=== After the deletion
Apple  Banana
Tomato Pear Durian
```
#### data.txt檔案內容
```plain text
Apple Kiwi Banana 
Tomato Pear Durian
```

---
#### Solution

```python linenums="1"
f = open("data.txt", 'r+')
d = f.read()
r = input()
print("=== Before the deletion")
print(d)
data = d.replace(r, "")
print("=== After the deletion")
print(data)
"""
必須回到檔案的頭才能寫入
"""
f.seek(0)
f.write(data)
f.close()
```


- Reference
	- [TQC+ 程式語言Python 905 字串資料刪除 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-905-%e5%ad%97%e4%b8%b2%e8%b3%87%e6%96%99%e5%88%aa%e9%99%a4/)
- Link
	- [[replace()用法]]
	- [[Python 903 成績資料]]