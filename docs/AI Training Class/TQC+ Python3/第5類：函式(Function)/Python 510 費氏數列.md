#Python #TQC 
#### 題目說明：

請撰寫一程式，計算費氏數列（Fibonacci numbers），使用者輸入一正整數num (num>=2)，並將它傳遞給名為compute()的函式，此函式將輸出費氏數列前num個的數值。

> 提示：費氏數列的某一項數字是其前兩項的和，而且第0項為0，第一項為1，表示方式如下：  
$$F_0=0$$$$F_1 = 1$$ $$F_n - F_{n-1} + F_{n-2}$$


#### 範例輸入1

```
10
```

#### 範例輸出1

```
0 1 1 2 3 5 8 13 21 34 
```

#### 範例輸入2

```
20
```

#### 範例輸出2

```
0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987 1597 2584 4181 
```

---
#### Solution
```python linenums="1"
def compute(x):
	if(x > 1):
		return compute(x - 1) + compute(x - 2)
	return x
for i in range(eval(input())):
	print(compute(i), end = " ")
```

> [!attention]
> 記住用遞迴來做運算會最快

- Reference
	- [費波那契數列 ( 費氏數列 ) - Python 教學 | STEAM 教育學習網 (oxxostudio.tw)](https://steam.oxxostudio.tw/category/python/example/fibonacci.html)
	- [TQC+ 程式語言Python 510 費氏數列 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-510-%e8%b2%bb%e6%b0%8f%e6%95%b8%e5%88%97/)