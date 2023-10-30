#Python #String #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入一個句子（至少有五個詞，以空白隔開），並輸出該句子倒數三個詞。

#### 範例輸入

```
Many foreign students study in FJU
```

#### 範例輸出

```
study in FJU
```
---
#### Solution
```python linenums="1"
n = input()
l = n.split()
for i in range(3):
	print(l[-3+i], end = " ")
```
或者使用join() =>
```python linenums="1"
a = input()
l = a.split()

print(' '.join(l[-3::]))
```

---
#### join()的用法
在Python 3中，`join()`是一個用於字符串操作的內置方法，用於將序列中的字符串元素連接為一個單獨的字符串。

`join()`方法是由一個字符串（稱為分隔符）調用的，並且它接受一個可迭代的對象（如列表、元組等）作為參數。它會將可迭代對象中的每個元素轉換為字符串，然後使用分隔符將它們連接起來形成一個新的字符串。

以下是使用`join()`方法的示例：

```python linenums="1"
my_list = ['Hello', 'World', 'Python']
result = ' '.join(my_list)
print(result)
# 輸出：Hello World Python

my_tuple = ('apple', 'banana', 'cherry')
result = '-'.join(my_tuple)
print(result)
# 輸出：apple-banana-cherry

my_string = 'Hello, World!'
result = ''.join(my_string.split(', '))
print(result)
# 輸出：HelloWorld!
```

在這些示例中，我們使用了不同的可迭代對象（列表、元組、字串），並使用不同的分隔符（空格、連字符、空字符串）來調用`join()`方法。該方法將元素連接成一個新的字符串。

需要注意的是，`join()`方法僅適用於包含字符串元素的可迭代對象。如果可迭代對象包含非字符串元素，將會拋出一個`TypeError`異常。在使用`join()`方法之前，確保將所有元素轉換為字符串，以便順利進行連接操作。

- Reference
	- [TQC+ 程式語言Python 803 倒數三個詞](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-803-%e5%80%92%e6%95%b8%e4%b8%89%e5%80%8b%e8%a9%9e/)