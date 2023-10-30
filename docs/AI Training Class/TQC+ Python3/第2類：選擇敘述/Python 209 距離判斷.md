#Python #TQC 
#### 題目說明：

請使用選擇敘述撰寫一程式，讓使用者輸入一個點的平面座標x和y值，判斷此點是否與點(5, 6)的距離小於或等於15，如距離小於或等於15顯示【Inside】，反之顯示【Outside】。

> [!hint]
> 計算平面上兩點距離的公式：
> $$\sqrt{(x1−x2)^2+(y1−y2)^2}$$


#### 範例輸入1

```
7
20
```

#### 範例輸出1

```
Inside
```

#### 範例輸入2

```
30
35
```

#### 範例輸出2

```
Outside
```

---
#### Solution
```python linenums="1"
x = eval(input())
y = eval(input())
d = (((5 - x)**2)+((6 - y)**2))**0.5
if(d <= 15):
	print("Inside")
else:
	print("Outside")
```

- Reference
	- [TQC+ 程式語言Python 209 距離判斷 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-209-%e8%b7%9d%e9%9b%a2%e5%88%a4%e6%96%b7/)
- Link
	- [[Python 108 座標距離計算]]