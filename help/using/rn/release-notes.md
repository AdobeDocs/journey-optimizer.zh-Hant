---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d87dde2cbc172affa17610b28e092a0da0d7d38f
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 53%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會整合到每月最後一週的發行說明一起發表。[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。


## 2025年4月發行說明 {#25-4-rn}


**發行日期**： 2025年4月29至30日


### 新功能 {#25-04-features}

此版本隨附的新功能詳述如下。

<table>
<thead>
<tr>
<th><strong>Adobe Express整合（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer現在與Adobe Express整合，可讓您透過journey orchestration順暢地連線創意資產。 此整合可簡化跨行銷活動設計和部署個人化內容的程式。 </p>
<p>此功能目前處於「有限可用性」。</p>
<img src="assets/do-not-localize/express_resize.gif">
<p>如需詳細資訊，請參閱<a href="../integrations/express.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Calendar view for campaign and journey inventory (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new calendar view is now available for campaigns and journey activations. This feature provides a visual representation of scheduled activities, allowing you to view and manage your campaigns and journeys more effectively. Selecting a calendar item opens a right rail with detailed information. This feature is currently in Limited Availability.</p>
<img src="assets/do-not-localize/calendar.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager as a Cloud Service整合（全面發佈）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer與Adobe Experience Manager as a Cloud Service之間整合的一般可用性。 此整合可針對個人化客戶歷程啟用順暢的內容來源及管理。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Personalization編輯器 — 透過實踐學習</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在提供個人化遊樂場，您可以在其中實驗個人化運算式。 它可讓您探索範例範本和裝載，以幫助您開始並試用您自己的個人化運算式。</p>
<p>如需詳細資訊，請參閱<a href="../personalization/personalize.md#playground">詳細文件</a>。</p>
<p>推出日期： 2025年4月24日</p>
<img src="assets/do-not-localize/templating-playground.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>批次細分完成後觸發每日歷程執行（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>對於每日排程的歷程，新選項可讓您定義最多6小時的時間範圍，以等待批次分段工作的對象資料，確保歷程以最新資料執行，如果未準備就緒則予以跳過。 批次對象評估後觸發選項僅適用於一組組織（可用性限制）。 若要取得存取權，請和您的 Adobe 代表聯絡。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/read-audience.md#schedule">詳細文件</a>。</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Simulate content variations (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>With the General Availability release, the feature now includes support for multilingual content and content experiments, enabling you to test variations across different languages and treatments. Additionally, it now supports contextual attributes (in addition to profile attributes), allowing for even more dynamic and situational content testing.</p>
<img src="assets/do-not-localize/variants.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>品牌一致性分數(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>品牌一致性分數功能可直接在電子郵件設計工具中提供清楚的意見回饋，協助您檢視內容是否與品牌的語調、風格和指導方針一致。</p>
<p>如需詳細資訊，請參閱<a href="../content-management/brands-score.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>LINE頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 已擴充其跨頻道功能，以包含對 LINE 頻道的支援。此增強功能可讓您建立、編輯和預覽 LINE 體驗，以啟用更個人化且吸引人的互動。透過 LINE，您可以與更多客戶連絡、傳送相關內容並改善您的參與度。</p>
<p>Adobe Journey Optimizer客戶可依請求啟用LINE頻道。 請聯絡Adobe客戶服務或您的Adobe代表，為您的組織啟用此功能。</p>
<p>如需詳細資訊，請參閱<a href="../line/get-started-line.md">詳細文件</a>。</p></td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Custom SMS provider (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports custom SMS providers, allowing you to integrate your preferred SMS services for enhanced communication flexibility.</p>
<p>For more information, refer to the <a href="../sms/sms-configuration-custom.md">detailed documentation</a>.</p></td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>歷程量度</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程量度現已推出，可讓您衡量您的活動對業務關鍵指標的影響，並針對您的績效提供更清楚的深入分析。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/success-metrics.md">詳細文件</a>。</p>
<p>推出日期： 2025 年 4 月 9 日</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decisioning - New ranking formula builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create specific Decisioning ranking formulas by defining and combining criteria from a new improved interface. Ranking formulas allow you to define rules that will determine which decision items should be presented first, rather than taking into account the priority scores.  </p>
</td>
</tr>
</tbody>
</table>
-->

### 功能改進 {#25-04-improv}

**電子郵件頻道**

<!--* **Personalized URL tracking**

  For increased flexibility and control over your email settings, you can now personalize all your URL tracking parameters at once at the email channel configuration level, instead of doing it in the Email designer for each link in your content. -->

* **電子郵件設計工具** — 推出日期： 2025 年 4 月 1 日

  為了增強 Journey Optimizer 協助工具，電子郵件設計工具現在提供兩個新欄位：它們對應至電子郵件內容 `<html>` 元素中的 `<title>` 元素和 `lang` 屬性。 除了電子郵件&#x200B;**[!UICONTROL 內文]**&#x200B;區段的&#x200B;**[!UICONTROL 預覽文字]**&#x200B;欄位外，您還可以定義這些設定。 [閱讀全文](../email/email-metadata.md)

<!--- **Email designer themes** (Beta) - Availability date: May 5, 2025

  You can now quickly apply pre-approved styling themes to your email content to ensure brand consistency across all emails, speed up your campaign creation process and independently produce hight-quality emails while reducing dependency on design teams. -->

**沙箱工具**

<!--- **Decisioning sandbox copy**

  Decisioning objects can now be copied between sandboxes, streamlining testing and deployment workflows.-->

* **自訂動作的沙箱工具**

  自訂動作現在包含在可以使用沙箱工具功能複製的Adobe Journey Optimizer物件清單中，以簡化測試和部署。 [閱讀全文](../configuration/copy-objects-to-sandbox.md)

* **行銷活動的沙箱工具** — 推出日期： 2025年4月3日

  您現在可以使用套件匯出和匯入功能，跨多個沙箱複製行銷活動。 行銷活動會連同與輪廓、對象、結構描述、內嵌訊息以及從屬物件相關的所有項目一起複製。 有些項目不會複製，例如決定項目、資料使用標籤及語言設定。 [閱讀全文](../configuration/copy-objects-to-sandbox.md#custom-actions)

**個人化**

<!--- **Pills activation**  

  A new "Pills" button has been to the personalization editor. When enabled, profile and contextual attributes display as pills, enhancing the readability of your code.-->

* **在屬性窗格中填入屬性** — 使用日期： 2025年4月2日

  個人化編輯器的屬性窗格，現在預設僅顯示已填入的屬性。 若要檢視所有屬性，請使用設定按鈕來關閉&#x200B;**[!UICONTROL 僅顯示填入的屬性]**&#x200B;選項。 [閱讀全文](../personalization/personalization-build-expressions.md)


* **新的內容屬性**

  新的內容屬性&#x200B;**訊息設定檔ID**&#x200B;現在可從個人化編輯器選取。 這是訊息導向屬性，可唯一識別傳送中傳送至每個目標設定檔的每個訊息。 例如，此唯一識別碼可用作URL追蹤引數，以區分收件者開啟或點按的每個連結。

**導覽**

* **內容管理** — 推出日期： 2025 年 4 月 2 日

  為了輕鬆管理您的內容範本與片段，您現在可以使用資料夾將其更有效地整理至結構化階層之中。請在[內容範本](../content-management/access-content-templates.md#folders)和[片段](../content-management/manage-fragments.md#folders)一節瞭解更多資訊。

  >[!AVAILABILITY]
  >
  >此改善功能僅適用於一組組織 (有限可用性)。

<!--- **Folders for content templates and fragments** - Availability date: May 5, 2025

  Previously available for a set of organizations (LA), folders are now available to all users (GA) to manage their content templates and fragments. Folders let you organize your content templates and fragments more easily and effectively into a structured hierarchy.

- **Folders for landing pages** - Availability date: May 5, 2025

  To easily manage your landing pages, you can now also use folders to organize them more effectively into a streamlined hierarchy.  -->

<!--- **Right rail in campaigns list**  

  A right rail has been added to the campaigns list, providing detailed information when a campaign is selected.-->

<!--**Playbooks**

- **Create your own playbooks (Beta)**
  
  You can now create your own playbooks in Adobe Journey Optimizer, enabling greater customization and flexibility in journey planning.-->




