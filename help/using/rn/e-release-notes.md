---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 004eb41b084f32993ec437f589e4e3d2cf7500d3
workflow-type: ht
source-wordcount: '350'
ht-degree: 100%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於[發行說明](release-notes.md)。

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2023 年 10 月搶先發行說明 {#oct-rn-2023}

**發行日期**：2023 年 10 月 25 至 26 日

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
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
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
<th><strong>簡訊中的多媒體訊息服務 (MMS) (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過簡訊管道，您現在可以傳送多媒體訊息服務 (MMS) 訊息，來與客戶分享影像、GIF 或影片，藉此增強通訊交流。 請注意，此功能目前僅適用於 Beta 版的 Sinch。</p>
<!--img src="assets/channel-reports.png"/-->
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

### 改進項目 {#oct-2023-improvements}

此發行版本隨附下列改進項目。

**對象**

* 您現在可以鎖定從 CSV 檔案上傳至歷程和行銷活動中的目標對象。
* 您現在可以鎖定透過對象構成所建立的對象，並在歷程中運用擴充屬性。

>[!AVAILABILITY]
>
>這些功能目前以 Private Beta 的形式提供。

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**行銷活動**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* 當您的其中一個行銷活動發生錯誤時，警告圖示現在會與行銷活動的狀態一起出現在行銷活動清單中。

**歷程**

* 現在，您可在任何等待時間中定義的最長期間是 29 天，而不是 30 天。這適用於：

   * [等待活動](../building-journeys/wait-activity.md)中的&#x200B;**時間長度**&#x200B;欄位
   * [歷程屬性](../building-journeys/journey-gs.md#entrance)中的&#x200B;**重新進入等待期**
   * [一般](../building-journeys/general-events.md#events-specific-time)和[反應](../building-journeys/reaction-events.md)事件的逾時定義中的&#x200B;**等待**&#x200B;欄位。

**通道設定中的同意**

* 您現在可以在通道表面層級選取行銷動作。在表面中使用時，會運用與該行銷動作相關的所有同意政策，以尊重客戶的偏好設定。

**決策管理**

* 已更新與決策管理介面中的優惠方案上限相關的幾個標籤。
