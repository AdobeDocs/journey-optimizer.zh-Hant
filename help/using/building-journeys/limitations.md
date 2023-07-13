---
solution: Journey Optimizer
product: journey optimizer
title: 歷程限制
description: 進一步瞭解歷程限制
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，限制
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 48%

---

# 限制 {#journey-limitations}

以下是有關使用歷程的限制。

## 一般動作限制

* 沒有傳送限制。 
* 如果出現錯誤，將系統地執行三次重試。您無法根據收到的錯誤訊息調整重試次數。 
* 內建 **反應** 事件可讓您對開箱即用的動作做出反應(請參閱此 [頁面](../building-journeys/reaction-events.md))。 如果您想要對透過自訂動作傳送的訊息做出反應，則需要設定專用事件。 
* 您無法同時進行兩個動作，必須逐一新增。

## 歷程版本限制 {#journey-versions-limitations}

* 從 v1 中的事件活動開始的歷程無法從其他版本中的事件開始。歷程的開頭不可為 **對象資格** 事件。
* 以「 」開始的歷程 **對象資格** v1中的活動必須一律以「 」開頭 **對象資格** 在後續版本中。
* 在中選擇的對象和名稱空間 **對象資格** （第一個節點）無法在新版本中變更。
* 所有歷程版本中的重新進入規則必須相同。
* 以「 」開始的歷程 **讀取對象** 在後續版本中無法以其他事件開頭。
 
## 自訂動作限制

* 自訂動作 URL 不支援動態參數。 
* 僅支援 POST 和 PUT 呼叫方法. 
* 查詢參數或標題的名稱不得以「.」開頭 或 &quot;$&quot;。 
* 不允許使用 IP 位址. 
* 內部 Adobe 位址 (.adobe.) 是不允許的。 
## 事件限制

* 對於系統產生的事件，必須先在 Journey Optimizer 中設定用於啟動客戶歷程的串流資料，才能取得唯一的協調流程 ID。  此協調流程ID必須附加至傳入Adobe Experience Platform的串流裝載。 此限制不適用於規則型事件。 
## 資料來源限制

* 可在客戶歷程中利用外部資料來源即時查詢外部資料。 這些來源必須可透過REST API使用、支援JSON並能夠處理大量請求。

## 在建立設定檔的同時開始的歷程 {#journeys-limitation-profile-creation}

在 Adobe Experience Platform 中建立/更新以 API 為基礎的設定檔會有延遲。對於第 95 個百分位數的請求，服務層級目標 (SLT) 從接收到統一設定檔的延遲時間小於 1 分鐘，每秒請求量為 20K (RPS)。

如果在建立設定檔的同時觸發歷程，並立即從設定檔服務檢查/擷取資訊，則可能無法正常運作。

您可以從以下兩種解決方案中選擇一種：

* 在第一個事件後新增等待活動，為 Adobe Experience Platform 提供執行擷取至設定檔服務所需的時間。

* 設定不會立即運用設定檔的歷程。 例如，如果歷程的設計是要確認帳戶的建立，則體驗事件可能包含傳送第一個確認訊息（名字、姓氏、電子郵件地址等）所需的資訊。

## 讀取對象限制

* 串流對象一律為最新狀態，但擷取時不會計算批次對象。 它們僅在每日批次評估時間每天進行評估。
