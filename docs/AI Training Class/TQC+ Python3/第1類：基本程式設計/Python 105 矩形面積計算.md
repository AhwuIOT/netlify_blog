#Python #TQC 
#### 題目說明：

請撰寫一程式，輸入兩個正數，代表一矩形之寬和高，計算並輸出此矩形之高（Height）、寬（Width）、周長（Perimeter）及面積（Area）。

> [!hint]
> 輸出浮點數到小數點後第二位。

#### 範例輸入

```
23.5
19
```

#### 範例輸出

```
Height = 23.50
Width = 19.00
Perimeter = 85.00
Area = 446.50 
```

---
#### Solution
```python linenums="1"
h = eval(input())
w = eval(input())
print("Height = %.2f"%h)
print("Width = %.2f"%w)
print("Perimeter = %.2f"%((w+h)*2))
print("Area = %.2f"%(w*h))
```
- Reference
	- [TQC+ 程式語言Python 105 矩形面積計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-105-%e7%9f%a9%e5%bd%a2%e9%9d%a2%e7%a9%8d%e8%a8%88%e7%ae%97/)
