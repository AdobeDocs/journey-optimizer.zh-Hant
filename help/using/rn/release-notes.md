---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d971d857a480868f5ef502f3a3f2c209afc93cca
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 70%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

![電子報](../assets/do-not-localize/nl-icon.png)立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，把每季最新產品更新、精彩故事、使用案例、提示等內容直接傳送到您的收件匣。

## 2024 年 8 月搶先發行說明 {#e-2024}

**發行日期**：2024 年 8 月 20-21 日

>[!CAUTION]
>
>**在發行日期**&#x200B;之前，以下的早期發行說明可能會有所變更，恕不另行通知。 連結、畫面和更新檔案會在發行日期發佈。
>

### 新功能 {#e-features}

此發行版本提供下列詳細介紹的新功能。

<!--table>
<thead>
<tr>
<th><strong>Guided Channel Setup</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Guided Channel Setup enables you to automate and validate channel setup in a unified experience, speeding up the process of getting started with Journey Optimizer. This new guided setup streamlines rapid channel configuration, ensuring all necessary resources are readily installed and working within Experience Platform, Journey Optimizer, and Data Collection. This enables marketing, product and data engineering teams to quickly begin with campaign and journey creation.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Content Cards</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content card is a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Improved Channel Configurations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The current channel surface capabilities have been enhanced for a consistent approach across all channels. You can now define, manage, and reuse these configurations for any of your channels, including Web, In-app messaging, or Code-based experience.</p>
<p><ul>
<li>Channel surfaces are now renamed to <strong>Channel configurations</strong></li>
<li>You can attach one or multiple marketing actions to enforce consent and data governance policies</li>
<li>Object level access control (OLAC) is now available for each channel configuration, allowing you to decide which of your users are allowed to create or use specific configurations</li>
<li>For some channels, you can create channel configurations that target multiple platforms. An example here would be an In-app messaging channel configuration that can target a web page, an iOS app and an Android app.</li>
</ul></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Marketo Engage自訂動作</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將 Adobe Journey Optimizer 與Adobe Marketo Engage 整合，來建置您的 B2B 使用案例。 新的自訂動作可讓您從歷程將資料收錄到 Marketo。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>內容片段中的變數</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>片段現在可以在<a href="../personalization/use-expression-fragments.md">運算式片段</a>和<a href="../email/use-visual-fragments.md">視覺片段</a>中使用輸入變數。 您可以使用這些變數，在行銷活動和歷程中個人化您的訊息內容和引數。</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP 暖身工作流程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>推出日期：8 月 13 日</p>
<p>如果您使用全新的 IP 位址傳送電子郵件，現在可以直接從使用者介面輕鬆執行 IP 暖身工作流程。 Adobe Journey Optimizer 提供標準化和有效率的方式，讓您的 IP 位址按照最佳實務來暖身，以實現最佳傳遞能力。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/ip-warmup-gs.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


### 改進項目 {#e-improvements}

此版本帶來下列改善專案。

**歷程**

<!--* In the **Condition** activity, by default, the Time condition is now set by hour, from 00:00 to 12:00. [Read more](../building-journeys/condition-activity.md#time_condition)-->
* 建立歷程時，警示現在會顯示在下拉式清單中，以與行銷活動警示保持一致，並提供一致的使用者體驗。 [閱讀全文](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* 歷程工具列中的縮放選項已改善：現在可以看到縮放百分比，您現在可以輕鬆將縮放值重設為100%。

**對象**

* 自訂上傳的對象（CSV檔案）現在可與Privacy and Security Shield附加元件搭配使用。
* 鎖定自訂上傳（CSV檔案）對象時，您現在可以在行銷活動和歷程中使用檔案中的屬性。 這些屬性可用於個人化編輯器和歷程進階運算式編輯器，以個人化您的訊息。

## 2024 年 7 月發行說明 {#24-7-2024}

**發行日期**：2024 年 7 月 30-31 日

### 新功能 {#27-4-features}

此發行版本提供下列新功能。

<table>
<thead>
<tr>
<th><strong>具有任何提供者的 SMS 頻道 (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了預設提供者 Sinch、Infobip 和 Twilio 之外，您現在可以在 Journey Optimizer 設定其他 SMS 提供者。</p>
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>如需詳細資訊，請參閱<a href="../sms/sms-configuration-custom.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>聯合客群構成 (可用性限制)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 現已提供聯合客群構成。它可讓企業自行組合資料，以便在各種使用案例中能善加運用。有了這種新方法，身為 Adobe Real-Time 客戶資料平台和/或 Adobe Journey Optimizer 使用者，您就可以直接聯合現有資料倉儲中的資料集，透過單一系統建置並擴充 Adobe 體驗平台的客群及屬性。</p>
<p>如需詳細資訊，請參閱<a href="https://experienceleague.adobe.com/zh-hant/docs/federated-audience-composition/using/home"  target="_blank">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改進項目 {#27-4-improvements}

此發行版本隨附下列改進項目。

**歷程**

* (有效日期：7 月 8 日) **歷程事件設定中的進階運算式編輯器** - 您現在可以在設定事件時善用進階運算式編輯器，讓您定義更複雜的運算式或在事件 ID 條件中使用函數。[了解更多](../event/about-creating.md#adv-exp-editor)

