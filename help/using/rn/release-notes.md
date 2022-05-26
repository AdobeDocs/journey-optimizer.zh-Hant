---
title: 發行說明
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: dd60e576aaded21efd9718341d1c4f26267ae001
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 34%

---

# 發行說明 {#release-notes}

本頁面列出[!DNL Journey Optimizer]所有新功能和改進項目。您還可以參閱[最新文件更新](documentation-updates.md)頁面以了解更多變更。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變動，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target=&quot;_blank&quot;}。

![電子報](../assets/do-not-localize/nl-icon.png) 立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} ，直接把每季最新產品更新、激勵人心的故事、使用案例、提示等內容傳送到您的收件匣。

## 2022 年 5 月發行 {#may-2022-release}

### 新功能

<!--table>
<thead>
<tr>
<th><strong>Message Frequency Rules</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now set cross-channel business rules that will automatically exclude over-solicited profiles from messages and actions.</p>
<img src="assets/frequency-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/frequency-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>電子郵件密件抄送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用電子郵件密件抄送（Email BCC，盲碳拷貝）功能來儲存Adobe Journey Optimizer發送的電子郵件。 在電子郵件預設中啟用此選項，以便將發送的每封電子郵件都盲目複製到您的密件抄送地址。</p>
<img src="assets/bcc-rn.gif"/>
<p>如需詳細資訊，請參閱<a href="../configuration/email-settings.md#bcc-email">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Decision Management - AI Ranking auto-optimization model</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use trained model systems in Decision Management. This new capability ranks offers to display for a given profile.</p>
<img src="assets/optimization.gif"/>
<p>For more information, refer to the <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer審計日誌</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以監視用戶對Adobe Journey Optimizer資源執行的操作。</p>
<img src="assets/audit-rn.gif"/>
<p>如需詳細資訊，請參閱<a href="../reports/audit-logs.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改進項目

**個人化**

* **用於字元隱藏的新幫助程式函式** - `mask` helper函式允許您將字串的一部分替換為「X」字元。 [了解更多](../personalization/functions/string.md#mask)

**登陸頁面**

* **沒有表單的登錄頁**  — 您現在可以建立並發佈不包含表單且不需要訪問者執行任何操作的登錄頁。
* **登錄頁模板**  — 現在，您可以將登錄頁另存為模板，並在建立其他登錄頁時重新使用它。 [了解更多](../landing-pages/lp-templates.md)
* **返回首頁**  — 現在，您可以從同一登錄頁內的任何子頁添加到首頁的連結。
* **自定義JavaScript支援**  — 現在，您可以將自定義JavaScript添加到登錄頁內容中，以執行高級樣式設定或將自定義行為添加到登錄頁。	[了解更多](../landing-pages/lp-custom-js.md)

<!--**Decision management**

* **HTML and JSON files support** - You can now drag and drop external HTML and JSON files from the AEM repository into the offer representation content.-->

**歷程**

* **讀取段**  — 一次性讀取段行程現在在行程執行30天後移至「已完成」狀態。 對於計畫的讀取段，它是在上次執行該事件後30天。 [閱讀全文](../building-journeys/read-segment.md)
* **表達式編輯器** - [限](../building-journeys/functions/functionlimit.md) 已添加函式，以允許您限制清單的項數。 的 [排序](../building-journeys/functions/functionsort.md) 函式現在允許您對清單對象進行排序。 對listObject的支援也添加到 [斷層](../building-journeys/functions/functiondistinct.md) 和 [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) 的子菜單。
