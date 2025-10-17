---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 9c80306d1dad057272b43339c940fec77e2441b1
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 45%

---

# 搶鮮版發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能增強並修正錯誤。所有變更都會在每月底整合於[發行說明](release-notes.md)。


## 2025年10月發行前注意事項 {#25-10-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。連結、畫面及更新的文件會在發行當日發佈於發行說明。

另請參閱 [Adobe Experience Platform 搶鮮版發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**：2025年10月22日

### 全新功能 {#oct-25-10-features}



<table>
<thead>
<tr>
<th><strong>自訂動作監視和報告</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此功能可讓您更清楚地了解歷程健康狀況和執行，包括生命週期狀態和績效警示。您現在可以快速了解自訂動作中發生異常狀況的時間、位置和原因。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>用於擷取動作行銷活動的新API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現已提供新的Journey Optimizer API，可讓您以程式設計方式擷取及檢查行銷活動相關資料，例如詳細資訊、版本和設定。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>忠誠度應用程式的新來源聯結器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform現在提供新的來源聯結器，適用於Talon.One、Chariceline和Kobie忠誠度應用程式。 這些聯結器可讓您將忠誠度資料順暢地串流至Adobe Experience Platform，並在Journey Optimizer中利用這些資料。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件頻道中的決策支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將決定原則新增至電子郵件歷程與行銷活動。決策原則是優惠方案的容器，可運用決策引擎以動態方式傳回最佳內容，傳送給每個對象成員。</p>
<p> 此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API觸發的電子郵件行銷活動的高輸送量模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>API 觸發的行銷活動現在提供新的高輸送量模式。此模式專為大規模即時傳訊 (每秒最多 5000 筆交易) 而設計，可提供更高的可用性並降低延遲。</p>
<p>此功能僅適用於電子郵件管道，以及已購買 Adobe 高輸送量交易訊息附加產品的組織。請聯絡您的 Adobe 代表以取得更多資訊。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>無訊息時數/基於時間的排除</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>無訊息小時可讓您定義電子郵件、簡訊、推播和WhatsApp頻道的時間型排除專案。 它們可確保在特定時段內不會傳送任何訊息，協助您遵守客戶偏好設定和合規性要求。</p>
<p>您可以透過規則集套用無訊息時數，這些規則集可指派給行銷活動或歷程中的個別動作，以進行精確控制。 透過簡化這些流程。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>
<table>
<thead>
<tr>
<th><strong>執行中繼資料協助程式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>個人化編輯器中提供新的「executionMetadata」協助程式功能。 它可讓您將內容相關資訊附加至任何原生動作，並將其擷取至資料集，以匯出至外部系統。</p>
<p>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。</p>
<p>如需詳細資訊，請參閱<a href="../personalization/functions/helpers.md#execution-metadata">詳細文件</a></p>
<p>推出日期： 2025年10月13日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>實驗代理程式已推出！</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>由<a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator.html" target="_blank">Adobe Experience Platform Agent Orchestrator</a>提供支援，Experimentation Agent可在Journey Optimizer中使用。 </p>
<p>Experimentation Agent是AI支援的工具，可更新您跨網站、電子郵件、推送訊息和應用程式執行和管理數位實驗的方式。 它可協助您更有效率地執行實驗、組織業務目標，以及產生可操作的深入分析，並著重說明哪些有效果、哪些無效以及下一步該在何處實驗。</p>
<p>如需詳細資訊，請參閱<a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html" target="_blank">詳細文件</a></p>
<p>推出日期： 2025年10月10日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件的 PDF 附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以對透過 Journey Optimizer 傳送的電子郵件訊息附加靜態 PDF 檔案。</p>
<ul>
<li>您每年最多可以為每個設定檔傳送 6 封含有 PDF 附件的訊息。</li>
<li>每個附件允許的大小上限為 5 MB。</li>
<li>如需其他大小或流量，您可以購買 PDF 附件附加元件。如需詳細資訊，請聯絡您的 Adobe 代表。</li>
</ul>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../email/pdf-attachments.md">詳細文件</a></p>
<p>推出日期：2025 年 9 月 30 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>用於擷取歷程的公用API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>新的Journey Optimizer API現在可用於擷取歷程及其關聯的物件，例如行銷活動和表面。</p>
<p>如需詳細資訊，請參閱<a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">詳細文件</a></p>
<p>推出日期：2025 年 9 月 25 日</p>
</td>
</tr>
</tbody>
</table>


### 改善

**在鎖定目標中選取可重複使用的規則**

現在，您可以在歷程及行銷活動中搭配使用目標定位規則與訊息最佳化功能時，運用規則產生器。<!-- [Read more](../FILE.md) -->

WhatsApp頻道&#x200B;**的**&#x200B;執行欄位

除了電子郵件和簡訊之外，現在也可以更新WhatsApp預設執行欄位。 您也可以覆寫WhatsApp歷程活動進階引數或WhatsApp頻道設定中的執行欄位全域設定。<!-- [Read more](../FILE.md) -->

**新歷程警示**

新的預先設定警示可用於歷程： [超過的設定檔捨棄率](../reports/alerts.md#alert-discard-rate) （超過臨界值的過去5分鐘捨棄設定檔與輸入設定檔的比率）、[超過的自訂動作錯誤率](../reports/alerts.md#alert-custom-action-error-rate) （超過臨界值的自訂動作錯誤與成功HTTP呼叫的比率）以及[超過的設定檔錯誤率](../reports/alerts.md#alert-profile-error-rate) （超過臨界值的過去5分鐘錯誤設定檔與輸入設定檔的比率）。 您可以修改臨界值，並訂閱個別歷程層級警示與全域警示。

推出日期：2025 年 10 月 14 日

Mailto （取消訂閱）位址的&#x200B;**自訂屬性支援**

透過Journey Optimizer，如果您在Adobe之外管理同意，則可在電子郵件設定中定義您自己的一鍵式取消訂閱連結和自訂取消訂閱電子郵件地址，藉此設定外部自訂端點。 當您的收件者按一下取消訂閱連結時，Journey Optimizer 會將一些預設的輪廓特定參數附加至同意更新事件。

若要進一步個人化您的自訂端點，您現在可以定義將附加至同意事件的自訂屬性。 [閱讀全文](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>此功能自2025年8月起已可用於自訂&#x200B;**[!UICONTROL 一鍵取消訂閱URL]**，現在已針對「有限可用性」中的&#x200B;**[!UICONTROL Mailto （取消訂閱）]**&#x200B;選項發行。 請聯絡您的 Adobe 代表以取得存取權。

推出日期： 2025年10月6日