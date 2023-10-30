#Python #TQC 
#### 題目說明：

假設一賽跑選手在x分y秒的時間跑完z公里，請撰寫一程式，輸入x、y、z數值，最後顯示此選手每小時的平均英哩速度（1英哩等於1.6公里）。

> [!hint]
> 輸出浮點數到小數點後第一位。

#### 範例輸入

```
10
25
3
```

#### 範例輸出

```
Speed = 10.8
```

---
#### Solution
```python linenums="1"
x = eval(input())
y = eval(input())
z = eval(input())
print("Speed = %.1f"%(z/1.6/((y/60+x)/60)))
```

> [!tip]
> 平均英哩 = 英哩 / 小時
> 公哩 / 1.6 = 英哩
> 分 / 60 = 小時
- Reference
	- [TQC+ 程式語言Python 106 公里英哩換算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-106-%e5%85%ac%e9%87%8c%e8%8b%b1%e5%93%a9%e6%8f%9b%e7%ae%97/)