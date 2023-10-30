#Python #TQC 
#### 題目說明：

請撰寫一程式，輸入數個整數並儲存至集合，以輸入-9999為結束點（集合中不包含-9999），最後顯示該集合的長度（Length）、最大值（Max）、最小值（Min）、總和（Sum）。

#### 範例輸入

```
34
-23
29
7
0
-1
-9999
```

#### 範例輸出

```
Length: 6
Max: 34
Min: -23
Sum: 46
```

---
#### Solution
```python linenums="1"
S = set()
while True:
  a = eval(input())
  if(a == -9999):break
  else:
    S.add(a)

print("Length: %d"%len(S))
print('Max: %d'%max(S))
print('Min: %d'%min(S))
print('Sum: %d'%sum(S))
```
- Reference
	- [Python3 集合]https://www.runoob.com/python3/python3-set.html