- Reference
	- https://stackoverflow.com/questions/31593201/how-are-iloc-and-loc-different

兩者之間主要差別在於:

- `loc` 根據特定的**標籤**選取行（和/或列）
    
- `iloc` 根據整數**位置**選取行（和/或列）
    

為了說明，我們設定一個具有索引的pandas字符序列 `s`：
```python
>>> s = pd.Series(list("abcdef"), index=[49, 48, 47, 0, 1, 2]) 
49    a
48    b
47    c
0     d
1     e
2     f

>>> s.loc[0]    # value at index label 0
'd'

>>> s.iloc[0]   # value at index location 0
'a'

>>> s.loc[0:1]  # rows at index labels between 0 and 1 (inclusive)
0    d
1    e

>>> s.iloc[0:1] # rows at index location between 0 and 1 (exclusive)
49    a
```

以下是當傳入不同對象時，`s.loc` 和 `s.iloc` 之間的一些區別/相似之處：

|<對象>|描述|`s.loc[<object>]`|`s.iloc[<object>]`|
|---|---|---|---|
|`0`|單項|_索引標籤_ 處的值`0`（字符串`'d'`）|_索引位置_0處的值（字符串`'a'`）|
|`0:1`|切片|**兩**行（標籤`0`和`1`）|**一行**（第一行位於位置 0）|
|`1:47`|具有越界末端的切片|**零**行（空系列）|**五行**（位置 1 開始）|
|`1:47:-1`|帶有負步長的切片|**三行**（標籤`1`返回`47`）|**零**行（空系列）|
|`[2, 0]`|整數列表|具有給定標籤的**兩行**|具有給定位置的**兩行**|
|`s > 'e'`|Bool系列（表示哪些值具有該屬性）|**一**排（含`'f'`）|`NotImplementedError`|
|`(s>'e').values`|布爾數組|**一**排（含`'f'`）|和...一樣`loc`|
|`999`|int 對像不在索引中|`KeyError`|`IndexError`（出界）|
|`-1`|int 對像不在索引中|`KeyError`|返回最後一個值`s`|
|`lambda x: x.index[3]`|可調用應用於系列（此處返回索引中的第三項）|`s.loc[s.index[3]]`|`s.iloc[s.index[3]]`|
`loc` 的標籤查詢功能遠不止於整數索引，值得強調一些額外的例子。

以下是一個索引包含字符串對象的 Series：

```python
>>> s2 = pd.Series(s.index, index=s.values)
>>> s2
a    49
b    48
c    47
d     0
e     1
f     2
```

由於 `loc` 是基於標籤的，因此可以使用 `s2.loc['a']` 獲取 Series 中的第一個值。它還可以使用非整數對象進行切片：

```python
>>> s2.loc['c':'e']  # all rows lying between 'c' and 'e' (inclusive)
c    47
d     0
e     1
```

對於 DateTime 索引，我們不需要傳入完整的日期/時間來根據標籤進行查詢。例如：

```python
>>> s3 = pd.Series(list('abcde'), pd.date_range('now', periods=5, freq='M')) 
>>> s3
2021-01-31 16:41:31.879768    a
2021-02-28 16:41:31.879768    b
2021-03-31 16:41:31.879768    c
2021-04-30 16:41:31.879768    d
2021-05-31 16:41:31.879768    e
```

那麼，只需要以下程式碼就可以獲取 2021 年 3 月/4 月的行數據：

```python
>>> s3.loc['2021-03':'2021-04']
2021-03-31 17:04:30.742316    c
2021-04-30 17:04:30.742316    d
```

## Rows and Columns

`loc` 和 `iloc` 在處理 DataFrame 時的工作方式與處理 Series 時相同。值得注意的是，這兩種方法都可以同時對列和行進行索引。

當給定一個元組時，第一個元素用於索引列，如果存在第二個元素，則用於索引行。

下面定義一個 DataFrame：

```python
>>> import numpy as np 
>>> df = pd.DataFrame(np.arange(25).reshape(5, 5),  
                      index=list('abcde'), 
                      columns=['x','y','z', 8, 9])
>>> df
    x   y   z   8   9
a   0   1   2   3   4
b   5   6   7   8   9
c  10  11  12  13  14
d  15  16  17  18  19
e  20  21  22  23  24
```

Then for example:

```python
>>> df.loc['c': , :'z']  # rows 'c' and onwards AND columns up to 'z'
    x   y   z
c  10  11  12
d  15  16  17
e  20  21  22

>>> df.iloc[:, 3]        # all rows, but only the column at index location 3
a     3
b     8
c    13
d    18
e    23
```

有時我們希望混合使用標籤和位置索引方法來對行和列進行索引，以某種方式結合 `loc` 和 `iloc` 的功能。

例如，請看以下的 DataFrame。該如何最好地對`列`進行切片，包括 `c`，並選取前四個行？

```python
>>> import numpy as np 
>>> df = pd.DataFrame(np.arange(25).reshape(5, 5),  
                      index=list('abcde'), 
                      columns=['x','y','z', 8, 9])
>>> df
    x   y   z   8   9
a   0   1   2   3   4
b   5   6   7   8   9
c  10  11  12  13  14
d  15  16  17  18  19
e  20  21  22  23  24
```

我們可以使用`iloc`的方​​法來實現這個結果：:

```python
>>> df.iloc[:df.index.get_loc('c') + 1, :4]
    x   y   z   8
a   0   1   2   3
b   5   6   7   8
c  10  11  12  13
```

[`get_loc()`](http://pandas.pydata.org/pandas-docs/version/0.19.1/generated/pandas.Index.get_loc.html)是一個索引方法，意思是“獲取該索引中標籤的位置”。請注意，由於切片 with `iloc`不包括其端點，==因此如果我們也想要行“c”，則必須向該值加 1。==