#Python #TQC 
#### 題目說明：

請撰寫一程式，輸入一圓的半徑，並加以計算此圓之面積和周長，最後請印出此圓的半徑（Radius）、周長（Perimeter）和面積（Area）。

> [!hint]
>提示1：需import math模組，並使用math.pi。  
>提示2：輸出浮點數到小數點後第二位。

#### 範例輸入1

```
10
```

#### 範例輸出1

```
Radius = 10.00
Perimeter = 62.83
Area = 314.16
```

#### 範例輸入2

```
2.5
```

#### 範例輸出2

```python linenums="1"
Radius = 2.50
Perimeter = 15.71
Area = 19.63
```

---
#### Solution
```python linenums="1"
import math
a = eval(input())
print("Radius = %.2f"%a)
print("Perimeter = %.2f"%((a*2)*math.pi))
print("Area = %.2f"%((a**2)*math.pi))
```
- Reference
	- [TQC+ 程式語言Python 104 圓形面積計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-104-%e5%9c%93%e5%bd%a2%e9%9d%a2%e7%a9%8d%e8%a8%88%e7%ae%97/)