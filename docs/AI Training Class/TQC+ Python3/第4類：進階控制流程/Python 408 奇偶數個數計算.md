#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入十個整數，計算並輸出偶數和奇數的個數。

#### 範例輸入

```
69
48
19
91
83
22
18
37
82
40
```

#### 範例輸出

```
Even numbers: 5
Odd numbers: 5
```

---
#### Solution
```python linenums="1" linenums="1"
even = 0
odd = 0
for i in range(10):
	a = eval(input())
	if(a % 2 == 0):
		even += 1
	else:
		odd += 1
print("Even numbers: %d"%even)
print("Odd numbers: %d"%odd)
```

- Reference
	- [TQC+ 程式語言Python 408 奇偶數個數計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-408-%e5%a5%87%e5%81%b6%e6%95%b8%e5%80%8b%e6%95%b8%e8%a8%88%e7%ae%97/)