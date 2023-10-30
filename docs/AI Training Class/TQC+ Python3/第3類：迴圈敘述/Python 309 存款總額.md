#Python #TQC 
#### 題目說明：

請使用迴圈敘述撰寫一程式，提示使用者輸入金額（如10,000）、年收益率（如5.75），以及經過的月份數（如5），接著顯示每個月的存款總額。


>[!hint]
>四捨五入，輸出浮點數到小數點後第二位。

舉例：  
假設您存款$10,000，年收益為5.75%。  
過了一個月，存款會是：10000 + 10000 * 5.75 / 1200 = 10047.92  
過了兩個月，存款會是：10047.92 + 10047.92 * 5.75 / 1200 = 10096.06  
過了三個月，存款將是：10096.06 + 10096.06 * 5.75 / 1200 = 10144.44  
以此類推。

#### 範例輸入

```
50000
1.3
5
```

#### 範例輸出

```
Month    Amount
  1   50054.17
  2   50108.39
  3   50162.68
  4   50217.02
  5   50271.42
```

---
#### Solution
```python linenums="1"
money = eval(input())
p = eval(input())
m = eval(input())
SUM = money
print("Month\tAmount")
for i in range(1, m+1):
	SUM = SUM + (SUM * (p / 1200))
	print("{}\t{:.2f}".format(i, SUM))
```

> [!attention]
> 題目中沒提及輸出格式所以應該不用太在意

- Reference
	- [TQC+ 程式語言Python 309 存款總額 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-309-%e5%ad%98%e6%ac%be%e7%b8%bd%e9%a1%8d/)