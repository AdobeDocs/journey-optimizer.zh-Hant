---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: c2ce36d65df939f2445f783eea7376b0765bdcd7
workflow-type: tm+mt
source-wordcount: '1858'
ht-degree: 82%

---

# 發行說明 {#release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。

先前的發行說明可在[本頁](release-notes-2022.md)取得。您還可以參閱[最新文件更新](documentation-updates.md)頁面以了解更多變更。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

![電子報](../assets/do-not-localize/nl-icon.png)立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，把每季最新產品更新、精彩故事、使用案例、提示等內容直接傳送到您的收件匣。


## 2023年4月發行說明 {#apr-rn-2023}

<!--Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Release date**: April 27, 2023-->

### 新功能{#apr-2023-features}

<table>
<thead>
<tr>
<th><strong>Web通道（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer正透過新增對網頁頻道的支援，來擴充其跨頻道功能。 您現在可以透過智慧且直覺的視覺介面，以其他任何管道形式製作、變更和預覽網路體驗，以個人化您的使用者體驗。 請注意，目前您只能在Journey Optimizer中建立促銷活動中的網頁體驗。</p>
<img src="assets/do-not-localize/web-authoring.gif"/>
<p>如需詳細資訊，請參閱<a href="../web/get-started-web.md">詳細文件</a>。</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>行動上線快速入門工作流程（測試版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>全新行動入門快速入門工作流程現已推出。 使用此新產品功能來快速設定Mobile SDK，以開始收集和驗證行動事件資料，並透過Adobe Journey Optimizer傳送行動推播通知。 這項功能可透過資料收集首頁公開測試版存取。</p>
<img src="../push/assets/mobile-wf-home.png"/>
<p>如需詳細資訊，請參閱<a href="../push/mobile-onboarding-wf.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>New Journey dashboard (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> The Journey dashboard is now split in two tabs:</p>
<ul><li>Use the <strong>Overview</strong> tab to access a new dashboard which displays key metrics related to your journeys.</li>
<li>Use the <strong>Browse</strong> tab to access the list of all journeys.</li></ul>
<p>This capability is accessible in all journeys as a public beta.</p>
<img src="assets/do-not-localize/journey-dashboard.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Personalized Optimization AI ranking model (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalized Optimization AI ranking models are now generally available in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

### 改進項目 {#april-2023-improvements}

**歷程**

* 歷程畫布現在會在訊息活動和結束標籤上顯示活動ID。 這可改進報表和重新定位。
* 設定窗格的版面配置已得到改善，該面板會顯示在動作、資料來源、事件和歷程中。
* 歷程已新增護欄：
   * 歷程中的活動數目現在上限為50個。 [閱讀全文](../start/guardrails.md#journeys-guardrails-journeys)
   * 數量 **即時歷程** 現在，一個組織的每個沙箱最多只能有100個。 測試模式中的歷程不會納入考量。 [閱讀全文](../start/guardrails.md#journeys-guardrails-journeys)

* 新增 [電子郵件](../email/create-email.md), [簡訊](../sms/create-sms.md) 或 [推播](../push/create-push.md) 在歷程中執行動作時，現在依預設會在目前歷程中使用該管道的最後一個使用曲面預先填入曲面。
* 您現在可以在自訂動作中定義靜態或動態查詢參數。 [了解更多](../action/about-custom-action-configuration.md#url-configuration)

**報告**

* 您現在可以匯出Journey Optimizer報表為PDF。

**內容設計工具**

* Adobe Journey Optimizer內容設計工具已更新，現在更輕鬆存取設計樣式和元件。 此新版本建議改善使用者體驗，並隨附效能提升、深色模式部分相容性，以及新的協助工具標準支援。



## 2023年3月發行說明 {#mar-2023}

### 新功能{#mar-2023-features}

<table>
<thead>
<tr>
<th><strong>應用程式內通道 (一般可用性)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在行銷活動中將個人化的應用程式內訊息傳送給您的應用程式使用者。使用 Journey Optimizer 來設計通知並自訂訊息版面、顯示、文字及按鈕，以建立順暢的體驗。</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>如需詳細資訊，請參閱<a href="../in-app/get-started-in-app.md">詳細文件</a>。</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>SMS 點擊追蹤</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過 SMS 點擊追蹤，您可以監控縮短 URL 的效果、識別誰點擊了 URL，並利用此資料透過後續行銷活動重新鎖定這些客戶。</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>如需詳細資訊，請參閱<a href="../sms/create-sms.md#sms-content">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在您的歷程使用標籤 (測試版)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>身為 Journey Optimizer 從業人員，您現在可以使用標籤來組織業務物件。標籤是一種快速、簡便的物件分類方法，用於改進搜尋。此功能目前處於測試階段，僅適用於歷程。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/tags.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>



### 改進項目 {#mar-2023-improvements}

**歷程**

* 新&#x200B;**限制 API** 可讓您設定每秒傳送事件數的上限，防止外部系統或 API 出現流量尖峰。當達到設定限制時，所有後續 API 呼叫會以接收順序排入佇列並盡快處理。請注意，此功能僅支援跨所有沙箱進行一種限制設定。[了解更多](../configuration/external-systems.md)
* 已增強歷程畫布，提供更簡單且改善的使用者體驗。 在畫布的每個路徑結尾處，已移除空白預留位置。 您現在只需將活動拖曳到路徑結尾即可新增活動。
* 在歷程畫布，**結束**&#x200B;標籤的標籤不再自動設定為先前活動的名稱。使用者可視需要手動新增自訂標籤。
* 歷程屬性中的預設逾時和錯誤持續時間已從 5 秒變更為 30 秒。[了解更多](../configuration/external-systems.md#timeout)
* 讀取區段活動的預設限制速率已從每秒 20,000 則訊息變更為每秒 5,000 則訊息。[了解更多](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* 已將護欄新增至測試模式，僅監聽透過介面傳送的事件。 不會考慮透過外部工具傳送的事件。 [進一步了解](../building-journeys/testing-the-journey.md)


<!-- 
* When adding an Email, SMS or Push action in a journey, the surface is now pre-filled, by default, with the last used surface for that channel.
* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)
* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**決定管理**

* 為避免與 Adobe Experience Platform 最近發佈的標籤功能產生混淆，「決策管理」標籤已重新命名為「集合限定詞」。 

   請注意，雖然「標籤」一詞不再用於決策管理使用者介面，但仍用於 API 及資料集等後端服務。

* 您現在可以每天、每週或每月重設優惠方案限定計數器。[了解更多](../offers/offer-library/add-constraints.md#capping)

* 您也可以選擇應查看哪個 Adobe Experience Platform 事件以設定 Offer Decisioning 上限。[了解更多](../offers/offer-library/add-constraints.md#capping)

* 已在版位建立畫面中新增其他參數。它們可讓您控制某個活動內容是否可在多個版位之間複製，以及指定是否應將該活動內容的內容與中繼資料包含在 API 回應中。 [了解更多](../offers/offer-library/creating-placements.md)

**個人化**

* 您現在可以在運算式編輯器中包含字串式設定檔屬性的預設遞補文字。如果選取的屬性未傳回任何結果，則會顯示這些值。[了解更多](../personalization/personalization-build-expressions.md#add)

**報告**

* 報告介面控件功能已得到改善，可自訂使用者檢視其資料的方式。透過這項改善，使用者現在可以在多個視覺效果選項之間進行選擇，包括圖表、表格和環圈圖。 

   若要存取最新的介面工具集，請注意您必須重設不同的報告儀表板。 如需儀表板客製化的詳細資訊，請參閱[詳細文件](../reports/global-report.md#modify-dashboard)。

## 2023年2月發行說明 {#feb-2023}

### 新功能{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>應用程式內頻道 (測試版)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在行銷活動中將個人化的應用程式內訊息傳送給您的應用程式使用者。使用 Journey Optimizer 來設計通知並自訂訊息版面、顯示、文字及按鈕，以建立順暢的體驗。</p>
<p><strong>注意</strong> - 此功能目前為測試版，僅供測試版客戶使用。 若要加入測試版計畫，請連絡 Adobe 客戶服務。</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>如需詳細資訊，請參閱<a href="../in-app/get-started-in-app.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>將 Journey Optimizer 資料集匯出至雲端儲存空間目的地 (測試版)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以與雲端儲存空間位置建立即時連線，以匯出資料集的內容。 可用目的地包括：Amazon S3 雲端儲存空間、 Azure Blob、Azure Data Lake Gen 2、資料登陸區、Google 雲端儲存空間、SFTP。</p>
<p><strong>注意</strong> - 此功能目前為測試版，所有 Adobe Journey Optimizer 使用者都能使用。 如果您尚未擁有存取權，請與 Adobe 代表合作，取得目的地的存取權。</p>
<img src="assets/do-not-localize/gif-destinations.gif"/>
<p>如需詳細資訊，請參閱<a href="../data/export-datasets.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the <strong>Objective</strong> tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objective]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted as needed.
+++




<table>
<thead>
<tr>
<th><strong>Use Tags in your Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. Tags are currently only available for Journeys.</p>
</td>
</tr>
</tbody>
</table>

-->

### 改進項目 {#feb-2023-improvements}

**歷程**

* 此&#x200B;**重新進入等待期**&#x200B;欄位已新增至歷程屬性。 此欄位可讓您定義在允許設定檔在單一歷程中再次進入歷程 (從事件或區段資格開始) 之前等待的時間。這可防止同一事件多次錯誤觸發歷程。預設情況下，欄位會設為 5 分鐘。 [了解更多](../building-journeys/journey-gs.md#entrance)

* 改進了&#x200B;**歷程開始與結束日期**。如果您尚未指定開始日期，則現在會在發佈時自動新增開始日期。針對&#x200B;**讀取區段**&#x200B;歷程，您現在可以新增結束日期。 這可讓設定檔在達到日期時自動退出。 [進一步了解](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**管理**

* **允許清單** - 您現在可以將允許清單下載為 .csv 檔案。 [了解更多](../configuration/allow-list.md#download-allowed-list)

* **電子郵件介面** - 電子郵件介面設定已新增額外檢查：如果&#x200B;**回覆 (電子郵件) 地址**&#x200B;或 **密件副本電子郵件地址**&#x200B;未正確設定，則無法再建立電子郵件介面。您必須已設定或使用其他設定。 [了解更多](../email/email-settings.md#reply-to-email)

* **電子郵件介面** - 在 **URL 追蹤參數**&#x200B;電子郵件介面設定的區段，每個&#x200B;**值**&#x200B;欄位已從 255 個字元更新為 5 KB，以與 Adobe Analytics 追蹤相容。 [進一步了解](../email/email-settings.md#url-tracking)

**決定管理**

* **版位** - 版位建立畫面中已新增其他參數。 它們可讓您控制某個活動內容是否可在多個版位之間複製，以及指定是否應將該活動內容的內容與中繼資料包含在 API 回應中。 [了解更多](../offers/offer-library/creating-placements.md)

* **URL 個人化** - 將 URL 新增為優惠方案表示法的內容時，您現在可以使用運算式編輯器對這些 URL 進行個人化設定。[了解更多](../offers/offer-library/add-representations.md)

## 2023 年 1 月發行說明{#jan-2023-release}

### 新功能{#jan-2023-features}

<table>
<thead>
<tr>
<th><strong>資料衛生</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform 提供一套資料整理功能，可讓您以程式化方式刪除消費者記錄與資料集，管理儲存的資料。 此功能現已可供 Adobe Journey Optimizer 使用。 </p>
<p>您可管理資料存放區，確保資訊以預期方式使用、在需要修正錯誤資料時更新，以及在組織原則認為有需要時刪除。</p>
<p><strong>注意</strong> - 資料整理功能目前僅適用已購買 <strong>Healthcare Shield</strong> 與<strong>隱私權與安全性防護</strong>附加產品的組織。</p><p>如需詳細資訊，請參閱<a href="../privacy/data-hygiene.md">詳細文件</a>。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件內容範本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以建立獨立內容範本，這些範本可用於歷程及行銷活動，以快速重複使用。</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>在<a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=zh-Hant">此影片</a>瞭解如何建立、編輯並使用內容範本。如需詳細資訊，請參閱<a href="../email/content-templates.md">詳細文件</a>。
</p>
</td>
</tr>
</tbody>
</table>

### 改進項目 {#jan-2023-improvements}

**歷程**

* 在歷程中新增&#x200B;**區段資格**&#x200B;或&#x200B;**讀取區段**&#x200B;時，現已預設為使用上次使用的命名空間預先填入命名空間。 請參閱[區段資格](../building-journeys/segment-qualification-events.md#about-segment-qualification)與[讀取區段](../building-journeys/read-segment.md#configuring-segment-trigger-activity)部分。

* 在歷程畫布中，工具列提供新按鈕，可讓您下載歷程的螢幕擷取畫面。

**電子郵件設計工具**

* 您現可從&#x200B;**匯出 HTML** 功能表匯出電子郵件內容。 匯出的檔案可在封存 (.ZIP) 檔案取得。

**管理**

* 新子段落提供建議以建立&#x200B;**回覆 (電子郵件)** 地址，並確保正確的回覆管理。 [了解更多](../email/email-settings.md#reply-to-email)

* 在建立或編輯 **IP 集區**&#x200B;時，關聯的 PTR 記錄現可顯示在 IP 清單，以及當游標暫留在選取的 IP 位址時顯示。 [了解更多](../configuration/ip-pools.md#create-ip-pool)

* 在通道表面選擇 IP 集區後，現在當游標暫留在 IP 位址時，立即可見 PTR 記錄資訊。 [了解更多](../email/email-settings.md#subdomains-and-ip-pools)

* 已更新使用者介面以編輯 [PTR 記錄](../configuration/ptr-records.md#edit-ptr-record)與[執行欄位](../configuration/primary-email-addresses.md)。

* 已改進使用者介面以建立並編輯子網域。 [了解更多](../configuration/delegate-subdomain.md)

* 已更新黑名單&#x200B;**最近上傳**&#x200B;畫面。 [了解更多](../configuration/manage-suppression-list.md#recent-uploads)

**行銷活動**

* 現可自動產生允許執行 API 觸發行銷活動的 cURL 請求範例，並可在行銷活動畫面使用。 [進一步了解](../campaigns/api-triggered-campaigns.md)


**個人化**

* 提供新輔助函式：formatCurrency、charCodeAt、stringToDate、toString、formatNumber 與 toHexString。 此外，toDateTimeOnly 函式現可接受字串、日期、較長與整型欄位類型。 [了解更多](../personalization/functions/functions.md)
