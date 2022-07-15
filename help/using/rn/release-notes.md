---
title: 發行說明
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ac3c49c16a2496b3d5bc9b803589644b69c6565c
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 100%

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
<th><strong>傳送簡訊給使用者（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以透過與 <b>Sinch</b> 或 <b>Twilio</b> 的整合在 Journey Optimizer 裡建立、個人化和傳送簡訊。</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>簡訊管道目前僅可用於一組組織（可用性限制）。 如需詳細資訊，請聯絡您的 Adobe 代表。</p>
<p>在<a href="../messages/create-sms.md">詳細文件</a>中了解如何建立和傳送簡訊。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>透過與 Adobe Stock 整合，更快找到影響力更大的圖片</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Stock 和 Adobe Journey Optimizer 電子郵件設計工具整合外掛程式，為客戶提供了用於訊息製作的導覽、授權和儲存影像的簡單方法。 您還可以藉由</br>新的<b>找到類似的相片庫</b>選項找出與影像內容、顏色和組成相符的影像庫。 </p>
<img src="assets/do-not-localize/stock-rn.gif"/>
<p>如需詳細資訊，請參閱<a href="../design/stock.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在所有電子郵件上使用密件副本電子郵件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用密件副本電子郵件（密件副本）功能來儲存 Adobe Journey Optimizer 傳送的電子郵件。 在電子郵件預設集中啟用此選項，以便將每封傳送的電子郵件以密件副本方式寄至密件副本地址。</p>
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

<table>
<thead>
<tr>
<th><strong>在沙箱之間複製物件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，您可以從 Journey Optimizer 沙箱將體驗重新建立到另一個沙箱，例如從非生產沙箱重新建立到生產沙箱。 這個新功能可將整個 Journey 從一個環境複製到另一個環境，包括 Journey 賴以正確運作的任何物件。 除了 Journeys 之外，您還可以複製其他元件，如 Offirs、Messages、Schemas、Datasets、Data Sources、Events 和 Actions。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/copy-to-sandbox.md">詳細文件</a>。
</td>
</tr>
</tbody>
</table>

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

* **HTML 和 JSON 檔案支援** — 您現在可以將外部 HTML 和 JSON 檔案從 Adobe Experience Cloud 資產庫拖放到優惠方案聲明內容中。 [了解更多](../offers/offer-library/add-representations.md#html-json)


**電子郵件**

* **另存為範本** — 您現在可以將電子郵件內容另存為範本，並在建立其他郵件時重複使用它。 [進一步了解](../design/email-templates.md)

<!--
**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.

-->

**管理**

<!--* **Allowed list in the UI** - You can now use the Journey Optimizer user interface to add new email addresses or domains to the allowed list.-->

* **預覽追蹤 URL 參數** — 設定訊息預設集時，如果定義 URL 追蹤參數，則將顯示結果追蹤 URL 的動態預覽。 [了解更多](../configuration/email-settings.md#url-tracking)

* **訊息預設集版本** — 現在，當更新訊息預設集時，處理時間最多只需 3 小時。 [了解更多](../configuration/message-presets.md#edit-message-preset)

* **IP 池版本** — 現在，當更新 IP 池時，處理時間最多只需 3 小時。 [了解更多](../configuration/ip-pools.md#edit-ip-pool)

<!--* **Personalize tracking URL parameters** - You can now use the Expression Editor to configure URL tracking parameters in your message presets. [Learn more](../configuration/email-settings.md#url-tracking)-->

<!--
**Reporting**

* **Performance measurement** - A new **Reporting** tab is now available in the Administration > Configurations menu to set up reporting data sources.
-->
