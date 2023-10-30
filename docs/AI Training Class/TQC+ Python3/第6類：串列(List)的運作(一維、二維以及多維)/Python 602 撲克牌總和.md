#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入52張牌中的5張，計算並輸出其總和。

> 提示：J、Q、K以及A分別代表11、12、13以及1。

#### 範例輸入

```
5
10
K
3
A
```

#### 範例輸出

```
32
```

---
#### Solution
```python linenums="1"
result = 0
for i in range(5):
  a = input()
  if (a == 'J'): result += 11
  elif(a == 'Q'): result += 12
  elif(a == 'K'): result += 13
  elif(a == 'A'): result += 1
  elif(int(a)<11):
    result += int(a)
print(result)
```
- Reference
	- [TQC+ 程式語言Python 602 撲克牌總和 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-602-%e6%92%b2%e5%85%8b%e7%89%8c%e7%b8%bd%e5%92%8c/)