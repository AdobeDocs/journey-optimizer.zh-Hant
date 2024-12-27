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
source-git-commit: a8b49bf278b26a31b0da9532fb07f211f397119e
workflow-type: tm+mt
source-wordcount: '2361'
ht-degree: 99%

---

# 護欄與限制 {#limitations}

權利、產品限制和效能護欄列於 [Adobe Journey Optimizer 產品說明頁面](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}。

在啟動](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=zh-Hant){target="_blank"}之前，您還需要注意即時客戶輪廓資料的[護欄。

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

## SMS 護欄 {#sms-guardrails}

* MMS 適用的媒體檔案可透過支援的 URL 加入。請確定媒體檔案已個別上傳。
* 訊息回饋同步目前不適用於 MMS。
* 同意管理在 MMS 的 SMS 通道層級運作。

### 網頁管道護欄 {#web-guardrails}

[!DNL Journey Optimizer] 網路行銷活動會選擇以其他管道上不曾有過互動的新輪廓為目標。這樣做會增加可互動輪廓總數，如果其超過您購買的可互動輪廓合約數量，可能會影響成本。 各個套件的授權量度都列在 [Journey Optimizer 產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}頁面上。


## 子網域護欄 {#subdomain-guardrails}

預設情況下，[!DNL Journey Optimizer]可讓您總共委派最多 10 個子網域 (包含電子郵件與 Web 管道)。

然而，根據您的授權合約，您最多可委派 100 個子網域。 請聯絡您的 Adobe 聯絡人，了解更多您有權使用的子網域數量。

## 片段護欄 {#fragments-guardrails}

* 視覺片段僅可用於電子郵件管道。
* 運算式片段不適用於應用程式內管道。

## 歷程護欄 {#journeys-guardrails}

### 一般歷程護欄 {#journeys-guardrails-journeys}

* 歷程中的活動數限定為最多 50 個。活動數會顯示於歷程畫布的左上方區段。這有助於提高可讀性、QA 及疑難排解。
* 當您發佈歷程時，我們會自動縮放和調整，以確保輸送量與穩定性達到最高。 當您一次接近 100 個即時歷程的里程碑時，您會看到此成果的 UI 中出現通知。 如果您看到此通知，並需要一次將歷程擴充至 100 個即時歷程以上，請建立客戶服務支援服務單，我們將協助您達成目標。
  <!-- DOCAC-10977 * As you publish journeys, we automatically scale and adjust to ensure maximum throughput and stability. As you near the milestone of 500 live journeys at one time, you will see a notification appear in the UI on this achievement. If you see this notification and have a need to extend your journeys beyond 500 live journeys at a time, please create a ticket for customer care and we will help you reach your goals.-->
* 在歷程中使用客群資格時，該客群資格活動最多可能需要 10 分鐘，才會啟用和接聽進入或退出客群的輪廓。
* 輪廓的歷程執行個體大小上限為 1MB。在歷程執行過程中收集的所有資料都會儲存在該歷程執行個體中。因此，來自傳入事件的資料、從 Adobe Experience Platform 擷取的輪廓資訊、自訂動作回應等會儲存在該歷程執行個體中，並影響歷程大小。當歷程以事件開始時，建議限制該事件承載的大小上限 (例如：低於 800 KB)，以避免在歷程執行中經過幾項活動後達到該限制。 當達到該限制時，輪廓處於錯誤狀態並將從歷程中排除。
* 除了歷程活動中使用的逾時之外，還有一個不會顯示在介面且無法變更的全域歷程逾時。 此全域逾時會在個人進入歷程 91 天後停止其進度。 [閱讀全文](../building-journeys/journey-properties.md#global_timeout)


### 一般動作 {#general-actions-g}

* 如果出現錯誤，將系統地執行三次重試。您無法根據收到的錯誤訊息調整重試次數。除 HTTP 401、403 和 404 外，會對所有 HTTP 錯誤執行重試。
* 內建的&#x200B;**反應**&#x200B;事件可讓您對開箱即用的動作做出反應。 在[本頁](../building-journeys/reaction-events.md)中瞭解更多。如果要對透過自訂動作傳送的訊息做出反應，則需設定專用事件。
* 您無法同時進行兩個動作，必須逐一新增。
* 輪廓無法在同一歷程中同時出現多次。如果啟用重新進入，輪廓可以重新進入歷程，但必須完全退出歷程的上一個執行個體，才能執行此動作。[閱讀全文](../building-journeys/end-journey.md)

### 歷程版本 {#journey-versions-g}

* 從 v1 中的事件活動開始的歷程無法從其他版本中的事件開始。您無法透過&#x200B;**客群資格**&#x200B;事件開始歷程。
* 在 v1 中以&#x200B;**客群資格**&#x200B;活動開始的歷程，在後續版本中必須一律以&#x200B;**客群資格**&#x200B;開始。
* 在&#x200B;**客群資格** (第一個節點) 中選擇的客群與命名空間在新版本中無法變更。
* 所有歷程版本中的重新進入規則必須相同。
* 以&#x200B;**讀取客群**&#x200B;開始的歷程在後續版本中無法以另一個事件開始。
* 您無法建立使用增量讀取方式的新讀取客群歷程版本。 您必須重複歷程。

### 自訂動作 {#custom-actions-g}

* 為每個主機和每個沙箱的所有自訂動作，定義 1 分鐘內 300,000 次呼叫的上限。請參見[此頁面](../action/about-custom-action-configuration.md)。此限制是根據客戶使用情況來設定，可保護自訂動作鎖定為目標的外部端點。您必須在以對象為基礎的歷程考慮這一點，透過定義適當的讀取率 (使用自訂動作時為每秒 5000 個輪廓)。如有需要，您可以透過上限/節流 API 定義較高的上限或節流限制來覆寫此設定。 請參閱[此頁面](../configuration/external-systems.md)。
* 自訂動作 URL 不支援動態參數。
* 支援 POST、PUT 和 GET 呼叫方法
* 查詢參數或標題的名稱不得以「.」開頭 或 &quot;$&quot;
* 不允許使用 IP 位址
* 內部 Adobe 地址 (`.adobe.*`) 不允許在 URL 及 API 中使用。
* 無法移除內建自訂動作。
* 自訂動作僅在使用請求或回應裝載時支援 JSON 格式。 請參閱[此頁面](../action/about-custom-action-configuration.md#custom-actions-limitations)。
* 使用自訂動作選擇要作為目標的端點時，請確定：

   * 此端點可使用來自[節流 API](../configuration/throttling.md) 或[設定 API 上限](../configuration/capping.md)的設定來支援歷程的輸送量，藉此加以限制。 請留意，節流設定不可低於 200 TPS。任何目標端點必須支援至少 200 TPS。
   * 此端點的回應時間必須儘可能縮短。 根據預期輸送量，高回應時間可能會影響實際輸送量。

### 活動 {#events-g}

* 對於系統產生的事件，必須先在 Journey Optimizer 中設定用於啟動客戶歷程的串流資料，才能取得唯一的協調流程 ID。 此協調流程 ID 必須附加至傳入 Adobe Experience Platform 的串流裝載。 此限制不適用於規則型事件。
* 業務事件不能與單一事件或客群資格活動結合使用。
* 單一歷程 (從事件或客群資格開始) 包含可防止同一事件多次錯誤觸發歷程的護欄。 在預設情況下，輪廓重新進入時會暫時封鎖 5 分鐘。例如，如果某個事件在 12:01 觸發特定輪廓的歷程，而另一個事件在 12:03 達到時間限制 (無論是相同事件或是不同事件觸發相同歷程)，則此輪廓的歷程將不會再次開始。
* Journey Optimizer 需將事件串流至資料收集核心服務 (DCCS)，才能觸發歷程。 批次擷取的事件，或來自內部Journey Optimizer資料集的事件（訊息回饋、電子郵件追蹤等）無法用於觸發歷程。 對於無法取得串流事件的使用案例，請根據這些事件建置對象，然後改為使用&#x200B;**讀取對象**&#x200B;活動。 技術上可使用對象資格，但不建議使用，因為它可能會根據所使用的操作導致下游挑戰。


### 資料來源 {#data-sources-g}

* 可在客戶歷程中利用外部資料來源即時查詢外部資料。 這些來源必須可透過 REST API 使用、支援 JSON 並且能夠處理大量請求。
* 內部 Adobe 地址 (`.adobe.*`) 不允許在 URL 及 API 中使用。

>[!NOTE]
>
>現已支援回應，對於外部資料來源使用案例，您應該使用自訂動作，而非資料來源。

### 歷程與輪廓建立 {#journeys-limitation-profile-creation}

在 Adobe Experience Platform 中建立/更新以 API 為基礎的輪廓會有延遲。對於第 95 個百分位數的請求，服務層級目標 (SLT) 從接收到統一輪廓的延遲時間小於 1 分鐘，每秒請求量為 20K (RPS)。

如果在建立輪廓的同時觸發歷程，並立即從輪廓服務檢查/擷取資訊，則可能無法正常運作。

您可以從以下兩種解決方案中選擇一種：

* 在第一個事件後新增等待活動，為 Adobe Experience Platform 提供執行擷取至輪廓服務所需的時間。

* 設定不會立即運用輪廓的歷程。 例如，如果歷程的設計是要確認帳戶的建立，則體驗事件可能包含傳送第一個確認訊息 (名字、姓氏、電子郵件地址等) 所需的資訊。

### 更新輪廓 {#update-profile-g}

特定護欄套用於&#x200B;**[!UICONTROL 更新輪廓]**&#x200B;活動。它們會在[本頁面](../building-journeys/update-profiles.md)中列出。


### 讀取對象 {#read-segment-g}

下列護欄適用於&#x200B;**[!UICONTROL 讀取對象]**&#x200B;活動：

* 串流客群一律為最新狀態，但擷取時不會計算批次客群。 它們僅在每日批次評估時間每天進行評估。
* 對於使用&#x200B;**讀取客群**&#x200B;活動的歷程，則可同時開始的歷程次數有其上限。 系統將執行重試，但請避免同時開始超過五個歷程 (使用&#x200B;**讀取客群**、已排程或「盡快」開始)，方法是將其分散在一段時間內開始，例如相隔 5 到 10 分鐘。
* **讀取客群**&#x200B;活動無法搭配 Adobe Campaign 活動使用。
* **讀取客群**&#x200B;活動只能作為歷程中的第一個活動，或商業事件活動後的第一個活動。
* 歷程只能有一個&#x200B;**讀取客群**&#x200B;活動。
* 另請參閱[此頁面](../building-journeys/read-audience.md)中關於如何使用&#x200B;**讀取客群**&#x200B;活動的建議。
* 擷取匯出工作時，預設會對對象觸發的歷程 (從&#x200B;**讀取客群**&#x200B;或&#x200B;**商業事件**&#x200B;開始) 套用重試。如果在匯出工作建立期間發生錯誤，將每隔 10 分鐘進行重試，最長為 1 小時。在這之後，我們會將其視為失敗。因此，這些類型的歷程可在排程時間後最多 1 小時執行。


### 對象資格 {#audience-qualif-g}

下列護欄適用於&#x200B;**[!UICONTROL 對象資格]**&#x200B;活動：

* 對象資格活動無法與 Adobe Campaign 活動搭配使用。


### 運算式編輯器 {#expression-editor}

* 從讀取客群、客群資格或業務事件活動開始的歷程中，無法使用體驗事件欄位群組。 您需要建立新對象，以及在歷程中使用非對象條件。


### 應用程式內活動 {#in-app-activity-limitations}

* 此功能目前不適用於醫療保健客戶。

* 個人化只能包含輪廓屬性。

* 應用程式內活動無法搭配 Adobe Campaign 活動使用。

* 應用程式內顯示會繫結至歷程期限，這表示當輪廓的歷程結束時，該歷程中的所有應用程式內訊息將不再顯示該輪廓。  因此，無法直接從歷程活動停止應用程式內訊息。 而是必須結束整個歷程，才能停止將應用程式內訊息顯示給輪廓。

* 在測試模式中，應用程式內顯示取決於歷程的有效期限。 為避免歷程在測試期間過早結束，請調整&#x200B;**[!UICONTROL 等待]**&#x200B;活動的&#x200B;**[!UICONTROL 等待時間]**&#x200B;值。

* **[!UICONTROL 回應]**&#x200B;活動無法用於對應用程式內開啟或點按做出反應。

* 啟動延遲可能發生在使用者輪廓到達畫布中的應用程式內活動的時刻和他們開始看到該應用程式內訊息的時刻之間。

* 應用程式內訊息內容大小限制為 2Mb。 包含大型影像可能會阻礙發佈過程。



### 跳轉活動 {#jump-g}

特定護欄適用於&#x200B;**[!UICONTROL 跳轉]**&#x200B;活動。它們會[在本頁面](../building-journeys/jump.md#jump-limitations)中列出。

### 行銷活動 {#ac-g}

下列護欄適用於 **[!UICONTROL Campaign v7/v8]** 和 **[!UICONTROL Campaign Standard]** 活動：

* Adobe Campaign 活動不能與讀取對象或對象資格活動搭配使用。
* 這些活動無法與應用程式內活動搭配使用。

## 客群護欄 {#audience}

您可以在指定的沙箱中發佈最多 10 個客群組合。如果您達到此臨界值，則需要刪除組合以釋放空間，才能發佈新的組合。

## 決策管理護欄 {#decision-management}

### 效能護欄 {#performance-guardrails}

傳遞輸送量對應至決策管理應用程式服務可在指定時間內傳遞的決策回應數。 每秒的決策數如下表所示。

| API | 每秒決策數 |
|---------|----------|
| 決策 API 請求 | 每秒 500 個 |
| Edge Decisioning API 請求與 Edge 分段 | 每秒 1500 個 |
| Edge Decisioning API 請求不含 Edge 分段 | 每秒 5000 個 |

### 限制 {#offers-limitations}

決策管理限制如下所列。

* **核准的個人化優惠 + 遞補優惠** - 核准的個人化優惠與核准的遞補優惠合併計算，最多 10,000 個。
* **決策** - 最多 10,000 個決策。
* **即時決策** - Offer Decisioning 應用程式服務支援最多 1,000 個即時決策。
* **每個回應傳回的優惠數** - Offer Decisioning 在請求中的所有決策範圍，支援每個請求最多傳回 100 個優惠。
* **集合** - 最多 10,000 個集合。
* **每個決策的集合** - 每個決策最多 30 個集合。
* **決定規則 + 排名函數** - 決定規則和排名函數合併計算，最多 10,000 個。
* **位置** - 最多 1,000 個位置。
* **每個決策的位置** - 每個決策最多 30 個位置。
* **每個決策的排名方法** - Offer Decisioning 應用程式服務支援每個決策最多 30 個排名函數。
* **AI 排名模型** - Offer Decisioning 應用程式服務支援最多 5 個 AI 排名模型。
* **每個優惠或集合的集合限定詞** - 在任何單一個人化優惠或單一集合中，Offer Decisioning 應用程式服務支援最多 20 個集合限定詞。
* **集合限定詞總數** -Offer Decisioning 應用程式服務支援最多 1,000 個集合限定詞。