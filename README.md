# homework

## 畫0.8相關度

```
./listing_5_1.py ../data graph08.dot
fdp -T png -o graph08.png data graph08.dot
```

## 畫0.3相關度

```
./listing_5_1.py --jaccard_index_threshold 0.3 ../data graph03.dot
fdp -T png -o graph08.png data graph03.dot
```

---
## listing_5_1.py 使用的套件
* argparse 用來讓人輸入使用引數
* networkx 畫圖

--- 
## 重要語法說明

用於計算惡意程式jaccard距離

```
def jaccard(set1,set2):
    intersection = set1.intersection(set2)
    intersection_length = float(len(intersection))
    union = set1.union(set2)
    union_length = float(len(union))
    return intersection_length / union_length
```

