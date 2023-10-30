#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入一個正整數，將此正整數以反轉的順序輸出，並判斷如輸入0，則輸出為0。

#### 範例輸入1

```
31283
```

#### 範例輸出1

```
38213
```

#### 範例輸入2

```
0
```

#### 範例輸出2

```
0
```

#### 範例輸入3

```
135790
```

#### 範例輸出3

```
097531
```

---
#### Solution
```python linenums="1" linenums="1"
a = input()
print(a[::-1])
```

>[!attention]
>不用太拘泥於正整數

- Reference
	- [TQC+ 程式語言Python 404 數字反轉判斷 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-404-%e6%95%b8%e5%ad%97%e5%8f%8d%e8%bd%89%e5%88%a4%e6%96%b7/)