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
source-git-commit: 128a56b543f470bf967fd195fde73ff7b32b2a17
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 34%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

**至發行日期之前，下方早期發行說明如有變更，恕不另行通知**。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024 年 8 月搶先發行說明 {#e-2024}

**發行日期**：2024 年 8 月 20-21 日

### 新功能 {#e-features}

此發行版本提供下列詳細介紹的新功能。


<table>
<thead>
<tr>
<th><strong>引導式管道設定</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>引導式管道設定可讓您在統一體驗中自動執行行動管道設定的步驟，以更快開始使用Journey Optimizer。 此設定有助於快速設定行銷管道，確保所有必要資源都能隨時在Experience Platform、Journey Optimizer和資料收集中取得。 這可讓您的行銷團隊立即開始行銷活動和歷程建立。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>內容卡片</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>內容卡是Adobe Journey Optimizer中的新數位傳訊功能，可直接在行動應用程式和網站中提供個人化且吸引人的內容。 與傳統的推播通知不同，內容卡片可順暢地整合到使用者介面中，提供永久、非侵入式更新，以增強使用者互動和體驗。</p>
<p>此功能可讓行銷人員向使用者呈現相關的豐富媒體內容，促進更高參與度，並確保看到重要訊息，而不會中斷使用者旅程。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>已改善通道設定</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>已增強目前的管道表面功能，以在所有管道中採取一致的方法。 您現在可以為任何管道定義、管理和重複使用這些設定。</p>
<p><ul>
<li>管道表面現在已重新命名為<strong>管道設定</strong></li>
<li>從管道設定詳細目錄，您現在可以為所有管道建立可重複使用的管道設定，包括現在的Web、應用程式內傳訊或程式碼型體驗</li>
<li>物件層級存取控制(OLAC)現在可用於每個通道設定，可讓您決定允許哪些使用者建立或使用特定設定</li>
<li>對於某些管道，您可以建立以多個平台為目標的管道設定。 以下為可鎖定網頁、iOS應用程式和Android應用程式的應用程式內傳訊頻道設定範例。</li>
</ul></p>
<p>如需詳細資訊，請參閱<a href="../configuration/ip-warmup-gs.md">詳細文件</a>。</p>
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
<p>推出日期： 8月13日</p>
<p>如果您使用全新的 IP 位址傳送電子郵件，現在可以直接從使用者介面輕鬆執行 IP 暖身工作流程。 Adobe Journey Optimizer 提供標準化和有效率的方式，讓您的 IP 位址按照最佳實務來暖身，以實現最佳傳遞能力。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/ip-warmup-gs.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

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

* 在&#x200B;**條件**&#x200B;活動中，預設的Time條件現在會依小時設定，從00:00到12:00。 [閱讀全文](../building-journeys/condition-activity.md#time_condition)
* 建立歷程時，警示現在會顯示在下拉式清單中，以與行銷活動警示保持一致，並提供一致的使用者體驗。 [閱讀全文](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* 歷程工具列中的縮放選項已改善：現在可以看到縮放百分比，您現在可以輕鬆將縮放值重設為100%。

**對象**

* 自訂上傳的對象 (CSV 檔案) 現在可與「隱私權與安全防護板」搭配使用。
* 鎖定自訂上傳（CSV檔案）對象時，您現在可以在行銷活動和歷程中使用檔案中的屬性。 這些屬性可用於個人化編輯器和歷程進階運算式編輯器，以個人化您的訊息。

<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
