---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 4fbb879f40952aaef5b197b170578bf9e27f10f9
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 95%

---

# 發行說明 {#release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。

先前的發行說明可在[本頁](release-notes-2022.md)取得。您還可以參閱[最新文件更新](documentation-updates.md)頁面以了解更多變更。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

![電子報](../assets/do-not-localize/nl-icon.png)立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，把每季最新產品更新、精彩故事、使用案例、提示等內容直接傳送到您的收件匣。


## 2023年3月改進 {#march-2023}

**管理歷程中的標籤**

身為Journey Optimizer從業人員，您現在可以使用標籤來組織業務物件。 標籤是一種快速、簡便的對象分類方法，用於改進搜索。 此功能目前為測試版，僅適用於歷程。 [了解更多](../building-journeys/tags.md)

## 2023 年 2 月發行說明 {#feb-2023}

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

<!--
* **Placements** - Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)
-->

* **URL 個人化** - 將 URL 新增為優惠方案表示法的內容時，您現在可以使用運算式編輯器對這些 URL 進行個人化設定。[了解更多](../offers/offer-library/add-representations.md)

<!--
* **Capping** - You can now reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)

* **Capping** - You can now choose which Adobe Experience Platform event should be looked at for offer decisioning capping. [Learn more](../offers/offer-library/add-constraints.md#capping)
-->

## 2023 年 1 月發行版本 {#jan-2023-release}

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
