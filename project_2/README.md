<nav class="pagination" role="navigation">
    <a class="previous pagination__newer btn btn-small btn-tertiary" href="../"> 主頁</a>
</nav>

## 基於深度學習模型於前景注意力之行人重識別系統
### 簡介
##### 碩士論文

**Python, Pytorch, 行人偵測, Person Re-ID, 特徵比對, 行人跟蹤演算法, 語意分割**

現在為了安全監控、尋人或商家人流分析等目的監控攝影機隨處可見，由於相機分辨率和拍攝角度的緣故，拍攝到的畫面品質偏低通常無法有效使用人臉識別，這時Person Re-ID就是一個非常重要的技術，能使用品質偏低的畫面透過身型、顏色等其他特徵在跨攝影機中搜索目標人物，快速篩選可能目標減少人力和時間的消耗。 

此論文嘗試用深度學習的方法達成Person Re-ID，將使用Attention Module增加行人的重要特徵權重的深度模型作為Person Re-ID模型，和其他模型相結合，製作出行人搜索系統

#### 行人偵測
[YOLOv5](https://github.com/ultralytics/yolov5)

#### Person Re-ID & 前景注意力
使用ResNet-50作為backbone的網路，加上Attention Module增加行人的重要特徵權重，依據搜索條件選擇是否加上語意分割模型

<br>
<br>

---

#### 應用1-行人跟蹤

**行人偵測, Person Re-ID, 行人跟蹤算法**

用追蹤來輔助特徵比對，Person Re-ID模型實際用於影片時牽涉到特徵儲存，會受到儲存空間影響，儲存量多寡也會影響比對時間，因此需要一種演算法對比對特徵進行刪減。

##### 行人跟蹤算法

將行人偵測和Person Re-ID模型輸出的特徵，第一個frame輸出特徵後儲存，在之後的frame與儲存特徵進行比對，並儲存特徵讓後續的正進行比對。

比對方式為計算特徵之間的餘弦相似性後每個特徵以相似性作為權重進行投票，取加權結果最高判斷為一樣ID，並在相似性都低於閥值時判斷為新的人，當多個結果判斷為同一ID時，取相對權重較高的的一方為該ID，較低的一方則取權重第二高ID，將其相似性與閥值進行比較，如高於閥值再次重複上述有多個相同結果時的算法，如低於閥值則判斷為新的人。

<img src="/images/reidflow.gif"/>
<br>

##### 測試
輸入:影片

搜索條件:
* 同時追蹤多人
* frame by frame 擷取影片中行人進行特徵比對、賦予ID

<img src="/images/terrace1-c1.gif"/>

<br>
<br>

---

#### 應用2-Database搜尋

**行人偵測, Person Re-ID, 語意分割, 特徵比對**

模擬ATM情境，一共22人，平均每人5.5張圖片，拍攝不同位置、不同視角的俯視圖，作為Database測試我們的系統

##### 特徵比對

Person Re-ID模型提取特徵和Database中所有圖的特徵比較後，進一步使用語義分割模型得到的屬性來刪除具有不同屬性的圖像，屬性包括衣服的顏色和類型。

<img src="/images/Retrieval.png"/>

##### 測試

輸入:圖片

搜索條件:
* 單人追蹤
* 從Database中找出目標

<img src="/images/white.jpg"/>
<br>
<br>
<img src="/images/yellow.jpg"/>

<br>
<br>
<br>
<nav class="pagination" role="navigation">
    <a class="previous pagination__newer btn btn-small btn-tertiary" href="../"> &larr;&nbsp;back&nbsp;&nbsp;</a>
    <a class="previous pagination__newer btn btn-small btn-tertiary" href="#top"> &uarr;&nbsp;top&nbsp;</a>
</nav>

<br>