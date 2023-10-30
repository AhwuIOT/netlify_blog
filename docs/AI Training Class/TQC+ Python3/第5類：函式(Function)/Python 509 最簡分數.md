#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入二個分數，分別是x/y和m/n（其中x、y、m、n皆為正整數），計算這兩個分數的和為p/q，接著將p和q傳遞給名為compute()函式，此函式回傳p和q的最大公因數（Greatest Common Divisor, GCD）。再將p和q各除以其最大公因數，最後輸出的結果必須以最簡分數表示。

#### 範例輸入1

```
1,2
1,6
```

#### 範例輸出1

```
1/2 + 1/6 = 2/3
```

#### 範例輸入2

```
12,16
18,32
```

#### 範例輸出2

```
12/16 + 18/32 = 21/16
```

---
#### Solution
```python linenums="1"
import math
def compute(x, y):
	return math.gcd(x, y)
x, y = eval(input())
m, n = eval(input())
p = int((x * n + y * m) /(compute(x * n + y * m, y * n)))
q = int(y * n / (compute(x * n + y * m, y * n)))
print("{}/{} + {}/{} = {}/{}".format(x,y,m,n,p,q))
	
```

> [!attention]
> 小心除完後會是浮點數的話記得要轉為int數

- Reference
	- [TQC+ 程式語言Python 509 最簡分數 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-509-%e6%9c%80%e7%b0%a1%e5%88%86%e6%95%b8/)