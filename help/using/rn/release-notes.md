---
title: 發行說明
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ca9cb62770c1c50b2683486de48435d5b47b8729
workflow-type: ht
source-wordcount: '2697'
ht-degree: 100%

---

# 發行說明 {#release-notes}

本頁面列出[!DNL Journey Optimizer]所有新功能和改進項目。您還可以參閱[最新文件更新](documentation-updates.md)頁面以了解更多變更。



## 2022 年 2 月發佈內容 {#feb-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>訂閱項目登陸頁面</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在 Journey Optimizer 建立並設計登陸頁面，引導您的使用者存取線上表單，以便他們可以選擇加入或選擇退出接收您的通訊，或訂閱電子報等特定服務。</p>
<p>有關詳細資訊，請參閱<a href="../landing-pages/create-lp.md">詳細文件</a>及相關<a href="../landing-pages/lp-use-cases.md">使用範例</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>全新個人化運算式資料庫</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 現在提供資料庫，您可以在其中存取預先定義的個人化運算式。 這些運算式由管理員使用者設定。</p>
<p>如需詳細資訊，請參閱<a href="../personalization/personalization-library.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>傳遞資訊透過 UTM 追蹤參數追蹤郵件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在 Journey Optimizer 訊息內容中，您現在可以將 UTM 參數加入連結：提供有關該連結的其他資料，幫助您確定某人按下連結的位置及原因。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/message-presets.md#configure-email-settings">詳細文件</a>。</p-->
</td>
</tr>
</tbody>
</table>

### 改進項目

**歷程**

* 為了最佳化效能，所有處於測試模式且一週內未觸發的歷程現在將切換回「草稿」狀態。 [閱讀全文](../building-journeys/testing-the-journey.md#important_notes)
* 已最佳化 Journey Optimizer 和 Adobe Campaign Classic 的整合，以便提高效能。 上限預設設定已變更為 4000 次呼叫 / 5 分鐘。	[閱讀全文](../action/acc-action.md#important-notes)

**報告**

* 現在可以根據狀態篩選傳遞：
   * 您現在可以從「訊息執行」清單排除傳遞清單中的證明。
   * 您可以選擇從即時/全域報告排除測試事件。

* 您現在可以存取有關最佳化傳送時間資料的報告：即時訊息的人數，以及經過 1 小時最佳化、2 小時最佳化等訊息的人數。

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**決策管理**

* 排名和 AI 排名現在分類在單一標籤。

## 2022 年 1 月發行版本 {#january-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>歷程 — 使用個人資料上限條件最佳化 IP 提升</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>當在歷程中設定<strong>條件</strong>活動時，您現在可以定義個人資料上限。 此新條件類型允許您為歷程路徑設定個人資料的最大數量。 當達到此限制後，輸入的個人資料將採用替代路徑。 這樣，您就可以提高傳遞量 (IP 提升)。 例如，您可能希望透過分割執行來加快網域上的傳遞量：在第 1 天傳送 1000 則訊息，在第 2 天傳送 2000 則訊息等。</p>
<p>有關詳細資訊，請參閱<a href="../building-journeys/condition-activity.md#profile_cap">詳細文件</a>及相關<a href="../building-journeys/ramp-up-deliveries-uc.md">使用範例</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程 — 讀取區段改進</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>增量讀取</strong>選項已加入循環<strong>讀取區段</strong>活動。 此選項允許您僅將目標設定在自上次執行歷程以來進入區段的個人。 第一次執行始終將目標設定在所有區段成員。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">詳細文件</a>。
</td>
</tr>
</tbody>
</table>

### 改進項目

**歷程**

* Journey Optimizer 步驟事件現在可以連結到 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hant) 中的其他資料集。  內建「歷程步驟事件」方案中的 **profileID** 欄位現在定義為身分欄位。 [了解更多](../reports/sharing-overview.md#integration-cja)

**Offer Decisioning**

* 對於在已發佈訊息中直接或間接引用的優惠方案、遞補優惠、優惠收藏或優惠決定，現在將在對應訊息中自動反映您的更新，無需重新發佈。 [了解更多](../offers/offers-e2e.md#insert-decision-in-email)

* 在模擬給定測試設定檔將提供哪些服務時，您現在可以修改預設模擬設定，並針對用於疑難排解的模擬查看對應的代碼。 [進一步了解](../offers/offer-activities/simulation.md#define-simulation-settings)

**管理**

* 管理員現在可以使用 CNAME 設定子網域來編輯 PTR 記錄。 [進一步了解](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**個人化**

* **加入收藏夾** — 為了協助在使用個人化功能時提高效率，我們引進了儲存收藏夾的概念。 將不同屬性加入收藏夾功能表可快速存取您使用頻率最高的項目。 [了解更多](../personalization/personalize.md#fav)

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
<p>如需 CNAME 子網域委派的詳細資訊，請參閱 <a href="../configuration/delegate-subdomain.md#cname-subdomain-delegation">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


## 2021 年 10 月發行版本 {#oct-2021-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>決定管理 — 優惠模擬</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以模擬將哪些優惠傳遞至測試設定檔中 Journey Optimizer UI 的指定位置。 這可讓您在投入生產之前，輕鬆驗證決定邏輯，包括資格限制和排名演算法。 此功能可讓非技術和技術使用者快速測試 Offer Decisioning 並針對潛在問題進行疑難排解。</p>
<p>如需詳細資訊，請參閱<a href="../offers/offer-activities/simulation.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>決定管理 — 個人化您的優惠</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用 Adobe Experience Platform 設定檔屬性和區段，利用在 Journey Optimizer UI 中找到的相同運算式編輯器元件，來個人化優惠內容。 </p>
<p>如需詳細資訊，請參閱<a href="../offers/offer-library/creating-personalized-offers.md#custom-text">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


另請參閱 [Adobe Experience Platform 10 月發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html?lang=zh-Hant){target=&quot;_blank&quot;} 以瞭解更多變更。

### 改進項目

**歷程**

* **運算式編輯器**  - 身為超級使用者，您現在可以使用函式來處理地圖。 此功能可與訂閱清單搭配運用。 例如，您現在可以從區段的訂閱清單取得電子郵件地址。 [在本範例進一步了解](../building-journeys/message-to-subscribers-uc.md)

* **監控**  - 已增強即時歷程和測試模式的步驟事件。 [新欄位](../reports/sharing-field-list.md#serviceevents) 已新增與設定檔匯出作業有關的內容。 為了提供更佳的使用者體驗，步驟事件欄位現在會整理成不同類別。 所有先前的步驟事件欄位仍可在 [stepEvents](../reports/sharing-legacy-fields.md) 類別中使用。
* **協助工具**  - 歷程已導入協助工具增強功能。
* **集合**  - 現在支援包含子物件的物件陣列。 [閱讀全文](../building-journeys/collections.md)
* **清單**  - 已改善歷程、事件、動作、資料來源的清單畫面。

**報告**

* **全域檢視中的資料格式**  - 您現在可以在&#x200B;**執行**&#x200B;標籤中的&#x200B;**全域檢視**&#x200B;切換數字與百分比 。 [進一步了解](../messages/message-monitoring.md)


**管理**

* **編輯訊息預設集**  - 您現在可以編輯訊息預設集並監視其更新狀態。 [進一步了解](../configuration/message-presets.md#edit-message-preset)
* **編輯 PTR 記錄**  - 您現在可以編輯 PTR 記錄並監視其更新狀態。 [進一步了解](../configuration/ptr-records.md#edit-ptr-record)

**個人化**

* **新的日期格式協助工具功能**  - 您現在可以指定日期字串的呈現方式。 [進一步了解](../personalization/functions/dates.md#format-date)


**決定管理**

* **評估排序**  - 全新改進的決定建立流程不僅可讓您更順暢瀏覽於決定物件之間，而且讓您能夠完全控制決定引擎如何評估優惠集合。 其中包括哪些集合會一起進行評估或分別評估，以及應以何種順序評估集合。 [進一步了解](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

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

<th><strong>報告－以更好的方式深入解析目標閱聽眾</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>在報告中提供新指標：即時和全域報告都會顯示已鎖定和已排除對象的電子郵件和推送訊息。 </br> 若要存取最新指標，請注意，您必須為每個頻道和報告類型重新設定不同的報告儀表板。 如需儀表板客製化的詳細資訊，請參閱<a href="../reports/live-report.md">詳細文件。</a></p>
<p>訊息執行清單中包含新欄顯示每個訊息執行的目標設定檔數量。 </p>
<p>如需詳細資訊，請參閱<a href="../messages/message-monitoring.md">詳細文件</a>。</p>
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
<p>請參閱<a href="../building-journeys/functions/functionfilter.md">篩選</a>和<a href="../building-journeys/functions/functionintersect.md">交集</a>函式。</p>
</td>
</tr>
</tbody>
</table>

### 改進項目

**歷程**

* 在佈建步驟事件期間建立並由系統產生的方案和資料集現在改為唯讀模式，可避免重要方案發生任何意外修改。 [進一步了解](../reports/sharing-overview.md)
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
<p>使用 Adobe Journey Optimizer 在最適當的時間自動向您接洽的每個客戶傳送推播通知或電子郵件。「傳送時間最佳化」採用 Adobe 的 AI 服務，可根據立即可用的歷史開啟率和點按率，預測傳送電子郵件或推送訊息的最佳時機，最大化參與程度。</p>
<p>此功能目前為測試版本，僅供測試版客戶使用。 若要加入測試版計畫，請連絡 Adobe 客戶服務。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journeys-message.md#send-time-optimization">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>在商業活動中利用方案關係 — 查閱表格管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在當您設定商業活動時，可以利用方案之間的關係。除了可在當設定單一事件時、當在歷程中、在個人化訊息和在個人化自訂動作中使用條件時運用連結表格的欄位，同時還包含此功能。</p>
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
<p>個人化 URL 會根據設定檔屬性，將收件者帶往網站特定頁面或個人化微網站。 您現在可以在 Adobe Journey Optimizer 的訊息內容加入個人化 URL。 URL 個人化可套用至文字和影像，同時使用個人資料或內容資料。</p>
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
<th><strong>定義要排除的傳送地址 — 隱藏清單</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在可從使用者介面在隱藏清單新增電子郵件地址和網域，可逐一新增或透過 CSV 檔案上傳大量新增。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


### 改進項目

**歷程**

* **動態標頭** - 您現在可以在 HTTP 標頭參數中傳遞動態資料。 接收歷程動作 HTTP 呼叫的整合系統可使用這些參數 (例如時間戳記或追蹤 ID)。 [進一步了解](../action/about-custom-action-configuration.md#url-configuration)
* **Dynamic URL 路徑** - 您現在可以為自訂動作設定動態 URL 路徑。 [進一步了解](../action/about-custom-action-configuration.md#url-configuration)
* 讀取區段的總節流率已從每秒 17,000 則訊息變更為每秒 20,000 則訊息。 [進一步了解](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**使用者介面**

* **搜尋**  - 在每個頁面上，您現在可以直接從「統一的 Experience Cloud」搜尋欄位搜尋業務物件和說明文章。 [進一步了解](../start/user-interface.md#unified-search)
* **收件者**  - 在 Adobe Journey Optimizer 首頁顯示收件者元素的功能，現在已擴充至其他業務物件。 透過此更新，快速鍵包括您最近存取的訊息、歷程、區段、方案、資料集、資料來源、事件、動作、來源和目的地。 [進一步了解](../action/about-custom-action-configuration.md#passing-collection)

**內容設計**

* **背景**  - 即時預覽現在支援背景影像。 [進一步了解](../messages/preview.md)
* **一鍵選擇退出的連結**  - 您可以在電子郵件內容中插入新類型的連結：**選擇退出**&#x200B;連結可讓使用者只要按一下即可取消訂閱接收您的通訊，無須重新導向至登陸頁面以確認選擇退出。 [進一步了解](../messages/consent.md#one-click-opt-out-link)

**個人化**

* **運算式編輯器**  - 您現在可在定義個人化時輕鬆新增回傳值：當個人資料的個人化欄位空白時，將顯示回傳值。 [進一步了解](../personalization/functions/helpers.md)

**電子郵件設定**

* **允許清單**  - 您現在可以透過 API 呼叫，在非生產沙箱上啟用和停用允許清單。 [進一步了解](../messages/allow-list.md#enable-allow-list)
* **導覽**  - 可在 **管理 > 管道 > 電子郵件設定 > 一般** 功能表中存取的隱藏清單，已移至新的 **隱藏清單** 子功能表，收集所有相關功能以便更輕鬆存取。 [進一步了解](../configuration/manage-suppression-list.md#access-suppression-list)

**決定管理**

* 建立優惠方案時新增和設定代表的方式已更新，以改善使用者體驗。 特別是，現在只有當您定義代表的影像類型內容時，才會顯示資料庫。[進一步了解](../offers/offer-library/creating-personalized-offers.md#representations)

### 修正

* 修正訊息標籤導覽的協助工具問題。
* 修正電子郵件設計工具標籤的本地化問題。
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
<p>您現在可以運用方案間的關係，將一個資料集作為其他資料集的查閱表格。 接著，當設定單一事件時、當在歷程中、在個人化訊息和在個人化自訂動作中使用條件時，您就可以運用連結表格中的所有欄位。</p>
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
<p>如需詳細資訊，請參閱<a href="../messages/allow-list.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改進項目

**歷程**

* 對於在同一沙箱同時執行的所有讀取區段，其總節流率限制為每秒 17,000 則訊息。 [閱讀全文](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* **快取期間** 欄位已從資料來源設定窗格中移除。 [閱讀全文](../datasource/about-data-sources.md)
* 對於外部資料來源，現在會自動定義每秒 15 次呼叫的上限規則。 [閱讀全文](../configuration/external-systems.md#capping)
* 對於即時歷程，歷程屬性畫面現在會顯示發佈日期和發佈歷程的使用者名稱。 [閱讀全文](../building-journeys/journey-gs.md#change-properties)
* 在歷程清單畫面中，已新增歷程類型篩選器。 [閱讀全文](../start/user-interface.md#filter-lists)
* **[!UICONTROL Throttling rate]** 參數已新增至讀取區段活動中。 [閱讀全文](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**預覽和測試訊息**

* 身分和命名空間現在會顯示在 **[!UICONTROL Preview]** 畫面中。 [閱讀全文](../messages/preview.md#preview-your-messages)
* 校樣的測試電子郵件數目現在限制為 10 則。
* 已在校樣中限制&#x200B;**主旨行首碼** 允許的字元。 [閱讀全文](../messages/preview.md#send-proofs)

**個人化運算式編輯器**

* 已重新命名並重新排序協助工具下拉式清單。

### 修正

* 修正導致批次電子郵件傳遞重複傳送訊息的問題。
* 當重試期間結束後未執行電子郵件傳送時，現在會據此產生事件。
* 修正「PTR 記錄」畫面中缺少 IP 資訊的問題。
* 現在運算式編輯器中已導入本地化的優惠邊欄。
* 修正資訊快顯視窗的間距錯誤。
* 修正當電子郵件設計工具中上傳 HTML 檔案時，內部樣式表包含未支援的 `background-image` 屬性問題。
