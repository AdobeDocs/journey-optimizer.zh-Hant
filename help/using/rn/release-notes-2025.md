---
solution: Journey Optimizer
product: journey optimizer
title: 2025 年發行說明
description: Journey Optimizer 2025 年發行說明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: aa8c74de-748b-4947-a972-14703f6ab4a7
source-git-commit: 14758fa4db49aed686c1554718337983d3812595
workflow-type: tm+mt
source-wordcount: '5035'
ht-degree: 99%

---

# 發行說明 2025 年 {#release-notes-2025}

此頁面列出了於 2025 年發行的 [!DNL Journey Optimizer] 所有功能和改進項目。

## 2025 年 7 月發行說明 {#25-7-rn}

**發行日期**：2025 年 7 月 29 日

### 全新功能 {#features-25-7}

此版本隨附的新功能詳述如下。

#### 功能

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
<p>之前以 Beta 版本發行，目前此功能所有環境都適用 (一般可用性)。</p>
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
<p>您現在可以將決定原則新增至電子郵件歷程與行銷活動。決策原則是優惠方案的容器，可運用決策引擎以動態方式傳回最佳內容，傳送給每個對象成員。</p>
<p>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。</p>
如需詳細資訊，請參閱<a href="../experience-decisioning/create-decision.md">詳細文件</a></p>
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
<p>先前僅開放請求，現在所有使用者均可使用 LINE 頻道 (一般可用性)。</p>
<p>如需詳細資訊，請參閱<a href="../../rp_landing_pages/line-landing-page.md">詳細文件</a>。</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程試運行</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程試運行是 Adobe Journey Optimizer 中的特殊歷程發佈模式，允許歷程從業人員使用真實的生產資料，即可測試歷程，不用聯絡實際客戶，或是更新設定檔資訊。此功能可協助歷程從業人員，針對歷程設計、客群目標市場選擇，累積信心，然後再將歷程發佈上線。</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-dry-run.md">詳細文件</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>歷程的補充識別碼</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>目前您可以使用輪廓 ID 和其他識別碼（例如訂購 ID、訂閱 ID 或處方 ID）來觸發歷程，即可允許同一設定檔同時出現在同一歷程中許多次。這能啟用某些情境，同時管理許多訂單或訂閱，每個執行個體還會依循自己的歷程路徑操作。</p>
<p>之前以「限量」的名義發行，現在所有環境都可以在歷程中使用補充識別碼。在此「一般可用性」版本中，功能現在包含對「讀取對象」歷程的支援。</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/supplemental-identifier.md">詳細文件</a></p>
</td>
</tr>
</tbody>
</table>

### 產品內警報

您現在可以訂閱 Journey Optimizer 產品發行的&#x200B;**電子郵件和產品內警報**。

若要訂閱：

* 瀏覽至 **Adobe Experience Cloud 偏好設定**。
* 在&#x200B;**通知**&#x200B;下，尋找 **Journey Optimizer 新發行版本**
* 啟用應用程式內通知和電子郵件通知

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}


### 歷程條件的變更 {#ee-change@}

自 7 月 8 日開始，在新的客戶組織中，歷程條件中使用的運算式編輯器不再支援使用體驗事件來建立運算式。因此，[Experience Platform 資料來源](../datasource/adobe-experience-platform-data-source.md)中的體驗事件無法用於建立運算式。使用體驗事件建立運算式/邏輯的替代方法和最佳做法可參考[這裡](../building-journeys/exp-event-lookup.md)。

在單一歷程中存取歷程內容事件資料的方式不會變更。在運算式和個人化編輯器中，使用者可以繼續存取透過初始歷程事件傳入的資料。

在[本常見問題集](../building-journeys/exp-event-lookup.md#faq-ee)中深入瞭解。

### 改良功能 {#25-7-improv}

以下列舉部分發布內容附上的改良功能。

* **行銷活動**

   * **行銷活動中有多個傳入動作** — 為簡化行銷活動協調，您現在可以在單一行銷活動中定義數個傳入動作。此功能可讓您同時向不同位置提供多個程式碼型體驗、應用程式內訊息、內容卡或網頁動作，每個動作都包含特定內容。
     [閱讀全文](../campaigns/campaign-action.md#multi-action)

   * **行銷活動詳細目錄重組** — 排程和 API 觸發的行銷活動現在分割為行銷活動詳細目錄中的個別索引標籤，以便更輕鬆導覽和管理。

[閱讀全文](../campaigns/manage-campaigns.md)

* **資料管理**
   * **決策管理系統資料集更新** — 已刪除的個人化和遞補優惠現在在「decision_object_repository_personalized_offers」和「decision_object_repository_fallback_offers」資料集中標示為已封存。資料集中的現有記錄不會變更。

[閱讀全文](../offers/export-catalog/access-dataset.md)

* **歷程**
   * **歷程沙箱工具增強功能** — 使用封裝匯出和匯入功能，跨多個沙箱複製歷程時，現在也可使用下列功能：
      * 選取目標上的現有事件
      * 複製獨立於歷程之外的事件
      * 偵測欄位群組/資料來源關係，如果它們存在，則在目標連結至它們，如果不存在，則建立它們。

[閱讀全文](../configuration/copy-objects-to-sandbox.md)

* **頻道 — 應用程式內**
   * **應用程式內金鑰/值配對** — 使用應用程式內訊息，您可以定義金鑰和值配對，以在訊息承載中包含自訂變數。這些金鑰-值配對可讓您根據特定設定和使用案例傳遞其他資料。[閱讀全文](../in-app/design-in-app.md)

* **頻道 — 內容卡**

   * **規則型行銷活動取消資格** — 編輯其他傳遞規則時，先前的「傳遞規則」選項已取代為三種不同的規則類型，以便更妥善地控制訊息時間與可見度：
      * 顯示訊息條件：決定何時顯示內容卡的條件。
      * 關閉訊息條件：暫時隱藏內容卡的條件。如果再次符合顯示條件，則可重新顯示。
      * 取消訊息資格條件：永久阻止內容卡再次顯示的條件。

[閱讀全文](../content-card/design-content-card.md)

* **決策**
   * **移轉工具 API** — Journey Optimizer 團隊目前正在處理移轉工具 API，以將決策管理實體移轉至決策。此工具可讓您在沙箱之間無縫移轉，並具備相依性解析和復原功能。如有興趣，請聯絡您的 Adobe 代表。

* **個人化**
   * 個人化編輯器已新增新協助程式函數「SHA256」。此函數用於計算及傳回字串的 sha256 雜湊。

[閱讀全文](../personalization/functions/string.md#sha256)


## 2025 年 6 月發行說明 {#25-6-rn}

**發行日期**：2025 年 6 月 18 日

### 全新功能 {#25-06-features}

此版本隨附的新功能詳述如下。

<table>
<thead>
<tr>
<th><strong>決策中的 Adobe Experience Platform 資料集 (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>先前可用於個人化的 Adobe Experience Platform 資料集現在可用於決策。這可讓您將決策屬性的定義擴充至資料集中的其他資料，以便進行定期變更的大量更新，而無需一次手動更新一個屬性。例如，可用性、等待時間等。</p>
<p>所有客戶都可在公開測試版中，使用此功能。如果您想要存取權，請聯絡您的客戶代表。</p>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/aep-data-exd.md">詳細文件</a>。</p>
<p>推出日期：2025 年 6 月 20 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>RCS 傳送訊息</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以透過第三方提供者透過與自訂SMS提供者解決方案整合來設定、自訂及傳遞Rich Communication Services (RCS)訊息。</p>
<p>如需詳細資訊，請參閱<a href="../sms/sms-configuration-custom.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>程式碼型體驗內容中的表單欄位</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您可以立即到 JSON 或 HTML 內容範本中，定義特定可編輯欄位，即便不是技術使用者，也能輕鬆地在製作程式碼型體驗頻道上的表單檢視中編輯內容，不用要操作任何程式碼。<br />此外，當定義程式碼型體驗內容範本時，目前可以在範本中插入決定原則，增加可重複使用性，方便使用。</p>
<img src="assets/do-not-localize/form-fields.gif">
<p>如需詳細資訊，請參閱<a href="../code-based/code-based-form-fields.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Custom delegation method for subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking messages.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>歷程中的內容決策活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您目前可以透過歷程畫布中的專用內容決策活動，將個人化優惠方案納入歷程中，然後在歷程活動，包括條件和自訂動作中使用。</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>此功能僅適用於一組組織 (有限可用性)，將透過未來版本在全球推出。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/content-decision.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程試運行</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程試運行是 Adobe Journey Optimizer 中的特殊歷程發佈模式，允許歷程從業人員使用真實的生產資料，即可測試歷程，不用聯絡實際客戶，或是更新設定檔資訊。此功能可協助歷程從業人員，針對歷程設計、客群目標市場選擇，累積信心，然後再將歷程發佈上線。</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>此功能僅適用於一組組織 (有限可用性)，將透過未來版本在全球推出。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-dry-run.md">詳細文件</a>。</p>

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>暫停並繼續歷程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您立即可以暫停，繼續歷程。在不中斷客戶體驗的情況下，此功能可讓歷程從業人員暫時暫停即時歷程，藉此提供更大控制力，帶來更多彈性。 暫停時，系統就不會傳送任何通訊，設定檔會維持在暫停狀態，直到繼續歷程為止。</p>
<p>您只能暫停並繼續單一歷程，或可執行大量暫停，然後繼續另一組歷程操作。</p>
<p>此外，您還可以將全域篩選器套用至已暫停歷程，即可根據屬性排除設定檔。</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>此功能僅適用於一組組織 (有限可用性)，將透過未來版本在全球推出。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-pause.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>提高實驗勝率</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>擴大實驗獲勝者的規模，讓您能夠透過自動或手動方式，將實驗的獲勝變化版本推廣給所有客群參考。此功能可確保一旦確定高績效人才，您就可以大幅提高影響力和效率，不必再不斷進行人工監督。</p>
<p>如需詳細資訊，請參閱<a href="../content-management/content-experiment.md">詳細文件</a>。</p>
<p>推出日期：2025 年 6 月 2 日</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>衝突與優先順序</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>請在 Journey Optimizer 中，管理行銷活動和歷程流量和時間非常重要，才能避免過多的互動，給客戶帶來負擔。Journey Optimizer 目前有提供幾種可用於衝突管理和優先排序的工具，以前只適用於有限存取 (LA) 組織 - 現已普遍開放使用 (GA)。</p>
<p>此功能之前以 [限量] 的名義發行，目前所有環境都可以使用。 已在此一般可用性版本中，引進以下增強功能：</p>
<ul>
<li>擴展支援：除了閱讀受眾歷程之外，衝突管理工具目前還有支援單一歷程和受眾資格歷程。</li>
<li>改善的疑難排解：查詢服務中目前有提供兩種新的步驟事件欄位，讓您能分析設定檔遭到歷程或行銷活動拒絕的原因。</li>
<li>增強報告：報告目前可以指定哪些特定規則會將設定檔排除在歷程，或是行銷活動之外，提供更高透明度和可操作的洞察力。</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>如需詳細資訊，請參閱<a href="../conflict-prioritization/gs-conflict-prioritization.md">詳細文件</a>。</p>
<p>推出日期：2025 年 6 月 3 日</p>
</td>
</tr>
</tbody>
</table>

### 改良功能 {#25-06-improv}

以下列舉部分發布內容附上的改良功能。

* **頻道規則集**

   * 上限專用&#x200B;**自訂持續時間視窗** - 頻道規則集設定畫面中目前有提供新的&#x200B;**間隔**&#x200B;欄位，讓您可以根據指定持續時間，選擇數天、數週或數月內套用頻率上限規則。

   * **每小時重設上限頻率** - 您目前可以將每小時上限套用至頻道規則集。此功能僅適用於一組組織 (有限可用性)。 請聯絡您的客戶服務以啟用這項功能。

   * **每日持續時間** - 先前在「有限可用性」中提供，現在所有客戶都可以使用頻道規則集中的「每日」頻率上限。

  如需詳細資訊，請參閱[詳細文件](../conflict-prioritization/channel-capping.md)。

* **程式碼型體驗**

   * 現在可在程式碼型體驗內容範本中新增決策原則，以便用於利用可編輯表單欄位中的優惠方案。[閱讀全文](../code-based/code-based-form-fields.md)

   * 只要到程式碼型體驗歷程，或透過行銷活動版本畫面，就可以立即直接新增決策原則，不用開啟個人化編輯器。[閱讀全文](../code-based/create-code-based.md#edit-code)

* **電子郵件設計工具的自訂 CSS 支援**

  Journey Optimizer 目前可讓您直接在電子郵件設計工具中，將自訂 CSS 新增至電子郵件內容。[閱讀全文](../email/custom-css.md)

* **新的行銷活動索引標籤式導覽**

  新的導覽模式讓您可以更快速地存取內容製作，能在行銷活動中，支援進一步擴充設定。[閱讀全文](../campaigns/create-campaign.md)

* **決策**

   * **沙箱複製和決策** (推出日期：2025 年 6 月 3 日) - 決策物件現在可以在沙箱之間複製，以便簡化測試，同時部署工作流程。[閱讀全文](../configuration/copy-objects-to-sandbox.md#decisioning)

   * **決策規則的決策項目屬性支援** (推出日期：2025 年 6 月 4 日) * 您現在可以運用決策項目屬性來建立決策規則。[閱讀全文](../experience-decisioning/rules.md#create)

* **互動式訊息執行 API 更新** — 推出日期：2025 年 6 月 6 日

  互動式訊息執行 API 讓您可以立即刪除即將執行的行銷活動排程。[閱讀全文](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}


## 2025 年 5 月發行說明 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### 全新功能 {#25-05-features}

此版本隨附的新功能詳述如下。

<table>
<thead>
<tr>
<th><strong>行銷活動和歷程庫存的行事曆視圖</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程和行銷活動清單中，目前只有提供行事曆視圖。 行事曆視圖讓您可以透過視覺化方式，呈現個別清單中的所有歷程，同時啟用行銷活動。</p>
<p>目前此變更只限開放給部分組織使用 (有限可用性)。若想請求存取權，請使用<a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">這份表單</a>。</p>
<img src="assets/do-not-localize/calendar.gif">
<p>如需詳細資訊，請參閱下列區段：<a href="../building-journeys/journey-ui.md">瀏覽並篩選您的歷程</a>、<a href="../campaigns/manage-campaigns.md">存取行銷活動</a>。</p>
<p>推出日期：2025 年 5 月 28 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager 內容片段整合</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過整合 Adobe Experience Manager 與 Adobe Journey Optimizer，您就可以立即在 Journey Optimizer 內容中，輕鬆使用 Adobe Experience Manager 內容片段。 這種順暢連線讓您能更輕鬆地直接在 Journey Optimizer 中存取，同時使用 AEM 內容。</p>
<p>此功能之前可用於一系列有限公司組織 (LA)，目前改為 GA，同時具備以下增強功能：您目前可以使用編輯器模式，定義片段簽名中的預留位置、對應個人化值。</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>如需詳細資訊，請參閱<a href="../integrations/aem-fragments.md">詳細文件</a>。</p>
<p>推出日期：2025 年 5 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager 動態媒體整合</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dynamic Media 資產現在可直接在 Journey Optimizer 中使用和存取。此整合可讓您：</p>
<ul>
<li>透過即時更新，集中一處管理資產</li>
<li>立即修改資產設定，例如長寬的數字</li>
<li>更新內容並新增個人化欄位，以便自訂動態媒體範本。</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>之前以「限量」的名義發行，目前此功能所有環境都適用 (一般可用性)。</p>
<p>如需詳細資訊，請參閱<a href="../integrations/aem-dynamic.md">詳細文件</a>。</p>
<p>推出日期：2025 年 5 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>事件觸發歷程的補充識別碼</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>目前您可以使用輪廓 ID 和其他識別碼（例如訂購 ID、訂閱 ID 或處方 ID）來觸發歷程，即可允許同一設定檔同時出現在同一歷程中許多次。這能啟用某些情境，同時管理許多訂單或訂閱，每個執行個體還會依循自己的歷程路徑操作。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/supplemental-identifier.md">詳細文件</a>。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>推出日期：2025 年 5 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>模擬內容變化版本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>此功能之前以 [限量] 的名義發行，目前所有環境都可以使用。 在 [一般可用性] 發行版本中，此功能現在包含對多語言內容和內容實驗的支援，讓您能夠測試不同語言和處理方式的變化。 此外，目前有支援內容屬性（除了設定檔屬性外），以便允許進行更多動態和情境式內容測試。</p>
<img src="assets/do-not-localize/variants.gif">
<p>如需詳細資訊，請參閱<a href="../test-approve/simulate-sample-input.md">詳細文件</a>。</p>
<p>推出日期：2025 年 5 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>將讀取客群排程與批次分段工作同步處理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>完成批次分段後，就可以立即觸發日常歷程執行目前所有客戶都可以在每日排程的歷程中，使用此選項。 此選項可讓您定義的時間視窗長達 6 小時之久，等待批次分段作業的客群資料，確保使用到最新資料，執行歷程。或者如果還未準備好，就可以直接跳過。</p>
<p>之前以「限量」的名義發行，目前此功能所有環境都適用 (一般可用性)。</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>如需詳細資訊，請參閱<a href="../building-journeys/read-audience.md#schedule">詳細文件</a>。</p>
<p>推出日期：2025 年 5 月 20 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自訂簡訊提供者</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 目前可讓您在預設選項之外，設定以下其他 SMS 提供者：Sinch、Infobip 和 Twilio。 透過自訂 SMS 提供者設定，您就可以直接整合第三方提供者，運用動態訊息的進階來承載自訂，同時管理同意偏好設定（選擇加入/選擇退出），以便確保有遵守法規遵循規範。</p>
<p>如需詳細資訊，請參閱<a href="../sms/sms-configuration-custom.md">詳細文件</a>。</p>
<p>之前以「限量」的名義發行，目前此功能所有環境都適用 (一般可用性)。</p>
<p>推出日期：2025 年 5 月 20 日</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件設計工具中的主題</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>目前您可以快速套用事先審核通過的主題，以便確保所有電子郵件的品牌都有保持一致性，加快投放行銷活動的流程，個別製作高品質的電子郵件，同時減少對設計團隊的依賴。</p>
<p>此功能目前為 Beta 版本，僅供 Beta 版客戶使用。若要加入 Beta 版計畫，請聯絡 Adobe 代表。</p>
<img src="assets/do-not-localize/themes.gif">
<p>如需詳細資訊，請參閱<a href="../email/apply-email-themes.md">詳細文件</a>。</p>
<p>推出日期：2025 年 5 月 14 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>決策 — 全新 AI 公式產生器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您可以馬上從改善的新介面，定義並結合條件，以便建立特定決策排名公式。 您可以定義自訂排名公式，這類公式會透過引導式介面，結合 AI 模型分數、優惠方案優先順序、設定檔屬性、優惠方案屬性和內容訊號，不會只單純仰賴靜態優惠方案的優先順序。</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/ranking/ranking-formulas.md">詳細文件</a>。</p>
<p>推出日期：2025 年 5 月 14 日</p>
</td>
</tr>
</tbody>
</table>

### 改良功能 {#25-05-improv}

以下列舉部分發布內容附上的改良功能。


* **沙箱副本的全新行銷活動物件支援** — 推出日期：2025 年 5 月 15 日

  當使用套件匯出和匯入功能跨眾多沙箱複製活動時，也會立即複製以下相依性：頻道設定、實驗變體和設定、決策策略和項目。[閱讀全文](../configuration/copy-objects-to-sandbox.md)

* **登陸頁面的資料夾** — 推出日期：2025 年 5 月 9 日

  為了輕鬆管理登陸頁面，您可以立即使用資料夾，便可更有效地將資料夾整理成精簡的階層。[閱讀全文](../landing-pages/manage-lp.md)

* **直接郵件：SFTP 連線的 SSH 金鑰支援** — 推出日期：2025 年 5 月 5 日

  除了具有密碼驗證型別的現有 SFTP 之外，還可在直接郵件檔案路由設定中，立即將直接郵件檔案匯出至具有 SSH 金鑰驗證的 SFTP 伺服器。 [閱讀全文](../direct-mail/direct-mail-configuration.md)

* **啟用 [膠囊狀] 按鈕來執行個人化** — 推出日期：2025 年 5 月 5 日

  個人化編輯器已新增新的 [膠囊狀] 按鈕。啟用時，設定檔和內容屬性都會以 [膠囊狀] 按鈕形式顯示，增強驗證碼的可讀性。[閱讀全文](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >在接下來 30 天內，會將此功能逐步推廣到合適環境。

* **網頁管道**&#x200B;中的 [重新導向至 URL] 支援 — 推出日期：2025 年 5 月 20 日

  Journey Optimizer 網頁管道目前可讓您將訪客重新導向至其他現有網址，而不是重新導向視覺化編輯器中製作的新變化版本。 此功能可用來執行比較兩種截然不同頁面的實驗，而不只是用來更改頁面中的少數元素。 [閱讀全文](../web/create-web.md#web-redirect-to-url)

* **範本和片段的資料夾** — 推出日期：2025 年 5 月 20 日

  資料夾讓您可以更輕鬆有效地將內容範本、片段整理成結構化的階層。以前可供一組組織 (LA) 使用的資料夾，現在可供所有使用者 (GA) 管理其內容範本和片段。 請到[內容範本](../content-management/access-content-templates.md#folders)和[片段](../content-management/manage-fragments.md#folders)專區，閱讀更多內容。

* **電子郵件範本中的點擊追蹤** — 推出日期：2025 年 5 月 20 日

  請在以下位置點擊追蹤：`<area>`位於電子郵件內容中影像地圖內的元素，目前有提供原生支援[!DNL Journey Optimizer]。 這是為了確保影像地圖區域收到與標準超連結相同的追蹤包裝、追蹤資料和附加參數。[深入了解訊息追蹤](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **行銷活動清單中的右側邊欄** — 推出日期：2025 年 5 月 20 日

  現在，在行銷活動清單中，選取行銷活動會開啟窗格並顯示其詳細資訊。

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.-->

<!--* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->



## 2025 年 4 月發行說明 {#25-4-rn}

**發布內容日期**：2025 年 4 月 29-30 日

### 全新功能 {#25-04-features}

此發布內容版本隨附的新功能，會詳述如下。

<table>
<thead>
<tr>
<th><strong>個人化編輯器：透過實踐學習</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>目前有提供個人化遊樂場，您可以在裡面實驗個人化運算式。這讓您可以探索範例範本和裝載，以便協助您開始使用，可以自己試用看看個人化運算式。</p>
<p>如需詳細資訊，請參閱<a href="../personalization/personalize.md#playground">詳細文件</a>。</p>
<p>推出日期： 2025 年 4 月 24 日</p>
<img src="assets/do-not-localize/templating-playground.gif"/>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Adobe Experience Manager as a Cloud Service integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The integration between Adobe Journey Optimizer and Adobe Experience Manager as a Cloud Service is now released in General Availability (GA). This integration enables seamless content sourcing and management for personalized customer journeys.</p>
<p>For more information, refer to the <a href="../integrations/aem-templates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>Simulate content variations (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>With the General Availability release, the feature now includes support for multilingual content and content experiments, enabling you to test variations across different languages and treatments. Additionally, it now supports contextual attributes (in addition to profile attributes), allowing for even more dynamic and situational content testing.</p>
<img src="assets/do-not-localize/variants.gif">
</td>
</tr>
</tbody>
</table>-->

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
<p>客戶可按請求，啟用 Adobe Journey Optimizer 的 LINE 頻道。請聯絡 Adobe 客戶服務，或是您的 Adobe 代表，為貴組織啟用這項功能。</p>
<p>如需詳細資訊，請參閱<a href="../../rp_landing_pages/line-landing-page.md">詳細文件</a>。</p></td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Custom SMS provider (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports custom SMS providers, allowing you to integrate your preferred SMS services for enhanced communication flexibility.</p>
<p>For more information, refer to the <a href="../sms/sms-configuration-custom.md">detailed documentation</a>.</p></td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>歷程量度</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程量度現已推出，可讓您衡量您的活動對業務關鍵指標的影響，並針對您的績效提供更清楚的深入分析。</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
<p>如需詳細資訊，請參閱<a href="../building-journeys/success-metrics.md">詳細文件</a>。</p>
<p>推出日期： 2025 年 4 月 9 日</p>
</td>
</tr>
</tbody>
</table>



<!--<table>
<thead>
<tr>
<th><strong>Calendar view for campaign and journey inventory (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new calendar view is now available for campaigns and journey activations. This feature provides a visual representation of scheduled activities, allowing you to view and manage your campaigns and journeys more effectively. Selecting a calendar item opens a right rail with detailed information. This feature is currently in Limited Availability.</p>
<img src="assets/do-not-localize/calendar.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Adobe Express 整合 (可用性限制)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 目前可以整合入 Adobe Express，讓您可以透過歷程協調，順利連上創意資產。此整合能簡化跨行銷活動設計、部署個人化內容的程序。 </p>
<p>此整合目前不適用於 Healthcare Shield 或 Privacy 和 Security Shield。</p>
<img src="assets/do-not-localize/express_resize.gif">
<p>如需詳細資訊，請參閱<a href="../integrations/express.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>批次分段完成後，就會觸發每日歷程執行 (可用性限制)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>針對每日既定行程，新增選項可讓您定義的時間視窗長達 6 小時之久，等待批次分段作業的受眾資料，確保使用到最新資料來執行歷程，或者如果尚未準備好，就會直接跳過。[批次客群評估後就會觸發] 選項僅適用於一組組織 (可用性限制)。若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/read-audience.md#schedule">詳細文件</a>。</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Themes in the Email Designer (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply pre-approved styling themes to your email content to ensure brand consistency across all emails, speed up your campaign creation process and independently produce hight-quality emails while reducing dependency on design teams.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>品牌聯名分數 (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>品牌聯名分數功能可直接在電子郵件設計工具中，提供清晰的意見回饋，協助您了解內容是否符合品牌的語氣、樣式和方針。Beta 提供此功能。</p>
<p>如需詳細資訊，請參閱<a href="../content-management/brands-score.md">詳細說明文件</a>。</p>
<img src="assets/do-not-localize/brand-score.gif">
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decisioning - New AI formula builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create specific Decisioning ranking formulas by defining and combining criteria from a new improved interface. Ranking formulas allow you to define rules that will determine which decision items should be presented first, rather than taking into account the priority scores.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table>
-->

### 改良功能 {#25-04-improv}

**行銷活動預覽 API**

除了現有的校訂傳送功能外，新的 API 也可預覽行銷活動。[閱讀全文](https://developer.adobe.com/journey-optimizer-apis/references/simulations/#operation/createCampaignPreview){target="_blank"}。

**沙箱工具**

* **自訂動作的沙箱工具**

  自訂動作目前已加入在 Adobe Journey Optimizer 物件清單中，可以使用沙箱工具功能複製，以便簡化測試和部署。[閱讀全文](../configuration/copy-objects-to-sandbox.md)

* **行銷活動適用的沙箱工具** — 推出日期： 2025 年 4 月 3 日

  您現在可以使用套件匯出和匯入功能，跨多個沙箱複製行銷活動。 行銷活動會連同與輪廓、對象、結構描述、內嵌訊息以及從屬物件相關的所有項目一起複製。 有些項目不會複製，例如決定項目、資料使用標籤及語言設定。 [閱讀全文](../configuration/copy-objects-to-sandbox.md#custom-actions)

**個人化**

* **新的內容屬性**

  新的內容屬性、**訊息設定檔識別碼**&#x200B;目前都可以從個人化編輯器那邊選取。這是訊息導向屬性，唯一標識出的每條訊息，都會傳送到交付中的每個目標設定檔。例如，此唯一識別碼可用作網址追蹤參數，以便區分收件者開啟或點選的每個連結。

* **請在屬性窗格中填入屬性** — 使用日期：2025 年 4 月 2 日

  個人化編輯器的屬性窗格，現在預設僅顯示已填入的屬性。 若要檢視所有屬性，請使用設定按鈕來關閉&#x200B;**[!UICONTROL 僅顯示填入的屬性]**&#x200B;選項。 [閱讀全文](../personalization/personalization-build-expressions.md)

**電子郵件頻道**

* **個人化網址追蹤** — 推出日期： 2025 年 4 月 30 日

  為了提高彈性和對電子郵件設定之控制力，您目前可以到電子郵件頻道設定層級那邊，一次將所有網址追蹤參數最佳化，不必到電子郵件設計工具，專為內容中的每個連結，執行以上操作。[閱讀全文](../email/surface-personalization.md#personalize-url-tracking)

* **電子郵件設計工具** — 推出日期： 2025 年 4 月 1 日

  為了增強 Journey Optimizer 協助工具，電子郵件設計工具現在提供兩個新欄位：它們對應至電子郵件內容 `<html>` 元素中的 `<title>` 元素和 `lang` 屬性。 除了電子郵件&#x200B;**[!UICONTROL 內文]**&#x200B;區段的&#x200B;**[!UICONTROL 預覽文字]**&#x200B;欄位外，您還可以定義這些設定。 [閱讀全文](../email/email-metadata.md)

**使用案例教戰手冊**

* **教戰手冊製作與分享 (Private beta)** - 您可以立即建立、管理並分享自己的使用案例教戰手冊。此功能目前僅作為 Private Beta 使用，可提供給某些組織參考。若想取得存取權，請聯絡 Adobe 代表。[閱讀全文](../start/playbooks.md)

**導覽**

* **內容管理** — 推出日期： 2025 年 4 月 2 日

  為了輕鬆管理您的內容範本與片段，您現在可以使用資料夾將其更有效地整理至結構化階層之中。請在[內容範本](../content-management/access-content-templates.md#folders)和[片段](../content-management/manage-fragments.md#folders)一節瞭解更多資訊。

  >[!AVAILABILITY]
  >
  >此改善功能僅適用於一組組織 (有限可用性)。

<!--- **Folders for content templates and fragments** - Availability date: May 5, 2025

  Previously available for a set of organizations (LA), folders are now available to all users (GA) to manage their content templates and fragments. Folders let you organize your content templates and fragments more easily and effectively into a structured hierarchy.



<!--- **Right rail in campaigns list**  

  A right rail has been added to the campaigns list, providing detailed information when a campaign is selected.-->

<!--**Playbooks**

- **Create your own playbooks (Beta)**
  
  You can now create your own playbooks in Adobe Journey Optimizer, enabling greater customization and flexibility in journey planning.-->



## 2025 年 3 月發行說明 {#25-3-rn}

### 全新功能 {#25-03-features}

此版本隨附的新功能詳述如下。

<!--table>
<thead>
<tr>
<th><strong>Integration with Adobe Express (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Adobe Express integration in Adobe Journey Optimizer lets you use Adobe Express's editing tools directly during content creation, enabling you to resize, remove backgrounds, crop, and convert assets to JPEG or PNG.<p>
<p>Adobe Express integration in Adobe Journey Optimizer is currently only available for a set of organizations (Limited Availability). It cannot be deployed for use with Healthcare Shield or Privacy and Security Shield.</p>
<p>For more information, refer to the <a href="../integrations/express.md">detailed documentation</a>.</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Journey metrics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey metrics are now available, allowing you to measure the impact of your activities across the key metrics of your business and to provide clearer insights into your performance.</p>
<p>For more information, refer to the <a href="../building-journeys/success-metrics.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table-->

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
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>與 Dynamic Media 的整合（有限可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dynamic Media 資產現在可直接在 Journey Optimizer 中使用和存取。此整合可讓您：
<ul>
<li>透過即時更新集中管理資產</li>
<li>立即修改您的資產設定，例如寬度和高度</li>
<li>更新您的內容並新增個人化欄位，以自訂 Dynamic Media 範本</li>
</ul>
<p>
<p>此整合僅適用於一組組織 (有限可用性)。若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>如需詳細資訊，請參閱<a href="../integrations/aem-dynamic.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>與 Adobe GenStudio 的整合 (有限可用性)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>為了提升行銷效率及維持品牌一致性，您現在可以將 GenStudio for Performance Marketing 體驗與 Journey Optimizer 緊密整合。這使您能夠利用 GenStudio 的 AI 支援內容建立以及 Journey Optimizer 的進階協調功能。<p>
<p>Journey Optimizer 中的 GenStudio 整合目前無法與 Healthcare Shield 或 Privacy and Security Shield (有限可用性) 搭配使用。</p>
<p>如需詳細資訊，請參閱<a href="../integrations/genstudio.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>彈性客群評估限制 (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>靈活的受眾評估以前僅供一組組織 (LA) 使用，現在可供所有使用者 (GA) 使用。此功能可讓您根據需要針對選定的客群執行細分工作，確保在將客群鎖定目標至 Journey Optimizer 歷程和行銷活動之前，始終擁有最新的客群資料。</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>如需詳細資訊，請參閱<a href="../audience/creating-a-segment-definition.md#flexible">詳細說明文件</a>。</p>
</tr>
</tbody>
</table>
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
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### 改良功能 {#25-03-improv}

**個人化編輯器** (推出日期：3 月 12 日)

已更新 Journey Optimizer 個人化編輯器，並新增功能：
* **已更新程式碼編輯器設計** – 更簡潔的現代化介面，可改善使用性和焦點。
* **搜尋和取代** – 新增的功能可在編輯器中快速尋找和取代內容。
* **復原與重做支援** – 可讓您輕鬆還原或重新套用變更。
* **可自訂的字型大小** – 可調整編輯器的字型大小，以提升可讀性。
* **內嵌 JSON 驗證** – 為 JSON 內容提供即時用戶端驗證，以加速錯誤偵測。
* **自動完成設定檔和內容屬性** – 提供智慧型建議以簡化內容建立。
* **增強語法強調** – 讓程式碼結構在視覺上更加不同，來改善可讀性。

![展示個人化編輯器新功能的影片](assets/do-not-localize/personalization-editor.gif)

如需詳細資訊，請參閱[詳細文件](../personalization/personalization-build-expressions.md)。

**核准**

定義核准原則的條件時，您現在可以選擇依標籤和/或物件類別篩選。

如需詳細資訊，請參閱[詳細文件](../test-approve/approval-policies.md)。

**設定**

* 您現可指派 Adobe Experience Platform 統一標籤至管道設定。這可讓您輕鬆分類，以及改善所有清單的搜尋和導覽體驗。[了解更多](../configuration/channel-surfaces.md#channel-config-tags)

* 在 Journey Optimizer 設定或編輯電子郵件子網域時，如果您可在上層網域可使用，您現在可以選擇自行管理相關的 DMARC 記錄。 [了解更多](../configuration/dmarc-record.md#set-up-dmarc)

**業務規則**

您現在可以在包含批次細分的歷程和行銷活動中，使用每日頻率上限。為確保每日頻率上限規則的準確性，請確保在製作行銷活動或歷程時選擇最高優先順序的命名空間。在[平台身分識別服務指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}之中進一步了解命名空間優先順序

提醒您，規則集中的每日頻率上限僅適用於一組組織（可用性限制）。 若想取得存取權，請聯絡您的 Adobe 代表。

如需有關業務規則的詳細資訊，請參閱[詳細說明文件](../conflict-prioritization/rule-sets.md)。

**內容範本**

HTML 類型內容範本現已棄用。請注意，您仍可使用之前在 [!DNL Journey Optimizer] 中建立的現有 HTML 內容範本。[深入瞭解內容範本](../content-management/content-templates.md)


<!--**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->




## 2025 年 2 月發行說明 {#25-02-rn}

**發行日期**：2025 年 2 月 18-19 日


### 全新功能 {#25-02-features}

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
<li> 建立歷程規則集以控制設定檔專案進入歷程。 限制設定檔在指定期間內輸入歷程的頻率，或設定檔可同時註冊的歷程數。 在歷程層級套用這些專案，以確保適當地進入管理。</li></ul></p>
<p>業務規則以前僅可供一組組織 (LA) 使用，目前可供所有使用者使用 (GA)。歷程網域業務規則仍僅可用於有限的一組組織 (LA)。</p>
<p>如需詳細資訊，請參閱<a href="../conflict-prioritization/rule-sets.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用 AI 助理，產生登陸頁面</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在就可以使用 AI 助理，為登陸頁面製作引人入勝的內容，包括全頁設計、個人化文字和自訂視覺效果。</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>如需詳細資訊，請參閱<a href="../content-management/generative-lp.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>擁有 AI 助理 (Beta) 的品牌</strong><br/></th>
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
<th><strong>疑難排解自訂動作</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以直接從 Adobe Journey Optimizer 進行真正的 API 呼叫，以驗證自訂動作設定。這項新功能可協助您在歷程中使用自訂動作之前或之後，進行疑難排解。  </p>
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
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>推出日期：2025 年 1 月 28 日</p>
</tr>
</tbody>
</table>
</table>


### 改良功能 {#25-02-improvements}

以下列出了 2 月發行的改進項目。

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
