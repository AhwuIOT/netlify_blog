#Python #TQC 
#### 題目說明：

全字母句（Pangram）是英文字母表所有的字母都出現至少一次（最好只出現一次）的句子。請撰寫一程式，要求使用者輸入一正整數k（代表有k筆測試資料），每一筆測試資料為一句子，程式判斷該句子是否為Pangram，並印出對應結果True（若是）或False（若不是）。

> [!hint]
> 不區分大小寫字母

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示 第1組

3  
The quick brown fox jumps over the lazy dog  
**True**  
Learning Python is funny  
**False**  
Pack my box with five dozen liquor jugs  
**True**

---

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示 第2組

2  
Quick fox jumps nightly above wizard  
**True**  
These can be weapons of terror  
**False**

---
#### Solution
```python linenums="1"
n = eval(input())
for i in range(n):
  Str = input()
  check = set(Str.lower())
  check.remove(' ')
  print(len(check)==26)
```

> [!attention]
> 注意要用lower()把所有字母轉為小寫，然後去掉空白

- Reference
	- [TQC+ 程式語言Python 706 全字母句](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-706-%e5%85%a8%e5%ad%97%e6%af%8d%e5%8f%a5/)