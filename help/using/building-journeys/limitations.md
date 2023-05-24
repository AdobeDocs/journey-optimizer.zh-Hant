---
solution: Journey Optimizer
product: journey optimizer
title: 行程限制
description: 瞭解有關Journey限制的更多資訊
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 旅程，限制
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 60%

---

# 限制 {#journey-limitations}

以下是與使用旅行有關的限制。

## 一般操作限制

* 沒有傳送限制。 
* 如果出現錯誤，將系統地執行三次重試。您無法根據收到的錯誤訊息調整重試次數。 
* 內置 **反應** 事件允許您對現成操作做出反應(請參閱 [頁](../building-journeys/reaction-events.md))。 如果要對通過自定義操作發送的消息做出反應，則需要配置專用事件。 
* 您無法同時進行兩個動作，必須逐一新增。

## 行程版本限制 {#journey-versions-limitations}

* 從 v1 中的事件活動開始的歷程無法從其他版本中的事件開始。您無法透過&#x200B;**區段資格**&#x200B;事件開始歷程。
* 在 v1 中，以&#x200B;**區段資格**&#x200B;活動開始的歷程在後續版本中必須一律以&#x200B;**區段資格**&#x200B;開始。
* 中選擇的段和命名空間 **段資格** （第一個節點）在新版本中無法更改。
* 所有歷程版本中的重新進入規則必須相同。
* 以&#x200B;**讀取區段**開始的歷程在下一個版本中無法以另一個事件開始。
 

## 自定義操作限制

* 自訂動作 URL 不支援動態參數。 
* 僅支援 POST 和 PUT 呼叫方法. 
* 查詢參數或標題的名稱不得以「.」開頭 或 &quot;$&quot;。 
* 不允許使用 IP 位址. 
* 內部 Adobe 位址 (.adobe.) 是不允許的。 

## 事件限制

* 對於系統產生的事件，必須先在 Journey Optimizer 中設定用於啟動客戶歷程的串流資料，才能取得唯一的協調流程 ID。  此業務流程ID必須附加到流負載中進入Adobe Experience Platform。 此限制不適用於規則型事件。 

## 資料源限制

* 在客戶行程中，可利用外部資料源即時查找外部資料。 這些源必須可通過REST API使用，支援JSON並能夠處理請求量。

## 與建立配置檔案同時開始的行程 {#journeys-limitation-profile-creation}

在 Adobe Experience Platform 中建立/更新以 API 為基礎的設定檔會有延遲。對於第 95 個百分位數的請求，服務層級目標 (SLT) 從接收到統一設定檔的延遲時間小於 1 分鐘，每秒請求量為 20K (RPS)。

如果同時觸發「行程」以建立配置檔案，並立即從「配置檔案服務」中檢查/檢索資訊，則它可能無法正常工作。

您可以從以下兩種解決方案中選擇一種：

* 在第一個事件後新增等待活動，為 Adobe Experience Platform 提供執行擷取至設定檔服務所需的時間。

* 設定不會立即運用設定檔的歷程。 例如，如果行程旨在確認帳戶建立，則體驗事件可能包含發送第一個確認消息（名字、姓氏、電子郵件地址等）所需的資訊。

## 讀取段限制

* 串流區段一律為最新狀態，但擷取時不會計算批次區段。 它們僅在每日批次評估時間每天進行評估。
