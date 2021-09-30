---
title: 發行說明
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: bb52c8e92621815c61528558aca6fbc326230e00
workflow-type: tm+mt
source-wordcount: '1526'
ht-degree: 18%

---

# 發行說明 {#release-notes}

本頁面列出[!DNL Journey Optimizer]的所有新功能和改善項目。您也可以參閱最新的[文件更新](documentation-updates.md)。



## 2021年9月發行 {#september-2021-release}

### 新功能

<table>
<thead>
<tr>

<th><strong>報表 — 更深入分析目標受眾</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>報表中提供新量度：即時和全域報表中都會顯示電子郵件和推送訊息的已定位和已排除。 </br> 若要存取最新量度，請注意，您必須重設每個管道和報表類型的不同報表控制面板。有關儀表板自定義的詳細資訊，請參閱<a href="reports/live-report.md">詳細文檔。</a></p>
<p>訊息執行清單中的新欄會顯示每個訊息執行的目標設定檔數量。 </p>
<p>如需詳細資訊，請參閱<a href="message-monitoring.md">詳細文件</a>。</p>
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
<p>您現在可以在自訂動作參數中傳遞集合或資料清單，這些參數將在執行階段動態填入。 支援兩種集合：簡單集合和對象集合。 先前建立的自訂動作將可繼續運作。 </p>
<p>有關集合的詳細資訊，請參閱<a href="building-journeys/collections.md">詳細檔案</a>。 </p>
<p>篩選器和交叉函式已添加到高級表達式編輯器中可用的函式清單中。 這提供更多篩選和比較集合的可能性。</p>
<p>請參閱<a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionfilter.html">filter</a>和<a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functiontintersect.html">intersect</a>函式的相關文檔。</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decision Management - Personalize your offers</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now personalize content added to your offers' representations using the expression editor.</p>
<p>For more information, refer to the <a href="offers/offer-library/creating-personalized-offers.md#content">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### 改良功能

**歷程**

* 布建步驟事件期間建立的系統產生的結構描述和資料集現在為唯讀模式，可避免重要結構的任何意外修改。 [了解更多](reports/sharing-overview.md)
* 乾淨地標籤&#x200B;**Wait**&#x200B;活動，並標籤將顯示在畫布中。 標籤也會用於報表和測試模式記錄檔，以清楚識別您正在執行的動作。 [了解更多](building-journeys/about-journey-activities.md#best-practices)
* 使用搜尋來篩選&#x200B;**Events**&#x200B;和&#x200B;**Action**&#x200B;類別中的元素，以更快找到事件和動作。 不再篩選協調活動。 [了解更多](building-journeys/using-the-journey-designer.md)
* 在規則型或業務事件中定義事件ID條件時，「包含」運算子現在可用於欄位的字串類型。 [了解更多](event/about-creating.md)

**電子郵件設定**

* 當IP池與消息預設集關聯時，您現在可以編輯它，更新為非同步。 您也可以檢查每個IP池的更新狀態。 [了解更多](configuration/ip-pools.md#edit-ip-pool)

## 2021 年 8 月發行版本 {#august-2021-release}

### 新功能

<table>
<thead>
<tr>

<th><strong>在最佳時機傳送訊息 — 傳送時間最佳化</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>使用 Adobe Journey Optimizer 在最適當的時間自動向您接洽的每個客戶傳送推播通知或電子郵件。「傳送時間最佳化」採用Adobe的AI服務，可根據歷史開啟率和立即可用的點按率，預測傳送電子郵件或推送訊息的最佳時機，以最大化參與。</p>
<p>此功能目前為測試版，僅供測試版客戶使用。 若要加入測試版計畫，請連絡Adobe客戶服務。</p>
<p>如需詳細資訊，請參閱<a href="building-journeys/journeys-message.md#send-time-optimization">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>在業務事件中利用架構關係 — 查閱表格管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在設定業務事件時，運用結構之間的關係。 除了可在設定單一事件、在歷程中使用條件、在訊息個人化和在自訂動作個人化中時，運用連結表格的欄位外，還有此功能。</p>
<p>如需詳細資訊，請參閱<a href="event/experience-event-schema.md#leverage_schema_relationships">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>個人化URL</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>個人化URL會根據設定檔屬性，將收件者帶往網站的特定頁面或個人化微網站。 在Adobe Journey Optimizer中，您現在可以將個人化新增至訊息內容中的URL。 URL個人化可套用至文字和影像，以及使用設定檔資料或內容資料。</p>
<p>如需詳細資訊，請參閱<a href="personalization/personalization-syntax.md#perso-urls">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>請確定您的電子郵件已送達您的使用者 — 電子郵件重試</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以根據預設來定義重試期間，以確保當不再需要重試時，就不再進行重試。例如，對於包含僅一天有效連結的密碼重設交易式訊息，您可以將重試期間設為24小時。 請注意，重試設定只會套用至電子郵件通道。</p>
<p>如需詳細資訊，請參閱<a href="configuration/retries.md#retry-duration">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>定義要從發送中排除的地址 — 隱藏清單</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在可從用戶介面新增電子郵件地址和網域到隱藏清單中，逐一新增或透過 CSV 檔案上傳大量新增皆可。</p>
<p>如需詳細資訊，請參閱<a href="configuration/manage-suppression-list.md#add-addresses-and-domains">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Customer Alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now subscribe to event-based alerts regarding Adobe Journey Optimizer activities. The user interface allows you to view a history of received alerts based on metrics revealed by Adobe Experience Platform Observability Insights. The UI also allows you to view, enable, and disable available alert rules.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.
</p>
<p>For more information, refer to the <a href="https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html">Adobe Experience Platform documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### 改良功能

**歷程**

* **動態標題**  — 您現在可以以HTTP標題參數傳遞動態資料。接收歷程動作 HTTP 呼叫 (例如時間戳記或追蹤 ID) 的整合系統可使用這些參數。 [了解更多](action/about-custom-action-configuration.md#url-configuration)
* **動態URL路徑**  — 您現在可以為自訂動作設定動態URL路徑。[了解更多](action/about-custom-action-configuration.md#url-configuration)
* 讀取段的總節流率已從每秒17,000條消息更改為每秒20,000條消息。 [了解更多](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**使用者介面**

* **搜尋**  — 現在，您可以在每個頁面上，直接從「統一Experience Cloud」搜尋欄位搜尋業務物件和說明文章。[了解更多](user-interface.md#unified-search)
* **收件**  — 從Adobe Journey Optimizer首頁顯示的收件元素現在已擴充至其他業務物件。透過此更新，您最近存取的捷徑包括訊息、歷程、區段、結構、資料集、資料來源、事件、動作、來源和目的地。 [了解更多](action/about-custom-action-configuration.md#passing-collection)

**內容設計**

* **背景**  — 現在即時預覽支援背景影像。[了解更多](preview.md)
* **一鍵式選擇退出連結**  — 您可以在電子郵件內容中插入新類型的連結：「選 **擇退** 出」連結可讓使用者只要按一下，就能取消訂閱收到您的通訊內容，而不需重新導向至登陸頁面以確認選擇退出。[了解更多](message-tracking.md#one-click-opt-out-link)

**個人化**

* **運算式編輯器**  — 您現在可以在定義個人化時輕鬆新增回傳值：當設定檔的個人化欄位空白時，將顯示回傳值。[了解更多](personalization/functions/helpers.md)

**電子郵件設定**

* **允許清單**  — 現在可以透過API呼叫，在非生產沙箱上啟用和停用允許清單。[了解更多](allow-list.md#enable-allow-list)
* **導航**  — 可在「管理」>「通道」>「電子郵件配置」>「一般」 **菜單下訪問的隱藏清單已移至新的「隱藏清單」子菜單，該子菜單** 將收集 **** 所有相關功能，以便更方便地訪問。[了解更多](configuration/manage-suppression-list.md#access-suppression-list)

**決定管理**

* 建立優惠時新增和設定代表的方式已更新，以改善使用者體驗。 在其中，現在只有當您定義代表的影像類型內容時，才會顯示資料庫。[了解更多](offers/offer-library/creating-personalized-offers.md#representations)

### 修正

* 修正訊息標籤導覽的協助工具問題。
* 修正電子郵件設計工具標籤的本地化問題。
* 修正在歷程中選取多個節點並按一下屬性面板上「刪除」時的問題。
* 修正無法將新標題新增至歷程中使用之動作的問題。
* 您現在可以透過使用者介面中更明確的警告，找出訊息預設集建立失敗的原因。


## 2021 年 7 月發行版本 {#july-2021-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>在訊息中使用中繼資料 — 查詢表格管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過您已載入Journey Optimizer中的參考資料豐富您的體驗。 例如，在體驗事件中查詢訂房ID的中繼資料，或在體驗事件中從SKU尋找產品資訊以用於畫布。 </p>
<p>您現在可以運用結構間的關係，將一個資料集用作其他資料集的查閱表格。 接著，在設定單一事件、在歷程中使用條件、在訊息個人化和在自訂動作個人化中時，您就可以運用連結表格中的所有欄位。</p>
<p>如需詳細資訊，請參閱<a href="event/experience-event-schema.md#leverage_schema_relationships">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>允許的清單</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在沙箱層級定義特定的傳送安全清單，以便擁有安全的環境以用於測試用途。 在可能發生錯誤的非生產執行個體上，允許的清單可確保您沒有將不需要的訊息傳送給客戶的風險。 此功能是透過利用隱藏API來啟用。</p>
<p>如需詳細資訊，請參閱<a href="allow-list.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改良功能

**歷程**

* 在同一沙箱中同時執行的所有讀取區段的總節流率限制為每秒17,000條訊息。 [閱讀全文](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* 已從資料源配置窗格中刪除&#x200B;**快取持續時間**&#x200B;欄位。 [閱讀全文](datasource/about-data-sources.md)
* 對於外部資料來源，現在會自動定義每秒15次呼叫的上限規則。 [閱讀全文](configuration/external-systems.md#capping)
* 對於即時歷程，歷程屬性畫面現在會顯示發佈日期和發佈歷程的使用者名稱。 [閱讀全文](building-journeys/journey-gs.md#change-properties)
* 在歷程清單畫面中，已新增歷程類型篩選器。 [閱讀全文](user-interface.md#section_lgm_hpz_pgb)
* 已在讀取區段活動中新增&#x200B;**[!UICONTROL Throttling rate]**&#x200B;參數。 [閱讀全文](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**預覽和測試訊息**

* 身分和命名空間現在會顯示在&#x200B;**[!UICONTROL Preview]**&#x200B;畫面中。 [閱讀全文](preview.md#preview-your-messages)
* 校樣的測試電子郵件數目現在限制為10個。
* 校樣中&#x200B;**主旨行首碼**&#x200B;允許的字元現已受限。 [閱讀全文](preview.md#send-proofs)

**個人化運算式編輯器**

* 已重新命名並重新排序協助程式下拉式清單。

### 修正

* 修正導致為批次電子郵件傳送傳送重複訊息的問題。
* 當重試期間結束後未執行電子郵件傳送時，現在會據此產生事件。
* 修正「PTR記錄」畫面中缺少IP資訊的問題。
* 現已實作運算式編輯器中選件邊欄的本地化。
* 修正資訊快顯視窗中的錯誤間距。
* 修正了上傳HTML檔案時，不支援具有`background-image`屬性的內部樣式表時，電子郵件設計工具中的問題。
