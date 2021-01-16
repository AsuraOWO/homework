# 資財三乙 107AB0747 林昊霆 期末報告

## 第8章的檔案
![](https://imgur.com/OWZ5Clo.png)

#### 這次會用到的檔案
* complete_detector.py (主程式)
* run_complete_detector.sh (執行程式)

---

## complete_detector.py 用到的套件
### 最重要的套件是sklearn的 RandomForestClassifier 以及 FeatureHasher 
![](https://imgur.com/MD2fKGL.png)
### 透過 RandomForestClassifier  及 FeatureHasher 來提取特徵讓機器學習訓練提取惡意程式的特徵 

---

## run_complete_detector.sh 檔
![](https://imgur.com/I8Td1di.png)

---

## 執行結果

### 執行 run_complete_detector.sh
```
  $ run_complete_detector.sh 
```

### 繪製ROC曲線
### 在調整靈敏度時，接收器操作特徵（ROC）曲線測量的是檢測器的真實陽性率（成功檢測到的惡意軟件的百分比）和錯誤陽性率（被錯誤標記為惡意軟件的良性軟件的百分比）的變化。
### 靈敏度越高，得到的假陽性越多，但是會提高檢測率。靈敏度越低，錯誤越少。

### 檢測結果為假陽性率約為1％，可以檢測到測試集中約94％的惡意軟件樣本 

![](https://imgur.com/k4Yp1gu.png)

---


