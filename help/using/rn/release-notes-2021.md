---
solution: Journey Optimizer
product: journey optimizer
title: 舊版發行說明（2021年）
description: Journey Optimizer 2021發行說明
exl-id: 0e43be98-f471-4860-be84-8f99ab93e983
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '2077'
ht-degree: 0%

---

# 發行說明2021年 {#release-notes-2021}

本頁面列出 [!DNL Journey Optimizer] 於2021年發行。


## 2021年11月發行 {#november-2021-release}

<table>
<thead>
<tr>
<th><strong>CNAME子網域委派</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer現在支援CNAME。 CNAME或標準名稱記錄是指向其他網域位址而非IP位址的記錄。 CNAME子網域委派可讓您建立子網域，並使用CNAME指向Adobe專屬記錄。 使用此設定，您和Adobe都有責任維護DNS，以便設定傳送、轉譯和追蹤電子郵件的環境。</p>
<p>如果貴組織的原則限制完整的子網域委派方法，則建議使用此方法。</p>
<p>如需CNAME子網域委派的詳細資訊，請參閱 <a href="../configuration/delegate-subdomain.md#cname-subdomain-delegation">詳細檔案</a>.</p>
</td>
</tr>
</tbody>
</table>


## 2021年10月發行 {#oct-2021-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>決策管理 — 選件模擬</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以模擬哪些優惠方案將傳遞至Journey Optimizer UI中指定位置的測試設定檔。 這可讓您在投入生產之前，輕鬆驗證決策邏輯，包括資格限制和排名演算法。 此功能可讓非技術和技術使用者快速測試決策管理，並疑難排解潛在問題。</p>
<p>如需詳細資訊，請參閱 <a href="../offers/offer-activities/simulation.md">詳細檔案</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>決策管理 — 個人化您的優惠方案</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用Adobe Experience Platform設定檔屬性和區段，使用在Journey Optimizer UI中找到的相同運算式編輯器元件，個人化優惠方案的內容。 </p>
<p>如需詳細資訊，請參閱 <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">詳細檔案</a>.</p>
</td>
</tr>
</tbody>
</table>


另請參閱 [Adobe Experience Platform 10月發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html){target=&quot;_blank&quot;}以取得更多變更。

### 改良功能

**歷程**

* **運算式編輯器**  — 身為超級用戶，您現在可以使用函式來處理地圖。 此功能可與訂閱清單搭配運用。 例如，您現在可以從訂閱清單中取得電子郵件地址。 [透過此範例了解更多資訊](../building-journeys/message-to-subscribers-uc.md)

* **監控**  — 已增強即時歷程和測試模式的步驟事件。 [新欄位](../reports/sharing-field-list.md#serviceevents) 已新增與設定檔匯出作業相關的內容。 為了提供更佳的使用者體驗，步驟事件欄位現在會組織成不同類別。 所有先前的步驟事件欄位仍可在 [stepEvents](../reports/sharing-legacy-fields.md) 類別。
* **協助工具**  — 歷程中已實作協助工具增強功能。
* **集合**  — 現在支援包含子物件的物件陣列。 [了解詳情](../building-journeys/collections.md)
* **清單**  — 已改善歷程、事件、動作、資料來源的清單畫面。

**報表**

* **全域檢視中的資料格式**  — 您現在可以在 **全域檢視** 的 **執行** 標籤。


**管理**

* **編輯訊息預設集**  — 您現在可以編輯訊息預設集並監視其更新狀態。 [深入了解](../configuration/channel-surfaces.md#edit-channel-surface)
* **編輯PTR記錄**  — 您現在可以編輯PTR記錄並監視其更新狀態。 [深入了解](../configuration/ptr-records.md#edit-ptr-record)

**個人化**

* **日期格式的新協助程式功能**  — 您現在可以指定日期字串的呈現方式。 [深入了解](../personalization/functions/dates.md#format-date)


**決策管理**

* **評估排序**  — 新的、改進的決策建立流程不僅讓您更順暢地在決策對象之間導航，而且讓您能夠完全控制決策引擎如何評估選件集合。 這包括哪些集合會一起評估，或分別評估，以及應評估集合的順序。 [深入了解](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### 修正

* 修正瀏覽器語言非英文時，無法顯示歷程清單、訊息清單和電子郵件設計工具的問題。
* 修正使用電子郵件設計工具中的運算式新增個人化時發生的語法錯誤：字元被錯誤逸出。
* 修正導覽至 **管理** 功能表。
* 修正使用業務事件測試歷程時觸發其他即時歷程的問題。


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
<p>報表中提供新量度：即時和全域報表中都會顯示電子郵件和推送訊息的已定位和已排除。 </br> 若要存取最新量度，請注意，您必須重設每個管道和報表類型的不同報表控制面板。 如需控制面板自訂的詳細資訊，請參閱 <a href="../reports/live-report.md">詳細檔案。</a></p>
<p>訊息執行清單中的新欄會顯示每個訊息執行的目標設定檔數量。 </p>
<p>如需詳細資訊，請參閱 <a href="../reports/global-report.md">詳細檔案</a>.</p>
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
<p>如需集合的詳細資訊，請參閱 <a href="../building-journeys/collections.md">詳細檔案</a>. </p>
<p>篩選器和交叉函式已添加到高級表達式編輯器中可用的函式清單中。 這提供更多篩選和比較集合的可能性。</p>
<p>請參閱 <a href="../building-journeys/functions/functionfilter.md">篩選</a> 和 <a href="../building-journeys/functions/functionintersect.md">相交</a> 函式。</p>
</td>
</tr>
</tbody>
</table>

### 改良功能

**歷程**

* 布建步驟事件期間建立的系統產生的結構描述和資料集現在為唯讀模式，可避免重要結構的任何意外修改。 [深入了解](../reports/sharing-overview.md)
* 乾淨地標籤 **等待** 活動，其標籤將顯示在畫布中。 標籤也會用於報表和測試模式記錄檔，以清楚識別您正在執行的動作。 [深入了解](../building-journeys/about-journey-activities.md#best-practices)
* 篩選 **事件** 和 **動作** 類別。 不再篩選協調活動。 [深入了解](../building-journeys/using-the-journey-designer.md)
* 在規則型或業務事件中定義事件ID條件時，「包含」運算子現在可用於欄位的字串類型。 [深入了解](../event/about-creating.md)

**電子郵件設定**

* 當IP池與消息預設集關聯時，您現在可以編輯它，更新為非同步。 您也可以檢查每個IP池的更新狀態。 [深入了解](../configuration/ip-pools.md#edit-ip-pool)


## 2021年8月發行 {#august-2021-release}

### 新功能

<table>
<thead>
<tr>

<th><strong>在最佳時機傳送訊息 — 傳送時間最佳化</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>在最佳時機為您與Adobe Journey Optimizer互動的每個客戶自動傳送推播或電子郵件。 「傳送時間最佳化」採用Adobe的AI服務，可根據歷史開啟率和立即可用的點按率，預測傳送電子郵件或推送訊息的最佳時機，以最大化參與。</p>
<p>此功能目前為測試版，僅供測試版客戶使用。 若要加入測試版計畫，請聯絡Adobe客戶服務。</p>
<p>如需詳細資訊，請參閱 <a href="../building-journeys/journeys-message.md#send-time-optimization">詳細檔案</a>.</p>
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
<p>如需詳細資訊，請參閱 <a href="../event/experience-event-schema.md#leverage_schema_relationships">詳細檔案</a>.</p>
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
<p>個人化URL會根據設定檔屬性，將收件者帶往網站的特定頁面或個人化微網站。 在Adobe Journey Optimizer中，您現在可以將個人化新增至訊息內容的URL。 URL個人化可套用至文字和影像，以及使用設定檔資料或內容資料。</p>
<p>如需詳細資訊，請參閱 <a href="../personalization/personalization-syntax.md#perso-urls">詳細檔案</a>.</p>
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
<p>您現在可以根據每個預設集定義重試期間，以確保不再需要重試嘗試時不再執行。 例如，對於包含僅一天有效連結的密碼重設交易式訊息，您可以將重試期間設為24小時。 請注意，重試設定只會套用至電子郵件通道。</p>
<p>如需詳細資訊，請參閱 <a href="../configuration/retries.md#retry-duration">詳細檔案</a>.</p>
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
<p>現在可從使用者介面逐一，透過CSV檔案上傳以大量模式，將電子郵件地址和網域新增至隱藏清單。</p>
<p>如需詳細資訊，請參閱 <a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">詳細檔案</a>.</p>
</td>
</tr>
</tbody>
</table>


### 改良功能

**歷程**

* **動態標題**  — 您現在可以以HTTP標題參數傳遞動態資料。 這些參數可供接收歷程動作HTTP呼叫的整合系統使用，例如時間戳記或追蹤ID。 [深入了解](../action/about-custom-action-configuration.md#url-configuration)
* **動態URL路徑**  — 您現在可以為自訂動作設定動態URL路徑。 [深入了解](../action/about-custom-action-configuration.md#url-configuration)
* 讀取段的總節流率已從每秒17,000條消息更改為每秒20,000條消息。 [深入了解](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**使用者介面**

* **搜尋**  — 現在，您可以在每個頁面上，直接從Unified Experience Cloud搜尋欄位搜尋業務物件和說明文章。 [深入了解](../start/user-interface.md#unified-search)
* **收件者**  — 從Adobe Journey Optimizer首頁顯示的收件者元素現在已擴充至其他商業物件。 透過此更新，您最近存取的捷徑包括訊息、歷程、區段、結構、資料集、資料來源、事件、動作、來源和目的地。 [深入了解](../action/about-custom-action-configuration.md#passing-collection)

**內容設計**

* **背景**  — 現在即時預覽支援背景影像。 [深入了解](../email/preview.md)
* **一鍵式選擇退出連結**  — 您可以在電子郵件內容中插入新類型的連結：the **選擇退出** 連結可讓使用者只要按一下即可取消訂閱，以免收到您的通訊，而無須重新導向至登錄頁面，以確認選擇退出。 [深入了解](../privacy/opt-out.md#one-click-opt-out-link)

**個人化**

* **運算式編輯器**  — 您現在可在定義個人化時輕鬆新增回傳值：當設定檔的個人化欄位空白時，將顯示回傳值。 [深入了解](../personalization/functions/helpers.md)

**電子郵件設定**

* **允許的清單**  — 現在，您可以透過API呼叫，在非生產沙箱上啟用和停用允許清單。 [深入了解](../configuration/allow-list.md#enable-allow-list)
* **導覽**  — 查禁清單，可在 **管理>管道>電子郵件設定>一般** 功能表，已移至新 **隱藏清單** 子功能表，可收集所有相關功能以便更輕鬆存取。 [深入了解](../configuration/manage-suppression-list.md#access-suppression-list)

**決策管理**

* 建立優惠方案時新增和設定表示法的方式已更新，以改善使用者體驗。 尤其是，現在只有當您定義表示的影像類型內容時，才會顯示資產資料庫。 [深入了解](../offers/offer-library/creating-personalized-offers.md#representations)

### 修正

* 修正訊息標籤導覽的協助工具問題。
* 修正電子郵件設計工具標籤的本地化問題。
* 修正在歷程中選取多個節點並按一下屬性窗格上「刪除」時的問題。
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
<p>透過已載入Journey Optimizer中的參考資料豐富您的體驗。 例如，在體驗事件中查詢訂房ID的中繼資料，或在體驗事件中從SKU尋找產品資訊以用於畫布。 </p>
<p>您現在可以運用結構間的關係，將一個資料集用作其他資料集的查閱表格。 接著，在設定單一事件、在歷程中使用條件、在訊息個人化和在自訂動作個人化中時，您就可以運用連結表格中的所有欄位。</p>
<p>如需詳細資訊，請參閱 <a href="../event/experience-event-schema.md#leverage_schema_relationships">詳細檔案</a>.</p>
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
<p>如需詳細資訊，請參閱 <a href="../configuration/allow-list.md">詳細檔案</a>.</p>
</td>
</tr>
</tbody>
</table>

### 改良功能

**歷程**

* 在同一沙箱中同時執行的所有讀取區段的總節流率限制為每秒17,000條訊息。 [了解詳情](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* 此 **快取期間** 欄位已從資料來源設定窗格中移除。 [了解詳情](../datasource/about-data-sources.md)
* 對於外部資料來源，現在會自動定義每秒15次呼叫的上限規則。 [了解詳情](../configuration/external-systems.md#capping)
* 對於即時歷程，歷程屬性畫面現在會顯示發佈日期和發佈歷程的使用者名稱。 [了解詳情](../building-journeys/journey-gs.md#change-properties)
* 在歷程清單畫面中，已新增歷程類型篩選器。 [了解詳情](../start/user-interface.md#filter-lists)
* 此 **[!UICONTROL Throttling rate]** 參數已新增至讀取區段活動中。 [了解詳情](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**預覽和測試**

* 身分和命名空間現在會顯示在 **[!UICONTROL Preview]** 螢幕。 [了解詳情](../email/preview.md#preview-your-messages)
* 校樣的測試電子郵件數目現在限制為10個。
* 允許的字元 **主旨行首碼** 校樣中的內容現在有限。 [了解詳情](../email/preview.md#send-proofs)

**個人化運算式編輯器**

* 已重新命名並重新排序協助程式下拉式清單。

### 修正

* 修正導致為批次電子郵件傳送傳送重複訊息的問題。
* 當重試期間結束後未執行電子郵件傳送時，現在會據此產生事件。
* 修正「PTR記錄」畫面中缺少IP資訊的問題。
* 現已實作運算式編輯器中選件邊欄的本地化。
* 修正資訊快顯視窗中的錯誤間距。
* 修正上傳HTML檔案時，內部樣式表包含 `background-image` 不支援屬性。
