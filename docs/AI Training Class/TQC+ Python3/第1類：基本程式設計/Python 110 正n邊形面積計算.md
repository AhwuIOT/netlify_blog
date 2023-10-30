#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入兩個正數n、s，代表正n邊形之邊長為s，計算並輸出此正n邊形之面積（Area）。

> [!hitn]
> 提示1：建議使用import math模組的math.pow及math.tan  
> 提示2：正n邊形面積的公式如下：
> $$Area=(n∗s^2)/(4∗tan(pi/n)) $$
> 提示3：輸出浮點數到小數點後第四位

#### 範例輸入

```
8
6
```

#### 範例輸出

```
Area = 173.8234
```

---
#### Solution
```python linenums="1"
import math
n = eval(input())
s = eval(input())
a = (n*(s**2)) / (4*math.tan(math.pi/n))
print("Area = %.4f"%a)

```
- Reference
	- [TQC+ 程式語言Python 110 正n邊形面積計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-110-%e6%ad%a3n%e9%82%8a%e5%bd%a2%e9%9d%a2%e7%a9%8d%e8%a8%88%e7%ae%97/)