---
title: Journey Optimizer護欄
description: 瞭解有關Journey Optimizer護欄的詳細資訊
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 1780310da6d8a952dd22b9ee9a0b23516efddb5f
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 4%

---

# 護欄和限制 {#limitations}

權利、產品限制和效能保護欄列於 [Adobe Journey Optimizer產品說明頁](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}。

當使用 [!DNL Adobe Journey Optimizer] 時，您將找到下面其他護欄和限制。

## 消息護欄 {#message-guardrails}

* 無法將附件添加到具有 [!DNL Journey Optimizer]。
* 不能使用同一發送域從 [!DNL Adobe Journey Optimizer] 和其他產品，比如 [!DNL Adobe Campaign] 或 [!DNL Adobe Marketo Engage] 例如。


## 決策管理護欄 {#offer-guardrails}

決策管理的效能保護欄和靜態限制列在 [AdobeOffer decisioningApp Service產品說明頁](https://helpx.adobe.com/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;}。


## 登錄頁護欄 {#lp-guardrails}

* 只有一個 **窗體** 可在單個首頁中使用元件。
* 的 **窗體** 不能在子頁中使用元件。
* 不能向登錄頁添加前標。
* 無法選擇 **編碼您自己的** 選項。

## 旅行護欄 {#journeys-guardrails}

### 一般操作 {#general-actions-g}

* 沒有發送限制。
* 在出現錯誤時系統地執行三次重試。 無法根據收到的錯誤消息調整重試次數。
* 內置 **反應** 事件允許您對現成操作做出反應。 在[本頁](../building-journeys/reaction-events.md)中瞭解更多。如果要對通過自定義操作發送的消息做出反應，則需要配置專用事件。
* 不能並行放置兩個操作，必須依次添加它們。
* 今天的行程中存在技術限制，使配置檔案在同一行程中多次出現。 配置檔案仍然可以重新輸入行程（基於設定），但只有在他完全退出此行程的上一個實例後才能執行。
* 在大多數情況下，配置檔案不能在同一行程中同時出現多次。 如果啟用重新入門，則配置檔案可以重新輸入行程，但在他完全退出此行程的上一個實例之前，無法重新輸入。 [閱讀全文](../building-journeys/journey-end.md)

### 歷程版本 {#journey-versions-g}

* 從v1中的事件活動開始的行程不能從其他版本中的事件以外的內容開始。 您不能以 **段資格** 的子菜單。
* 從 **段資格** v1中的活動必須始終以 **段資格** 版。
* 中選擇的段和命名空間 **段資格** （第一個節點）在新版本中無法更改。
* 在所有行程版本中，重入規則必須相同。
* 從 **讀取段** 無法以下版本中的其他事件開始。

### 自訂動作 {#custom-actions-g}

* 自定義操作URL不支援動態參數。
* 僅支援POST和PUT調用方法
* 查詢參數或標頭的名稱不能以「」開頭。 或 &quot;$&quot;
* 不允許IP地址
* 內部Adobe地址(.adobe.) 不允許。

### 活動 {#events-g}

* 對於系統生成的事件，必須先在Journey Optimizer內配置用於啟動客戶行程的流資料，才能獲取唯一的業務流程ID。 此業務流程ID必須附加到流負載中進入Adobe Experience Platform。 此限制不適用於基於規則的事件。
* 業務事件不能與單一事件或分部資格活動一起使用。

### 資料源 {#data-sources-g}

* 在客戶行程中，可利用外部資料源即時查找外部資料。 這些源必須可通過REST API使用，支援JSON並能夠處理請求量。

### 旅程和配置檔案建立 {#journeys-limitation-profile-creation}

在Adobe Experience Platform，存在與基於API的配置檔案建立/更新相關的延遲。 在每秒20K請求(RPS)的卷上，從接收到統一配置檔案的服務級別目標(SLT)的延遲小於95%請求數的1分鐘。

如果同時觸發到配置檔案建立的行程，並立即從配置檔案服務中檢查/檢索資訊，則該行程可能無法正常工作。

您可以從以下兩種解決方案中選擇一種：

* 在第一個事件後添加等待活動，為Adobe Experience Platform提供執行接收配置檔案服務所需的時間。

* 設定不立即利用配置檔案的行程。 例如，如果行程旨在確認帳戶建立，則體驗事件可能包含發送第一個確認消息（名字、姓氏、電子郵件地址等）所需的資訊。

### 讀取區段 {#read-segment-g}

* 流化段始終是最新的，但在檢索時不會計算批段。 它們僅在每日批處理評估時間進行評估。
* 對於使用「讀取段」活動的行程，可以同時啟動的行程數最多。 系統將執行重試，但請避免在同一時間開始超過5次旅程（使用讀取段、計畫或「盡快」），方法是將它們隨時間分佈，例如5到10分鐘。
