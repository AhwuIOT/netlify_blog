#Python #TQC 
#### 題目說明：

請使用選擇敘述撰寫一程式，讓使用者輸入一個正整數，然後判斷它是否為偶數（even）。

#### 範例輸入1

```
56
```

#### 範例輸出1

```
56 is an even number.
```

#### 範例輸入2

```
21
```

#### 範例輸出2

```
21 is not an even numb
```

---
#### Solution
```python linenums="1"
a = eval(input())
if (a % 2 == 0):
	print("{} is an even number.".format(a))
else:
	print("{} is not an even number.".format(a))
```

- Reference 
	- [TQC+ 程式語言Python 201 偶數判斷 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-201-%e5%81%b6%e6%95%b8%e5%88%a4%e6%96%b7/)