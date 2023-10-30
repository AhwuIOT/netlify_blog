#Python #TQC 
#### 題目說明：

請使用選擇敘述撰寫一程式，讓使用者輸入一個字元，判斷它是包括大、小寫的英文字母（alphabet）、數字（number）、或者其它字元（symbol）。例如：a為英文字母、9為數字、$為其它字元。

#### 範例輸入1

```
P
```

#### 範例輸出1

```
P is an alphabet.
```

#### 範例輸入2

```
@
```

#### 範例輸出2

```
@ is a symbol.
```

#### 範例輸入3

```
7
```

#### 範例輸出3

```
7 is a number.
```

---
#### Solution

```python linenums="1"
a = input()
if(a.isdigit()):
	print("{} is a number.".format(a))
elif(a.isalpha()):
	print("{} is an alphabet.".format(a))
else:
	print("{} is a symbol.".format(a))
```


> [!Note]
> 要注意因題目說只有一個字元輸入，所以不需要太去在意超過了一個字元後的可能性

- Reference
	- [TQC+ 程式語言Python 205 字元判斷 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-205-%e5%ad%97%e5%85%83%e5%88%a4%e6%96%b7/)