---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: dc313d7cbee9e412b9294b644fddbc7840f90339
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 20%

---

# 發行說明 {#release-notes}

[!DNL Adobe Journey Optimizer] 持續提供新功能、現有功能的增強功能和錯誤修正。 所有變更都會在本發行說明中於每月的最後一週整合。

先前的發行說明位於 [本頁](release-notes-2022.md). 您還可以參閱[最新文件更新](documentation-updates.md)頁面以了解更多變更。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變動，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}.

![電子報](../assets/do-not-localize/nl-icon.png) 註冊 [Adobe Journey Optimizer季刊](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} 今天，每季都會直接收到最新產品更新、精彩故事、使用案例、秘訣等內容。


## 2023 年 1 月發行版本 {#jan-2023-release}

### 新功能{#jan-2023-features}


<table>
<thead>
<tr>
<th><strong>資料檢疫</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform提供一套資料衛生功能，可讓您透過程式化刪除消費者記錄和資料集，管理儲存的資料。 此功能現在已可供Adobe Journey Optimizer使用。 </p>
<p>您可以管理資料存放區，以確保資訊可如預期般使用、在需要修正錯誤資料時更新，以及在組織原則認為有需要時刪除。</p>
<p><strong>注意</strong>  — 資料衛生功能目前僅適用於購買了Healthcare Shield附加產品的組織。</p>
<p>如需詳細資訊，請參閱<a href="../privacy/data-hygiene.md">詳細文件</a>。
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Email content templates</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create standalone content templates that can be leveraged across journeys and campaigns for quick reuse.</p> 
<p>For more information, refer to the <a href="../personalization/get-started-dynamic-content.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>
-->

### 改進項目 {#jan-2023-improvements}

**歷程**

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

* 新增 **區段資格** 或 **讀取區段** 在歷程中，現在預設會使用上次使用的命名空間預先填入命名空間。 請參閱 [區段資格](../building-journeys/segment-qualification-events.md#about-segment-qualification) 和 [讀取區段](../building-journeys/read-segment.md#configuring-segment-trigger-activity) 區段。

* 在歷程畫布中，工具列中提供新按鈕，可讓您下載歷程的螢幕擷取畫面。

**電子郵件設計工具**

* 您現在可以從 **匯出HTML** 功能表。 匯出的檔案可在封存(.ZIP)檔案中使用。

**管理**

* 新小節提供關於建立 **回覆（電子郵件）** 地址，並確保正確的回復管理。 [了解更多](../email/email-settings.md#reply-to-email)

* 建立或編輯時 **IP池**，關聯的PTR記錄現在會顯示在IP清單中，並將游標暫留在選定的IP地址上。 [了解更多](../configuration/ip-pools.md#create-ip-pool)

* 在通道表面中選擇IP池後，現在當將游標暫留在IP地址上時，PTR記錄資訊將可見。 [了解更多](../email/email-settings.md#subdomains-and-ip-pools)

* 要編輯的使用者介面 [PTR記錄](../configuration/ptr-records.md#edit-ptr-record) 和 [執行欄位](../configuration/primary-email-addresses.md) 已更新。

* 用於建立及編輯子網域的使用者介面已經過改良。 [了解更多](../configuration/delegate-subdomain.md)

* 隱藏清單 **最近上載** 畫面已更新。 [了解更多](../configuration/manage-suppression-list.md#recent-uploads)

**行銷活動**

* 現在會自動產生允許API觸發促銷活動執行的cURL要求範例，並可在促銷活動畫面中使用。 [進一步了解](../campaigns/api-triggered-campaigns.md)

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**個人化**

* 提供新的協助程式功能：formatCurrency、charCodeAt、stringToDate、toString、formatNumber和toHexString。 此外，toDateTimeOnly函式現在接受字串、日期、長和整型欄位類型。 [了解更多](../personalization/functions/functions.md)
