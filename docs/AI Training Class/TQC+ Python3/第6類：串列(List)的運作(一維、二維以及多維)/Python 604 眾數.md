#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入十個整數作為樣本數，輸出眾數（樣本中出現最多次的數字）及其出現的次數。


>[!hint]
>假設樣本中只有一個眾數。

#### 範例輸入

```
34
18
22
32
18
29
30
38
42
18
```

#### 範例輸出

```
18
3
```

---
#### Solution
```python linenums="1"
d = {}
for i in range(10):
	a = input()
	if(a in d):
		d[a] += 1
	else:
		d[a] = 1
for key, value in d.items():
	if(value == max(d.values())):
		print(int(key))
		print(value)
```

>[!tip]
>用dictionary的方式比較直覺，雖然題目有說只有一個眾數

- Reference
	- [Python3 字典 items() 方法 | 菜鸟教程 (runoob.com)](https://www.runoob.com/python3/python3-att-dictionary-items.html)
	- [TQC+ 程式語言Python 604 眾數 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-604-%e7%9c%be%e6%95%b8/)