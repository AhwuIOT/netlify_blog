#Python #TQC 
#### 題目說明：

某次選舉有兩位候選人，分別是No.1: Nami、No.2: Chopper。請撰寫一程式，輸入五張選票，輸入值如為1即表示針對1號候選人投票；輸入值如為2即表示針對2號候選人投票，如輸入其他值則視為廢票。每次投完後需印出目前每位候選人的得票數，最後印出最高票者為當選人；如最終計算有相同的最高票數者或無法選出最高票者，顯示【=> No one won the election.】。

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示

2  
**Total votes of No.1: Nami =  0**  
**Total votes of No.2: Chopper =  1**  
**Total null votes =  0**  
1  
**Total votes of No.1: Nami =  1**  
**Total votes of No.2: Chopper =  1**  
**Total null votes =  0**  
8  
**Total votes of No.1: Nami =  1**  
**Total votes of No.2: Chopper =  1**  
**Total null votes =  1**  
2  
**Total votes of No.1: Nami =  1**  
**Total votes of No.2: Chopper =  2**  
**Total null votes =  1**  
2  
**Total votes of No.1: Nami =  1**  
**Total votes of No.2: Chopper =  3**  
**Total null votes =  1**  
**=> No.2 Chopper won the election.**

---
#### Solution
```python linenums="1" linenums="1"
no1 = no2 = no3 = 0

for i in range(5):
	n = input()
	if(n=="1"):
		no1 += 1
		print("Total votes of No.1: Nami = %d"%no1)
		print("Total votes of No.2: Chopper = %d"%no2)
		print("Total null votes = %d"%no3)
	elif(n=="2"):
		no2 += 1
		print("Total votes of No.1: Nami = %d"%no1)
		print("Total votes of No.2: Chopper = %d"%no2)
		print("Total null votes = %d"%no3)
	else:
		no3 += 1
		print("Total votes of No.1: Nami = %d"%no1)
		print("Total votes of No.2: Chopper = %d"%no2)
		print("Total null votes = %d"%no3)
if(no1 > no2):
	print("No.1 Nami won the election.")
elif(no2 > no1):
	print("No.2 Chopper won the election.")
else:
	print("No one won the election.")
```
- Reference
	- [TQC+ 程式語言Python 409 得票數計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-409-%e5%be%97%e7%a5%a8%e6%95%b8%e8%a8%88%e7%ae%97/)