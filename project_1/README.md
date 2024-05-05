### 3D手勢辨識
### 簡介
##### 大學畢業專題

**Python, Tensorflow, 關鍵點檢測**

本專題希望對手勢進行即時的手部關節點預測及手勢分類，並對預測方式進行調整比較準確率，使用Kinect V2拍攝的深度圖作為輸入，即時顯示預測關節點和分類結果。
#### 手部關節偵測
**Depth map 處理**

輸入從深度相機捕捉圖片，設置一個閥值限制距離，找出離相機最近物體的質心，以此點為中心向外擴張，截下此區域作為網路輸入。
  
**3D關鍵點偵測**

輸入用ResNet-50作為backbone的網路，用於回歸初始關節位置，因手掌關節和手指關節的活動範圍不同回歸複雜度也不同，把手掌關節回歸和手指關節回歸分為兩個分支，將來自初始特徵提取模塊的feature maps 輸入到不同分支中更多局部特徵，用作引導特徵提取的約束。


<img src="/images/depthmap2point.gif"/>
<br>
<br>

---

#### 手勢分類
**3D向量計算**

通過測量兩個向量的夾角的餘弦值來度量兩個向量是否大致指向相同的方向，紫色和藍色為兩個向量，\theta為向量間夾角，得到餘弦相似度，設閥值，小於閥值判斷為彎曲，分別判斷五根手指是否彎曲。

<img src="/images/gesture.gif"/>
<br>
<br>

---

### 即時預測
<img src="/images/handc.gif"/>

<br>
<br>
<br>
<nav class="pagination" role="navigation">
    <a class="previous pagination__newer btn btn-small btn-tertiary" href="\.."> &larr;&nbsp;back&nbsp;&nbsp;</a>
    <a class="previous pagination__newer btn btn-small btn-tertiary" href="#top"> &uarr;&nbsp;top&nbsp;</a>
</nav>

<br>