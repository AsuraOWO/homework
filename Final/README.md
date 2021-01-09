# 期末報告

---

## CH8用到的套件
### 最重要的套件是sklearn的 RandomForestClassifier 以及 FeatureHasher 
![](https://imgur.com/MD2fKGL.png)

---

### 透過 RandomForestClassifier  及 FeatureHasher 來提取特徵讓機器學習訓練提取惡意程式的特徵 


---

## 執行結果

### 繪製ROC曲線
### 在調整靈敏度時，接收器操作特徵（ROC）曲線測量的是檢測器的真實陽性率（成功檢測到的惡意軟件的百分比）和錯誤陽性率（被錯誤標記為惡意軟件的良性軟件的百分比）的變化。
### 靈敏度越高，得到的假陽性越多，但是提高您的檢測率。靈敏度越低，錯誤越少

### 檢測結果為假陽性率約為1％，可以檢測到測試集中約94％的惡意軟件樣本 

![](https://imgur.com/k4Yp1gu.png)

---


