---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: e47c95ac8981356bcfb742105cbf1faa5d53c189
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 22%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會整合到每月最後一週的發行說明一起發表。[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}。

## 2025年2月發行說明 {#25-02-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**發行日期**： 2025年2月18至19日


### 全新功能 {#25-02-features}

此版本隨附的新功能詳述如下。

<table>
<thead>
<tr>
<th><strong>建立和管理商業規則</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用規則集建立商業規則。 規則集是規則群組，可協助您限制行銷活動中傳送的訊息和跨管道的歷程動作，並控制歷程中的設定檔專案。<p>
<p><ul><li>建立管道規則集，以限制跨一或多個管道傳送的訊息數。 將它們套用至行銷活動或歷程動作，以強制執行規則集中定義的規則。 管道規則集可讓您根據通訊型別套用上限規則。 例如，設定規則集以限制「促銷訊息」，並針對「電子報」設定另一個規則集。 根據您傳送的通訊型別，在您的行銷活動或歷程動作中套用適當的規則集。</li>
<li> 建立歷程規則集以控制設定檔專案進入歷程。 限制設定檔在指定期間內輸入歷程的頻率，或設定檔可同時註冊的歷程數。 在歷程層級套用這些專案，以確保適當的進入管理。</li></p>
<p>先前可供一組組織(LA)使用的商業規則，現在可供所有使用者使用(GA)。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/rule-sets.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用AI助理產生登陸頁面</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以藉助AI助理，為登陸頁面製作引人入勝的內容，包括全頁設計、個人化文字和自訂視覺效果。</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>如需詳細資訊，請參閱<a href="../content-management/generative-lp.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>具有AI助理(Beta)的品牌</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以設定自己的品牌，以定義品牌的視覺和口頭識別。 </p>
<p>此功能以私人測試版的形式發行給有限的客戶群。 未來版本將逐步開放所有客戶使用。</p>
<p>如需詳細資訊，請參閱<a href="../content-management/brands.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>疑難排解您的自訂動作（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以直接從Adobe Journey Optimizer發出真正的API呼叫，以驗證自訂動作設定。 </p>
<p>如需詳細資訊，請參閱<a href="../action/troubleshoot-custom-action.md">詳細文件</a>。</p>
<p> 此功能僅適用於一組組織（可用性限制）。 若要取得存取權，請和您的 Adobe 代表聯絡。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>彈性的對象評估（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>彈性的受眾評估可讓您視需求針對選取的受眾執行細分工作，確保在將受眾鎖定目標至Journey Optimizer歷程和行銷活動之前，您始終擁有最新的受眾資料。</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>如需詳細資訊，請參閱<a href="../audience/creating-a-segment-definition.md#flexible">詳細文件</a>。</p>
<p>此功能僅適用於一組組織（可用性限制）。 若要取得存取權，請和您的 Adobe 代表聯絡。</p>
<p>推出日期：2025年1月28日</p>
</tr>
</tbody>
</table>
</table>


### 改進項目 {#25-02-improvements}

以下改良功能隨2月更新提供。

* **歷程** — 您現在可以從管理區段傳送API呼叫來測試自訂動作。 這項新功能可協助您在歷程中使用自訂動作之前或之後，進行疑難排解。 [閱讀全文](../action/troubleshoot-custom-action.md)

* **資料集存留時間(TTL)** — 從本月開始，存留時間(TTL)護欄將推出至新沙箱和新組織中的Journey Optimizer系統產生的資料集，如下所示：

   * 輪廓存放區中的資料為 90 天
   * 資料湖中的資料為 13 個月

  此變更將在後續階段中推出至現有客戶沙箱。

  在[專屬常見問答集](../data/datasets-ttl.md#frequently-asked-questions)中進一步瞭解此更新。

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **直接郵件** — 直接郵件通道設定中的檔案路由現在支援新的伺服器型別，資料登陸區域。 [閱讀全文](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **簡訊** — 您現在可以覆寫傳遞、回饋、傳入和回撥URL，以管理來自多區域端點的簡訊傳遞。 為了支援此功能，已在API認證設定中新增欄位覆寫URL。 此變更僅適用於Sinch提供者。 [閱讀全文](../sms/sms-configuration-sinch.md)

* **Personalization** （推出日期： 2025年1月29日） — 新的日期/時間協助程式功能可用於個人化編輯器。 [閱讀全文](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **電子郵件設定** — 如果您在Adobe外部管理同意，您現在可以設定自訂取消訂閱電子郵件地址和自訂一鍵取消訂閱URL，做為電子郵件通道設定的一部分。 [瞭解詳情](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **決策** （推出日期： 2025年1月28日） — 決策現在在編輯專案目錄的結構描述時支援物件資料型別。 [閱讀全文](../experience-decisioning/catalogs.md)

