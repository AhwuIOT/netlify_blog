#Python #String 
#### 說明
在Python中，`split()`是一個內建函式，用於將字符串分割成子字符串列表。它的用法如下：

```python
string.split(sep=None, maxsplit=-1)
```

`split()`方法可以接受兩個可選的參數：`sep`和`maxsplit`。以下是參數的說明：

- `sep`（可選）：指定用於分割字符串的分隔符。默認情況下，分隔符為空格。`sep`可以是一個字符串，也可以是多個字符串的元組。如果省略該參數，則使用空格作為分隔符。
- `maxsplit`（可選）：指定最大分割次數。默認情況下，`maxsplit`為-1，表示不限制分割次數。如果指定了正整數，則最多進行`maxsplit`次分割。

`split()`方法返回一個列表，其中包含分割後的子字符串。

#### 範例
以下是一些示例：

```python
# 使用默認的空格分隔符分割字符串
sentence = "Hello, world! How are you?"
words = sentence.split()
print(words)
# 輸出: ['Hello,', 'world!', 'How', 'are', 'you?']

# 使用逗號作為分隔符分割字符串
numbers = "1,2,3,4,5"
num_list = numbers.split(',')
print(num_list)
# 輸出: ['1', '2', '3', '4', '5']

# 使用冒號和空格作為分隔符分割字符串
data = "John:25 Mary:30 David:28"
info_list = data.split(': ')
print(info_list)
# 輸出: ['John', '25 Mary', '30 David', '28']

# 限制分割次數為2
sentence = "Hello, world, how, are, you?"
words = sentence.split(', ', 2)
print(words)
# 輸出: ['Hello', 'world', 'how, are, you?']
```

這些示例展示了如何使用`split()`方法在不同的情境下將字符串分割成子字符串列表。通過指定不同的分隔符和分割次數，您可以根據需要進行自定義的字符串分割操作。