---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 68c09769a32aeb1132f09e0f9082c7ccb6d17a8b
workflow-type: tm+mt
source-wordcount: '1152'
ht-degree: 71%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

![電子報](../assets/do-not-localize/nl-icon.png)立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，把每季最新產品更新、精彩故事、使用案例、提示等內容直接傳送到您的收件匣。


## 2024年6月早期發行說明 {#24-6-2024}

**在發行日期前，以下早期發行說明可能會有所變更，恕不另行通知**.

**發行日期**： 2024年6月18至19日

### 新功能 {#june24-features}

此發行版本提供下列詳細介紹的新功能。

<table>
<thead>
<tr>
<th><strong>IP熱身工作流程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>如果您使用全新的IP位址傳送電子郵件，現在可以直接從使用者介面輕鬆執行IP熱身工作流程。 Adobe Journey Optimizer提供標準化和有效率的方式，讓您的IP位址按照最佳實務來熱身，以實現最佳傳遞能力。</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Content Fragments customization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define specific fields in a fragment that can be edited when the fragment is added to a campaign or journey. This allows for the adjustment of content portions at the time of use, providing flexibility to override default values with context-specific details.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->


<table>
<thead>
<tr>
<th><strong>Adobe Journey Optimizer中的AI助理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI Assistant是使用者介面功能，可用於導覽和瞭解Adobe概念，並取得您特定環境的營運見解。 它適用於Adobe Experience Cloud的多個產品，包括Adobe Journey Optimizer。</p>
<p>如需詳細資訊，請參閱<a href="../start/ai-assistant.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Reporting with Customer Journey Analytics (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer reporting is now fully integrated with Customer Journey Analytics capabilities, standardizing reporting across both platforms and improving data consistency and reliability. This seamless integration between Journey Optimizer and Customer Journey Analytics provides a clearer view of performance metrics, enabling users to make more informed decisions.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns  (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Experimentation in journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Already available in campaigns, Adobe Journey Optimizer now supports experiments in journeys. Experiments are randomized trials, which in the context of online testing, means that you expose some randomly selected users to a given variation of a message, and another randomly selected set of users to some other variation or treatment. After exposure, you can then measure the outcome metrics you are interested in, such as opens of emails, subscriptions, or purchases.</p>
</td>
</tr>
</tbody>
</table-->



<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### 改進項目 {#june24-improvements}

此發行版本隨附下列改進項目。


**決策管理**

* **決策管理中的多規則支援**  — 您現在可以在決定管理中，為指定優惠新增最多10個上限規則。 這可讓您針對活動內容傳送方式提高控制等級。[了解更多](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

<!--**Content fragments**

* Fragments can now be edited, and changes can be propagated across all live journeys and campaigns where they are used.
* New statuses for content fragments have been introduced: **Draft**, **Live**, **Publishing**, and **Archived**. 
* To use a fragment in a journey or campaign, it must now be in the **Live** status. A new step has been added to the fragment creation process, allowing the fragment to be published and made available for use in journeys and campaigns. Note that fragment publishing requires a new permission.
   
   **CAUTION** - Since **Draft** and **Live** statuses have been introduced with Journey Optimizer June release, all fragments created before this release have the **Draft** status, even if they are used in a journey or campaign. Learn how to update your existing fragments in this section.-->

**歷程**

* 歷程全域逾時已從30天增加至91天。
* Adobe Journey Optimizer現在支援隱私權刪除/存取請求，以及資料生命週期管理請求。
* 您現在可以調整歷程詳細目錄中的欄大小。
* **事件設定中的進階運算式編輯器** 現在為GA — 您現在可以在設定事件時運用進階運算式編輯器，讓您定義更複雜的運算式或在事件ID條件中使用函式。 此功能以「有限可用性」形式向選定客戶發佈。 <!--[Read more](../event/about-creating.md)-->
* **合併原則** 現在為GA — 歷程使用的合併原則現在在整個歷程中可見且一致。 此功能以「有限可用性」形式向選定客戶發佈。 <!--[Read more](../building-journeys/journey-gs.md#merge-policies)-->



**行銷活動**

* 在Adobe Journey Optimizer中建立行銷活動時，您現在可以在新強制回應視窗中選擇行銷活動型別（已排程或觸發）。

<!--**Email channel**

* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**簡訊頻道**

* 您現在可以使用單一API設定，為每個沙箱新增唯一的短程式碼，讓流程更有效率且簡化。
  <!--* You can now modify existing SMS configurations.-->

**應用程式內頻道**

* **運算式片段**  — 運算式片段現在可用於 **應用程式內頻道**. <!--[Read more](../personalization/use-expression-fragments.md)-->


* 您現在可以使用Edge Delivery外掛程式，取得瞭解傳入實作並進行疑難排解所需的資訊。



## 2024 年 5 月發行說明 {#may-2024}

**發行日期**：2024 年 5 月 21 日至 22 日

### 新功能 {#e-features}

此發行版本提供下列詳細介紹的新功能。

<table>
<thead>
<tr>
<th><strong>體驗決策──有限可用性</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>體驗決策透過提供稱為「決策項目」的集中行銷優惠目錄與複雜的決策引擎來簡化個人化。 此引擎運用規則與排名標準來選取並呈現最相關的決定項目給每個人。</p>
<p>這些決策項目透過新的程式碼型體驗管道無縫整合到廣泛的傳入介面，現在可在 Journey Optimizer 行銷活動中存取。Experience Decisioning 決策原則僅可用於程式碼型的體驗活動。</p>
<p>體驗決策目前僅可適用於一組組織 (可用性限制)。 若要取得存取權，請和您的 Adobe 代表聯絡。</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/gs-experience-decisioning.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件介面個人化：開放限量使用</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您可以在建立電子郵件頻道介面時，馬上定義動態子網域和個人化標題參數，就能提高電子郵件設定彈性，更能夠掌握得當。</p>
<p>電子郵件介面個人化目前僅開放給某些組織使用 (開放限量使用)。 若要取得存取權，請和您的 Adobe 代表聯絡。</p>
<p>如需詳細資訊，請參閱<a href="../email/surface-personalization.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### 改進項目 {#e-improvements}

此發行版本隨附下列改進項目。

**體驗決策** (限量)

從 Beta 版到此版本，新增了以下改善：

* **體驗決策 + 程式碼型的體驗** ：您現在可以利用體驗決策功能在程式碼型的行銷活動中使用決策項目。 注意：程式碼型的體驗管道和體驗決策不適用於已購買 Adobe Healthcare Shield 以及 Privacy and Security Shield 附加產品的組織。[閱讀全文](../code-based/get-started-code-based.md)
* **內容資料** - 現在您可以在決策規則和排名公式中利用 Adobe Experience Platform 的內容資料。[閱讀全文](../experience-decisioning/context-data.md)
* **新權限** - 決策管理資源現在有新的「管理體驗決策」權限可用。 它可讓您管理與體驗決策相關的權限。[閱讀全文](../experience-decisioning/gs-experience-decisioning.md)
* **上限規則** - 您現在可以為體驗決策中的指定決策項目新增多個上限規則。 這可讓您針對活動內容傳送方式提高控制等級。[閱讀全文](../experience-decisioning/items.md#capping)
* **報告** - 現在您可以使用[!DNL Customer Journey Analytics]建立體驗決策活動的自訂報告儀表板。 [閱讀全文](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**電子郵件頻道**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **垃圾郵件評分** (Beta) - 您現在可以在專用的垃圾郵件報告中檢查您的內容垃圾郵件評分。 使用 SpamAssassin，Adobe Journey Optimizer 現在可以測試您的電子郵件內容並為其評分，以指出 ISP 或信箱提供者是否將其視為垃圾郵件。 [閱讀全文](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >此功能目前為 Beta 版本，僅供 Beta 版客戶使用。若要加入 Beta 版計畫，請聯絡 Adobe 代表。

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**歷程**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **mTLS 支援** - 自訂動作現在支援 mTLS 驗證。 自訂動作或歷程中不需要額外設定即可啟用 mTLS；當偵測到啟用 mTLS 的端點時，它會自動發生。 [閱讀全文](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **查詢事件中的表格** - 現在，當使用物件陣列內的屬性定義關聯性時，您可以運用查詢資料集中的資料。 查閱值將在歷程 (條件、自訂動作等) 以及訊息個人化中使用。 [閱讀全文](../event/experience-event-schema.md#relationships_limitations)
* **事件設定中的進階運算式編輯器** (LA) - 您現在可以在設定事件時運用進階運算式編輯器，讓您定義更複雜的運算式或在事件 ID 條件中使用函數。 此功能以「限量」形式向選定的客戶發布。[閱讀全文](../event/about-creating.md)
* **合併原則** (LA) - 歷程使用的合併原則現在在整個歷程中可見且一致。 此功能以「限量」形式向選定的客戶發布。[閱讀全文](../building-journeys/journey-gs.md#merge-policies)

**全球化**

作為我們不斷努力提供統一使用者體驗的一部分，我們統一了 Adobe Experience Cloud 產品和應用程式中使用的術語。 這會影響德文術語「標題」，在與物件名稱相關時會變更為「標籤」。 這些變更將會逐步在使用者介面與檔案中逐步推出。



