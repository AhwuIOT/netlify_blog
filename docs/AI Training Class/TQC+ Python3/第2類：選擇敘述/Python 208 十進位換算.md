#Python #TQC 
#### 題目說明：

請使用選擇敘述撰寫一程式，讓使用者輸入一個十進位整數num(0 ≤ num ≤ 15)，將num轉換成十六進位值。

> [!hint]
> 轉換規則 = 十進位0~9的十六進位值為其本身，十進位10~15的十六進位值為A~F。

#### 範例輸入1

```
13
```

#### 範例輸出1

```
D
```

#### 範例輸入2

```
8
```

#### 範例輸出2

```
8
```

---
#### Solution
```python linenums="1"
a = eval(input())
if((a<=15) & (a >=0)):
	if(a == 10):
		print("A")
	elif(a == 11):
		print("B")
	elif(a == 12):
		print("C")
	elif(a == 13):
		print("D")
	elif(a == 14):
		print("E")
	elif(a == 15):
		print("F")
	else:
		print("{}".format(a))
```

>[!hint]
>注意要對輸入的數值作區別，若超過16則不會有任何印出的內容

- Reference
	- [TQC+ 程式語言Python 208 十進位換算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-208-%e5%8d%81%e9%80%b2%e4%bd%8d%e6%8f%9b%e7%ae%97/)
