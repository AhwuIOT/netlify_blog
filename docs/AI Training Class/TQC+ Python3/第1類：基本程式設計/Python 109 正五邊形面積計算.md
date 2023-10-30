#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入一個正數s，代表正五邊形之邊長，計算並輸出此正五邊形之面積（Area）。

> [!hint]
> 提示1：建議使用import math模組的math.pow及math.tan  
> 提示2：正五邊形面積的公式：
> $$Area=(5∗s^2)/(4∗tan(pi/5))$$
> 
> Area=(5∗s2)/(4∗tan(pi/5))  
> 提示3：輸出浮點數到小數點後第四位。

#### 範例輸入

```
5
```

#### 範例輸出

```
Area = 43.0119
```

---
#### Solution
```python linenums="1"
import math
x = eval(input())
a = (5*(x**2)) / (4*math.tan(math.pi/5))
print("Area = %.4f"%a)
```
- Reference
	- [TQC+ 程式語言Python 109 正五邊形面積計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-109-%e6%ad%a3%e4%ba%94%e9%82%8a%e5%bd%a2%e9%9d%a2%e7%a9%8d%e8%a8%88%e7%ae%97/)