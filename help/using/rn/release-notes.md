---
title: 發行說明
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 52cc27108ed4d99511ef612c0bd81d3435d1f45b
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 42%

---

# 發行說明 {#release-notes}

本頁面列出[!DNL Journey Optimizer]所有新功能和改進項目。您還可以參閱[最新文件更新](documentation-updates.md)頁面以了解更多變更。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變動，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target=&quot;_blank&quot;}。

![電子報](../assets/do-not-localize/nl-icon.png) 立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} ，直接把每季最新產品更新、激勵人心的故事、使用案例、提示等內容傳送到您的收件匣。

## 2022 年 6 月發行版本 {#june-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>將SMS發送給用戶</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>可用日期： <b>6月27日</b></p>
<p></p>
<p>您現在可以通過與Windows的整合在Journey Optimizer建立、個性化和發送SMS <b>辛奇</b> 或 <b>Twilio</b>。</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>如需詳細資訊，請參閱<a href="../messages/create-sms.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>通過Adobe Stock整合，更快地查找影響力更大的映像</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>可用日期： <b>6月23日</b></p>
<p></p>
<p>Adobe Stock和Adobe Journey Optimizer電子郵件設計器整合插件為客戶提供了導航、許可和保存影像以用於郵件創作的簡單方法。 </br> 新 <b>查找類似的股票照片</b> 選項還允許您查找與影像內容、顏色和組成匹配的「儲存」照片。 </p>
<img src="assets/do-not-localize/stock-rn.gif"/>
<p>如需詳細資訊，請參閱<a href="../design/stock.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在所有電子郵件上使用電子郵件密件抄送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用電子郵件密件抄送（Email BCC，盲碳拷貝）功能來儲存Adobe Journey Optimizer發送的電子郵件。 在電子郵件預設中啟用此選項，以便將發送的每封電子郵件都盲目複製到您的密件抄送地址。</p>
<img src="assets/do-not-localize/bcc-rn.gif"/>
<p>如需詳細資訊，請參閱<a href="../configuration/bcc-email.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<!--table>
<thead>
<tr>
<th><strong>Copy objects between sandboxes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now re-create the experiences from a Journey Optimizer sandbox to another, for example from a non-production sandbox to a production sandbox. This new capability copies an entire Journey, including any objects the Journey depends on to run correctly, from one environment to another. In addition to Journeys, you can also copy other components, such as Offers, Messages, Schemas, Datasets, Data Sources, Events, and Actions.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content. In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### 改進項目

**決策管理**

* **HTML和JSON檔案支援**  — 您現在可以將外部HTML和JSON檔案從Adobe Experience Cloud資產庫拖放到優惠表示內容中。 [進一步了解](../offers/offer-library/add-representations.md#html-json)

<!--
**Email**

* **Save as template** - You can now save an email content as a template and reuse it when creating other messages.

**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.

-->

**管理**

<!--* **Allowed list in the UI** - You can now use the Journey Optimizer user interface to add new email addresses or domains to the allowed list.-->

* **預覽跟蹤URL參數**  — 配置消息預設時，如果定義URL跟蹤參數，則現在將顯示結果跟蹤URL的動態預覽。 [了解更多](../configuration/email-settings.md#url-tracking)

<!--* **Personalize tracking URL parameters** - You can now use the Expression Editor to configure URL tracking parameters in your message presets. [Learn more](../configuration/email-settings.md#url-tracking)-->

<!--
**Reporting**

* **Performance measurement** - A new **Reporting** tab is now available in the Administration > Configurations menu to set up reporting data sources.
-->
