### 讓聊天不再單調——DC音樂機器人
|職位|姓名|學號|任務|
|:--:|:--:|:--:|:--:|
|組長|沈煒皓|C109118129|監督|
|組員|王貿新|C109118130|程式開發|
|組員|柯永誠|C10911810|資料庫|
|組員|李昱承|C109118122|文書|
|組員|曾忠隆|C109126156|測試專員|
---
### 內容:

本bot為使用戶在操作Discord軟體時，能夠快速在文字頻道當中獲取想要聆聽的音樂，並在語音頻道即時的分享給朋友聆聽。

範疇：
所有的Discord用戶

---
### 任務內容:
| 任務 | 說明 | 需時(天) | 前置任務 |
| :-: | :---------: | :--------: | :-----: |
| 1 | 題目構想 | 1 | - |
| 2 | 研擬計畫 | 1 | 1 |
| 3 | 架構流程 | 2 | 1 |
| 4 | 任務分配 | 3 | 2, 3 |
| 5 | 資料庫建立 | 15 | 4 |
| 6 | 程式開發 | 40 | 4 |
| 7 | 程式測試 | 10 | 5, 6 |
| 8 | 撰寫使用手冊 | 5 | 7 |
| 9 | 使用者訓練 | 2 | 8 |
| 10 | 使用者測試 | 7 | 9 |
---
### 甘特圖:
```mermaid
gantt
    title 甘特圖
    
    section 任務
    題目構想: a1, 2022-10-10, 1d  
    研擬計畫: a2, after a1, 1d     
    架構流程: a3, after a1, 2d     
    任務分配: a4, after a3, 3d    
    資料庫建立: a5, after a4, 15d   
    程式開發: a6, after a4, 40d    
    程式測試: a7, after a6, 10d     
    撰寫使用手冊: a8, after a7, 5d          
    使用者訓練: a9, after a8, 2d    
    使用者測試: a10, after a9, 7d
```

---
### PERT/CPM圖:
```mermaid
classDiagram

任務1 題目構想 --> 任務2 研擬計畫
任務1 題目構想 --> 任務3 架構流程

任務2 研擬計畫 --> 任務4 任務分配
任務3 架構流程 --> 任務4 任務分配

任務4 任務分配 --> 任務5 資料庫建立
任務4 任務分配 --> 任務6 程式開發

任務5 資料庫建立 --> 任務7 程式測試
任務6 程式開發 --> 任務7 程式測試

任務7 程式測試 --> 任務8 撰寫使用手冊

任務8 撰寫使用手冊 --> 任務9 使用者訓練

任務9 使用者訓練 --> 任務10 使用者測試

任務1 題目構想 : 開始：第1天
任務1 題目構想 : 結束：第1天
任務1 題目構想 : 需時：1天

任務2 研擬計畫 : 開始：第1天
任務2 研擬計畫 : 結束：第1天
任務2 研擬計畫 : 需時：1天

任務3 架構流程 : 開始：第1天
任務3 架構流程 : 結束：第2天
任務3 架構流程 : 需時：2天

任務4 任務分配 : 開始：第3天
任務4 任務分配 : 結束：第6天
任務4 任務分配 : 需時：4天

任務5 資料庫建立 : 開始：第7天
任務5 資料庫建立 : 結束：第21天
任務5 資料庫建立 : 需時：15天

任務6 程式開發 : 開始：第7天
任務6 程式開發 : 結束：第46天
任務6 程式開發 : 需時：40天

任務7 程式測試 : 開始：第47天
任務7 程式測試 : 結束：第56天
任務7 程式測試 : 需時：10天

任務8 撰寫使用手冊 : 開始：第57天
任務8 撰寫使用手冊 : 結束：第61天
任務8 撰寫使用手冊 : 需時：5天

任務9 使用者訓練 : 開始：第62天
任務9 使用者訓練 : 結束：第63天
任務9 使用者訓練 : 需時：2天

任務10 使用者測試 : 開始：第64天
任務10 使用者測試 : 結束：第70天
任務10 使用者測試 : 需時：7天
```
關鍵路徑: 1 -> 3 -> 4 -> 6 -> 7 -> 8 -> 9 -> 10
---
### 功能性需求與非功能性需求:
功能性需求:
- 提供搜尋功能
- 提供基本MP3功能
- 提供音樂推薦功能
- 提供新影片推播
- 提供管理後台

非功能性需求:
- 效能問題
> 能夠快速的反映結果
- 使用性
> UI化的控制面版，易於操作與使用
- 維護性
> 原始碼做註解，以便下一次的維護
- 可靠度
> 24hr運作，不會造成無法使用的問題
- 資料安全
> 使用本地資料庫，以及做好sql注入攻擊的防護

---
### 功能分解圖:
![FDD](FDD.jpg "FDD")







---
### 需求分析圖及文字說明:
一個DC音樂機器人的需求分析簡述如下：
- 管理者可以藉由輸入指令來獲取當前運行的狀況。
- 管理者可以藉由加載網頁來獲取當前運行的狀況。
- 使用者可以藉由輸入指令來搜尋音樂且能夠選擇音樂後播放音樂。
- 使用者可以藉由輸入指令來訂閱頻道獲得最新動態通知。
- 訂閱任何頻道都要儲存頻道資料
- 播放任何音樂都要儲存音樂資料

![UML](UML.png "UML")
---
### 使用案例圖與使用案例說明:
1.使用者透過搜尋找到喜歡的音樂並聆聽<br>
2.使用者透過播放器上面的按鈕來播放與暫停<br>
3.使用者透過指令來追蹤喜歡的頻道<br>

使用案例說明 - 1:

| 使用案例名稱 | 搜尋歌曲 |
|:------------|:--------|
|**行動者:**|使用者|
|**說明:**|如何透過搜尋找到喜歡的音樂|
|**完成動作:**|1.輸入指令，並在搜尋欄輸入關鍵字<br>2.搜尋後，跳出可能的音樂選項<br>3.點選選項後，開始播放|

使用案例圖 - 1:<br>
![UML1](UML1.png "UML1")

使用案例說明 - 2:
| 使用案例名稱 | 控制播放器 |
|:------------|:----------|
|**行動者:**|使用者|
|**說明:**|如何控制播放器|
|**完成動作:**|1.按下按鈕後便會執行對應動作|

使用案例圖 - 2:<br>
![UML2](UML2.png "UML2")

使用案例說明 - 3:
| 使用案例名稱 | 訂閱頻道 |
|:------------|:--------|
|**行動者:**|使用者|
|**說明:**|如何追蹤喜歡的頻道|
|**完成動作:**|1.輸入指令，並在指令內填入參數<br>2.送出後，系統會做紀錄<br>3.完成後，即可在頻道有動作時推播|

使用案例圖 - 3:<br>
![UML3](UML3.png "UML3")



---
### 動態模擬畫面:
[使用者案例1模擬畫面](https://www.figma.com/proto/Zo0ObYiY29YDC16TDFRk66/Untitled?node-id=7%3A1415&scaling=min-zoom&page-id=0%3A1&starting-point-node-id=7%3A1415)

### DFD:
![DFD](DFD.jpg "DFD")

### DFD-level0:
![DFD-0](DFD-0.png "DFD-0")

### 類別圖:
![Class Diagram](Class_Diagram.png "Class Diagram")
