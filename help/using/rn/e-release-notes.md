---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 18d74badf3f5ea98f613d6b31303aa3108c979a5
workflow-type: ht
source-wordcount: '294'
ht-degree: 100%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

**至發行日期之前，下方早期發行說明如有變更，恕不另行通知**。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024 年 7 月搶先發行說明 {#e-2024}

**發行日期**：2024 年 7 月 30-31 日

### 新功能 {#e-features}

此發行版本提供下列詳細介紹的新功能。

<table>
<thead>
<tr>
<th><strong>IP 暖身工作流程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>如果您使用全新的 IP 位址傳送電子郵件，現在可以直接從使用者介面輕鬆執行 IP 暖身工作流程。 Adobe Journey Optimizer 提供標準化和有效率的方式，讓您的 IP 位址按照最佳實務來暖身，以實現最佳傳遞能力。</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


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
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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
<!--p>For more information, refer to the <a href="https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/home"  target="_blank">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Marketo Engage custom action</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now integrate Adobe Journey Optimizer with Adobe Marketo Engage to build your B2B use cases. From a journey, a new custom action allows you to ingest data into Marketo.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Improved channel configurations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The current channel surface capabilities have been enhanced for a consistent approach across all channels. You can now define, manage, and reuse these configurations for any of your channels.</p>
<p><ul>
<li>Channel surfaces are now renamed to <strong>Channel configurations</strong></li>
<li>From the Channel configurations inventory you can now create reusable channel configurations for all channels, including now Web, In-app messaging, or Code-based experience</li>
<li>Object level access control (OLAC) is now available for each channel configuration, allowing you to decide which of your users are allowed to create or use specific configurations</li>
<li>For some channels, you can create channel configurations that target multiple platforms. An example here would be an In-app messaging channel configuration that can target a web page, an iOS app and an Android app.</li>
</ul></p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
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

**歷程**

* (上市日期： 7 月 8 日) 您現在可以在設定事件時善用進階運算式編輯器，讓您定義更複雜的運算式或在事件 ID 條件中使用函式。[了解更多](../event/about-creating.md#adv-exp-editor)

**對象**

* 自訂上傳的對象 (CSV 檔案) 現在可與「隱私權與安全防護板」搭配使用。
<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
