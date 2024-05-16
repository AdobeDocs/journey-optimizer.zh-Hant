---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 8dacf28f4c3217a57e648b3c80e1724d9794c9ea
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 34%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

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
<p>這些決策專案透過新的程式碼型體驗管道(現在可在Journey Optimizer促銷活動中存取)無縫整合到廣泛的傳入介面。 Experience Decisioning決定原則僅適用於程式碼型體驗行銷活動。</p>
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
<p>如需詳細資訊，請參閱<a href="../configuration/ip-warmup-gs.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>商業規則 — Beta版</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以建立精細的頻率上限規則，並透過規則集將其套用至不同型別的行銷通訊。 </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>本機查詢的多實體支援 — Beta版</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>待定</p>
</td>
</tr>
</tbody>
</table>


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

**體驗決策**

從Beta版到洛杉磯版，已新增下列改善專案：

* **Experience Decisioning +程式碼型體驗(LA)**：您現在可以善用Experience Decisioning功能，在程式碼型行銷活動中使用決定專案。 注意：程式碼型體驗通道和體驗決策不適用於已購買AdobeHealthcare Shield和Privacy and Security Shield附加產品的組織。 [閱讀全文](../code-based/get-started-code-based.md)
* 您現在可以在決定規則和排名公式中善用Adobe Experience Platform的內容資料。 [閱讀全文](../experience-decisioning/context-data.md)
* 決策管理資源現在有新的「管理體驗決策」權限可用。 它可讓您管理與Experience Decisioning相關的許可權。 [閱讀全文](../experience-decisioning/gs-experience-decisioning.md)
* 您現在可以為體驗決策中的指定決策項目新增多個上限規則。 這可讓您提高控制優惠傳送方式的等級。 [閱讀全文](../experience-decisioning/items.md#capping)
* 您現在可以使用建立Experience Decisioning行銷活動的自訂報告控制面板 [!DNL Customer Journey Analytics]. [閱讀全文](../experience-decisioning/cja-reporting.md)


**Offer Decisioning**

* **多規則支援**  — 您現在可以在決定管理中，為指定優惠新增最多10個上限規則。 這可讓您針對活動內容傳送方式提高控制等級。
* **稽核** - **變更記錄** 標籤可讓您檢視對優惠或決定所做的所有變更已移除。 與優惠和決定相關的變更現在可以在以下連結檢視：**稽核**&#x200B;選單。


**電子郵件頻道**

* **清單 — 取消訂閱**  — 繼大量寄件者的最新Gmail和Yahoo公告後，Journey Optimizer支援「post/1-click」清單取消訂閱選項。
* **垃圾郵件評分**  — 您現在可以在專用的垃圾郵件報告中檢查您的內容垃圾郵件評分。 使用SpamAssassin，Adobe Journey Optimizer現在可以測試您的電子郵件內容，並賦予分數以指出ISP提供者是否將其視為垃圾郵件。 [閱讀全文](../content-management/spam-report.md)


**對象**

* 現在可搭配Healthcare Shield或Privacy and Security Shield使用受眾構成和自訂上傳（CSV檔案）的受眾和屬性。

**個人化**

* **查詢表**  — 現在，當使用物件陣列內的屬性定義關聯性時，您可以運用查詢資料集中的資料。 查閱值將在歷程（條件、自訂動作等）中使用 和訊息個人化。
* **運算式片段**  — 運算式片段現在可用於應用程式內頻道。

**歷程**

* **合併原則**  — 您現在可以設定合併原則，並在歷程中使用。
* **mTLS支援** - Journey Optimizer API和自訂動作現在支援mTLS通訊協定。
