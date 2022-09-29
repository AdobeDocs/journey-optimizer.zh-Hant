---
title: Journey Optimizer護欄和限制
description: 深入了解Journey Optimizer護欄
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 9c0f604680787dbdf5fb820074408edad78f8bfb
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 3%

---

# 護欄和限制 {#limitations}

權益、產品限制和效能護欄列於 [Adobe Journey Optimizer產品說明頁面](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}。

當使用 [!DNL Adobe Journey Optimizer] 時，您將找到下面其他護欄和限制。

## 消息護欄 {#message-guardrails}

* 您無法將附件新增至具有 [!DNL Journey Optimizer].
* 您無法使用相同的傳送網域，從 [!DNL Adobe Journey Optimizer] 和其他產品，如 [!DNL Adobe Campaign] 或 [!DNL Adobe Marketo Engage] 例如，


## 決策管理護欄 {#offer-guardrails}

決策的效能護欄和靜態限制列於 [AdobeOffer decisioning應用程式服務產品說明頁面](https://helpx.adobe.com/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;}。


## 登錄頁面護欄 {#lp-guardrails}

* 只有一個 **表單** 元件可用於單一主要頁面。
* 此 **表單** 元件無法用於子頁面中。
* 您無法將預先標題新增至登錄頁面。
* 您無法選取 **自行編碼** 選項。

## 歷程護欄 {#journeys-guardrails}

### 一般動作 {#general-actions-g}

* 沒有發送限制。
* 發生錯誤時會系統地執行三次重試。 您無法根據收到的錯誤訊息調整重試次數。
* 內建 **反應** 事件可讓您對現成可用的動作做出反應。 在[本頁](../building-journeys/reaction-events.md)中瞭解更多。如果您想對透過自訂動作傳送的訊息做出反應，需要設定專用事件。
* 您無法同時放置兩個動作，您必須逐一新增。
* 在大多數情況下，設定檔無法同時在同一歷程中出現多次。 如果已啟用重新進入，設定檔可以重新進入歷程，但必須完全退出歷程的先前例項，才能執行此動作。 [閱讀全文](../building-journeys/journey-end.md)

### 歷程版本 {#journey-versions-g}

* 從v1中的事件活動開始的歷程，無法以其他版本中的事件以外的項目開始。 您無法以 **區段資格** 事件。
* 從 **區段資格** v1中的活動必須一律以開頭 **區段資格** 在其他版本中。
* 在 **區段資格** （第一個節點）無法在新版本中變更。
* 所有歷程版本中的重新進入規則必須相同。
* 從 **讀取區段** 無法從下一個版本中的其他事件開始。

### 自訂動作 {#custom-actions-g}

* 自訂動作URL不支援動態參數。
* 僅支援POST和PUT呼叫方法
* 查詢參數或標題的名稱不得以「。」開頭 或 &quot;$&quot;
* 不允許IP地址
* 內部Adobe地址(.adobe.) 不允許。

### 活動 {#events-g}

* 針對系統產生的事件，在Journey Optimizer中必須先設定用來起始客戶歷程的串流資料，才能取得唯一的協調ID。 此協調ID必須附加至傳入Adobe Experience Platform的串流裝載。 此限制不適用於規則型事件。
* 業務事件不能與單一事件或區段資格活動搭配使用。
* 單一歷程（從事件或區段資格開始）包含防止同一事件多次錯誤觸發歷程的護欄。 設定檔重新進入預設會暫時封鎖5分鐘。 例如，如果某個事件在12:01對特定設定檔觸發歷程，而另一個事件在12:03到達（無論是相同事件或是不同事件觸發相同歷程），該歷程將不會對此設定檔重新開始。

### 資料來源 {#data-sources-g}

* 可在客戶歷程中運用外部資料來源，即時查詢外部資料。 這些來源必須可透過REST API使用、支援JSON並且能夠處理請求量。

### 歷程與設定檔建立 {#journeys-limitation-profile-creation}

在Adobe Experience Platform中建立/更新以API為基礎的設定檔會有延遲。 延遲方面的服務級別目標(SLT)從接收到第95個百分位數請求的統一配置檔案小於1分鐘，每秒20K請求(RPS)量。

如果歷程同時觸發至設定檔建立，並立即從設定檔服務檢查/擷取資訊，則可能無法正常運作。

您可以從以下兩種解決方案中選擇一種：

* 在第一個事件後新增等待活動，為Adobe Experience Platform提供執行擷取至設定檔服務所需的時間。

* 設定不會立即運用設定檔的歷程。 例如，如果歷程的設計是要確認帳戶的建立，則體驗事件可能包含傳送第一個確認訊息（名字、姓氏、電子郵件地址等）所需的資訊。

### 讀取區段 {#read-segment-g}

* 串流區段一律為最新狀態，但擷取時不會計算批次區段。 它們僅在每日批次評估時間每天進行評估。
* 若為使用讀取區段活動的歷程，則有最多可同時開始的歷程次數。 系統將執行重試，但請避免在完全同時開始的五個歷程（具有讀取區段、排程或「盡快」），方法是隨著時間分散，例如5到10分鐘。

### 運算式編輯器 {#expression-editor}

* 從讀取區段、區段資格或業務事件活動開始的歷程中，無法使用體驗事件欄位群組。

