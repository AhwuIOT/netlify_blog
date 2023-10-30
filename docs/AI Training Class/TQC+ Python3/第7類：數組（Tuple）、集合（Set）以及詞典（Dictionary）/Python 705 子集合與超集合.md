#Python #TQC 
#### 題目說明：

請撰寫一程式，依序輸入五個、三個、九個整數，並各自儲存到集合set1、set2、set3中。接著回答：set2是否為set1的子集合（subset）？set3是否為set1的超集合（superset）？

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示

**Input to set1:**  
3  
28  
-2  
7  
39  
**Input to set2:**  
2  
77  
0  
**Input to set3:**  
3  
28  
12  
99  
39  
7  
-1  
-2  
65  
**set2 is subset of set1: False**  
**set3 is superset of set1: True**

---
#### Solution
```python linenums="1"
S1 = set()
S2 = set()
S3 = set()
print("Input to set1:")
for i in range(5):
	S1.add(eval(input()))
print("Input to set2:")
for i in range(3):
	S2.add(eval(input()))
print("Input to set3:")
for i in range(9):
	S3.add(eval(input()))
print("set2 is subset of set1:", S2.issubset(S1))
print("set3 is superset of set1:", S3.issuperset(S1))
```

> [!attention]
> 注意題目需要的語法issubset()；issuperset()


- Reference
	- [TQC+ 程式語言Python 705 子集合與超集合](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-705-%e5%ad%90%e9%9b%86%e5%90%88%e8%88%87%e8%b6%85%e9%9b%86%e5%90%88/)
