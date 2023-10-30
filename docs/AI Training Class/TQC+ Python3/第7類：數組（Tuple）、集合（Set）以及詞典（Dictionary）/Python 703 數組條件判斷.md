#Python #TQC 
#### 題目說明：

請撰寫一程式，輸入一些字串至數組（至少輸入五個字串），以字串”end”為結束點（數組中不包含字串”end”）。接著輸出該數組，再分別顯示該數組的第一個元素到第三個元素和倒數三個元素。

#### 範例輸入

```
president
dean
chair
staff
teacher
student
end
```

#### 範例輸出

```
('president', 'dean', 'chair', 'staff', 'teacher', 'student')
('president', 'dean', 'chair')
('staff', 'teacher', 'student')
```

---
#### Solution
```python linenums="1"
l = []
while True:
  a = input()
  if(a == "end"):break
  else:
    l.append(a)

t = tuple(l)
print(t)
print(t[0:3])
print(t[-3::])
```
- Reference
	- [TQC+ 程式語言Python 703 數組條件判斷](https://jbprogramnotes.com/2020/05/tqc-%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80python-703-%E6%95%B8%E7%B5%84%E6%A2%9D%E4%BB%B6%E5%88%A4%E6%96%B7/)