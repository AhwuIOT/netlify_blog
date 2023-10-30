#Python #TQC 
#### 題目說明：

請撰寫一程式，以不定數迴圈的方式輸入身高與體重，計算出BMI之後再根據以下對照表，印出BMI及相對應的BMI代表意義（State）。假設此不定數迴圈輸入-9999則會結束此迴圈。標準如下表所示：

|BMI值|代表意義|
|---|---|
|BMI < 18.5|under weight|
|18.5 <= BMI < 25|normal|
|25.0 <= BMI < 30|over weight|
|30 <= BMI|fat|

> [!hint]
> BMI=體重(kg)/身高^2(m)，輸出浮點數到小數點後第二位。 不需考慮男性或女性標準。

#### 輸入與輸出會交雜如下，輸出的部份以粗體字表示
176  
80  
**BMI: 25.83**  
**State: over weight**  
170  
100  
**BMI: 34.60**  
**State: fat**  
-9999


---
#### Solution
```python linenums="1" linenums="1"
H = eval(input())
while H!= -9999:
  W = eval(input())
  BMI = W/((H/100)**2)
  if(BMI < 18.5):
    print(f'%.2f'%BMI)
    print(f'State:under weight')
  elif((BMI < 25) & (BMI >= 18.5)):
    print(f'%.2f'%BMI)
    print(f'State:normal')
  elif((BMI < 30) & (BMI >= 25)):
    print(f'%.2f'%BMI)
    print(f'State:over weight')
  else:
    print(f'%.2f'%BMI)
    print(f'State:fat')
  H = eval(input())
```

>[!attention]
>只輸入一次-9999就要break

- Reference
	- [TQC+ 程式語言Python 406 不定數迴圈-BMI計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-406-%e4%b8%8d%e5%ae%9a%e6%95%b8%e8%bf%b4%e5%9c%88-bmi%e8%a8%88%e7%ae%97/)