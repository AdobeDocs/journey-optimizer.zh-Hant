---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: f07a46e6fc42afb80275557dfe8bd27f51e4fad9
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 57%

---

# 發行說明 {#release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。

先前的發行說明可在[本頁](release-notes-2022.md)取得。您還可以參閱[最新文件更新](documentation-updates.md)頁面以了解更多變更。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

![電子報](../assets/do-not-localize/nl-icon.png)立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，把每季最新產品更新、精彩故事、使用案例、提示等內容直接傳送到您的收件匣。


## 2023年2月搶鮮版發行說明 {#feb-2023}

本節包含發行前資訊。 發行日期、功能和其他資訊可能會有所變更，恕不另行通知。詳細檔案將於發行日期提供。

可用性： **2023年2月22日**

### 改進項目 {#feb-2023-improvements}

**歷程**

* 此 **重新進入等待期** 欄位已新增至歷程屬性。 此欄位可讓您定義等待時間，再允許設定檔在單一歷程中再次進入歷程（從事件或區段資格開始）。 這可防止同一事件的歷程錯誤觸發多次。 依預設，欄位會設為5分鐘。

* 已對 **歷程開始和結束日期**. 如果您尚未指定開始日期，則現在會在發佈時自動新增開始日期。 針對 **讀取區段** 歷程，您現在可以新增結束日期。 這可讓設定檔在達到日期時自動退出。

* 已增強歷程畫布，提供更簡單且改善的使用者體驗。 畫布中每個路徑的結尾處，已移除空白預留位置。 您現在只需將活動拖曳到節點之間的任何位置，即可新增活動。

* 已改善歷程中的逾時和錯誤管理。 逾時和錯誤路徑現在一律會新增在畫布上。 有新的工具列按鈕可顯示/隱藏這些路徑。

* 引入了一種新型系統報警。 自訂動作失敗時，您現在可以收到通知。


**管理**

* **允許的清單**  — 您現在可以將允許的清單下載為.csv檔案。

* **電子郵件介面**  — 電子郵件表面設定已新增額外檢查：如果 **回覆（電子郵件）地址** 或 **密件副本電子郵件地址** 未正確設定，則無法再建立電子郵件表面。 您必須已設定或使用其他設定。

* **電子郵件介面**  — 在電子郵件表面設定的URL追蹤參數區段中，每個 **值** 欄位已從255個字元更新為5 KB，以與Adobe Analytics追蹤相容。

**決策管理**

* **版位**  — 版位建立畫面中已新增其他參數。 它們可讓您控制某個優惠方案是否可在多個版位之間複製，以及指定是否應將該優惠方案的內容和中繼資料包含在API回應中。

* **URL個人化**  — 將URL新增為選件表示法的內容時，您現在可以使用運算式編輯器來個人化這些URL。



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

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

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

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**個人化**

* 提供新輔助函式：formatCurrency、charCodeAt、stringToDate、toString、formatNumber 與 toHexString。 此外，toDateTimeOnly 函式現可接受字串、日期、較長與整型欄位類型。 [了解更多](../personalization/functions/functions.md)
