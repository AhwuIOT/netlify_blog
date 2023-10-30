#Python #String #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入一字串和一字元，並將此字串及字元作為參數傳遞給名為compute()的函式，此函式將回傳該字串中指定字元出現的次數，接著再輸出結果。

#### 範例輸入

```
Our country is beautiful
u
```

#### 範例輸出

```
u occurs 4 time(s)
```


---
#### Solution

```python linenums="1"
def compute(Str, s):
	return Str.count(s)
Str = input()
s = input()
print("{} occurs {} time(s)".format(s, compute(Str, s)))
```

> [!attention]
> 注意count()使用方法

- Reference
	- [TQC+ 程式語言Python 806 字元次數計算](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-806-%e5%ad%97%e5%85%83%e6%ac%a1%e6%95%b8%e8%a8%88%e7%ae%97/)