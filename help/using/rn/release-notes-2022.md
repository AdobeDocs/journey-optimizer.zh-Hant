---
title: 2022 年發行說明
description: Journey Optimizer 2022 年發行說明
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# 2022 年發行說明 {#release-notes-2022}

此頁面列出了於 2022 年發行的所有 [!DNL Journey Optimizer] 功能和改善。


## 2022 年 7 月發行版本 {#july-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>全新內嵌訊息流程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 為歷程的訊息編寫提供全新流程。 線上傳送訊息消息將為使用者節省大量時間，並簡化在 Journey Optimizer 建立和傳遞電子郵件、推播通知或簡訊的工作流程。 透過將訊息作為單獨的步驟刪除，作為 Journey Canvas 動作的一部分都可內嵌編輯，使用者需要按更少的按鈕並導覽較少的畫面來設計和編輯其內容。</p>
<img src="assets/do-not-localize/inline.gif"/>
<p>如需詳細資訊，請參閱<a href="../messages/get-started-content.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>以屬性為基礎的存取控制 (可用性限制)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，您可以使用定義組織或資料使用範圍的標籤標示身分綱要欄位。 管理員可以使用權限介面定義涵蓋 XDM 綱要欄位的存取原則，並更好地管理使用者或使用者群組 (內部、外部或協力廠商使用者) 的存取權限，以及管理對特定類型資料 (即敏感個人資料/SPD) 的存取權限。</p>
<p>以屬性為基礎的存取控制目前僅限於選定使用者，將在未來的版本中同步到所有環境。</p>
<p>如需詳細資訊，請參閱<a href="../administration/attribute-based-access.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>批次決策作業</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，您可以從使用者介面執行批次決策作業，這樣我就不需要開發人員來執行批次 API 作業，而且我可以減少行銷所需的時間。 此新介面允許您建立作業及管理目前/過去的作業。</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>如需詳細資訊，請參閱<a href="../offers/batch-delivery.md">詳細文件。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在您的決定中自動執行最佳優惠方案 (可用性限制)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，您可以在決策管理中使用個人化最佳化模型系統。 這種新種類模型允許您根據區段及優惠方案市場對優惠進行最佳化及個人化。</p>
<p>個人化最佳化 AI 模型的使用目前僅限於選定使用者，將在未來的版本中同步到所有環境。</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>如需詳細資訊，請參閱<a href="../offers/ranking/personalized-optimization-model.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改進項目

**歷程**

* **結束歷程** — 在歷程畫布中， **結束**&#x200B;活動已從調色盤中刪除。 現在，每個路徑的末端預設新增結束標籤而且無法移除。 這種改善能夠更好地報告客戶從歷程退出的位置，不需要由歷程業者採取任何動作。 請參閱 [文件](../building-journeys/journey-end.md) 及 [功能影片](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}。


* 此 **個人資料時區** 「歷程屬性」中的選項現在預設為未勾選。 [了解更多](../building-journeys/timezone-management.md#timezone-from-profiles)

**訊息**

* 訊息預設集現在是 **頻道介面**。 [進一步了解](../configuration/channel-surfaces.md)

**管理**

* **PTR 記錄版本** - 現在當更新 PTR 記錄時，處理時間最多只需 3 小時。 [了解更多](../configuration/ptr-records.md#processing)

* **允許清單 UI** — 您現在可以使用 Journey Optimizer 使用者介面將新電子郵件地址或網域新增到允許清單。 [了解更多](../configuration/allow-list.md)

* **允許清單邏輯更新** - 現在，即使清單為空，允許清單邏輯在功能啟用後立即適用。 [了解更多](../configuration/allow-list.md#logic)

* **URL 追蹤參數** - 現在，您可以使用運算式編輯器在電子郵件介面中設定 URL 追蹤參數 (即預設集)。 [了解更多](../configuration/email-settings.md#url-tracking)

**決策管理**

* **對象規模** - 當建立決定規則、選擇區段或規則以設定優惠方案適用性或將區段或規則新增到決定範圍時，新的對象規模預估元件現在顯示在使用者介面中。


## 2022 年 6 月發行版本 {#june-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>傳送簡訊給使用者（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以透過與 <b>Sinch</b> 或 <b>Twilio</b> 的整合在 Journey Optimizer 裡建立、個人化和傳送簡訊。</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>簡訊管道目前僅可用於一組組織（可用性限制）。 如需詳細資訊，請聯絡您的 Adobe 代表。</p>
<p>在<a href="../messages/create-sms.md">詳細文件</a>中了解如何建立和傳送簡訊。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>透過與 Adobe Stock 整合，更快找到影響力更大的圖片</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Stock 和 Adobe Journey Optimizer 電子郵件設計工具整合外掛程式，為客戶提供了用於訊息製作的導覽、授權和儲存影像的簡單方法。 您還可以藉由</br>新的<b>找到類似的相片庫</b>選項找出與影像內容、顏色和組成相符的影像庫。 </p>
<!--img src="assets/do-not-localize/stock-rn.gif"/-->
<p>如需詳細資訊，請參閱<a href="../design/stock.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在所有電子郵件上使用密件副本電子郵件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用密件副本電子郵件（密件副本）功能來儲存 Adobe Journey Optimizer 傳送的電子郵件。 在電子郵件預設集中啟用此選項，以便將每封傳送的電子郵件以密件副本方式寄至密件副本地址。</p>
<!--img src="assets/do-not-localize/bcc-rn.gif"/-->
<p>如需詳細資訊，請參閱<a href="../configuration/bcc-email.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>在沙箱之間複製物件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，您可以從 Journey Optimizer 沙箱將體驗重新建立到另一個沙箱，例如從非生產沙箱重新建立到生產沙箱。 這個新功能可將整個 Journey 從一個環境複製到另一個環境，包括 Journey 賴以正確運作的任何物件。 除了 Journeys 之外，您還可以複製其他元件，如 Offirs、Messages、Schemas、Datasets、Data Sources、Events 和 Actions。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/copy-to-sandbox.md">詳細文件</a>。
</td>
</tr>
</tbody>
</table>




### 改進項目

**決策管理**

* **HTML 和 JSON 檔案支援** — 您現在可以將外部 HTML 和 JSON 檔案從 Adobe Experience Cloud 資產庫拖放到優惠方案聲明內容中。 [了解更多](../offers/offer-library/add-representations.md#html-json)


**電子郵件**

* **另存為範本** — 您現在可以將電子郵件內容另存為範本，並在建立其他郵件時重複使用它。 [進一步了解](../design/email-templates.md)


**管理**

* **預覽追蹤 URL 參數** — 設定訊息預設集時，如果定義 URL 追蹤參數，則將顯示結果追蹤 URL 的動態預覽。 [了解更多](../configuration/email-settings.md#url-tracking)

* **訊息預設集版本** — 現在，當更新訊息預設集時，處理時間最多只需 3 小時。 [了解更多](../configuration/channel-surfaces.md#edit-channel-surface)

* **IP 池版本** — 現在，當更新 IP 池時，處理時間最多只需 3 小時。 [了解更多](../configuration/ip-pools.md#edit-ip-pool)




## 2022 年 5 月發行 {#may-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>訊息頻率規則</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以設定跨頻道的業務規則，這些業務規則將自動從訊息和動作中排除過度請求的設定檔。</p>
<!--img src="assets/do-not-localize/frequency-rn.gif"/-->
<p>如需詳細資訊，請參閱<a href="../configuration/frequency-rules.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>決定管理 - AI 排名自動最佳化模型</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，您可以在決定管理中使用經過訓練的模型系統。 此新功能排名可於指定的設定檔顯示。</p>
<!--img src="assets/do-not-localize/optimization.gif"/-->
<p>如需詳細資訊，請參閱<a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer 稽核記錄</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以監視使用者對 Adobe Journey Optimizer 資源執行的動作。</p>
<!--img src="assets/do-not-localize/audit-rn.gif"/-->
<p>如需詳細資訊，請參閱<a href="../privacy/audit-logs.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改進項目

**個人化**

* **用於字元隱藏的新輔助函式**—`mask`輔助函式允許您將字串的一部分替換為「X」字元。 [了解更多](../personalization/functions/string.md#mask)

**登陸頁面**

* **沒有表單的登陸頁面** - 您現在可以建立並發佈不包含表單且不需要訪客操作的登陸頁面。
* **登陸頁面範本** - 您現在可以將登陸頁面儲存為範本，並在建立其他登陸頁面時重複使用它。 [了解更多](../landing-pages/lp-templates.md)
* **返回主要頁面** - 您現在可以從同一登陸頁面內的任何子頁面新增到主要頁面的連結。
* **自訂 JavaScript 支援** - 您現在可以新增自訂 JavaScript 到登陸頁面的內容中，以執行進階樣式或新增自訂行為到登陸頁面。	[了解更多](../landing-pages/lp-custom-js.md)

**歷程**

* **讀取區段** - 一次性讀取區段歷程現在在歷程執行 30 天後移至「已完成」狀態。 對於已排程的讀取區段，是在上次執行該事件後的 30 天。 [了解更多](../building-journeys/read-segment.md)
* **運算式編輯器** - 已新增[限制](../building-journeys/functions/functionlimit.md)函式，以允許您限制清單項目的數目。 [排序](../building-journeys/functions/functionsort.md)函式現在允許您對清單物件進行排序。 對清單物件的支援也已新增到 [distinct](../building-journeys/functions/functiondistinct.md) 和 [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) 的函式。

**管理**

* **授權使用儀表板更新** - [!DNL Adobe Journey Optimizer]使用者介面中現在提供了授權使用儀表板，反映了&#x200B;**授權**&#x200B;平均設定檔豐富度的精確值。 您將看到此量度表示法中的一個數值下降，表示現在已正確報告授權限制。 [了解更多](../segment/license-usage.md)


## 2022 年 4 月發行版本 {#april-2022-release}

### 改進項目

**登陸頁面**

* **核取方塊的新選項「選擇加入/選擇退出」** - 現在，您可以在訂閱項目登錄頁面中插入選擇加入/選擇退出的核取方塊。 使用者需要勾選方塊同意 (選擇加入)，並取消勾選方塊移除其同意 (選擇退出)。 [了解更多](../landing-pages/design-lp.md#define-lp-specific-content)

* **預先填寫登陸頁面欄位** - 現在，使用者可以使用個人資料預先填寫登陸頁面欄位。 [進一步了解](../landing-pages/create-lp.md#configure-primary-page)

**決定管理**

* **邊緣決策 API** - 邊緣決策 API 可以提供並轉譯受決策管理管理的個人化服務。 您可以使用決策管理使用者介面 (UI) 或 API 建立您的優惠方案與其他相關物件。 [進一步了解](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**管理**

* **PTR 提交期間** - PTR 編輯的生效期間現在為幾個小時。 [了解更多](../configuration/ptr-records.md#processing)

**電子郵件設計**

* 提供 **20 個新電子郵件範本**，可在 Journey Optimizer 設計您的電子郵件內容。

**使用者介面**

* **Journey Optimizer UI 內容說明** - 內容說明連結已新增到 Journey Optimizer 的多個頁面。 可用時，請按一下「i」圖示可針對目前功能及存取權限的相關文章查看快速說明。

**整合 Adobe Campaign Standard**

作為 Adobe Campaign Standard 的客戶，您現在可以使用 Journey Optimizer 傳送電子郵件、推播通知和 SMS。 使用新的內建動作在 Journey Optimizer 善用 Campaign Standard 異動訊息傳送功能。  [了解更多](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## 2022 年 3 月發行 {#march-2022-release}

### 改進項目

**歷程**

* 為避免統一設定檔綱要存在不必要的欄位，預設情況下不再為設定檔啟用「歷程步驟事件」綱要。 如有需要，可以啟用。 [了解更多](../reports/sharing-overview.md)
* 跟匯出工作有關的新步驟活動現在由 Journey Optimizer 傳送到 Adobe Experience Platform。 已在文件中新增查詢範例。 [進一步了解](../reports/query-examples.md)

**決定管理**

* 現在您可以指定在所有使用者或單個特定設定檔中套用優惠上限設定，以及指定在個別或所有投放位置上套用。[了解更多](../offers/offer-library/add-constraints.md#capping)
* 批次決策 API 允許組織在一次呼叫中對給定區段中的所有設定檔使用決策管理功能。 區段中每個設定檔提供的內容都放在 AEP 資料集，可用於自訂批次處理工作流程。 [進一步了解](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**管理**

* 您現在可以在訊息預設層及在/從電子郵件標題啟用/停用取消訂閱連結，並在訊息層級設定自訂取消訂閱 URL。 [了解更多](../configuration/channel-surfaces.md#list-unsubscribe)
* 現在，可以透過生產或非生產沙箱的 [!DNL Journey Optimizer] 介面啟用或停用允許清單。 [進一步了解](../configuration/allow-list.md#enable-allow-list)

**個人化**

* 您現在可以在程式庫中儲存 40 多組個人化運算式。 [了解更多](../personalization/personalization-library.md)

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
<p>如需詳細資訊，請參閱<a href="../configuration/channel-surfaces.md#configure-email-settings">詳細文件</a>。</p-->
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

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

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

**決策管理**

* 對於在已發佈訊息中直接或間接引用的優惠方案、遞補優惠、優惠收藏或優惠決定，現在將在對應訊息中自動反映您的更新，無需重新發佈。 [了解更多](../offers/offers-e2e.md#insert-decision-in-email)

* 在模擬給定測試設定檔將提供哪些服務時，您現在可以修改預設模擬設定，並針對用於疑難排解的模擬查看對應的代碼。 [進一步了解](../offers/offer-activities/simulation.md#define-simulation-settings)

**管理**

* 管理員現在可以使用 CNAME 設定子網域來編輯 PTR 記錄。 [進一步了解](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**個人化**

* **加入收藏夾** — 為了協助在使用個人化功能時提高效率，我們引進了儲存收藏夾的概念。 將不同屬性加入收藏夾功能表可快速存取您使用頻率最高的項目。 [了解更多](../personalization/personalize.md#fav)
