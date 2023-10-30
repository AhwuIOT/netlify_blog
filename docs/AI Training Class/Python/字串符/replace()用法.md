#Python #String 
```python
str.replace(old, new[, max])
"""
- old -- 将被替换的子字符串。
- new -- 新字符串，用于替换old子字符串。
- max -- 可选字符串, 替换不超过 max 次
"""
```

---
```python
str = str = "this is string example....wow!!! this is really string"
print(str.replace("is", "was"))
print(str.replace("is", "was", 3))
"""
Output:
thwas was string example....wow!!! thwas was really string
thwas was string example....wow!!! thwas is really string
"""
```