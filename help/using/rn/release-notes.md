---
title: 發行說明
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 30d197f3eab05e2e38025189a6948a6c0fbd6d54
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 63%

---

# 發行說明 {#release-notes}

本頁面列出[!DNL Journey Optimizer]所有新功能和改進項目。您還可以參閱[最新文件更新](documentation-updates.md)頁面以了解更多變更。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變動，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target=&quot;_blank&quot;}。

![電子報](../assets/do-not-localize/nl-icon.png) 立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} ，直接把每季最新產品更新、激勵人心的故事、使用案例、提示等內容傳送到您的收件匣。

## 2022 年 8 月發行版本 {#aug-2022-release}

### 新功能

<!--table>
<thead>
<tr>
<th><strong>Create and manage campaigns in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use Journey Optimizer campaigns to deliver one-time content to a specific segment using various channels. When using journeys, actions are designed to be executed in sequence. With campaigns actions are performed simultaneously, either immediately, or based on a specified schedule. </p>
<p>For more information, refer to the <a href="../campaigns/get-started-with-campaigns.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>將SMS發送給用戶（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以透過與 <b>Sinch</b> 或 <b>Twilio</b> 的整合在 Journey Optimizer 裡建立、個人化和傳送簡訊。</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>在<a href="../messages/create-sms.md">詳細文件</a>中了解如何建立和傳送簡訊。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->



### 改進項目

**報告**

* 同意策略表和圖表現在可在Journey全球報告中找到。 這些小部件允許您跟蹤自定義操作中策略中排除的配置檔案。 [了解更多](../reports/journey-global-report.md#journey-global)

   要訪問最新小部件，請注意，您必須重置不同的報告儀表板。 有關儀表板自定義的詳細資訊，請參閱 [詳細文檔](../reports/global-report.md)。

**管理**

* 現在，可以更新主電話號碼以用於SMS頻道。 [了解更多](../configuration/primary-email-addresses.md)