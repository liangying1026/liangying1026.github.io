# 梁盈 Liang Ying

## 個人介紹

### 關於我
⼤學和研究所的研究領域為深度學習和電腦視覺，實作過手勢辨識和行人重識別的專案，碩士畢業後，擔任兩年軟體工程師，負責使用者介面開發和嵌入式應用。

### 技能
* 程式語言
  * C++
  * C 
  * Matlab 
  * Python
* 工具
  * Qt
  * Git
  * PyCharm
* 人工智慧應用
  * 深度學習框架
    * Pytorch
    * Keras
  * 擅長架構
    * Attention Module
    * GAN
    * Resnet
<br>  
      
### 工作經歷

* 使用 C++在Qt框架撰寫GUI，並修改與開發其中繪製圖形的API。
* 在GUI程式建立thread即時處理資料運算、傳送和接收、使用者操作和圖形呈現。
* 開發測試工具檢測前後端連線和儲存或傳遞的資料格式。
* 進行穩定性測試，分析及排除錯誤。
* 使用C語言在即時作業系統(FreeRTOS)，透過通訊介面(I2C)傳輸資料。
* 版本控管，分析與解決回報問題，依需求進行維護及優化，改善效能。


#### 專案
<nav class="pagination" role="navigation">
    <a class="previous pagination__newer btn btn-small btn-tertiary" href="\work_experience"> 信號偵蒐測向系統GUI</a>
</nav>
  
<br>  

### 在學專案
#### 3D手勢辨識

<img src="/project_1/images/gesture.gif"/>

使用深度學習模型，深度相機捕捉深度圖作為輸入，預測手部關節點再透過關節點預測手勢達成即時的手勢辨識，並對預測方式進行調整比較準確率。


開發語言 : Python

開發框架 : Tensorflow

開發環境 : Linux Ubuntu

Mean error:7.28mm
<nav class="pagination" role="navigation">
    <a class="previous pagination__newer btn btn-small btn-tertiary" href="project_1"> 詳細介紹</a>
</nav>

<br>

---
#### 基於深度學習模型於前景注意力之行人重識別系統

<img src="/project_2/images/reidflow.gif"/>

用深度學習的模型製作出行人搜索系統，現在為了安全監控、尋人或商家人流分析等目的監控攝影機隨處可見，Person Re-ID能使用品質偏低的畫面透過身型、顏色等特徵在跨攝影機中搜索目標人物，快速篩選可能目標減少人力和時間的消耗。

開發語言:Python

開發框架:Pytorch

開發環境:Linux Ubuntu

在模擬情境數據集，模擬ATM情境，一共22人，平均每人5.5張圖片，拍攝6種不同視角

Rank-1:91.2%

mAP:69.9%
<nav class="pagination" role="navigation">
    <a class="next pagination__older btn btn-small btn-tertiary" href="project_2">詳細介紹 </a>
</nav>

<br>
<br>

[Top](#梁盈-liang-ying)