### 期末專題報告:
|職位|姓名|學號|任務|
|:--:|:--:|:--:|:--:|
|組長|沈煒皓|C109118129|監督|
|組員|王貿新|C109118130|程式開發|
|組員|柯永誠|C1091110|資料庫|
|組員|李昱承|C109118122|文書|
|組員|曾忠隆|C109126156|測試專員|
---
### 內容:


---
### 任務內容:
| 任務 | 說明 | 需時(天) | 前置任務 |
| :-: | :---------: | :--------: | :-----: |
| 1 | 題目構想| 1 | - |
| 2 | 研擬計畫 | 1 | 1 |
| 3 | 架構流程 | 1 | 1 |
| 4 | 任務分配 | 4 | 2, 3 |
| 5 | 程式開發 | 70 | 4 |
| 6 | 程序測試 | 25 | 5 |
| 7 | 撰寫使用手冊 | 15 | 6 |
| 8 | 系統測試 | 20 | 6 |
| 9 | 使用者測試 | 20 | 7, 8 |
---
### 甘特圖:

---
### PERT/CPM圖:
```mermaid
classDiagram

任務1 題目構想 --|> 任務2 研擬計畫
任務1 題目構想 --> 任務3 架構流程
任務2 研擬計畫 --|> 任務4 任務分配
任務3 架構流程 --> 任務4 任務分配
任務4 任務分配 --> 任務5 程式開發
任務5 程式開發 --> 任務6 程式測試
任務6 程式測試 --> 任務8 系統測試
任務6 程式測試 --|> 任務7 撰寫使用手冊
任務7 撰寫使用手冊 --|> 任務9 使用者測試
任務8 系統測試 --> 任務9 使用者測試

任務1 題目構想 : 開始：第1天
任務1 題目構想 : 結束：第1天
任務1 題目構想 : 需時：1天

任務2 研擬計畫 : 開始：第1天
任務2 研擬計畫 : 結束：第1天
任務2 研擬計畫 : 需時：1天

任務3 架構流程 : 開始：第1天
任務3 架構流程 : 結束：第1天
任務3 架構流程 : 需時：1天

任務4 任務分配 : 開始：第2天
任務4 任務分配 : 結束：第5天
任務4 任務分配 : 需時：4天

任務5 程式開發 : 開始：第6天
任務5 程式開發 : 結束：第75天
任務5 程式開發 : 需時：70天

任務6 程式測試 : 開始：第76天
任務6 程式測試 : 結束：第100天
任務6 程式測試 : 需時：25天

任務7 撰寫使用手冊 : 開始：第101天
任務7 撰寫使用手冊 : 結束：第115天
任務7 撰寫使用手冊 : 需時：15天

任務8 系統測試 : 開始：第101天
任務8 系統測試 : 結束：第120天
任務8 系統測試 : 需時：20天

任務9 使用者測試 : 開始：第121天
任務9 使用者測試 : 結束：第140天
任務9 使用者測試 : 需時：20天
```

