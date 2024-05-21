---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
feature: Release Notes
hide: true
hidefromtoc: true
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: bd4e352378ba9f895a192b467a650013af669c4d
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 37%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

**在發行日期前，以下早期發行說明可能會有所變更，恕不另行通知**. 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024年5月早期發行說明 {#e-2024}

**發行日期**： 2024年5月21日至22日

### 新功能 {#e-features}

此發行版本提供下列詳細介紹的新功能。


<table>
<thead>
<tr>
<th><strong>體驗決策──有限可用性</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>體驗決策透過提供稱為「決策項目」的集中行銷優惠目錄與複雜的決策引擎來簡化個人化。 此引擎運用規則與排名標準來選取並呈現最相關的決定項目給每個人。</p>
<p>這些決策項目透過新的程式碼型體驗管道無縫整合到廣泛的傳入介面，現在可在 Journey Optimizer 行銷活動中存取。Experience Decisioning 決策原則僅可用於程式碼型的體驗活動。</p>
<p>體驗決策目前僅可適用於一組組織 (可用性限制)。 若要取得存取權，請和您的 Adobe 代表聯絡。</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/gs-experience-decisioning.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>IP熱身工作流程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>如果您使用全新的IP位址傳送電子郵件，現在可以直接從使用者介面輕鬆執行IP熱身工作流程。 Adobe Journey Optimizer提供標準化和有效率的方式，讓您的IP位址按照最佳實務來熱身，以實現最佳傳遞能力。</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


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

**體驗決策** （可用性限制）

從Beta版到本版本，已新增下列改良功能：

* **Experience Decisioning +程式碼型體驗**  — 您現在可以善用Experience Decisioning功能，在程式碼型行銷活動中使用決定專案。 注意：程式碼型的體驗管道和體驗決策不適用於已購買 Adobe Healthcare Shield 以及 Privacy and Security Shield 附加產品的組織。[閱讀全文](../code-based/get-started-code-based.md)
* **內容資料**  — 您現在可以在決定規則和排名公式中善用Adobe Experience Platform的內容資料。 [閱讀全文](../experience-decisioning/context-data.md)
* **新許可權**  — 新的「管理體驗決策」許可權現在可用於決策管理資源。 它可讓您管理與體驗決策相關的權限。[閱讀全文](../experience-decisioning/gs-experience-decisioning.md)
* **上限規則**  — 您現在可以在Experience Decisioning中為特定決定專案新增多個上限規則。 這可讓您針對活動內容傳送方式提高控制等級。[閱讀全文](../experience-decisioning/items.md#capping)
* **報告**  — 您現在可以使用以下專案建立Experience Decisioning行銷活動的自訂報告控制面板 [!DNL Customer Journey Analytics]. [閱讀全文](../experience-decisioning/cja-reporting.md)


**決策管理**

* **多規則支援**  — 您現在可以在決定管理中，為指定優惠新增最多10個上限規則。 這可讓您針對活動內容傳送方式提高控制等級。
* **稽核** - **變更記錄** 標籤可讓您檢視對優惠或決定所做的所有變更已移除。 與優惠和決定相關的變更現在可以在以下連結檢視：**稽核**&#x200B;選單。


**電子郵件頻道**

* **清單 — 取消訂閱**  — 繼大量寄件者的最新Gmail和Yahoo公告後，Journey Optimizer支援「post/1-click」清單取消訂閱選項。
* **垃圾郵件評分** （測試版） — 您現在可以在專用的垃圾郵件報告中檢查您的內容垃圾郵件評分。 使用SpamAssassin，Adobe Journey Optimizer現在可以測試您的電子郵件內容，並為它提供分數，以指出ISP或信箱提供者是否將其視為垃圾郵件。 此功能目前為測試版本，僅供測試版客戶使用。 若要加入 Beta 版計畫，請連絡 Adobe 客戶服務。


<!--[Read more](../content-management/spam-report.md)-->

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

**個人化**

* **運算式片段**  — 運算式片段現在可用於 **應用程式內頻道**.
  <!--[Read more](../personalization/use-expression-fragments.md)-->

**歷程**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **mTLS支援**  — 自訂動作現在支援mTLS驗證。 自訂動作或歷程中不需要額外設定即可啟用mTLS；偵測到啟用mTLS的端點時，會自動發生此情況。
* **查詢事件中的表格**  — 現在，當使用物件陣列內的屬性定義關聯性時，您可以運用查詢資料集中的資料。 查閱值將在歷程（條件、自訂動作等）中使用 和訊息個人化。
* **事件設定中的進階運算式編輯器**  — 您現在可以在設定事件時運用進階運算式編輯器，讓您定義更複雜的運算式，或在事件ID條件中使用函式。

**全球化**

為了提供統一的使用者體驗，我們統一了Adobe Experience Cloud產品和應用程式中使用的術語。 這會影響德文術語「標題」，在與物件名稱相關時會變更為「標籤」。 這些變更將會逐步在UI和檔案中推出。
