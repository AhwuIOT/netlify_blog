#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入兩個正整數x、y，並將x與y傳遞給名為compute()的函式，此函式回傳x和y的最大公因數。

#### 範例輸入1

```
12,8
```

#### 範例輸出1

```
4
```

#### 範例輸入2

```
4,6
```

#### 範例輸出2

```
2
```

--- 
#### Solution
```python linenums="1"
import math
def compute(x, y):
	return (math.gcd(x,y))
a, b = eval(input())
print(compute(a, b))
```

>[!attention]
>注意這裡的輸入，是x,y = eval(input())，輸入時用逗號隔開代表兩個輸入內容

- Reference
	- [TQC+ 程式語言Python 508 最大公因數 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-508-%e6%9c%80%e5%a4%a7%e5%85%ac%e5%9b%a0%e6%95%b8/)