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
source-git-commit: 1534106b7ed80376060d39a445d5e706df832e05
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 99%

---

# 護欄和限制 {#limitations}

權利、產品限制和效能護欄列於 [Adobe Journey Optimizer 產品說明頁面](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}。

在啟動](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=zh-Hant){target="_blank"}之前，您還需要注意即時客戶設定檔資料的[護欄。

當使用 [!DNL Adobe Journey Optimizer] 時，您將找到下面其他護欄和限制。

## 支援的瀏覽器 {#browsers}

Adobe [!DNL Journey Optimizer] 介面的設計可在最新版 Google Chrome 中以最佳方式運作。 您在舊版或其他瀏覽器上使用某些功能時可能會遇到問題。

## 訊息護欄 {#message-guardrails}

* 您無法向帶有[!DNL Journey Optimizer]的電子郵件新增附件。
* 您無法使用相同的傳送網域從[!DNL Adobe Journey Optimizer]和其他產品 (例如[!DNL Adobe Campaign]或[!DNL Adobe Marketo Engage]) 傳送訊息。


## 登陸頁面護欄 {#lp-guardrails}

* 一個主頁面只能使用一個&#x200B;**表單**&#x200B;元件。
* 此&#x200B;**表單**&#x200B;元件無法在子頁面中使用。
* 您無法將預覽文字新增至登陸頁面。
* 在設計登陸主要頁面時，您無法選取&#x200B;**自行編碼**&#x200B;選項。

## 歷程護欄 {#journeys-guardrails}

### 一般歷程護欄 {#journeys-guardrails-journeys}

* 歷程中的活動數限定為最多 50 個。活動數會顯示於歷程畫布的左上方區段。這有助於提高可讀性、QA 及疑難排解。
* 當您發佈歷程時，我們會自動縮放和調整，以確保輸送量與穩定性達到最高。 當您一次接近 100 個即時歷程的里程碑時，您會看到此成果的 UI 中出現通知。 如果您看到此通知，並需要一次將歷程擴充至 100 個即時歷程以上，請建立客戶服務支援服務單，我們將協助您達成目標。

### 一般動作 {#general-actions-g}

* 如果出現錯誤，將系統地執行三次重試。您無法根據收到的錯誤訊息調整重試次數。除HTTP 401、403和404外，會對所有HTTP錯誤執行重試。
* 內建的&#x200B;**反應**&#x200B;事件可讓您對開箱即用的動作做出反應。 在[本頁](../building-journeys/reaction-events.md)中瞭解更多。如果要對透過自訂動作傳送的訊息做出反應，則需設定專用事件。
* 您無法同時進行兩個動作，必須逐一新增。
* 設定檔無法在同一歷程中同時出現多次。如果啟用重新進入，設定檔可以重新進入歷程，但必須完全退出歷程的上一個執行個體，才能執行此動作。 [閱讀全文](../building-journeys/end-journey.md)

### 歷程版本 {#journey-versions-g}

* 從 v1 中的事件活動開始的歷程無法從其他版本中的事件開始。您無法透過&#x200B;**對象資格**&#x200B;事件開始歷程。
* 在 v1 中以&#x200B;**對象資格**&#x200B;活動開始的歷程，在後續版本中必須一律以&#x200B;**對象資格**&#x200B;開始。
* 在&#x200B;**對象資格** (第一個節點) 中選擇的對象與命名空間在新版本中無法變更。
* 所有歷程版本中的重新進入規則必須相同。
* 以&#x200B;**讀取對象**&#x200B;開始的歷程在後續版本中無法以另一個事件開始。
* 您無法建立使用增量讀取方式的新讀取對象歷程版本。 您需要複製歷程。

### 自訂動作 {#custom-actions-g}

* 自訂動作 URL 不支援動態參數。
* 僅支援 POST 和 PUT 呼叫方法
* 查詢參數或標題的名稱不得以「.」開頭 或 &quot;$&quot;
* 不允許使用 IP 位址
* 內部 Adobe 地址 (`.adobe.*`) 不允許在 URL 及 API 中使用。
* 無法移除內建自訂動作。

### 活動 {#events-g}

* 對於系統產生的事件，必須先在 Journey Optimizer 中設定用於啟動客戶歷程的串流資料，才能取得唯一的協調流程 ID。 此協調流程 ID 必須附加至傳入 Adobe Experience Platform 的串流裝載。 此限制不適用於規則型事件。
* 業務事件不能與單一事件或對象資格活動結合使用。
* 單一歷程 (從事件或對象資格開始) 包含可防止同一事件多次錯誤觸發歷程的護欄。 在預設情況下，設定檔重新進入時會暫時封鎖 5 分鐘。 例如，如果某個事件在 12:01 觸發特定設定檔的歷程，而另一個事件在 12:03 達到時間限制 (無論是相同事件或是不同事件觸發相同歷程)，則此設定檔的歷程將不會再次開始。
* Journey Optimizer 需將事件串流至資料收集核心服務 (DCCS)，才能觸發歷程。 批次收錄的事件，或來自內部 Journey Optimizer 資料集的事件 (訊息意見回饋、電子郵件追蹤等等) 無法用來觸發歷程。 對於無法取得串流事件的使用案例，請根據這些事件建置對象，然後改為使用&#x200B;**讀取對象**&#x200B;活動。 技術上可使用對象資格，但根據使用的動作，此舉可能會造成下游挑戰。

### 資料來源 {#data-sources-g}

* 可在客戶歷程中利用外部資料來源即時查詢外部資料。 這些來源必須可透過 REST API 使用、支援 JSON 並且能夠處理大量請求。
* 內部 Adobe 地址 (`.adobe.*`) 不允許在 URL 及 API 中使用。

### 歷程與設定檔建立 {#journeys-limitation-profile-creation}

在 Adobe Experience Platform 中建立/更新以 API 為基礎的設定檔會有延遲。對於第 95 個百分位數的請求，服務層級目標 (SLT) 從接收到統一設定檔的延遲時間小於 1 分鐘，每秒請求量為 20K (RPS)。

如果在建立設定檔的同時觸發歷程，並立即從設定檔服務檢查/擷取資訊，則可能無法正常運作。

您可以從以下兩種解決方案中選擇一種：

* 在第一個事件後新增等待活動，為 Adobe Experience Platform 提供執行擷取至設定檔服務所需的時間。

* 設定不會立即運用設定檔的歷程。 例如，如果歷程的設計是要確認帳戶的建立，則體驗事件可能包含傳送第一個確認訊息 (名字、姓氏、電子郵件地址等) 所需的資訊。

### 讀取對象 {#read-segment-g}

* 串流對象一律為最新狀態，但擷取時不會計算批次對象。 它們僅在每日批次評估時間每天進行評估。
* 對於使用讀取對象活動的歷程，則可同時開始的歷程次數有其上限。 系統將執行重試，但請避免同時開始超過五個歷程 (使用讀取對象、已排程或「盡快」開始)，方法是將其分散在一段時間內開始，例如相隔 5 到 10 分鐘。

### 運算式編輯器 {#expression-editor}

* 從讀取對象、對象資格或業務事件活動開始的歷程中，無法使用體驗事件欄位群組。 您需要建立新對象，以及在歷程中使用非對象條件。

