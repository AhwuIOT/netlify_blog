#Python #TQC 
#### 題目說明：

請使用選擇敘述撰寫一程式，讓使用者輸入一個正整數，然後判斷它是3或5的倍數，顯示【x is a multiple of 3.】或【x is a multiple of 5.】；若此數值同時為3與5的倍數，顯示【x is a multiple of 3 and 5.】；如此數值皆不屬於3或5的倍數，顯示【x is not a multiple of 3 or 5.】，將使用者輸入的數值代入x。

#### 範例輸入1

```
55
```

#### 範例輸出1

```
55 is a multiple of 5.
```

#### 範例輸入2

```
36
```

#### 範例輸出2

```
36 is a multiple of 3.
```

#### 範例輸入3

```
92
```

#### 範例輸出3

```
92 is not a multiple of 3 or 5.
```

#### 範例輸入4

```
15
```

#### 範例輸出4

```
15 is a multiple of 3 and 5.
```

---
#### Solution

```python linenums="1"
def func(x):
  if((x % 3 == 0) & (x % 5 != 0)):
    print(f'{x} is a multiple of 3.')
  elif((x % 3 != 0) & (x % 5 ==0)):
    print(f'{x} is a multiple of 5.')
  elif((x % 3 != 0) & (x % 5 !=0)):
    print(f'{x} is not a multiple of 3 and 5.')
  else:
    print(f'{x} is a multiple of 3 and 5.')

x = eval(input())
func(x)

```
- Reference
	- [TQC+ 程式語言Python 202 倍數判斷 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-202-%e5%80%8d%e6%95%b8%e5%88%a4%e6%96%b7/)