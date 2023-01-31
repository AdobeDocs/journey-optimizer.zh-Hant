---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 護欄和限制
description: 深入瞭解 Journey Optimizer 護欄
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 78675ca22d8ee9a93d9af128d5708c305523da78
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 94%

---

# 護欄和限制 {#limitations}

權益、產品限制和效能護欄列於 [Adobe Journey Optimizer產品說明頁面](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

您也需要注意 [開始前即時客戶設定檔資料的護欄](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=zh-Hant){target="_blank"}.

當使用 [!DNL Adobe Journey Optimizer] 時，您將找到下面其他護欄和限制。

## 訊息護欄 {#message-guardrails}

* 您無法向帶有[!DNL Journey Optimizer]的電子郵件新增附件。
* 您無法使用相同的傳送網域從[!DNL Adobe Journey Optimizer]和其他產品 (例如[!DNL Adobe Campaign]或[!DNL Adobe Marketo Engage]) 傳送訊息。


## 決策管理護欄 {#offer-guardrails}

決策的效能護欄和靜態限制列於 [AdobeOffer decisioning應用程式服務產品說明頁面](https://helpx.adobe.com/tw/legal/product-descriptions/offer-decisioning-app-service.html){target="_blank"}.


## 登陸頁面護欄 {#lp-guardrails}

* 一個主頁面只能使用一個&#x200B;**表單**&#x200B;元件。
* 此&#x200B;**表單**&#x200B;元件無法在子頁面中使用。
* 您無法將預覽文字新增至登陸頁面。
* 在設計登陸主要頁面時，您無法選取&#x200B;**自行編碼**&#x200B;選項。

## 歷程護欄 {#journeys-guardrails}

### 一般動作 {#general-actions-g}

* 沒有傳送限制。
* 如果出現錯誤，將系統地執行三次重試。您無法根據收到的錯誤訊息調整重試次數。
* 內建的&#x200B;**反應**&#x200B;事件可讓您對開箱即用的動作做出反應。 在[本頁](../building-journeys/reaction-events.md)中瞭解更多。如果要對透過自訂動作傳送的訊息做出反應，則需設定專用事件。
* 您無法同時進行兩個動作，必須逐一新增。
* 通常而言，設定檔無法在同一歷程中同時出現多次。如果啟用重新進入，設定檔可以重新進入歷程，但必須完全退出歷程的上一個執行個體，才能執行此動作。 [閱讀全文](../building-journeys/end-journey.md)

### 歷程版本 {#journey-versions-g}

* 從 v1 中的事件活動開始的歷程無法從其他版本中的事件開始。您無法透過&#x200B;**區段資格**&#x200B;事件開始歷程。
* 在 v1 中，以&#x200B;**區段資格**&#x200B;活動開始的歷程在後續版本中必須一律以&#x200B;**區段資格**&#x200B;開始。
* 在&#x200B;**區段資格** (第一個節點) 中選擇的區段和命名空間在新版本中無法變更。
* 所有歷程版本中的重新進入規則必須相同。
* 以&#x200B;**讀取區段**&#x200B;開始的歷程在下一個版本中無法以另一個事件開始。

### 自訂動作 {#custom-actions-g}

* 自訂動作 URL 不支援動態參數。
* 僅支援 POST 和 PUT 呼叫方法
* 查詢參數或標題的名稱不得以「.」開頭 或 &quot;$&quot;
* 不允許使用 IP 位址
* 內部 Adobe 位址 (.adobe.) 是不允許的。

### 活動 {#events-g}

* 對於系統產生的事件，必須先在 Journey Optimizer 中設定用於啟動客戶歷程的串流資料，才能取得唯一的協調流程 ID。 此協調流程 ID 必須附加至傳入 Adobe Experience Platform 的串流裝載。 此限制不適用於規則型事件。
* 業務事件不能與單一事件或區段資格活動結合使用。
* 單一歷程 (從事件或區段資格開始) 包含可防止為同一事件多次錯誤觸發歷程的護欄。 在預設情況下，設定檔重新進入時會暫時封鎖 5 分鐘。 例如，如果某個事件在 12:01 觸發特定設定檔的歷程，而另一個事件在 12:03 達到時間限制 (無論是相同事件或是不同事件觸發相同歷程)，則此設定檔的歷程將不會再次開始。
* Journey Optimizer 需將事件串流至資料收集核心服務 (DCCS)，才能觸發歷程。 批次收錄的事件，或來自內部 Journey Optimizer 資料集的事件 (訊息意見回饋、電子郵件追蹤等等) 無法用來觸發歷程。 若是無法取得串流事件的使用案例，請根據該事件建立區段，然後改用&#x200B;**讀取區段**&#x200B;活動。 技術上可使用區段資格，但可能根據使用動作而造成下游挑戰。

### 資料來源 {#data-sources-g}

* 可在客戶歷程中利用外部資料來源即時查詢外部資料。 這些來源必須可透過 REST API 使用、支援 JSON 並且能夠處理大量請求。

### 歷程與設定檔建立 {#journeys-limitation-profile-creation}

在 Adobe Experience Platform 中建立/更新以 API 為基礎的設定檔會有延遲。對於第 95 個百分位數的請求，服務層級目標 (SLT) 從接收到統一設定檔的延遲時間小於 1 分鐘，每秒請求量為 20K (RPS)。

如果在建立設定檔的同時觸發歷程，並立即從設定檔服務檢查/擷取資訊，則可能無法正常運作。

您可以從以下兩種解決方案中選擇一種：

* 在第一個事件後新增等待活動，為 Adobe Experience Platform 提供執行擷取至設定檔服務所需的時間。

* 設定不會立即運用設定檔的歷程。 例如，如果歷程的設計是要確認帳戶的建立，則體驗事件可能包含傳送第一個確認訊息 (名字、姓氏、電子郵件地址等) 所需的資訊。

### 讀取區段 {#read-segment-g}

* 串流區段一律為最新狀態，但擷取時不會計算批次區段。 它們僅在每日批次評估時間每天進行評估。
* 若為使用讀取區段活動的歷程，則有最多可同時開始的歷程次數。 系統將執行重試，但請避免在完全相同的時間，開始超過五個歷程 (使用讀取區段、排程或「盡快」)，方法是將其分散在一段時間內，例如相隔 5 到 10 分鐘。

### 運算式編輯器 {#expression-editor}

* 從「讀取」區段、「區段」資格或業務事件活動開始的歷程中，無法使用體驗事件欄位群組。 

