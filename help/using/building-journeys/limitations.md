---
solution: Journey Optimizer
product: journey optimizer
title: 歷程限制
description: 深入了解歷程限制
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# 限制 {#journey-limitations}

以下為與使用歷程相關的限制。

## 一般動作限制

* 沒有發送限制。 
* 發生錯誤時會系統地執行三次重試。 您無法根據收到的錯誤訊息調整重試次數。 
* 內建 **反應** 事件可讓您對現成可用的動作做出反應(請參閱 [頁面](../building-journeys/reaction-events.md))。 如果您想對透過自訂動作傳送的訊息做出反應，需要設定專用事件。 
* 您無法同時放置兩個動作，您必須逐一新增。

## 歷程版本限制 {#journey-versions-limitations}

* 從v1中的事件活動開始的歷程，無法以其他版本中的事件以外的項目開始。 您無法以 **區段資格** 事件。
* 從 **區段資格** v1中的活動必須一律以開頭 **區段資格** 在其他版本中。
* 在 **區段資格** （第一個節點）在新版本中無法變更。
* 所有歷程版本中的重新進入規則必須相同。
* 從 **讀取區段** 無法從下一個版本中的其他事件開始。
 

## 自訂動作限制

* 自訂動作URL不支援動態參數。 
* 僅支援POST和PUT呼叫方法。 
* 查詢參數或標題的名稱不得以「。」開頭 或「$」。 
* 不允許IP地址。 
* 內部Adobe地址(.adobe.) 不允許。
 

## 事件限制

* 對於系統產生的事件，必須先在Journey Optimizer中設定用來起始客戶歷程的串流資料，才能取得唯一的協調ID。 此協調ID必須附加至傳入Adobe Experience Platform的串流裝載。 此限制不適用於規則型事件。
 

## 資料來源限制

* 可在客戶歷程中運用外部資料來源，即時查閱外部資料。 這些來源必須可透過REST API使用、支援JSON並且能夠處理請求量。

## 從建立設定檔的同時開始的歷程 {#journeys-limitation-profile-creation}

在Adobe Experience Platform中建立/更新以API為基礎的設定檔時會有延遲。 延遲方面的服務級別目標(SLT)從接收到第95個百分位數請求的統一配置檔案小於1分鐘，每秒20K請求(RPS)量。

如果歷程同時觸發至設定檔建立，並立即從設定檔服務檢查/擷取資訊，則可能無法正常運作。

您可以從以下兩種解決方案中選擇一種：

* 在第一個事件後新增等待活動，讓Adobe Experience Platform有時間執行擷取至設定檔服務。

* 設定不會立即運用設定檔的歷程。 例如，如果歷程的設計是要確認帳戶的建立，則體驗事件可能包含傳送第一個確認訊息（名字、姓氏、電子郵件地址等）所需的資訊。

## 讀取區段限制

* 串流區段一律為最新狀態，但擷取時不會計算批次區段。 它們僅在每日批次評估時間每天進行評估。
