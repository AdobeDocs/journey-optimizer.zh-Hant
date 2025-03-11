---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 13bf2bca3997ff85aca619c8b610aaa0be9142f8
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 86%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會整合到每月最後一週的發行說明一起發表。[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2025年3月更新 {#25-03-rn}

**Personalization編輯器增強功能**

Journey Optimizer個人化編輯器已更新，其中包含新功能：
* **已更新程式碼編輯器設計** — 更簡潔的現代介面，可改善使用性和焦點。
* **搜尋和取代** — 新增在編輯器中快速尋找和取代內容的功能。
* **復原與重做支援** — 可讓您輕鬆還原或重新套用變更。
* **可自訂的字型大小** — 可調整編輯器的字型大小，以提升可讀性。
* **內嵌JSON驗證** — 為JSON內容提供即時使用者端驗證，以加速錯誤偵測。
* **設定檔和內容屬性的自動完成** — 提供智慧型建議以簡化內容建立。
* **加強的語法醒目提示** — 透過讓程式碼結構在視覺上更加不同，改善可讀性。

![在Personalization編輯器中顯示新功能的影片](assets/do-not-localize/personalization-editor.gif)

如需詳細資訊，請參閱[詳細文件](../personalization/personalization-build-expressions.md)。

## 2025 年 2 月發行說明 {#25-02-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**發行日期**：2025 年 2 月 18-19 日


### 新功能 {#25-02-features}

此版本隨附的新功能詳述如下。

<table>
<thead>
<tr>
<th><strong>建立和管理業務規則</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用規則集建立業務規則。 規則集是規則群組，可協助您限制行銷活動中傳送的訊息和跨管道的歷程動作，並控制進入歷程的設定檔專案。<p>
<p><ul><li>建立管道規則集，以限制跨一或多個管道傳送的訊息數。 將它們套用至行銷活動或歷程動作，以強制執行規則集中定義的規則。 管道規則集可讓您根據通訊類型套用上限規則。 例如，設定規則集以限制「促銷訊息」，並針對「電子報」設定另一個規則集。 根據您傳送的通訊類型，在您的行銷活動或歷程動作中套用適當的規則集。</li>
<li> 建立歷程規則集以控制設定檔專案進入歷程。 限制設定檔在指定期間內輸入歷程的頻率，或設定檔可同時註冊的歷程數。 在歷程層級套用這些專案，以確保適當地進入管理。</li></p>
<p>業務規則以前僅可供一組組織 (LA) 使用，目前可供所有使用者使用 (GA)。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/rule-sets.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用 AI 助理產生登入頁面</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以藉助 AI 助理，為登陸頁面製作引人入勝的內容，包括全頁設計、個人化文字和自訂視覺效果。</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>如需詳細資訊，請參閱<a href="../content-management/generative-lp.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>具有 AI 助理 (Beta) 的品牌</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以設定自己的品牌，以定義品牌的視覺和語言身分。 </p>
<p>此功能以私人測試版的形式發行給有限的客戶群。 未來版本將逐步開放所有客戶使用。</p>
<p>如需詳細資訊，請參閱<a href="../content-management/brands.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>疑難排解您的自訂動作</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以直接從 Adobe Journey Optimizer 進行真正的 API 呼叫，以驗證自訂動作設定。 </p>
<p>如需詳細資訊，請參閱<a href="../action/troubleshoot-custom-action.md">詳細文件</a>。</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>彈性客群評估 (可用性限制)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>彈性客群評估可讓您視需求針對選取的客群執行細分工作，確保在將客群鎖定目標至 Journey Optimizer 歷程和行銷活動之前，始終擁有最新的客群資料。</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>如需詳細資訊，請參閱<a href="../audience/creating-a-segment-definition.md#flexible">詳細文件</a>。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若要取得存取權，請和您的 Adobe 代表聯絡。</p>
<p>推出日期：2025 年 1 月 28 日</p>
</tr>
</tbody>
</table>
</table>


### 改進項目 {#25-02-improvements}

以下列出了 2 月發行的改進項目。

* **歷程** — 您現在可以從管理區段傳送 API 呼叫來測試自訂動作。 這項新功能可協助您在歷程中使用自訂動作之前或之後，進行疑難排解。 [閱讀全文](../action/troubleshoot-custom-action.md)

* **資料集存留時間 (TTL)** ：自本月起，將在新沙箱和新組織中，向 Journey Optimizer 系統產生的資料集，開放使用存留時間 (TTL) 護欄功能，如下所示：

   * 輪廓存放區中的資料為 90 天
   * 資料湖中的資料為 13 個月

  將在後續階段，開放現有客戶沙箱使用這項變更。 

  在[專屬常見問答集](../data/datasets-ttl.md#frequently-asked-questions)中進一步瞭解此項更新。

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **直接郵件** — 直接郵件管道設定的檔案路由現在支援新的伺服器類型，即資料登陸區域。 [閱讀全文](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS 簡訊** — 您現在可以覆寫傳送、回饋、傳入和回撥 URL，以管理來自多區域端點的 SMS 簡訊傳送。 為了支援此功能，已在 API Credentials 設定中新增欄位覆寫 URL。 此變更僅適用於 Sinch 提供者。 [閱讀全文](../sms/sms-configuration-sinch.md)

* **個人化** (推出日期： 2025 年 1 月 29 日) — 新的日期/時間協助程式功能可用於個人化編輯器。 [閱讀全文](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **電子郵件組態** — 如果您在 Adobe 外部管理同意聲明，現在可以在電子郵件管道設定中設定自訂的取消訂閱電子郵件地址和自訂的一鍵取消訂閱 URL。[閱讀全文](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **決策** (推出日期：2025 年 1 月 28 日) — 決策現在在編輯專案目錄的結構描述時支援物件資料類型。 [閱讀全文](../experience-decisioning/catalogs.md)

