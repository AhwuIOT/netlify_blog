#Python #TQC 
#### 題目說明：

請使用選擇敘述撰寫一程式，讓使用者輸入兩個整數a、b，然後再輸入一算術運算子 (+、-、*、/、//、%） ，輸出經過運算後的結果。

#### 範例輸入

```
30
20
*
```

#### 範例輸出

```
600
```

---
#### Solution

```python linenums="1"
a = eval(input())
b = eval(input())
c = input()
match c:
	case "+":
		print("{}".format(a+b))
	case "-":
		print("{}".format(a-b))
	case "*":
		print("{}".format(a*b))
	case "/":
		print("{}".format(a/b))	
	case "//":
		print("{}".format(a//b))
	case "%":
		print("{}".format(a%b))
```


>[!tip]
>如果使用match不行，也可直接使用if... elif...


- Reference
	- [TQC+ 程式語言Python 204 算術運算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-204-%e7%ae%97%e8%a1%93%e9%81%8b%e7%ae%97/)
	- [match/case比對](https://openhome.cc/zh-tw/python/flow-control/match-case/#matchcase-模式比對)