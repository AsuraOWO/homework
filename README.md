# homework

---

## 畫0.8相關度

```
./listing_5_1.py ../data graph08.dot
fdp -T png -o graph08.png data graph08.dot
```
![](https://imgur.com/0hrEZsm)

---

## 畫0.3相關度

```
./listing_5_1.py --jaccard_index_threshold 0.3 ../data graph03.dot
fdp -T png -o graph03.png data graph03.dot
```
![](https://imgur.com/Tf9Gwln)

---

## listing_5_1.py 重要的的套件
* argparse 用來讓人輸入使用引數
* networkx 畫圖

--- 

## 重要語法說明

用於計算惡意程式jaccard距離 得到的距離越大相似度越相近
```
def jaccard(set1,set2):
    intersection = set1.intersection(set2)
    intersection_length = float(len(intersection))
    union = set1.union(set2)
    union_length = float(len(union))
    return intersection_length / union_length
```

取得目標檔案識別格式(如檔案路徑之類的)
```
def getstrings(fullpath):
    strings = os.popen("strings '{0}'".format(fullpath)).read()
    strings = set(strings.split("\n"))
    return strings
```

確認檔案是否是我們要的檔案型態
```
def pecheck(fullpath):
    return open(fullpath).read(2) == "MZ"
```

使用argparse處理引數
最重要的引數調整 --jaccard_index_threshold用來調整門檻值
```
parser.add_argument(
    "--jaccard_index_threshold","-j",dest="threshold",type=float,
    default=0.8,help="Threshold above which to create an 'edge' between samples"
)
```
--- 

## 分析
### 門檻值0.8 -> 線越少
### 門檻值0.3 -> 線越多
### 表示門檻值越低 惡意程式相似度越高
