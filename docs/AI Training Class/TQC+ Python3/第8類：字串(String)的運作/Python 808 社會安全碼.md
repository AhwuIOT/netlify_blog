#Python #String #TQC 
#### 題目說明：

請撰寫一程式，提示使用者輸入一個社會安全碼SSN，格式為ddd-dd-dddd，d表示數字。若格式完全符合（正確的SSN）則顯示【Valid SSN】，否則顯示【Invalid SSN】。

#### 範例輸入1

```
329-48-4977
```

#### 範例輸出1

```
Valid SSN
```

#### 範例輸入2

```
837-a3-3000
```

#### 範例輸出2

```
Invalid SSN
```

---
#### Solution

```python linenums="1"
n = input()
n = n.replace("-","")
for i in range(len(n)):
	if not n[i].isdigit():
		print("Invalid SSN")
		break
else:
	print("Valid SSN")	

```

> [!attention]
> 注意else位置

- Reference
	- [TQC+ 程式語言Python 808 社會安全碼](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-808-%e7%a4%be%e6%9c%83%e5%ae%89%e5%85%a8%e7%a2%bc/)
- Link
	- [[replace()用法]]