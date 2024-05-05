### 信號偵蒐測向系統GUI
### 簡介

**C++, Qt, 使用者介面開發, C, 嵌入式系統, FreeRTOS**

使用C++在Qt框架下開發信號偵蒐測向系統的GUI，從實體網路接收資料，並建立thread以即時處理資料運算與接收，並在即時作業系統(FreeRTOS)使用C語言讀取週邊裝置訊息，在過程中修改與開發繪製圖形的API以完成前端數據和繪圖呈現。


### GUI
* 使用 C++在Qt框架撰寫GUI，並修改與開發其中繪製圖形的API。。
* 在GUI程式建立thread即時處理資料運算、傳送和接收、使用者操作和圖形呈現。
  
### Firmware
* 透過通訊介面(I2C)獲得周邊裝置資訊
* 在FreeRTOS建立task將獲得資訊發送至GUI

<br>
<img src="/work_experience/images/GUI.png"/>


<br>
<br>
<br>
<nav class="pagination" role="navigation">
    <a class="previous pagination__newer btn btn-small btn-tertiary" href="../"> &larr;&nbsp;back&nbsp;&nbsp;</a>
    <a class="previous pagination__newer btn btn-small btn-tertiary" href="#top"> &uarr;&nbsp;top&nbsp;</a>
</nav>

<br>
