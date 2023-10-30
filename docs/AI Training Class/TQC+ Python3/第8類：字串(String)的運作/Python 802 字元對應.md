#Python #TQC #String 
#### 題目說明：

請撰寫一程式，要求使用者輸入一字串，顯示該字串每個字元的對應ASCII碼及其總和。

#### 範例輸入

```
Kingdom
```

#### 範例輸出

```
ASCII code for 'K' is 75
ASCII code for 'i' is 105
ASCII code for 'n' is 110
ASCII code for 'g' is 103
ASCII code for 'd' is 100
ASCII code for 'o' is 111
ASCII code for 'm' is 109
713
```

---
#### Solution
```python linenums="1"
n = input()
SUM = 0
for i in range(len(n)):
	print("ASCII code for {} is {}".format(n[i], ord(n[i])))
	SUM += ord(n[i])
print(SUM)
```

---
#### ord()的使用方式
在Python 3中，`ord()`是一個內置函數，用於獲取給定字元的Unicode碼點（code point）。Unicode是一個標準，它為每個字符分配了一個唯一的數字值，這些數字值被稱為碼點。

`ord()`函數接受一個單個字符作為參數，並返回該字符的Unicode碼點值。它可以接受字串中的第一個字符，或者你可以直接傳遞字符。

以下是一些示例：

```python linenums="1"
print(ord('A'))  # 輸出：65
print(ord('a'))  # 輸出：97
print(ord('€'))  # 輸出：8364
```

在這些示例中，`ord()`函數返回了'A'、'a'和'€'這些字符對應的Unicode碼點值。這些碼點值可以用於字符比較、轉換或其他需要使用Unicode的操作。

需要注意的是，`ord()`函數僅適用於單個字符。如果你嘗試將一個包含多個字符的字串傳遞給`ord()`函數，將會拋出一個`TypeError`異常。

- Reference
	- [TQC+ 程式語言Python 802 字元對應](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-802-%e5%ad%97%e5%85%83%e5%b0%8d%e6%87%89/)