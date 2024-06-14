---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
feature: Release Notes
topic: Content Management
source-git-commit: 1840e32efbea7aaff50c497d6387232a4e02d2c9
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 26%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

**至發行日期之前，下方早期發行說明如有變更，恕不另行通知**。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024年6月早期發行說明 {#e-2024}

**發行日期**： 2024年6月18至19日

### 新功能 {#e-features}

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

### 改進項目 {#e-improvements}

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

**電子郵件頻道**

* **清單 — 取消訂閱**  — 繼大量寄件者的最新Gmail和Yahoo公告後，Journey Optimizer支援「post/1-click」清單取消訂閱選項。 <!--Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**簡訊頻道**

* 您現在可以使用單一API設定，為每個沙箱新增唯一的短程式碼，讓流程更有效率且簡化。
  <!--* You can now modify existing SMS configurations.-->

**應用程式內頻道**

* **運算式片段**  — 運算式片段現在可用於 **應用程式內頻道**. <!--[Read more](../personalization/use-expression-fragments.md)-->


* 您現在可以使用Edge Delivery外掛程式，取得瞭解傳入實作並進行疑難排解所需的資訊。


