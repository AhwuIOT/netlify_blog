#Python #String #TQC 
#### 題目說明：

請撰寫一程式，要求使用者輸入一個長度為6的字串，將此字串分別置於10個欄位的寬度的左邊、中間和右邊，並顯示這三個結果，左右皆以直線 |（Vertical bar）作為邊界。

#### 範例輸入

```
python
```

#### 範例輸出

```
|python    |
|  python  |
|    python|
```

---
#### Solution

```python linenums="1"
n = input()
print("|{:<10s}|".format(n))
print("|{}|".format(n.center(10)))
print("|{:>10s}|".format(n))
```

>[!attention]
>注意n.center()用法

- Reference
	- [TQC+ 程式語言Python 805 字串輸出](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-805-%e5%ad%97%e4%b8%b2%e8%bc%b8%e5%87%ba/)