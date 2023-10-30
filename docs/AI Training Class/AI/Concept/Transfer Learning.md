> [!Reference]
> 1. [Transfer Learning 轉移學習](https://medium.com/%E6%88%91%E5%B0%B1%E5%95%8F%E4%B8%80%E5%8F%A5-%E6%80%8E%E9%BA%BC%E5%AF%AB/transfer-learning-%E8%BD%89%E7%A7%BB%E5%AD%B8%E7%BF%92-4538e6e2ffe4)
> 2. [【QA】什麼是轉移學習（Transfer learning ）？](https://www.cupoy.com/qa/club/ai_tw/0000016D6BA22D97000000016375706F795F72656C656173654B5741535354434C5542/0000017B7B67ABF8000000276375706F795F72656C656173655155455354)
> 3. [Transfer Learning遷移學習](https://hackmd.io/@allen108108/H1MFrV9WH)
> 4. [A Newbie-Friendly Guide to Transfer Learning](https://www.v7labs.com/blog/transfer-learning-guide#transfer-learning-in-6-steps)

#### 目的
---
> ** 1.Source Data 與 Target Data 理解為不同的空間 ( Domain ) 中的資料點。由於 Source Data 已經有標籤完成，也就是說在 Source Domain 上已經有一個分類器可以將其分類。但在 Target Domain 上我們無法找出這樣的分類器。**
>
>**2. 希望做的事情就是將兩個不同 Domain 的資料點 map 到另外一個空間，在這個新的空間中，讓 Source Data 與 Target Data 的分布盡量接近，而且Source Data 在新空間中仍然可以被分類。這樣我們就可以利用 Source Data 協助 Target Data 進行分類。**


==也就是說：Transfer Learning就是把已經訓練好的模型、參數，轉移至另外的一個新模型上，讓新模型不必在重新設定許多東西==

From:[https://hackmd.io/@allen108108/H1MFrV9WH](https://hackmd.io/@allen108108/H1MFrV9WH#:~:text=Source%20Data%20%E8%88%87%20Target%20Data%20%E7%90%86%E8%A7%A3%E7%82%BA%E4%B8%8D%E5%90%8C%E7%9A%84%E7%A9%BA%E9%96%93%20(%20Domain%20)%20%E4%B8%AD%E7%9A%84%E8%B3%87%E6%96%99%E9%BB%9E%E3%80%82%E7%94%B1%E6%96%BC%20Source%20Data%20%E5%B7%B2%E7%B6%93%E6%9C%89%E6%A8%99%E7%B1%A4%E5%AE%8C%E6%88%90%EF%BC%8C%E4%B9%9F%E5%B0%B1%E6%98%AF%E8%AA%AA%E5%9C%A8%20Source%20Domain%20%E4%B8%8A%E5%B7%B2%E7%B6%93%E6%9C%89%E4%B8%80%E5%80%8B%E5%88%86%E9%A1%9E%E5%99%A8%E5%8F%AF%E4%BB%A5%E5%B0%87%E5%85%B6%E5%88%86%E9%A1%9E%E3%80%82%E4%BD%86%E5%9C%A8%20Target%20Domain%20%E4%B8%8A%E6%88%91%E5%80%91%E7%84%A1%E6%B3%95%E6%89%BE%E5%87%BA%E9%80%99%E6%A8%A3%E7%9A%84%E5%88%86%E9%A1%9E%E5%99%A8%E3%80%82)

#### 為什麼這麼做？
1. 數據標記耗時
2. 別人已經完成的訓練是否可以拿來借鑒？
3. 不同的訓練資料集是否彼此也有一定程度的辨識項目重疊性？

---
#### 方法分類
- Based on parameter
	- 權重分配對Source與Target進行移轉
	- 如果在Source有樣本和Target非常相似的話我們就可以加大此樣本的對應權重
- Based on features
	- 將Source和Target的特徵變換到同一空間
	- 基於特徵的方法轉換原始特徵以創建新的特徵表示。這種方法可以進一步分為兩個子類別，即非對稱和對稱基於特徵的遷移學習。
		- 非對稱方法轉換源特徵以匹配目標特徵。換句話說，我們從源域中獲取特徵並將它們擬合到目標特徵空間中。由於特徵分佈的邊際差異，在此過程中可能會丟失一些信息。
		- 對稱方法找到一個共同的潛在特徵空間，然後將源特徵和目標特徵轉換為這種新的特徵表示。
- Based on instance
	- 涵蓋了一個簡單的場景，其中Source中存在大量標記數據，而Target中的標記數據數量有限。域和特徵空間僅在邊緣分佈上有所不同。
		例如，假設我們需要建立一個模型來診斷老年人佔多數的特定區域的癌症。給出的目標域實例有限，並且可以從另一個年輕人佔多數的地區獲得相關數據。直接從另一個地區轉移所有數據可能會不成功，因為存在邊際分佈差異，並且老年人比年輕人患癌症的風險更高。在這種情況下，很自然地要考慮調整邊際分佈。基於實例的遷移學習將權重重新分配給損失函數中的Source實例。
- Based on relationship
	- 基於關係的遷移學習方法主要側重於學習源域和目標域之間的關係，並使用這些知識來導出過去的知識並在當前的上下文中使用它。
	- 這種方法將源域中學到的邏輯關係或規則轉移到目標域。
	- 例如，如果我們了解男性聲音中語音不同元素之間的關係，則可以顯著幫助分析另一種聲音中的句子。

From:[A Newbie-Friendly Guide to Transfer Learning](v7labs.com/blog/transfer-learning-guide)

#### 實際操作
1. 獲取以訓練好的模型
	- 第一步是根據任務的需求，選擇一個我們希望作為基礎訓練的預訓練模型。轉移學習要求預訓練源模型的知識與目標任務領域之間有著強烈的相關性，以確保它們是相容的。
		- 以下是一些可供使用的預訓練模型：
			用於計算機視覺任務：
			- VGG-16 
			- VGG-19 
			- Inception V3 
			- XCeption 
			- ResNet-50 
			用於自然語言處理任務：
			- Word2Vec 
			- GloVe 
			- FastText
2. 建立Base Model
	- 基礎模型是我們在第一步中選擇的架構之一，比如ResNet或Xception，與我們的任務密切相關。我們可以下載網絡權重，以節省額外訓練模型的時間。否則，我們需要使用網絡架構來從頭開始訓練模型。
	- 在某些情況下，基礎模型的最終輸出層的神經元數量可能會超過我們在使用案例中所需的數量。在這種情況下，我們需要刪除最終輸出層並相應地進行修改。
3. 凍結各層網路
	- 凍結來自預訓練模型的初始層對於避免使模型學習基本特徵非常重要。
	- 如果我們不凍結初始層，將會失去已經進行的所有學習。這將與從頭訓練模型無異，這樣會浪費時間和資源。
4. 添加新的可訓練層
	- 我們唯一重新使用的是基礎模型的特徵提取層。我們需要在這些層之上添加額外的層來預測模型的特殊任務，通常是最終輸出層。
5. 訓練新的層
	- 預訓練模型的最終輸出可能與我們模型所需的輸出不同。例如，預訓練模型在ImageNet數據集上訓練，其輸出是1000個類別。
	- 然而，我們的模型需要處理兩個類別。在這種情況下，我們需要對模型進行新的輸出層的訓練。
6. 微調模型
	- 改進性能的一種方法是微調。
	- 微調包括解凍基礎模型的一部分，然後以非常低的學習率對整個模型再次進行訓練。低學習率會提高模型在新數據集上的性能，同時防止過擬合。
---
#### 實際專案範例
1. [AI Maker 案例教學 - YOLOv7 影像辨識應用](https://docs.oneai.twcc.ai/s/casestudy-yolov7#AI-Maker-%E6%A1%88%E4%BE%8B%E6%95%99%E5%AD%B8---YOLOv7-%E5%BD%B1%E5%83%8F%E8%BE%A8%E8%AD%98%E6%87%89%E7%94%A8)
2. [15 Transfer Learning Projects in Deep Learning](https://www.projectpro.io/article/transfer-learning-projects/869#mcetoc_1h3h5knb213)
3. [Transfer Learning with Keras！](https://ithelp.ithome.com.tw/articles/10190971)