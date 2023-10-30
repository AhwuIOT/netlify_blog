#Python 
#### 用法:
在Python中，可以使用`sort()`方法對列表進行排序。該方法可以根據預設的升序排序規則對列表進行排序，也可以通過參數指定其他排序方式。

#### 範例:
以下是使用`sort()`方法的範例：

```python
# 範例1：對數字列表進行排序（升序）
numbers = [5, 2, 8, 1, 6]
numbers.sort()
print(numbers)  # 輸出: [1, 2, 5, 6, 8]

# 範例2：對字串列表進行排序（按照字母順序）
fruits = ['apple', 'banana', 'orange', 'kiwi']
fruits.sort()
print(fruits)  # 輸出: ['apple', 'banana', 'kiwi', 'orange']

# 範例3：對列表進行排序並指定遞減排序
numbers = [5, 2, 8, 1, 6]
numbers.sort(reverse=True)
print(numbers)  # 輸出: [8, 6, 5, 2, 1]

# 範例4：使用自訂的排序規則對列表進行排序
def custom_sort(element):
    # 假設希望按照元素長度進行排序
    return len(element)

fruits = ['apple', 'banana', 'orange', 'kiwi']
fruits.sort(key=custom_sort)
print(fruits)  # 輸出: ['kiwi', 'apple', 'banana', 'orange']

```

在這些範例中，`sort()`方法被應用於不同的列表，並且使用不同的參數來達到不同的排序目的。根據需求，你可以根據自己的情況選擇適合的排序方式和參數。