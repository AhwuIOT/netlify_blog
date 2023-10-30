#### 題目說明：

請撰寫一程式，要求使用者輸入檔名read.txt，以及檔案中某單字出現的次數。輸出符合次數的單字，並依單字的第一個字母大小排序。（單字的判斷以空白隔開即可）

#### 範例輸入

```
read.txt
3
```

#### 範例輸出

```
a
is
programming
```
#### read.txt檔案內容
```  
What is Python language
Python is a widely used high level general purpose interpreted dynamic programming language
Its design philosophy emphasizes code readability and its syntax allows programmers to express concepts in fewer lines of code than possible in languages such as C or Java
Python supports multiple programming paradigms including object oriented imperative and functional programming or procedural styles
It features a dynamic type system and automatic memory management and has a large and comprehensive standard library
The best way we learn anything is by practice and exercise questions We have started this section for those beginner to intermediate who are familiar with Python
```

----
#### Solution 

[[#解題思路]]

```python linenums="1"
f_name = input()
f = open(f_name, 'r')
l = []
D = {}
n = eval(input())
for line in f:
  for i in line.split():
    if i in D:
      D[i] += 1
    else:
      D[i] = 1
for j in D:
  if D[j] == n:
    l.append(j)

l.sort()

for result in l:
  print(result)

```
---
#### 解題思路
1. `f_name = input()`：程式會提示使用者輸入一個檔案名稱，並將輸入的值存儲在`f_name`變數中。
    
2. `f = open(f_name, 'r')`：打開指定名稱的檔案，使用讀取模式（'r'）。
    
3. `l = []`：創建一個空的列表`l`，用於存儲結果。
    
4. `D = {}`：創建一個空的字典`D`，用於存儲單詞計數。
    
5. `n = eval(input())`：提示使用者輸入一個數字，並將輸入的值存儲在`n`變數中。
    
6. `for line in f:`：對於讀取的檔案的每一行，執行以下操作。
    
7. `for i in line.split():`：對於==每一行中的單詞==，使用`split()`函式將其分割成單詞列表，並遍歷該列表。
    
8. `if i in D:`：==檢查字典`D`中是否已經存在該單詞。==
    
9. `D[i] += 1`：如果字典`D`已經存在該單詞，則將其計數加1。
    
10. `else:`：如果字典`D`中不存在該單詞，則執行以下操作。
    
11. `D[i] = 1`：在字典`D`中創建一個新的鍵值對，鍵是該單詞，值為1。
    
12. `for j in D:`：對於字典`D`中的每個鍵，執行以下操作。
    
13. `if D[j] == n:`：檢查該鍵對應的值是否等於輸入的數字`n`。
    
14. `l.append(j)`：如果該鍵對應的值等於`n`，則將該鍵添加到列表`l`中。
    
15. `l.sort()`：對列表`l`中的元素進行排序。
    
16. `for result in l:`：對於列表`l`中的每個元素，執行以下操作。
    
17. `print(result)`：輸出該元素。
    

總結來說，這段程式碼的目的是讀取一個檔案，將檔案中的單詞進行計數，然後找出在檔案中出現次數為指定數字的單詞並按字母順序輸出。

- Reference
	- [TQC+ 程式語言Python 908 單字次數計算](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-908-%e5%96%ae%e5%ad%97%e6%ac%a1%e6%95%b8%e8%a8%88%e7%ae%97/)
- Link
	- [[split()用法]]
