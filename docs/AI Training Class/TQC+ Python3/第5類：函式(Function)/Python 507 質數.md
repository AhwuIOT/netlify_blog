#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入一個整數x，並將x傳遞給名為compute()的函式，此函式將回傳x是否為質數（Prime number）的布林值，接著再將判斷結果輸出。如輸入值為質數顯示【Prime】，否則顯示【Not Prime】。

#### 範例輸入1

```
3
```

#### 範例輸出1

```
Prime
```

#### 範例輸入2

```
6
```

#### 範例輸出2

```
Not Prime
```

#### 範例輸入3

```
1
```

#### 範例輸出3

```
Not Prime
```

#### 範例輸入4

```
0
```

#### 範例輸出4

```
Not Prime
```

#### 範例輸入5

```
-5
```

#### 範例輸出5

```
Not Prime
```

---
#### Solution
```python linenums="1"
def compute(n):
  if n < 2:
    return False
  elif(n!=2):
    for i in range(2, n):
      if(n % i == 0):
        return False
      else:
        return True
  else:
    return True
      

a = eval(input())
if((a == 0 )| (a == 1)):
	print("Not Prime")
elif(compute(a)):
	print("Prime")
else:
	print("Not Prime")
```

> [!tip]
> 可以將比2小的數都設為Not Prime

- Reference
	- [TQC+ 程式語言Python 507 質數 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-507-%e8%b3%aa%e6%95%b8/)