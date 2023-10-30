#Python #TQC 
#### 題目說明：

請撰寫一程式，輸入X組和Y組各自的科目至集合中，以字串”end”作為結束點（集合中不包含字串”end”）。請依序分行顯示(1) X組和Y組的所有科目、(2)X組和Y組的共同科目、(3)Y組有但X組沒有的科目，以及(4) X組和Y組彼此沒有的科目（不包含相同科目）。

>[!hint]
>科目須參考範例輸出樣本，依字母由小至大進行排序。

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示

**Enter group X’s subjects:**  
Math  
Literature  
English  
History  
Geography  
end  
**Enter group Y’s subjects:**  
Math  
Literature  
Chinese  
Physical  
Chemistry  
end  
**[‘Chemistry’, ‘Chinese’, ‘English’, ‘Geography’, ‘History’, ‘Literature’, ‘Math’, ‘Physical’]**  
**[‘Literature’, ‘Math’]**  
**[‘Chemistry’, ‘Chinese’, ‘Physical’]**  
**[‘Chemistry’, ‘Chinese’, ‘English’, ‘Geography’, ‘History’, ‘Physical’]**

---
#### Solution
```python linenums="1"
X = set()
print("Enter group X's subjects:")
while True:
  a = input()
  if(a == "end"):break
  else:
    X.add(a)
Y = set()
print("Enter group Y's subjects:")
while True:
  a = input()
  if(a == "end"):break
  else:
    Y.add(a)
print(sorted(X | Y))
print(sorted(X & Y))
print(sorted(Y - X))
print(sorted(X ^ Y))
```
- Reference
	- [TQC+ 程式語言Python 707 共同科目](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-707-%e5%85%b1%e5%90%8c%e7%a7%91%e7%9b%ae/)
