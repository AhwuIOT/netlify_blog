#Python #TQC 
#### 題目說明：

請撰寫一程式，輸入數個整數並儲存至串列中，以輸入-9999為結束點（串列中不包含-9999），再將此串列轉換成數組，最後顯示該數組以及其長度（Length）、最大值（Max）、最小值（Min）、總和（Sum）。

#### 範例輸入

```
-4
0
37
19
26
-43
9
-9999
```

#### 範例輸出

```
(-4, 0, 37, 19, 26, -43, 9)
Length: 7
Max: 37
Min: -43
Sum: 44
```
---
#### Solution
```python linenums="1"
l = []
while True:
	n = eval(input())
	if(n!=-9999):
		l.append(n)
	else:
		break
t = tuple(l)
print(t)
print("Length: %d"%(len(t)))
print("Max: %d"%max(t))
print("Min: %d"%min(t))
print("Sum: %d"%sum(t))
```
- Reference
	- [TQC+ 程式語言Python 701 串列數組轉換](https://jbprogramnotes.com/2020/05/tqc-%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80python-701-%E4%B8%B2%E5%88%97%E6%95%B8%E7%B5%84%E8%BD%89%E6%8F%9B/)
	