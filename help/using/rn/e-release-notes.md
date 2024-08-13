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
source-git-commit: 9fdaff7a4364bb7ecfeec27446ed8f4b4ce34488
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 52%

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
<th><strong>Marketo Engage 自訂動作</strong><br/></th>
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
<th><strong>改善頻道設定</strong><br/></th>
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
