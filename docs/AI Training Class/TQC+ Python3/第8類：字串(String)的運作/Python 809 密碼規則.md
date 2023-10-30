#Python #String #TQC 
#### 題目說明：

請撰寫一程式，要求使用者輸入一個密碼（字串），檢查此密碼是否符合規則。密碼規則如下：  
　a. 必須至少八個字元。  
　b. 只包含英文字母和數字。  
　c. 至少要有一個大寫英文字母。  
　d. 若符合上述三項規則，程式將顯示檢查結果為【Valid password】，否則顯示【Invalid password】。

#### 範例輸入1

```
39Gfjkd98
```

#### 範例輸出1

```
Valid password
```

#### 範例輸入2

```
39dk8fh
```

#### 範例輸出2

```
Invalid password
```

---
#### Solution

```python linenums="1"
n = input()
for i in range(len(n)):
	if(len(n)<8 | ((not n[i].isdigit()) & (not n[i].isalpha()))):
		print("Invalid password")
		break
else:
	print("Valid password")

"""
另一寫法
"""
n = input()
if (len(n)<8 | (not n.isalnum())):
  print("Invalid password")
else:
  print("Valid password")
```

- Reference
	- [TQC+ 程式語言Python 809 密碼規則](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-809-%e5%af%86%e7%a2%bc%e8%a6%8f%e5%89%87/)