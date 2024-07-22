---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
feature: Release Notes
hide: true
hidefromtoc: true
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 2387b9912b1c4c2272643a85de6f5dcc9477b2cd
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 45%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

**至發行日期之前，下方早期發行說明如有變更，恕不另行通知**。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024 年 7 月搶先發行說明 {#e-2024}

**發行日期**： 2024年7月30至31日

### 新功能 {#e-features}

此發行版本提供下列詳細介紹的新功能。

<table>
<thead>
<tr>
<th><strong>IP熱身工作流程(GA)</strong><br/></th>
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
<th><strong>與任何提供者的SMS頻道(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在Journey Optimizer中設定其他簡訊提供者，以及預設提供者Sinch、Infobip和Twilio。</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Marketo Engage自訂動作</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將Adobe Journey Optimizer與Adobe Marketo Engage整合，以建置B2B使用案例。 新的自訂動作可讓您從歷程將資料擷取到Marketo。</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


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

* （可用性： 7月8日）您現在可以在設定事件時運用進階運算式編輯器，允許您定義更複雜的運算式或在事件ID條件中使用函式。 [了解更多](../event/about-creating.md#adv-exp-editor)

<!--* The `event-id` condition is now automatically filled during test mode. -->

**簡訊頻道**

* 您現在可以修改現有的SMS設定。

**應用程式內頻道**

* 運算式片段現在可用於應用程式內頻道。

**推播頻道**

* 您現在可以在Adobe Journey Optimizer通道組態設定中新增行動應用程式推送認證。 您不再需要在Adobe Experience Platform資料彙集中建立應用程式表面。

**對象**

* 現在可搭配Healthcare Shield和Privacy &amp; Security Shield附加元件使用受眾構成和自訂上傳（CSV檔案）的受眾和屬性。