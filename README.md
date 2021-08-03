# 梁盈 Liang Ying
## *人工智慧工程師 AI Engineer*

## 個人介紹


### 技能
* 人工智慧應用
  * 深度學習
  * 機器學習模型
* 深度學習框架
  * Pytorch
  * Keras
* 擅長架構
  * Attention Module
  * GAN
  * Resnet
* 程式語言
  * Python
  * Matlab  
<br>  
    
### 作品
- [Hand Pose Estimation](#hand-pose-estimation)
- [Person Re-Identification](#person-re-identification)

<br>
<br>

## 我的作品

### Hand Pose Estimation
### 簡介
####大學畢業專題

**Depth map 處理, 3D關鍵點偵測, 3D向量計算**

本專題希望對手勢進行即時的手部關節點預測及手勢分類，並對預測方式進行調整比較準確率，使用Kinect V2拍攝的深度圖作為輸入，即時顯示預測關節點和分類結果。
#### 手部關節偵測
**Depth map 處理**

輸入從深度相機捕捉圖片，設置一個閥值限制距離，找出離相機最近物體的質心，以此點為中心向外擴張，截下此區域作為網路輸入。
  
**3D關鍵點偵測**

輸入用ResNet-50作為backbone的網路，用於回歸初始關節位置，因手掌關節和手指關節的活動範圍不同回歸複雜度也不同，把手掌關節回歸和手指關節回歸分為兩個分支，將來自初始特徵提取模塊的feature maps 輸入到不同分支中更多局部特徵，用作引導特徵提取的約束。


<img src="/depthmap2point.gif"/>
<br>

#### 手勢分類
**3D向量計算**

通過測量兩個向量的夾角的餘弦值來度量兩個向量是否大致指向相同的方向，紫色和藍色為兩個向量，\theta為向量間夾角，得到餘弦相似度，設閥值，小於閥值判斷為彎曲，分別判斷五根手指是否彎曲。

<img src="/gesture.gif"/>
<br>

### 即時預測
<img src="/handc.gif"/>

[Top](#梁盈-liang-ying)
<br>

### Person Re-Identification
#### 行人偵測
- [YOLOv5](https://github.com/ultralytics/yolov5)

#### 特徵比對
- 特徵擷取深度神經網路
- 行人跟蹤演算法

<img src="/reidflow.gif"/>
<br>

#### 影片測試
<img src="/terrace1-c1.gif"/>

[Top](#梁盈-liang-ying)