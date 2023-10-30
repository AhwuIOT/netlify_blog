#### 題目說明：

請撰寫一程式，將使用者輸入的五個人的資料寫入data.dat檔，每一個人的資料為姓名和電話號碼，以空白分隔。再將檔案加以讀取並顯示檔案內容。

#### 範例輸入

```
Karen 123456789
Bonnie 235689147
Simon 987612345
Louis 675489321
Andy 019238475
```

#### 範例輸出

```
The content of "data.dat":
Karen 123456789

Bonnie 235689147

Simon 987612345

Louis 675489321

Andy 019238475
```

#### Solution
1.  **用二進制encoding
```python linenums="1"
with open("data.dat", "w", encoding = "utf-8") as f:
  for i in range(5):
    f.write(input()+"\n")
print('The content of "data.dat":')
with open("data.dat", "r", encoding = "utf-8")as f:
  for i in f:
    print(i)
```
2. **一般讀檔寫檔**
```python linenums="1"
# 寫入資料到檔案
with open('data.dat', 'w') as file:
    for _ in range(5):
        data = input()
        file.write(f"{data}\n")

# 讀取並顯示檔案內容
with open('data.dat', 'r') as file:
    content = file.read()
    print('The content of "data.dat":')
    print(content)
```

- Reference
	- [TQC+ 程式語言Python 909 聯絡人資料](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-909-%e8%81%af%e7%b5%a1%e4%ba%ba%e8%b3%87%e6%96%99/)
- Link
	- [[檔案讀寫參數]]