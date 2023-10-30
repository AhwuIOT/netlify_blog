#### 題目說明：

請撰寫一程式，要求使用者讀入read.dat（以UTF-8編碼格式讀取），第一列為欄位名稱，第二列之後是個人記錄。請輸出檔案內容並顯示男生人數和女生人數（根據”性別”欄位，0為女性、1為男性）。

#### 範例輸出

```
學號 姓名 性別 科系

101 陳小華 0 餐旅管理

202 李小安 1 廣告

303 張小威 1 英文

404 羅小美 0 法文

505 陳小凱 1 日文
Number of males: 3
Number of females: 2
```
#### read.dat檔案內容(請先存成.dat檔案)
```
學號 姓名 性別 科系
101 陳小華 0 餐旅管理
202 李小安 1 廣告
303 張小威 1 英文
404 羅小美 0 法文
505 陳小凱 1 日文
```

#### Solution
- **偷雞方式：不看index只看數字**
```python linenums="1"
D = {'male':0, 'females':0}
with open('read.dat', 'r', encoding='utf-8') as f:
    content = f.read()
    print(content)
    for i in content.split():
       if i == '1':
           D['females']  += 1
       elif i == '0':
           D['male'] += 1
print("Number of males:%d"%(D['male']))
print("Number of females:%d"%(D['females']))
```
- **最好用index**
```python linenums="1"
females = male = 0
with open("read.dat", 'r', encoding='utf-8')as f:
    content = f.readlines()
    for i in content:
        print(i)
        if i.split()[2]== '1':
            females += 1
        elif i.split()[2] == '0':
            male += 1
print("Number of male:%d"%male)
print("Number of females:%d"%females)
```

- Reference 
	- [TQC+ 程式語言Python 910 學生基本資料](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-910-%e5%ad%b8%e7%94%9f%e5%9f%ba%e6%9c%ac%e8%b3%87%e6%96%99/)
- Link
	- [[split()用法]]
	- [[Python中逐行讀取]]
