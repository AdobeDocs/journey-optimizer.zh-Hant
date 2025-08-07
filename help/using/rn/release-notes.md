---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: a53e94f0199cda211d32be55c8e9a52303dc3d25
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 35%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="有哪幾種新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會整合到每月最後一週的發行說明一起發表。[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。


## 行銷活動協調

**推出日期**：2025年8月4日

Journey Optimizer現在包含&#x200B;**Campaign Orchestration**，這是專為品牌啟動的批次行銷活動而建置的新功能。 此發行版本推出行銷活動協調畫布和增強型資料模型，共同讓行銷人員規劃、鎖定目標及提供個人化的跨頻道行銷活動。

![行銷活動協調流程GIF](assets/do-not-localize/release.gif)

它包含[關聯式結構描述和資料集](#oc-relational)和[行銷活動畫布](#oc-canvas)。 這兩項創新加在一起，在Journey Optimizer中開啟了協調批次行銷活動的新標準。 主要功能列於下方。

### 主要功能 {#oc-capabilities}

* **多步驟工作流程**

  使用專門建置的全新行銷活動協調畫布，推動複雜的多通道批次行銷活動。

* **隨選對象**

  隨選區隔對象以立即啟用。

* **多實體分段**

  使用商業內容（非人員維度），例如產品、商店、續約、預留等來建立對象。

* **預先傳送可見度**

  在推出之前和行銷活動執行期間，檢閱、調整及最佳化對象和行銷活動

### 行銷活動畫布 {#oc-canvas}

專為批次行銷活動建置的全新視覺協調介面。 此畫布可啟用：

* 多步驟、多頻道行銷活動流程的視覺化規劃

* 支援從關聯式查詢建立的隨選受眾

* 進階對象分割、等待和條件式邏輯

* 套用商業規則和篩選器後的精確預先傳送計數

### 關聯式結構描述和資料集 {#oc-relational}

Adobe Journey Optimizer現在支援連結至以人物為基礎的設定檔的關聯式實體（例如產品、商店、預訂、合約）。 這允許跨多維度資料結構的細分和個人化，啟用如下的使用案例：

* 每個預訂、訂閱或合約有一則訊息

* 根據相關實體屬性（例如產品類別或商店位置）的分段

* 增強定址能力（例如，傳送給與實體繫結的所有已知連絡人）

### 為什麼這很重要

此版本讓行銷人員可完全控制品牌啟動、受眾型批次行銷，結合彈性的資料模型與特意建置的協調體驗。 它專為即時歷程的批次行銷活動協調而設計，同時提供進階的個人化與擴充性。

### 了解更多

在[Campaign協調流程檔案](../orchestrated/gs-orchestrated-campaigns.md)中瞭解更多。

<!--
## August '25 pre release notes {#25-7-rn}

**Pre release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: August 19, 2025


### New capabilities {#Aug-25-8-features}

New capabilities coming with this release are detailed below.

### Improvements {#Aug-25-8-improv}

Improvements coming with this release are listed below.
-->


## 2025年7月發行說明 {#25-7-rn}

**發行日期**： 2025年7月29日

### 全新功能 {#features-25-7}

此版本隨附的新功能詳述如下。

#### 功能

<table>
<thead>
<tr>
<th><strong>WhatsApp頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在支援直接的WhatsApp傳訊，可順利整合至您的歷程和行銷活動，以改善收件者通訊和參與。 此原生管道提供立即可用的WhatsApp範本整合、訊息預覽、個人化、傳遞報告、Webhook、選擇加入和選擇退出同意管理等功能。</p>
<p>此功能先前在Beta中發行，現在可供所有環境使用（全面發佈）。</p>
<p><img src="../whatsapp/assets/do-not-localize/WA-Animation.gif"/><p>
<p>如需詳細資訊，請參閱<a href="../whatsapp/get-started-whatsapp.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>品牌</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以建立和自訂自己的品牌，以在整個通訊過程中清楚地定義您的視覺和語言識別。透過品牌一致性分數，您可以收到即時回饋，以了解您的內容對您的品牌基調、風格和方針的反映程度，協助您在傳送的每則訊息中始終保持一致的品牌形象。</p>
<p>此功能先前在Beta中發行，現在可供所有環境使用（全面發佈）。</p>
<p><img src="assets/do-not-localize/brand-score.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../content-management/brands.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在電子郵件頻道中使用決策</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將決定原則新增至電子郵件歷程與行銷活動。 決策原則是優惠方案的容器，可運用決策引擎以動態方式傳回最佳內容，供每個受眾成員傳送。</p>
<p>此功能以「有限可用性」提供。 請聯絡您的Adobe代表以取得存取權。</p>
如需詳細資訊，請參閱<a href="../experience-decisioning/create-decision.md">詳細檔案</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>LINE 頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 已擴充其跨頻道功能，以包含對 LINE 頻道的支援。此增強功能可讓您建立、編輯和預覽 LINE 體驗，以啟用更個人化且吸引人的互動。透過 LINE，您可以與更多客戶連絡、傳送相關內容並改善您的參與度。</p>
<p>先前僅開放請求，現在所有使用者均可使用LINE頻道（全面發佈）。</p>
<p>如需詳細資訊，請參閱<a href="../line/get-started-line.md">詳細文件</a>。</p></td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Optimization in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now empowers you with the tools to deliver personalized and optimized content to your campaigns' audience, allowing you to run content experiments, create rule-based targeting, and use advanced combinations of both, to maximize the effectiveness of your campaigns.</p>
<p>With Optimization, you can:</p>
<ul>
<li>Test multiple content variations to identify the most effective messaging.</li>
<li>Deliver personalized content based on user attributes and contextual data.</li>
<li>Combine targeting and experimentation for advanced campaign strategies.</li>
<li>Filter out users that do not match variant criteria.</li>
<li>Ensure fallback mechanisms to maintain user engagement.</li>
</ul>
<P>Once the campaign is live, profiles are evaluated against the defined criteria, and based on matching criteria, they are delivered with the appropriate experience or content from the campaign.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->



<table>
<thead>
<tr>
<th><strong>歷程練習</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程試運行是 Adobe Journey Optimizer 中的特殊歷程發佈模式，允許歷程從業人員使用真實的生產資料，即可測試歷程，不用聯絡實際客戶，或是更新設定檔資訊。此功能可協助歷程從業人員，針對歷程設計、客群目標市場選擇，累積信心，然後再將歷程發佈上線。</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>之前以「限量」的名義發行，目前此功能所有環境都適用（一般可用性）。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-dry-run.md">詳細檔案</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>歷程的補充ID</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>目前您可以使用輪廓 ID 和其他識別碼（例如訂購 ID、訂閱 ID 或處方 ID）來觸發歷程，即可允許同一設定檔同時出現在同一歷程中許多次。這能啟用某些情境，同時管理許多訂單或訂閱，每個執行個體還會依循自己的歷程路徑操作。</p>
<p>以前在「有限可用性」中發佈，現在所有環境都可以在歷程中使用補充ID。 在此「一般可用性」版本中，功能現在包含對「讀取對象」歷程的支援。</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/supplemental-identifier.md">詳細檔案</a></p>
</td>
</tr>
</tbody>
</table>

### 產品內警示

您現在可以訂閱Journey Optimizer產品發行的&#x200B;**電子郵件和產品內通知**。

要訂閱：

* 瀏覽至&#x200B;**Adobe Experience Cloud偏好設定**
* 在&#x200B;**通知**&#x200B;下，尋找&#x200B;**Journey Optimizer新發行版本**
* 啟用應用程式內通知和電子郵件通知

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}


### 歷程條件的變更 {#ee-change@}

自 7 月 8 日開始，在新的客戶組織中，歷程條件中使用的運算式編輯器不再支援使用體驗事件來建立運算式。因此，[Experience Platform 資料來源](../datasource/adobe-experience-platform-data-source.md)中的體驗事件無法用於建立運算式。使用體驗事件建立運算式/邏輯的替代方法和最佳做法可參考[這裡](../building-journeys/exp-event-lookup.md)。

在單一歷程中存取歷程內容事件資料的方式不會變更。在運算式和個人化編輯器中，使用者可以繼續存取透過初始歷程事件傳入的資料。

在[本常見問題集](../building-journeys/exp-event-lookup.md#faq-ee)中深入瞭解。

### 改良功能 {#25-7-improv}

以下列舉部分發布內容附上的改良功能。

* **行銷活動**

   * **行銷活動中有多個傳入動作** — 為簡化行銷活動協調，您現在可以在單一行銷活動中定義數個傳入動作。 此功能可讓您同時向不同位置提供多個程式碼型體驗、應用程式內訊息、內容卡片或網頁動作，每個動作都包含特定內容。
  <!-- [Read more](../FILE.md) -->

   * **行銷活動詳細目錄重組** — 排程和API觸發的行銷活動現在分割為行銷活動詳細目錄中的個別索引標籤，以便更輕鬆導覽和管理。

[閱讀全文](../campaigns/modify-stop-campaign.md)

* **資料管理**
   * **決定管理系統資料集更新** — 已刪除的個人化和遞補優惠現在在「decision_object_repository_personalized_offers」和「decision_object_repository_fallback_offers」資料集中標示為已封存。 資料集中的現有記錄不會變更。

[閱讀全文](../offers/export-catalog/access-dataset.md)

* **歷程**
   * **歷程沙箱工具增強功能** — 使用封裝匯出和匯入功能，跨多個沙箱複製歷程時，現在也可使用下列功能：
      * 選取目的地上的現有事件
      * 在歷程之外獨立複製事件
      * 正在偵測欄位群組/資料來源關係，如果它們存在，則在目的地連結至它們，如果不存在，則建立它們。

[閱讀全文](../configuration/copy-objects-to-sandbox.md)

* **頻道 — 應用程式內**
   * **應用程式內索引鍵/值配對** — 使用應用程式內訊息，您可以定義索引鍵和值配對，以在訊息裝載中包含自訂變數。 這些機碼值組可讓您根據特定設定和使用案例傳遞其他資料。 [閱讀全文](../in-app/design-in-app.md)

* **頻道 — 內容卡**

   * **規則型行銷活動取消資格** — 編輯其他傳遞規則時，先前的「傳遞規則」選項已取代為三種不同的規則型別，以便更妥善地控制訊息時間與可見度：
      * 顯示訊息條件：決定何時顯示內容卡的條件。
      * 關閉訊息，如果：暫時隱藏內容卡的條件。 如果再次符合顯示條件，則可重新顯示縮圖。
      * 符合以下條件時取消訊息資格：永久阻止內容卡再次顯示的條件。

[閱讀全文](../content-card/design-content-card.md)

* **決策**
   * **移轉工具API** - Journey Optimizer團隊目前正在處理移轉工具API，以將決定管理實體移轉至決定。 此工具可讓您在沙箱之間無縫移轉，並具備相依性解析和復原功能。 如有興趣，請洽詢您的Adobe代表。

* **個人化**
   * 新的協助程式功能「SHA256」已新增至個人化編輯器。 此函式用於計算及傳回字串的sha256雜湊。

[閱讀全文](../personalization/functions/string.md#sha256)
