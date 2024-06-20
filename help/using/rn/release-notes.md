---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ca743774017e8f6cf5f385119d9c71de6020bb19
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 63%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

![電子報](../assets/do-not-localize/nl-icon.png)立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，把每季最新產品更新、精彩故事、使用案例、提示等內容直接傳送到您的收件匣。


## 2024 年 6 月發行說明 {#24-6-2024}

**在發行日期前，以下早期發行說明可能會有所變更，恕不另行通知**.

**發行日期**：2024 年 6 月 18 日至 19 日

### 新功能 {#june-24-features}

此發行版本提供下列詳細介紹的新功能。

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


<table>
<thead>
<tr>
<th><strong>內容片段客製化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在片段中定義特定欄位，當片段新增到行銷活動或歷程時可以編輯這些欄位。 這允許在使用時調整內容部分，提供以內容特定的詳細資訊覆寫預設值的彈性。</p>
<img src="../content-management/assets/do-not-localize/gif-fragments.gif"/>
<p>如需詳細資訊，請參閱<a href="../content-management/customizable-fragments.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>




<table>
<thead>
<tr>
<th><strong>使用Customer Journey Analytics (Beta)製作報表</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer報告功能現在與Customer Journey Analytics功能完全整合，可跨兩個平台標準化報告，並改善資料一致性和可靠性。 Journey Optimizer與Customer Journey Analytics之間的緊密整合可讓您更清楚檢視績效量度，讓使用者能做出更明智的決策。</p>
<p>如需詳細資訊，請參閱<a href="../reports/report-gs-cja.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Journey Optimizer 中的 AI 助理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI 助理是使用者介面功能，可用於導覽和了解 Adobe 概念，並取得您特定環境的操作見解。 它適用於 Adobe Experience Cloud 的多種產品，包括 Adobe Journey Optimizer。</p>
<p>如需詳細資訊，請參閱<a href="../start/ai-assistant.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
<p>Multilingual content is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
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
<p>Experimentation in journeys is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
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

* **決策管理中的多規則支援** - 您現在可以在決定管理中，為指定優惠方案新增最多 10 個上限規則。這可讓您針對活動內容傳送方式提高控制等級。[了解更多](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

**內容片段**

>[!AVAILABILITY]
>
>請注意，這些增強功能將在首次發行後的數天內逐步推出。 雖然有些使用者可以立即存取，但有些使用者在其環境中使用前可能會遇到延遲問題。

* 片段現在可以編輯，並可以在使用它們的所有即時歷程和行銷活動中傳播變更。
* 已引進內容片段的新狀態：**草稿**，**即時**，**發佈**、和&#x200B;**已封存**。
* 若要在歷程或行銷活動中使用片段，它現在必須處於&#x200B;**即時**&#x200B;狀態。 已新增步驟至片段建立流程，可發佈片段並用於歷程及行銷活動。 請注意，片段發佈需要新的權限。

  **注意** - 由於 Journey Optimizer 已在 6 月發行版本中匯入&#x200B;**草稿**&#x200B;和&#x200B;**即時**&#x200B;狀態，因此在此版本之前建立的所有片段都具有&#x200B;**草稿**&#x200B;狀態，即使它們用於歷程或行銷活動中。在本節了解如何更新現有片段。

請閱讀以下內容： [內容片段](../content-management/fragments.md) 檔案。

**歷程**

* 歷程的全域逾時已延長至91天。 [閱讀全文](../building-journeys/journey-properties.md#global_timeout)

  任何建立的新歷程都會反映這個新的逾時。 請參考此 [常見問題集區段](../building-journeys/journey-properties.md#timeout-faq) 以進一步瞭解。 請注意，這些變更將會在6月期間逐步推出。


* Adobe Journey Optimizer現在支援隱私權刪除/存取請求，以及資料生命週期管理請求。 [閱讀全文](../privacy/requests.md)
* 您現在可以調整歷程詳細目錄中的欄大小。
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* **合併原則**&#x200B;現已正式上市 - 歷程使用的合併原則現在在整個歷程中可見且一致。 [閱讀全文](../building-journeys/journey-properties.md#merge-policies)



**行銷活動**

* 在Adobe Journey Optimizer中建立行銷活動時，您現在可以在新強制回應視窗中選擇行銷活動型別（已排程或觸發）。 [閱讀全文](../campaigns/create-campaign.md)

<!--**Email channel**

* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**簡訊頻道**

* 您現在可以使用單一API設定，為每個沙箱新增唯一的短程式碼，讓流程更有效率且簡化。 [了解更多](../sms/sms-configuration.md)

* 建立之後， **API Token** 欄位於 **API認證詳細資料** 頁面現在已遮罩。

<!--* You can now modify existing SMS configurations.-->

**應用程式內頻道**

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* 您現在可以使用Edge Delivery外掛程式，取得瞭解傳入實作並進行疑難排解所需的資訊。 [深入瞭解邊緣傳遞檢視](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.


**直接郵件頻道**

* 已購買Adobe的組織現在可使用直接郵件頻道 **Health Shield** 和 **隱私權與安全防護板** 附加方案。
