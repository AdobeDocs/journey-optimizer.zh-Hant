---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# 發行說明 {#release-notes}

本頁面列出 [!DNL Journey Optimizer]. 您也可以參閱 [最新檔案更新](documentation-updates.md) 頁面以取得更多變更。

[!DNL Adobe Journey Optimizer] 內建於 [!DNL Adobe Experience Platform] 並繼承其最新的創新和改進。 深入了解以下變更： [Adobe Experience Platform發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target=&quot;_blank&quot;}。

![電子報](../assets/do-not-localize/nl-icon.png) 註冊 [Adobe Journey Optimizer季刊](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}，每季會直接收到最新產品更新、精彩故事、使用案例、秘訣等內容。


## 2022年10月發行 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### 改良功能 {#oct-2022-improvements}

**歷程**

* 此 **重複時強制重新進入** 已在循環讀取區段排程參數中新增選項。 此選項可讓您讓歷程中仍存在的所有設定檔在下次執行時自動退出。 停用選項時，設定檔必須先完成歷程，才能在另一個發生次數中重新輸入。 [深入了解](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**管理**

* 使用者介面新增訊息，以警告子網域、登錄頁面子網域、PTR記錄和IP池設定是所有沙箱的共同設定，因此，對其中一個設定所做的任何修改也會影響生產沙箱。
* 已修改從使用者介面上傳隱藏清單為CSV檔案的步驟。 [深入了解](../configuration/manage-suppression-list.md#download-suppression-list)

**行銷活動**

* 您現在可以封存已完成和已停止的促銷活動。 [深入了解](../campaigns/modify-stop-campaign.md#archive)
