#Python #file 
### 方法一:使用readlines()逐行讀取
---
> [!Note] 
一般來說readlines()會一次讀取全部的行，並且將每行內容變為字串元素並且以List方式作為返回值格式
> 
#### 另一個語法readline()與readlines()差別如下:
|方法|描述|
|---|---|
|`readlines()`|讀取整個檔案的內容並以行為單位返回一個包含每行文字的列表 (list)。|
|`readline()`|每次只讀取檔案的一行文字，每次呼叫該方法會進行一次讀取，並返回該行文字。|

---

#### 範例
```python
# 假設有一個名為example.txt的檔案，其內容如下：
# Hello
# World
# This is an example file.

# 使用readlines()方法讀取檔案
with open('example.txt', 'r') as file:
    lines = file.readlines()
    print(lines)
    # 輸出: ['Hello\n', 'World\n', 'This is an example file.']

# 使用readline()方法讀取檔案
with open('example.txt', 'r') as file:
    line1 = file.readline()
    line2 = file.readline()
    print(line1)
    # 輸出: 'Hello\n'
    print(line2)
    # 輸出: 'World\n'

```

- Reference
	- [Read a file line by line in Python - GeeksforGeeks](https://www.geeksforgeeks.org/read-a-file-line-by-line-in-python/)
	