#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入四個數字x1、y1、x2、y2，分別代表兩個點的座標(x1, y1)、(x2, y2)。計算並輸出這兩點的座標與其歐式距離。

> [!hint]
> 歐式距離 =
> $$\sqrt{(x1−x2)^2+(y1−y2)^2}$$
> 兩座標的歐式距離，輸出到小數點後第4位


#### 範例輸入

```
2
1
5.5
8
```

#### 範例輸出

```
( 2 , 1 )
( 5.5 , 8 )
Distance = 7.8262
```

---
#### Solution
```python linenums="1"
x1 = eval(input())
y1 = eval(input())
x2 = eval(input())
y2 = eval(input())
a = (x1 - x2)**2
b = (y1 - y2)**2
c = (a + b)**0.5
print("( {} , {} )".format(x1, y1))
print("( {} , {} )".format(x2, y2))
print("Distance = %.4f"%c)
```
- Reference
	- [TQC+ 程式語言Python 108 座標距離計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-108-%e5%ba%a7%e6%a8%99%e8%b7%9d%e9%9b%a2%e8%a8%88%e7%ae%97/)