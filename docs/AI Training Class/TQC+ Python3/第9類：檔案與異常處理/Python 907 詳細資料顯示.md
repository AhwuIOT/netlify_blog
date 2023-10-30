#Python #String #TQC 
#### 題目說明：

請撰寫一程式，要求使用者輸入檔名read.txt，顯示該檔案的行數、單字數（簡單起見，單字以空白隔開即可，忽略其它標點符號）以及字元數（不含空白）。

#### 範例輸入

```
read.txt
```

#### 範例輸出

```
6 line(s)
102 word(s)
614 character(s)
```
---
#### read.txt檔案內容
```
What is Python language?
Python is a widely used high-level, general-purpose, interpreted, dynamic programming language.
Its design philosophy emphasizes code readability, and its syntax allows programmers to express concepts in fewer lines of code than possible in languages such as C++ or Java.
Python supports multiple programming paradigms, including object-oriented, imperative and functional programming or procedural styles.
It features a dynamic type system and automatic memory management and has a large and comprehensive standard library.
The best way we learn anything is by practice and exercise questions. We have started this section for those (beginner to intermediate) who are familiar with Python.
```

---
#### Solution

```python linenums="1" 
f_name = input()

f_line = f_word = f_char = 0

f = open(f_name, 'r')

for line in f:

	f_line += 1
	
	f_word += len(line.split())
	
	f_char += sum(len(i)for i in line.split())

print("%d line(s)"%f_line)

print("%d word(s)"%f_word)

print("%d character(s)"%f_char)
```
- Reference
	- [TQC+ 程式語言Python 907 詳細資料顯示 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-907-%e8%a9%b3%e7%b4%b0%e8%b3%87%e6%96%99%e9%a1%af%e7%a4%ba/)
	- [Read a file line by line in Python - GeeksforGeeks](https://www.geeksforgeeks.org/read-a-file-line-by-line-in-python/)
- Link
	- [[Python中逐行讀取]]
	