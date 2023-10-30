#Python #TQC 
#### 題目說明：

請撰寫一程式，以不定數迴圈的方式輸入一個正整數（代表分數），之後根據以下分數與GPA的對照表，印出其所對應的GPA。假設此不定數迴圈輸入-9999則會結束此迴圈。標準如下表所示：

|分　數|GPA|
|---|---|
|90 ~ 100|A|
|80 ~ 89|B|
|70 ~ 79|C|
|60 ~ 69|D|
|0 ~ 59|E|

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示

75  
**C**  
39  
**E**  
100  
**A**  
85  
**B**  
65  
**D**  
-9999


---
#### Solution
```python linenums="1"
while True:
  a = eval(input())
  if (a == -9999):break
  elif((a >= 0) & (a <=100)):
    if((a >=90) & (a <=100)):
      print('A')
    elif((a >=80) & (a <90)):
      print('B')
    elif((a >=70) & (a <80)):
      print('C')
    elif((a >=60) & (a <70)):
      print('D')
    else:
      print('E')
```
- Reference
	- [TQC+ 程式語言Python 405 不定數迴圈-分數等級 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-405-%e4%b8%8d%e5%ae%9a%e6%95%b8%e8%bf%b4%e5%9c%88-%e5%88%86%e6%95%b8%e7%ad%89%e7%b4%9a/)