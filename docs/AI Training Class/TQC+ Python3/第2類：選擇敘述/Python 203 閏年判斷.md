#Python #TQC 
#### 題目說明：

請使用選擇敘述撰寫一程式，讓使用者輸入一個西元年份，然後判斷它是否為閏年（leap year）或平年。其判斷規則為：每四年一閏，每百年不閏，但每四百年也一閏。

#### 範例輸入1

```
1992
```

#### 範例輸出1

```
1992 is a leap year.
```

#### 範例輸入2

```
2010
```

#### 範例輸出2

```
2010 is not a leap year.
```

---
#### Solution

```python linenums="1"
a = eval(input())
if ((a % 4 == 0) & (a % 100 != 0)|(a % 400 == 0)):
	print("{} is a leep year.".format(a))
else:
	print("{} is not a leep year.".format(a))
```
- Reference
	- [TQC+ 程式語言Python 203 閏年判斷 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-203-%e9%96%8f%e5%b9%b4%e5%88%a4%e6%96%b7/)