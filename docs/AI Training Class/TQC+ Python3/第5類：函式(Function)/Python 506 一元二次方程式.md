#Python #TQC 
#### 題目說明：

請撰寫一程式，將使用者輸入的三個整數（代表一元二次方程式$$ ax^2+bx+c=0  $$
的三個係數a、b、c）作為參數傳遞給一個名為compute()的函式，該函式回傳方程式的解，如無解則輸出【Your equation has no root.】

> 提示：輸出有順序性

#### 範例輸入1

```
2
-3
1
```

#### 範例輸出1

```
1.0, 0.5
```

#### 範例輸入2

```
9
9
8
```

#### 範例輸出2

```
Your equation has no root.
```

---
#### Solution
```python linenums="1"
import math
def compute(a, b, c):
	if (b**2 - 4*a*c >= 0):
		ans1 = (-b + math.sqrt(b**2 - 4 * a* c)) / (2 * a)
		ans2 = (-b - math.sqrt(b**2 - 4 * a* c)) / (2 * a)
		return ans1, ans2
	else:
		return 0
a = eval(input())
b = eval(input())
c = eval(input())
if(compute(a, b, c)!=0):
	ans1, ans2 = compute(a, b, c)
	print("{} {}".format(ans1, ans2))
else:
	print('Your equation has no root.')
```
- Reference
	- [TQC+ 程式語言Python 506 一元二次方程式 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-506-%e4%b8%80%e5%85%83%e4%ba%8c%e6%ac%a1%e6%96%b9%e7%a8%8b%e5%bc%8f/)