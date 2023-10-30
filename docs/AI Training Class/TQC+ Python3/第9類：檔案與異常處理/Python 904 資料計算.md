#Python #TQC #file 
#### 題目說明：

請撰寫一程式，讀取read.txt（每一列的格式為名字和身高、體重，以空白分隔）並顯示檔案內容、所有人的平均身高、平均體重以及最高者、最重者。

> 提示：輸出浮點數到小數點後第二位。

#### 範例輸出

```
Ben 175 65

Cathy 155 55

Tony 172 75
Average height: 167.33
Average weight: 65.00
The tallest is Ben with 175.00cm
The heaviest is Tony with 75.00kg
```
#### read.txt檔案內容
```
Ben 175 65
Cathy 155 55
Tony 172 75
```

---
#### Solution
```python linenums="1"
f = open("read.txt", 'r')
N = []
W = []
H = []
for i in f.readlines():
  print(i)
  line = i.split()
  N.append(line[0])
  H.append(int(line[1]))
  W.append(int(line[2]))

print("Average height: {:.2f}".format(sum(H) / 3))
print("Average weight: {:.2f}".format(sum(W) / 3))
print("The tallest is {} with {:.2f}cm".format(N[H.index(max(H))], max(H)))
print("The heaviest is {} with {:.2f}kg".format(N[W.index(max(W))], max(W)))
"""

其他寫法:

data = []

  

with open("read.txt","r") as file:

   for line in file:

       print(line)

       data.append(line.split())

  

name = [data[n][0] for n in range(3)]

height = [eval(data[h][1]) for h in range(3)]

weight = [eval(data[w][2]) for w in range(3)]

  

print('Average height: %.2f' %(sum(height) / 3))

print('Average weight: %.2f' %(sum(weight) / 3))

print('The tallest is %s with %.2fcm' %(name[height.index(max(height))], max(height)))

print('The heaviest is %s with %.2fkg' %(name[weight.index(max(weight))], max(weight)))

"""
```

>[!attention]
>要記得讀取檔案的結果值都是字串，要算平均記得要轉換成int格式


- Reference
	- [TQC+ 程式語言Python 904 資料計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-904-%e8%b3%87%e6%96%99%e8%a8%88%e7%ae%97/)
- Link
	- [[檔案讀寫參數]]