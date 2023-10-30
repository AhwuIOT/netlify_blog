#Python #TQC 
#### 題目說明：

請使用迴圈敘述撰寫一程式，讓使用者輸入一個正整數（<100），然後以三角形的方式依序輸出此數的相乘結果。
>[!hint]
>輸出欄寬為4，且需靠右對齊。

#### 範例輸入1

```
5
```

#### 範例輸出1

```
   1
   2   4
   3   6   9
   4   8  12  16
   5  10  15  20  25
```

#### 範例輸入2

```
12
```

#### 範例輸出2

```
   1
   2   4
   3   6   9
   4   8  12  16
   5  10  15  20  25
   6  12  18  24  30  36
   7  14  21  28  35  42  49
   8  16  24  32  40  48  56  64
   9  18  27  36  45  54  63  72  81
  10  20  30  40  50  60  70  80  90 100
  11  22  33  44  55  66  77  88  99 110 121
  12  24  36  48  60  72  84  96 108 120 132 144
```

---
#### Solution
```python linenums="1"
a = eval(input())
if(a < 100):
	for i in range(1, a+1):
		for j in range(1, i+1):
			print("{:>4d}".format(j*i), end = "")
		print()
```

> [!tip]
> 注意這個  j*i

- Reference
	- [TQC+ 程式語言Python 303 迴圈數值相乘 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-303-%e8%bf%b4%e5%9c%88%e6%95%b8%e5%80%bc%e7%9b%b8%e4%b9%98/)
	- [Python 中的 [:-1] 和 [::-1] (runoob.com)](https://www.runoob.com/note/51257)
