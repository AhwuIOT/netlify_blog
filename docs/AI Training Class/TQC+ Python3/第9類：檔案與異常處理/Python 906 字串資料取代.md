#Python #String #TQC 
#### 題目說明：

請撰寫一程式，要求使用者輸入檔名data.txt、字串s1和字串s2。程式將檔案中的字串s1以s2取代之。

#### 範例輸入

```
data.txt
pen
sneakers
```

#### 範例輸出

```
=== Before the replacement
watch shoes skirt
pen trunks pants
=== After the replacement
watch shoes skirt
sneakers trunks pants
```

#### data.txt內容
```
watch shoes skirt
pen trunks pants
```

---
#### Solution
```python linenums="1"
f = open("data.txt", 'r+')

d = f.read()

s1 = input()
s2 = input()

print("=== Before the deletion")

print(d)

data = d.replace(s1, s2)

print("=== After the deletion")

print(data)

f.seek(0)

f.write(data)

f.close()
```
- Reference
	- [TQC+ 程式語言Python 906 字串資料取代 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-906-%e5%ad%97%e4%b8%b2%e8%b3%87%e6%96%99%e5%8f%96%e4%bb%a3/)
- Link
	- [[replace()用法]]