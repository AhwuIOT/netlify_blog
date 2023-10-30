#Python #TQC 
#### 題目說明：

(1) 請撰寫一程式，以不定數迴圈的方式讓使用者輸入西元年份，然後判斷它是否為閏年（leap year）或平年。其判斷規則如下：每四年一閏，每百年不閏，但每四百年也一閏。  
(2) 假設此不定數迴圈輸入-9999則會結束此迴圈。

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示

2017  
**2017 is not a leap year.**  
2000  
**2000 is a leap year.**  
2016  
**2016 is a leap year.**  
2009  
**2009 is not a leap year.**  
2018  
**2018 is not a leap year.**  
-9999

---
#### Solution
```python linenums="1" linenums="1"
while True:
	n = eval(input())
	if(n == -9999): break
	else:
		if((n % 4 == 0) & (n % 100 !=0) | (n % 400 == 0)):
			print("{} is a leap year.".format(n))
		else:
			print("{} is not a leap year.".format(n))
```

- Reference
	- [TQC+ 程式語言Python 407 不定數迴圈-閏年判斷 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-407-%e4%b8%8d%e5%ae%9a%e6%95%b8%e8%bf%b4%e5%9c%88-%e9%96%8f%e5%b9%b4%e5%88%a4%e6%96%b7/)