#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入三位學生各五筆成績，接著再計算並輸出每位學生的總分及平均分數。

>[!hint]
>平均分數輸出到小數點後第二位。

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示

**The 1st student:**  
78  
89  
88  
70  
60  
**The 2nd student:**  
90  
78  
66  
68  
78  
**The 3rd student:**  
69  
97  
70  
89  
90  
**Student 1**  
**\#Sum 385**  
**\#Average 77.00**  
**Student 2**  
**\#Sum 380**  
**\#Average 76.00**  
**Student 3**  
**\#Sum 415**  
**\#Average 83.00**

---
#### Solution
```python linenums="1"
ID = ["1st", "2nd", "3rd"]
def compute(x):
  SUM = [0]*x
  for i in range(x):
    print("The {} student:".format(ID[i]))
    for j in range(5):
      SUM[i] += eval(input())
  return SUM

l = compute(3)
for i in range(3):
	print("Student %d"%(i+1))
	print("#Sum %d"%l[i])
	print("#Average %.2f"%(l[i]/5))

```

>[!attention]
>注意印出的號碼

- Reference
	- [TQC+ 程式語言Python 607 成績計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-607-%e6%88%90%e7%b8%be%e8%a8%88%e7%ae%97/)