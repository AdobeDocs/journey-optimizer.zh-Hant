---
title: 發行說明
description: Journey Optimizer 發行說明
source-git-commit: 77d392cc09bd0923faf3d27e951a17cd702d257c
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 11%

---


# 發行說明 {#release-notes}

本頁面列出[!DNL Journey Optimizer]的所有新功能和改善項目。您也可以參閱最新的[文件更新](documentation-updates.md)。


## 2021 年 8 月發行 {#august-2021-release}

### 新功能

<table>
<thead>
<tr>

<th><strong>在最佳時機傳送訊息 — 傳送時間最佳化</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>在最佳時機為您與Adobe Journey Optimizer互動的每個客戶自動傳送您的推播或電子郵件。 「傳送時間最佳化」採用Adobe的AI服務，可根據歷史開啟率和立即可用的點按率，預測傳送電子郵件或推送訊息的最佳時機，以最大化參與。</p>
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
<!--
<table>
<thead>
<tr>
<th><strong>Personalized URLs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalized URLs take recipients to specific pages of a website, or to a personalized microsite, depending on the profile attributes. In Adobe Journey Optimizer, you can now add personalization to URLs in your message content. URL personalization can be applied to text and images, and use profile data or contextual data.</p>
<p>For more information, refer to the <a href="documentation-updates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>請確定您的電子郵件已送達您的使用者 — 電子郵件重試</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以根據每個預設集定義重試期間，以確保不再需要重試嘗試時不再執行。 例如，對於包含僅一天有效連結的密碼重設交易式訊息，您可以將重試期間設為24小時。 請注意，重試設定只會套用至電子郵件通道。</p>
<p>如需詳細資訊，請參閱<a href="configuration/retries.md">詳細文件</a>。</p>
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

* **動態標題**  — 您現在可以以HTTP標題參數傳遞動態資料。這些參數可供接收歷程動作HTTP呼叫的整合系統使用，例如時間戳記或追蹤ID。 [了解更多](action/about-custom-action-configuration.md#url-configuration)
* **動態URL路徑**  — 您現在可以為自訂動作設定動態URL路徑。[了解更多](action/about-custom-action-configuration.md#url-configuration)
* 讀取段的總節流率已從每秒17,000條消息更改為每秒20,000條消息。 [閱讀全文](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**使用者介面**

* **搜尋**  — 現在，您可以在每個頁面上，直接從「統一Experience Cloud」搜尋欄位搜尋業務物件和說明文章。[了解更多](user-interface.md#unified-search)
* **收件**  — 從Adobe Journey Optimizer首頁顯示的收件元素現在已擴充至其他業務物件。透過此更新，您最近存取的捷徑包括訊息、歷程、區段、結構、資料集、資料來源、事件、動作、來源和目的地。 [了解更多](action/about-custom-action-configuration.md#passing-collection)

**內容設計**

* **背景**  — 現在即時預覽支援背景影像。[了解更多](preview.md)
* **一鍵式選擇退出連結**  — 您可以在電子郵件內容中插入新類型的連結：「選 **擇退** 出」連結可讓使用者只要按一下，就能取消訂閱收到您的通訊內容，而不需重新導向至登陸頁面以確認選擇退出。[了解更多](message-tracking.md#one-click-opt-out-link)

**個人化**

<!--* **Expression Editor** - You can now easily add a fall-back value when defining personalization: when personalization field is empty for a profile, the fall-back value will display. [Learn more](documentation-updates.md)-->

**電子郵件設定**

* **允許清單**  — 現在可以透過API呼叫，在非生產沙箱上啟用和停用允許清單。[了解更多](allow-list.md#enable-allow-list)

<!--* **Suppression list** - Adding email addresses and domains into the suppression list is now available from the user interface, either one by one, either in bulk mode through a CSV file upload. [Learn more](configuration/manage-suppression-list.md#add-addresses-and-domains)-->
<!--* **Navigation** - The suppression list, which was accessible under the **Channels > Email configuration > General** menu, has been moved to the **Channels > Email configuration > Suppression list** menu for easier access. [Learn more](configuration/manage-suppression-list.md#access-suppression-list)-->


### 修正

* 修正訊息標籤導覽的協助工具問題。
* 修正電子郵件設計工具標籤的本地化問題。
* 修正在歷程中選取多個節點並按一下屬性面板上「刪除」時的問題。
* 修正無法將新標題新增至歷程中使用之動作的問題。
* 您現在可以透過使用者介面中更明確的警告，找出訊息預設集建立失敗的原因。


## 2021年7月發行 {#july-2021-release}

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

