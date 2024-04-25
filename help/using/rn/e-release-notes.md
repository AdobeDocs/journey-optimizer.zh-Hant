---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: acd195e669d653b52ba7722e9e01db28a5a7d2b7
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 34%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024年4月早期發行說明 {#e-2024}

**發行日期**：2024年4月30日

### 新功能 {#e-features}

此版本提供下列詳細的新功能。

<!--table>
<thead>
<tr>
<th><strong>Business rules - Private Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>It is now possible to create and apply rule sets to your marketing communications.  </p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>體驗決策 — 有限可用性</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience Decisioning透過提供稱為「決策專案」的行銷優惠集中目錄和複雜的決策引擎，簡化了個人化。 此引擎運用規則和排名條件來選取最相關的決定專案，並將之呈現給每個人。</p>
<p>這些決策專案透過新的程式碼型體驗管道(現在可在Journey Optimizer促銷活動中存取)無縫整合到廣泛的傳入介面。 Experience Decisioning決定原則僅適用於程式碼型體驗行銷活動。</p>
<p>Experience Decisioning目前僅適用於一組組織（可用性限制）。 若要取得存取權，請聯絡您的Adobe代表。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Personalization - Local Lookups - Multi-Entity Support - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>TBD</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Infobip多媒體訊息服務(MMS)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過簡訊管道，您現在可以傳送多媒體訊息服務 (MMS) 訊息，來與客戶分享影像、GIF 或影片，藉此增強通訊交流。 這項功能先前只適用於Sinch，現在也適用於Infobip。</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow - LA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now easily perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### 改進項目 {#e-improvements}

此發行版本隨附下列改進項目。

<!--
* **Experience Decisioning + Code-based experiences (LA)**: You can now leverage the Experience decisioning feature to use decision items in your code-based campaigns. Note: The Code-based experience channel and Experience decisioning are not available for organizations that have purchased the Adobe Healthcare Shield and Privacy and Security Shield add-on offerings.
-->
<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**決策管理**

* 此 **變更記錄** 標籤可讓您檢視對優惠或決定所做的所有變更已移除。 與優惠和決定相關的變更現在可以在以下連結中檢視： **稽核** 功能表。

**體驗決策**

從Beta版到LA版，已新增下列改善功能：

* 您現在可以使用在決策規則中利用Adobe Experience Platform的內容資料 **內容資料** 標籤。
* 決策管理資源現在有新的「管理體驗決策」許可權可用。 它可讓您管理與Experience Decisioning相關的許可權。
* 您現在可以為一個選件新增多個上限規則。 這可讓您針對活動內容傳送方式提高控制等級。
* 您現在可以為體驗決策中的指定決策專案新增多個上限規則。 這可讓您針對活動內容傳送方式提高控制等級。
* 您現在可以使用建立Experience Decisioning行銷活動的自訂報告控制面板 [!DNL Customer Journey Analytics].

**歷程**

* **改善的歷程設計器**

   * 改良後的畫布UI提供更直覺且有效率的使用者體驗。
   * 活動會更清楚，且透過較少的點按就能在歷程畫布上呈現更多資訊。

* **新即時報告**：過去24小時的歷程報告現在可直接在歷程畫布中存取。

**設定**

* 您現在可以在通道表面層級選取行銷動作。在表面中使用時，會運用與該行銷動作相關的所有同意政策，以尊重客戶的偏好設定。
* 現在管道表面可以使用「物件層級存取控制」。

