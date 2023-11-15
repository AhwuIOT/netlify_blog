#Python #TQC 
#### 題目說明：

請使用選擇敘述撰寫一程式，要求使用者輸入購物金額，購物金額需大於8,000（含）以上，並顯示折扣優惠後的實付金額。購物金額折扣方案如下表所示：

|金　　額|折　扣|
|---|---|
|8,000（含）以上|9.5折|
|18,000（含）以上|9折|
|28,000（含）以上|8折|
|38,000（含）以上|7折|

#### 範例輸入

```
12000
```

#### 範例輸出

```
11400.0
```

---
#### Solution
```python linenums="1"
a = eval(input())
if(a >= 38000):
	print("{}".format(a*0.7))
elif((a >= 28000) & (a < 38000)):
	print("{}".format(a*0.8))
elif((a >= 18000) & (a < 28000)):
	print("{}".format(a*0.9))
elif(a >= 8000):
	print("{}".format(a*0.95))
else:
	print("{}".format(a))
```

- Reference
	- [TQC+ 程式語言Python 207 折扣方案 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-207-%e6%8a%98%e6%89%a3%e6%96%b9%e6%a1%88/)