---
title: Journey Optimizer限制
description: 深入了解Journey Optimizer限制
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: f177c9b2c7c7a7fa6182d07e773efd0683886d34
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 2%

---

# 限制 {#limitations}

權益、產品限制和效能護欄列於[ Adobe Journey Optimizer產品說明頁面](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}中。

使用[!DNL Adobe Journey Optimizer]時，您會發現以下其他限制。

## 訊息的限制

* 您無法向包含[!DNL Journey Optimizer]的電子郵件添加附件。
* [!DNL Journey Optimizer]中不支援電子郵件密件副本。

## 歷程限制

### 一般動作

* 沒有發送限制。 
* 發生錯誤時會系統地執行三次重試。 您無法根據收到的錯誤訊息調整重試次數。 
* 內建的&#x200B;**Reaction**&#x200B;事件可讓您對現成可用的動作做出反應。 在[本頁面](building-journeys/reaction-events.md)深入瞭解。如果您想對透過自訂動作傳送的訊息做出反應，需要設定專用事件。 
* 您無法同時放置兩個動作，您必須逐一新增。

### 訊息動作

* 新增多頻道訊息時，會傳送兩則訊息。

### 歷程版本 {#journey-versions-limitations}

* 從v1中的事件活動開始的歷程，無法以其他版本中的事件以外的項目開始。 您無法以&#x200B;**區段資格**&#x200B;事件開始歷程。
* v1中以&#x200B;**區段資格**&#x200B;活動開始的歷程，在進一步版本中必須一律以&#x200B;**區段資格**&#x200B;開頭。
* 在&#x200B;**區段資格**（第一個節點）中選擇的區段和命名空間在新版本中無法變更。
* 所有歷程版本中的重新進入規則必須相同。
* 從&#x200B;**讀取區段**開始的歷程，無法從下一個版本中的其他事件開始。
 

### 自訂動作

* 自訂動作URL不支援動態參數。 
* 僅支援POST和PUT呼叫方法。 
* 查詢參數或標題的名稱不得以「。」開頭 或 &quot;$&quot;. 
* 不允許IP地址。 
* 內部Adobe地址(.adobe.) 不允許。
 

### 事件

* 針對系統產生的事件，在Journey Optimizer中必須先設定用來起始客戶歷程的串流資料，才能取得唯一的協調ID。 此協調ID必須附加至傳入Adobe Experience Platform的串流裝載。 此限制不適用於規則型事件。
 

### 資料來源

* 可在客戶歷程中運用外部資料來源，即時查閱外部資料。 這些來源必須可透過REST API使用、支援JSON並且能夠處理請求量。

### 從建立設定檔的同時開始的歷程 {#journeys-limitation-profile-creation}

在Adobe Experience Platform中建立/更新以API為基礎的設定檔會有延遲。 延遲方面的服務級別目標(SLT)從接收到第95個百分位數請求的統一配置檔案小於1分鐘，每秒20K請求(RPS)量。

如果歷程同時觸發至設定檔建立，並立即從設定檔服務檢查/擷取資訊，則可能無法正常運作。

您可以從以下兩種解決方案中選擇一種：

* 在第一個事件後新增等待活動，為Adobe Experience Platform提供執行擷取至設定檔服務所需的時間。

* 設定不會立即運用設定檔的歷程。 例如，如果歷程的設計是要確認帳戶的建立，則體驗事件可能包含傳送第一個確認訊息（名字、姓氏、電子郵件地址等）所需的資訊。

### 讀取區段

* 串流區段一律為最新狀態，但擷取時不會計算批次區段。 它們僅在每日批次評估時間每天進行評估。
