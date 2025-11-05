---
solution: Journey Optimizer
product: journey optimizer
title: 舊版發行說明 (2021 年)
description: Journey Optimizer 2021 年發行說明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hidefromtoc: true
hide: true
exl-id: 0e43be98-f471-4860-be84-8f99ab93e983
source-git-commit: 0331f8fe2439d41c08ad88a6d0bd95dd150bab90
workflow-type: tm+mt
source-wordcount: '2035'
ht-degree: 100%

---

# 2021 年發行說明 {#release-notes-2021}

此頁面列出了於 2021 年發行的[!DNL Journey Optimizer]所有功能和改善。

## 2021 年 11 月發行版本 {#november-2021-release}

<table>
<thead>
<tr>
<th><strong>CNAME 子網域委派</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 現在支援 CNAME。 CNAME (正式名稱) 記錄是指向其他網域位址而非 IP 位址的記錄。 CNAME 子網域委派可讓您建立子網域，並使用 CNAME 指向 Adobe 特定記錄。 使用此設定，您和 Adobe 都有責任維護 DNS，針對電子郵件的傳送、轉譯和追蹤設定環境。</p>
<p>如果貴司的原則限制完整的子網域委派法，則建議使用此方法。</p>
<p>如需 CNAME 子網域委派的詳細資訊，請參閱<a href="../configuration/delegate-subdomain.md#cname-subdomain-setup">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


## 2021 年 10 月發行版本 {#oct-2021-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>決定管理 — 產品建議模擬</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以模擬將哪些產品建議傳遞至測試輪廓中 Journey Optimizer UI 的指定位置。 這可讓您在投入生產之前，輕鬆驗證決定邏輯，包括資格限制和排名演算法。 此功能可讓非技術和技術使用者快速測試決策管理並針對潛在問題進行疑難排解。</p>
<p>如需詳細資訊，請參閱<a href="../offers/offer-activities/simulation.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>決定管理 — 個人化您的產品建議</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用 Adobe Experience Platform 輪廓屬性和客群，利用 Journey Optimizer UI 中的相同運算式編輯器元件來個人化產品建議內容。 </p>
<p>如需詳細資訊，請參閱<a href="../offers/offer-library/creating-personalized-offers.md#custom-text">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


另請參閱 [Adobe Experience Platform 10 月發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html?lang=zh-Hant){target="_blank"}，以便瞭解更多變更。

### 功能改進

**歷程**

* **運算式編輯器** - 身為超級使用者，您現在可以使用函式來處理地圖。 此功能可與訂閱清單搭配運用。 例如，您現在可以從客群的訂閱清單取得電子郵件地址。[在本範例進一步了解](../building-journeys/message-to-subscribers-uc.md)

* **監控** - 已增強即時歷程和測試模式的步驟事件。 [新欄位](../reports/sharing-field-list.md#serviceevents) 已新增與輪廓匯出作業有關的內容。 為了提供更佳的使用者體驗，步驟事件欄位現在會整理成不同類別。 所有先前的步驟事件欄位仍可在 [stepEvents](../reports/sharing-legacy-fields.md) 類別中使用。
* **協助工具** - 歷程已導入協助工具增強功能。
* **集合** - 現在支援包含子物件的物件陣列。 [閱讀全文](../building-journeys/collections.md)
* **清單** - 已改善歷程、事件、動作、資料來源的清單畫面。

**報告**

* **全域檢視中的資料格式** - 您現在可以在&#x200B;**執行**&#x200B;標籤中的&#x200B;**全域檢視**&#x200B;切換數字與百分比 。 


**管理**

* **編輯訊息預設集** - 您現在可以編輯訊息預設集並監視其更新狀態。 [進一步了解](../configuration/channel-surfaces.md#edit-channel-surface)
* **編輯 PTR 記錄** - 您現在可以編輯 PTR 記錄並監視其更新狀態。 [進一步了解](../configuration/ptr-records.md#edit-ptr-record)

**個人化**

* **新的日期格式協助工具功能** - 您現在可以指定日期字串的呈現方式。 [進一步了解](../personalization/functions/dates.md#format-date)


**決定管理**

* **評估排序** - 全新改進的決定建立流程不僅可讓您更順暢瀏覽於決定物件之間，而且讓您能夠完全控制決定引擎如何評估產品建議集合。 其中包括哪些集合會一起進行評估或分別評估，以及應以何種順序評估集合。 [進一步了解](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### 修正

* 修正當瀏覽器語言非英文時，無法顯示歷程清單、訊息清單和電子郵件設計工具的問題。
* 修正當在電子郵件設計工具中使用運算式新增個人化時發生的語法錯誤：字元轉譯錯誤。
* 修正導覽至&#x200B;**管理**&#x200B;功能表時導致 404 錯誤的問題。
* 修正當使用商業活動測試歷程時觸發其他即時歷程的問題。


## 2021 年 9 月發行版本 {#september-2021-release}

### 新功能

<table>
<thead>
<tr>

<th><strong>報告－以更好的方式深入解析目標客群</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>在報告中提供新指標：即時和全域報告都會顯示已鎖定和已排除對象的電子郵件和推送訊息。 </br> 若要存取最新指標，請注意，您必須為每個頻道和報告類型重新設定不同的報告儀表板。 如需儀表板客製化的詳細資訊，請參閱<a href="../reports/live-report.md">詳細文件。</a></p>
<p>訊息執行清單中包含新欄顯示每個訊息執行的目標輪廓數量。 </p>
<p>如需詳細資訊，請參閱<a href="../reports/report-gs-cja.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>使用自訂動作以動態方式傳遞資料清單</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在自訂動作參數中傳遞集合或資料清單，這些參數將在執行階段以動態方式填入。 支援兩種集合：簡單集合和物件集合。 先前建立的自訂動作將可繼續運作。 </p>
<p>如需關於集合的詳細資訊，請參閱<a href="../building-journeys/collections.md">詳細文件</a>。 </p>
<p>篩選和交集函式已在進階運算式編輯器中加入可用函式清單。 這提供了更多可能性來篩選和比較集合。</p>
<p>請參閱<a href="../building-journeys/functions/list-functions.md#filter">篩選</a>和<a href="../building-journeys/functions/list-functions.md#intersect">交集</a>函式。</p>
</td>
</tr>
</tbody>
</table>

### 功能改進

**歷程**

* 在佈建步驟事件期間建立並由系統產生的結構描述和資料集現在改為唯讀模式，可避免重要結構描述發生任何意外修改。 [進一步了解](../reports/sharing-overview.md)
* 簡潔標示&#x200B;**等待**&#x200B;活動，並在畫布中顯示標籤。 標籤也會用於報告和測試模式記錄，以清楚識別您正在執行的動作。 [進一步了解](../building-journeys/about-journey-activities.md#best-practices)
* 使用搜尋，透過篩選&#x200B;**事件**&#x200B;和&#x200B;**動作**&#x200B;類別中的元素，更快找到您的事件和動作。 不再篩選協調活動。 [進一步了解](../building-journeys/using-the-journey-designer.md)
* 在規則型或商業活動中定義事件 ID 條件時，「包含」運算子現在可用於字串類型欄位。 [進一步了解](../event/about-creating.md)

**電子郵件設定**

* 當 IP 集區連結訊息預設集時，您現在可以加以編輯，進行非同步更新。 您也可以檢查每個 IP 集區的更新狀態。 [進一步了解](../configuration/ip-pools.md#edit-ip-pool)


## 2021 年 8 月發行版本 {#august-2021-release}

### 新功能

<table>
<thead>
<tr>

<th><strong>在最佳時機傳送訊息 - 傳送時間最佳化</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>使用 Adobe Journey Optimizer 在最適當的時間自動向您接洽的每個客戶傳送推播通知或電子郵件。「傳送時間最佳化」採用 Adobe 的 AI 服務，可根據立即可用的歷史開啟率和點按率，預測傳送電子郵件或推播訊息的最佳時機，以實現最大化參與程度。</p>
<p>此功能目前為測試版本，僅供測試版客戶使用。 若要加入測試版計畫，請連絡 Adobe 客戶服務。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/send-time-optimization.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>在商業活動中利用結構描述關係 — 查閱表格管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在當您設定商業活動時，可以利用結構描述之間的關係。除了可在當設定單一事件時、當在歷程中、在個人化訊息和在個人化自訂動作中使用條件時運用連結表格的欄位，同時還包含此功能。</p>
<p>如需詳細資訊，請參閱<a href="../event/experience-event-schema.md#leverage_schema_relationships">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>個人化 URL</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>個人化 URL 會根據輪廓屬性，將收件者帶往網站特定頁面或個人化微網站。 您現在可以在 Adobe Journey Optimizer 的訊息內容加入個人化 URL。 URL 個人化可套用至文字和影像，同時使用輪廓或內容資料。</p>
<p>如需詳細資訊，請參閱<a href="../personalization/personalization-syntax.md#perso-urls">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>請確定您的電子郵件已送達您的使用者 — 重試電子郵件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以根據預設來定義重試期間，以確保當不再需要重試時，就不再進行重試。例如，對於密碼重設異動訊息包含僅一天有效的連結，您可以將重試期間設為 24 小時。請注意，重試設定只會套用至電子郵件頻道。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/retries.md#retry-duration">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>定義要排除的傳送地址 — 禁止名單</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在可從使用者介面在禁止名單新增電子郵件地址和網域，可逐一新增或透過 CSV 檔案上傳大量新增。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


### 功能改進

**歷程**

* **動態標頭** - 您現在可以在 HTTP 標頭參數中傳遞動態資料。 接收歷程動作 HTTP 呼叫的整合系統可使用這些參數 (例如時間戳記或追蹤 ID)。 [進一步了解](../action/about-custom-action-configuration.md#url-configuration)
* **Dynamic URL 路徑** - 您現在可以為自訂動作設定動態 URL 路徑。 [進一步了解](../action/about-custom-action-configuration.md#url-configuration)
* 讀取客群的總節流率已從每秒 17,000 則訊息變更為每秒 20,000 則訊息。[進一步了解](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**使用者介面**

* **搜尋** - 在每個頁面上，您現在可以直接從「統一的 Experience Cloud」搜尋欄位搜尋業務物件和說明文章。 [進一步了解](../start/user-interface.md#unified-search)
* **收件者** - 在 Adobe Journey Optimizer 首頁顯示收件者元素的功能，現在已擴充至其他業務物件。 透過此更新，提供包括您最近存取的訊息、歷程、客群、結構描述、資料集、資料來源、事件、動作、來源和目的地的捷徑。[進一步了解](../action/about-custom-action-configuration.md#passing-collection)

**內容設計**

* **背景** - 即時預覽現在支援背景影像。 [進一步了解](../content-management/preview-test.md)
  <!--* **One-click opt-out link** - You can insert a new type of link into your email content: the **Opt-out** link allows users to unsubscribe from receiving your communications in just one click, without being redirected to a landing page to confirm opting out. [Learn more](../privacy/opt-out.md#one-click-opt-out-link)-->

**個人化**

* **運算式編輯器** - 您現在可在定義個人化時輕鬆新增回傳值：當輪廓的個人化欄位空白時，將顯示回傳值。 [進一步了解](../personalization/functions/helpers.md)

**電子郵件設定**

* **允許清單** - 您現在可以透過 API 呼叫，在非生產沙箱上啟用和停用允許清單。 [進一步了解](../configuration/allow-list.md#enable-allow-list)
* **導覽** - 可在&#x200B;**管理 > 管道 > 電子郵件設定 > 一般**&#x200B;功能表中存取的禁止名單，已移至新的&#x200B;**禁止名單**&#x200B;子功能表，收集所有相關功能以便更輕鬆存取。[進一步了解](../configuration/manage-suppression-list.md#access-suppression-list)

**決定管理**

* 建立產品建議時新增和設定代表的方式已更新，以改善使用者體驗。 特別是，現在只有當您定義代表的影像類型內容時，才會顯示資料庫。[進一步了解](../offers/offer-library/creating-personalized-offers.md#representations)

### 修正

* 修正訊息標籤導覽的協助工具問題。
* 已修正電子郵件設計工具標籤中的本地化問題。
* 修正在歷程中選取多個節點並在屬性面板上按一下「刪除」時的問題。
* 修正無法將新標題加入歷程使用的動作問題。
* 您現在可以透過使用者介面中更明確的警告，找出訊息預設集建立失敗的原因。


## 2021 年 7 月發行版本 {#july-2021-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>在訊息中使用中繼資料 — 管理查詢表格</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過您載入 Journey Optimizer 的參考資料豐富您的體驗。 例如，在體驗事件中查詢預訂 ID 的中繼資料，或在體驗事件中從 SKU 尋找產品資訊以用於畫布。 </p>
<p>您現在可以運用結構描述間的關係，將一個資料集作為其他資料集的查閱表格。 接著，當設定單一事件時、當在歷程中、在個人化訊息和在個人化自訂動作中使用條件時，您就可以運用連結表格中的所有欄位。</p>
<p>如需詳細資訊，請參閱<a href="../event/experience-event-schema.md#leverage_schema_relationships">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>允許清單</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在沙箱層級定義特定的傳送安全清單，以便擁有可用於測試目的的安全環境。 在可能發生錯誤的非生產執行個體上，允許清單可確保避免您將不需要的訊息傳送給客戶的風險。 此功能需透過隱藏 API 來啟用。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/allow-list.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

### 功能改進

**歷程**

* 對於在同一沙箱同時執行的所有讀取客群，其總節流率限制為每秒 17,000 則訊息。[閱讀全文](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* **快取期間** 欄位已從資料來源設定窗格中移除。 [閱讀全文](../datasource/about-data-sources.md)
* 對於外部資料來源，現在會自動定義每秒 15 次呼叫的上限規則。 [閱讀全文](../configuration/external-systems.md#capping)
* 對於即時歷程，歷程屬性畫面現在會顯示發佈日期和發佈歷程的使用者名稱。 [閱讀全文](../building-journeys/journey-gs.md#change-properties)
* 在歷程清單畫面中，已新增歷程類型篩選器。 [閱讀全文](../start/user-interface.md#filter-lists)
* **[!UICONTROL 節流率]**&#x200B;參數已新增至讀取客群活動中。[閱讀全文](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**預覽和測試**

* 身分識別和命名空間現在會顯示在&#x200B;**[!UICONTROL 預覽]**&#x200B;畫面中。[閱讀全文](../content-management/preview-test.md#preview-your-messages)
* 校樣的測試電子郵件數目現在限制為 10 則。
* 已在校樣中限制&#x200B;**主旨行首碼** 允許的字元。 [閱讀全文](../content-management/preview-test.md#send-proofs)

**個人化運算式編輯器**

* 已重新命名並重新排序協助工具下拉式清單。

### 修正

* 修正導致批次電子郵件傳遞重複傳送訊息的問題。
* 當重試期間結束後未執行電子郵件傳送時，現在會據此產生事件。
* 修正「PTR 記錄」畫面中缺少 IP 資訊的問題。
* 現在運算式編輯器中已實施本地化的產品建議邊欄。
* 修正資訊快顯視窗的間距錯誤。
* 已修正當電子郵件設計工具中上傳 HTML 檔案時，內部樣式表包含未支援的 `background-image` 屬性問題。
