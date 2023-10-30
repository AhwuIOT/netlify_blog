#Python #TQC 
#### 題目說明：

請使用選擇敘述撰寫一程式，根據使用者輸入的分數顯示對應的等級。標準如下表所示：

|分　數|等級|
|---|---|
|80 ~ 100|A|
|70 ~ 79|B|
|60 ~ 69|C|
|<= 59|F|

#### 範例輸入

```
79
```

#### 範例輸出

```
B
```

---
#### Solution

```python linenums="1"
a = eval(input())
if((a >= 80) & (a <= 100)):
  print('A')
elif((a >=70) & (a < 80)):
  print('B')
elif((a >= 60) & (a < 70)):
  print('C')
else:
  print('F')
```

- Reference
	- [TQC+ 程式語言Python 206 等級判斷 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-206-%e7%ad%89%e7%b4%9a%e5%88%a4%e6%96%b7/)