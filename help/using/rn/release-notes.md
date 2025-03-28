---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: e80554570d62d1ddb52516366be55711387c5d19
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 40%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會整合到每月最後一週的發行說明一起發表。[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。


## 2025年3月發行說明 {#25-3-rn}


### 新功能 {#25-03-features}

此版本隨附的新功能詳述如下。

<table>
<thead>
<tr>
<th><strong>與Adobe Express整合（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer中的Adobe Express整合可讓您在內容建立期間直接使用Adobe Express的編輯工具，讓您調整大小、移除背景、裁切，以及將資產轉換為JPEG或PNG。<p>
<p>Adobe Journey Optimizer中的Adobe Express整合目前僅適用於一組組織（可用性限制）。 無法部署以與Healthcare Shield或Privacy and Security Shield搭配使用。</p>
<p>如需詳細資訊，請參閱<a href="../integrations/express.md">詳細文件</a>。</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>歷程量度</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程量度現已推出，可讓您透過關鍵業務量度測量活動的影響，並針對您的績效提供更清楚的深入分析。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/success-metrics.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Calendar view for journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in Journey Optimizer to visualize all journeys activations. From this view, you can browse your journeys and check details and properties.<p>
<p>This change is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>與Dynamic Media整合（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dynamic Media資產現在可直接在Journey Optimizer中使用和存取。 此整合可讓您：
<ul>
<li>透過即時更新集中管理資產</li>
<li>立即修改您的資產設定，例如寬度和高度</li>
<li>更新您的內容並新增個人化欄位，以自訂Dynamic Media範本</li>
</ul>
<p>
<p>此整合僅適用於一組組織（可用性限制）。 若要取得存取權，請和您的 Adobe 代表聯絡。</p>
<p>如需詳細資訊，請參閱<a href="../integrations/aem-dynamic.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>與Adobe GenStudio整合（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>為了提升行銷效率及維持品牌一致性，您現在可以將GenStudio for Performance Marketing體驗與Journey Optimizer緊密整合。 這使您能夠利用GenStudio的AI支援內容建立以及Journey Optimizer的進階協調功能。<p>
<p>Journey Optimizer中的GenStudio整合目前無法與Healthcare Shield或Privacy and Security Shield （限量提供）搭配使用。</p>
<p>如需詳細資訊，請參閱<a href="../integrations/genstudio.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>LINE channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.<p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### 改進項目 {#25-03-improv}

**Personalization編輯器** （推出日期： 3月12日）

已更新 Journey Optimizer 個人化編輯器，並新增功能：
* **已更新程式碼編輯器設計** – 更簡潔的現代化介面，可改善使用性和焦點。
* **搜尋和取代** – 新增的功能可在編輯器中快速尋找和取代內容。
* **復原與重做支援** – 可讓您輕鬆還原或重新套用變更。
* **可自訂的字型大小** – 可調整編輯器的字型大小，以提升可讀性。
* **內嵌 JSON 驗證** – 為 JSON 內容提供即時用戶端驗證，以加速錯誤偵測。
* **自動完成設定檔和內容屬性** – 提供智慧型建議以簡化內容建立。
* **增強語法強調** – 讓程式碼結構在視覺上更加不同，來改善可讀性。

![在Personalization編輯器中顯示新功能的影片](assets/do-not-localize/personalization-editor.gif)

如需詳細資訊，請參閱[詳細文件](../personalization/personalization-build-expressions.md)。

**核准**

定義核准原則的條件時，您現在可以選擇依標籤和/或物件類別篩選。

如需詳細資訊，請參閱[詳細文件](../test-approve/approval-policies.md)。

**設定**

* 您現在可以將Adobe Experience Platform統一標籤指派給管道設定。 這可讓您輕鬆分類，並改善所有清單中的搜尋和導覽。 [了解更多](../configuration/channel-surfaces.md#channel-config-tags)

* 在Journey Optimizer中設定或編輯電子郵件子網域時，如果您可在上層網域中使用，您現在可以選擇自行管理相關的DMARC記錄。 [了解更多](../configuration/dmarc-record.md#set-up-dmarc)

**商業規則**

您現在可以在包含批次細分的歷程和行銷活動中，使用每日頻率上限。 為確保每日頻率上限規則的準確性，請確保在製作行銷活動或歷程時選擇最高優先順序的名稱空間。 在[平台身分服務指南](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}中進一步瞭解名稱空間優先順序

提醒您，規則集中的每日頻率上限僅適用於一組組織（可用性限制）。 若要取得存取權，請和您的 Adobe 代表聯絡。

如需商業規則的詳細資訊，請參閱[詳細檔案](../configuration/rule-sets.md)。

<!--**Content management**

To easily manage your fragments and your content templates, you can now use folders to organize them more effectively into a structured hierarchy. This improvement is only available for a set of organizations (Limited Availability). <!--To gain access, contact your Adobe representative.

**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->


