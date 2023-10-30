#Python #TQC 
#### 題目說明：

請使用選擇敘述撰寫一程式，讓使用者輸入三個邊長，檢查這三個邊長是否可以組成一個三角形。若可以，則輸出該三角形之周長；否則顯示【Invalid】。

>[!hint]
>檢查方法 = 任意兩個邊長之總和大於第三邊長。

#### 範例輸入1

```
5
6
13
```

#### 範例輸出1

```
Invalid
```

#### 範例輸入2

```
1
1
1
```

#### 範例輸出2

```
3
```

---
#### Solution
```python linenums="1"
a = eval(input())
b = eval(input())
c = eval(input())
if(((a+b)> c)&((a+c)>b)&((c+b)>a)):
	print("{}".format(a+b+c))
else:
	print("Invalid")
```
- Reference
	- [TQC+ 程式語言Python 210 三角形判斷 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-210-%e4%b8%89%e8%a7%92%e5%bd%a2%e5%88%a4%e6%96%b7/)