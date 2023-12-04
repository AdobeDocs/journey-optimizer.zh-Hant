---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 299b34dec2e864fff5eb874b3fd491da80bc0c16
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 100%

---

# 發行說明 {#release-notes}


>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。

先前的發行說明可在[本頁](release-notes-2023.md)取得。您還可以參閱[最新文件更新](documentation-updates.md)頁面以了解更多變更。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

![電子報](../assets/do-not-localize/nl-icon.png)立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，把每季最新產品更新、精彩故事、使用案例、提示等內容直接傳送到您的收件匣。

## 2023 年 10 月發行說明 {#oct-rn-2023}

### 新功能{#oct-2023-features}

此發行版本提供下列新功能。

<table>
<thead>
<tr>
<th><strong>沙箱工具</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>沙箱工具可讓您運用套件匯出和匯入功能，跨多個沙箱複製物件。 套件可以包含單一物件或多個物件。 套件中包含的任何物件都必須來自相同沙箱。</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<p>如需詳細資訊，請參閱<a href="../building-journeys/copy-to-sandbox.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>簡訊中的多媒體訊息服務 (MMS)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過簡訊管道，您現在可以傳送多媒體訊息服務 (MMS) 訊息，來與客戶分享影像、GIF 或影片，藉此增強通訊交流。 請注意，目前只有 Sinch 提供此功能。</p>
<img src="assets/do-not-localize/mms.gif"/>
<p>如需詳細資訊，請參閱<a href="../sms/create-sms.md#mms-content">詳細文件</a>。</p>
</tr>
</tbody>
</table>

### 改進項目 {#oct-2023-improvements}

此發行版本隨附下列改進項目。

**對象**

* 您現在可以鎖定從 CSV 檔案上傳至歷程和行銷活動中的目標對象。[了解更多](../audience/about-audiences.md#segments-in-journey-optimizer)
* 您現在可以鎖定透過對象構成所建立的目標對象，並在歷程中運用擴充屬性。 [了解更多](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>這些功能目前以 Private Beta 的形式提供。

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**行銷活動**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* 當您的其中一個行銷活動發生錯誤時，警告圖示現在會與行銷活動的狀態一起出現在行銷活動清單中。[了解更多](../campaigns/modify-stop-campaign.md#statuses)

**歷程**

* 現在，您可在任何等待時間中定義的最長期間是 29 天，而不是 30 天。此項改進的目的是在防止等待的持續時間超過 30 天的歷程期限。 這適用於：

   * [等待活動](../building-journeys/wait-activity.md)中的&#x200B;**時間長度**&#x200B;欄位
   * [歷程屬性](../building-journeys/journey-gs.md#entrance)中的&#x200B;**重新進入等待期**
   * [事件活動](../building-journeys/general-events.md#events-specific-time)逾時定義中的&#x200B;**等待**&#x200B;欄位。

<!--
**Consent in channel configuration**

* You can now select a marketing action at the channel surface level. When used in a surface, all consent policies associated with that marketing action are leveraged in order to respect the preferences of your customers.-->

**決策管理**

* 已更新與決策管理介面中的優惠方案上限相關的幾個標籤。 [了解更多](../offers/offer-library/add-constraints.md#capping)

