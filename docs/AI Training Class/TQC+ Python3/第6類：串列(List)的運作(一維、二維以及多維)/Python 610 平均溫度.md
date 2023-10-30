#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入四週各三天的溫度，接著計算並輸出這四週的平均溫度及最高、最低溫度。

> 提示1：平均溫度輸出到小數點後第二位。  
> 提示2：最高溫度及最低溫度的輸出，如為31時，則輸出31，如為31.1時，則輸出31.1。

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示，輸入值以紅字表示。

**Week 1:**

**Day 1:**23.1

**Day 2:**24

**Day 3:**23.5

**Week 2:**

**Day 1:**32

**Day 2:**33

**Day 3:**35.5

**Week 3:**

**Day 1:**29

**Day 2:**30

**Day 3:**26

**Week 4:**

**Day 1:**27.6

**Day 2:**25

**Day 3:**28.8

**Average: 28.13**

**Highest: 35.5**

**Lowest: 23.1**

---
#### Solution
```python linenums="1"
def compute(w, d):
  """
  用空list接資料最好
  """
  l = []

  for i in range(w):
    print("Week %d"%(i+1))
    for j in range(d):
      print("Day %d:"%(j+1),end = '')
      l.append(eval(input()))

  print("Average:%.2f"%(sum(l)/(w*d)))
  print("Highest:{}".format(max(l)))
  print("Lowest:{}".format(min(l)))
compute(4, 3)
```
- Reference
	- [TQC+ 程式語言Python 610 平均溫度 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-610-%e5%b9%b3%e5%9d%87%e6%ba%ab%e5%ba%a6/)