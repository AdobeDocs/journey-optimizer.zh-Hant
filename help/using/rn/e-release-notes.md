---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: fe8e38287939e289e04e07dfe5a2ca51172825e6
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 15%

---

# 搶鮮版發行說明 {#e-release-notes}

Adobe Journey Optimizer持續提供新功能、現有功能的增強功能，以及錯誤修正。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

## 2026年4月發行前注意事項 {#april-26-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。連結、畫面及更新的文件會在發行當日發佈於發行說明。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發布內容日期**：2026 年 4 月 28-29 日

### 全新功能 {#april-26-features}


<table>
<thead>
<tr>
<th><strong>歷程模擬</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將歷程設定為<strong>模擬</strong>。 此模式可讓您使用<strong>模擬的使用者</strong>來驗證您的邏輯。 這些是專為模擬建立的臨時設定檔，可讓您自由測試，而無需在Adobe Experience Platform中管理持續的測試設定檔。</p>
<p>檔案JIRA工作： <a href="https://jira.corp.adobe.com/browse/DOCAC-14050">DOCAC-14050</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>電子郵件動態寄件者</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過<strong>動態寄件者</strong>功能，您現在可以傳送傳送傳送實體（寄件者）與編寫實體（寄件者）不同的電子郵件。 支援此功能的電子郵件使用者端通常會將其轉譯為「代表寄件者的寄件者」或顯示「透過」指標。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>檔案JIRA工作： <a href="https://jira.corp.adobe.com/browse/DOCAC-14458">DOCAC-14458</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>歷程與行銷活動的資料夾</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將歷程和行銷活動組織到<strong>資料夾</strong>中，以改善介面中的導覽和管理。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>檔案JIRA工作： <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">DOCAC-14038</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>透過MCP整合Journey Optimizer AI Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer現在提供<strong>MCP （模型內容通訊協定）伺服器</strong>，直接在任何MCP相容應用程式中呈現行銷活動、忠誠度和沙箱作業。 透過這項整合，不同的角色可以圍繞相同的協調流程資料共同作業。 您可以對話式描述您的意圖，讓LLM叫用適當的MCP工具，而不需針對AJO REST API撰寫查詢或導覽多個UI畫面。 此功能目前在Claude Web和Desktop中提供。</p>
<p>此功能適用於公開Beta中的所有客戶。</p>
<p>檔案JIRA工作： <a href="https://jira.corp.adobe.com/browse/DOCAC-14509">DOCAC-14509</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>協調行銷活動的沙箱副本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>沙箱工具</strong>現在支援透過套件在沙箱之間匯出和匯入<strong>協調的行銷活動</strong>。</p>
<p>檔案JIRA工作： <a href="https://jira.corp.adobe.com/browse/DOCAC-13760">DOCAC-13760</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>協調行銷活動中的增量查詢活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>增量查詢</strong>活動現在可在<strong>協調的行銷活動</strong>中使用。 此目標定位活動會在每次行銷活動執行時執行您的查詢，並只傳回上次執行中未傳回的記錄。 您可以只傳送訊息或匯出新註冊、新金會員，或其他「自上次執行以來新增」區段，而不重新鎖定相同的設定檔。</p>
<p>檔案JIRA工作： <a href="https://jira.corp.adobe.com/browse/DOCAC-14262">DOCAC-14262</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>歷程仲裁 — AI模型</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在您的<strong>排名公式</strong>中使用<strong>AI模型</strong>，以根據客戶設定檔屬性和情境因素自動提升<strong>歷程優先順序分數</strong>，確保客戶進入最相關的歷程。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>檔案JIRA工作： <a href="https://jira.corp.adobe.com/browse/DOCAC-14295">DOCAC-14295</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>針對AI收件匣最佳化電子郵件：更新的工作流程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer現在包含新功能，可確保您的電子郵件結構最佳化，以供<strong>AI支援的收件匣</strong> （例如Gmail中的<strong>Apple Intelligence</strong>和<strong>Google Gemini</strong>）使用。 隨著AI助理日益控制收件者讀取和操作電子郵件的方式，此功能可幫助您編寫可在下游AI工作（包括摘要、分類、優先順序設定和意圖擷取）中妥善執行的內容。</p>
<p>檔案JIRA工作： <a href="https://jira.corp.adobe.com/browse/DOCAC-14520">DOCAC-14520</a></p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Journey fragments</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey fragments</strong> are reusable sets of journey nodes that you can build once and drop into any journey across your sandbox. Whether it's an eligibility check, a preferred channel routing logic, or a welcome sequence, fragments help teams move faster and stay consistent — without rebuilding the same logic from scratch every time. Once created, fragments are stored in a dedicated <strong>Fragment inventory</strong> and can be inserted into any journey using the <strong>Journey fragments</strong> activity.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-11529">DOCAC-11529</a></p>
<p>Availability date: May 4, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Personalization運算式的AI助理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer現在包含用於個人化運算式的AI助理。 您可以在設計電子郵件內容時，從Personalization編輯器和電子郵件Designer工具列開啟它。 以純文字描述您想要個人化的內容，而助理會產生個人化運算式，供您按原樣使用，或在後續的簡短對話中加以改良。
您也可以選取現有的個人化程式碼，並要求助理員加以說明、修正或提出改進建議。 產生運算式後，「顯示範例設定檔預覽」會針對一組有限的合成範例設定檔執行快速檢查。</p>
<p>如需詳細資訊，請參閱<a href="../content-management/generative-personalization-expressions.md">Personalization運算式的AI小幫手</a>。</p>
<p>推出日期： 2026年4月13日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>收件匣</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>收件匣</strong>是行動功能，可搭配<strong>內容卡</strong>使用，讓客戶在應用程式或網站中建立集中位置，以顯示傳送給使用者的訊息。 這可延長行銷通訊的存留期，確保即使在訊息關閉後，仍可存取訊息。</p>
<p>如需詳細資訊，請參閱<a href="../inbox/inbox-gs.md">詳細文件</a>。</p>
<p>推出日期： 2026年4月7日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程路徑實驗</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用新的<strong>最佳化</strong>節點來執行<strong>A/B測試</strong>或<strong>多臂吃角子老虎機</strong>實驗，以決定符合您以企業為中心的KPI的最佳途徑。 此工具可讓您測試並變更通訊、順序和時間，以便最好地觸及客戶。 此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/path-experimentation.md">詳細文件</a>。</p>
<p>推出日期： 2026年4月7日</p>
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
<p>您現在可以使用<strong>決策</strong>來個人化及最佳化您的電子郵件內容。 運用<strong>優先順序分數</strong>、<strong>公式</strong>或<strong>AI模型</strong>，向每位收件者顯示最相關的優惠和內容。 先前以「有限可用性」發行，現在此功能可用於所有環境（一般可用性）。 透過這個「一般可用性」版本，現在支援<strong>映象頁面</strong>。</p>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/create-decision-policy.md">詳細文件</a>。</p>
<p>推出日期： 2026年4月6日</p>
</td>
</tr>
</tbody>
</table>

### 改善 {#april-26-improv}

以下列舉部分發布內容附上的改良功能。

#### AI

* **行銷活動儀表板中的品牌一致性分數** — 您現在可以直接在行銷活動儀表板中評估您的品牌一致性分數，以確保內容保持在品牌上。 這可讓您快速驗證指引，而不需開啟內容設計工具。

  檔案JIRA工作： [DOCAC-14516](https://jira.corp.adobe.com/browse/DOCAC-14516)

#### 決策

* **將片段附加至決定專案** - Journey Optimizer現在提供將片段附加至決定專案的功能，而決定專案可透過決定原則，在程式碼型體驗和電子郵件行銷活動中運用。 此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。

  檔案JIRA工作： [DOCAC-14452](https://jira.corp.adobe.com/browse/DOCAC-14452)

* **已略過暫時無法使用的片段** — 在決定專案中使用片段時，如果Edge上暫時無法使用片段，則會略過該片段，而且歷程或行銷活動會繼續轉譯而不是失敗。 [閱讀全文](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  推出日期： 2026年4月14日

#### 電子郵件設計

* **電子郵件內容的進階HTML編輯器** — 進階HTML模式可讓您在電子郵件Designer中編輯內容的HTML來源、在來源中新增進階運算式（例如條件），以及在HTML檢視和案頭檢視之間切換，而不會遺失您的變更。 先前僅可用於電子郵件內容範本，此功能現在已部署至Designer電子郵件中的&#x200B;**電子郵件**&#x200B;內容。 目前處於「有限可用性」 — 請聯絡您的Adobe代表以取得存取權。 [閱讀全文](../email/email-expert-mode.md)

  推出日期： 2026年4月9日

#### 歷程路徑最佳化

* **實驗型別** — 您現在可以在設定路徑實驗時選擇A/B實驗（開始時固定分割）或多臂吃角子老虎機（每週更新權重的自動分割）。 [閱讀全文](../building-journeys/path-experimentation.md)

  推出日期： 2026年4月7日

* **路徑實驗：縮放成功者** — 您現在可以自動或手動將實驗的成功路徑轉出給完整受眾。 一旦確定獲勝者，您就可以擴大其觸及範圍和有效性，而無需持續監控實驗。 此功能僅適用於單一歷程（事件觸發和受眾資格）。 [閱讀全文](../building-journeys/path-experimentation.md#scale-winner)

  推出日期： 2026年4月7日

* **條件** - [最佳化](../building-journeys/optimize.md)活動是在歷程中建立條件路徑的新工具。 它取代之前的&#x200B;**條件**&#x200B;活動。 所有條件式邏輯都會保留，現在會透過&#x200B;**最佳化**&#x200B;活動的條件來處理。 先前以「有限可用性」發行，現在此功能可用於所有環境（一般可用性）。 [閱讀全文](../building-journeys/conditions.md)

  推出日期： 2026年4月7日

#### Adobe Experience Manager整合

* **內容警告器選取器** -AEM Assets和內容片段選取器現在已由&#x200B;**內容警告器選取器**&#x200B;取代，此統一模組可讓您瀏覽、搜尋、篩選和存取所有AEM Assets和AEM內容片段。 也包含Dynamic Media轉譯支援，可讓您在選取Dynamic Media資產時，從UI新增影像轉譯。 此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。

  檔案JIRA工作： [DOCAC-13802](https://jira.corp.adobe.com/browse/DOCAC-13802)

* **使用Dynamic Media的計時器開啟時間個人化** - Journey Optimizer與Adobe Experience Manager Dynamic Media整合可為Dynamic Media範本啟用開啟時間個人化，解除鎖定超個人化使用案例。 客戶可以在Adobe Experience Manager中建立和發佈個人化範本，並在Journey Optimizer中使用這些範本，在開放時間呈現資料。

  檔案JIRA工作： [DOCAC-13801](https://jira.corp.adobe.com/browse/DOCAC-13801)

* **Adobe Experience Manager內容片段變數支援** — 您可以在插入Adobe Experience Manager內容片段時選取&#x200B;**內容片段變數** （例如語言或頻道變數），以改善地區設定和多語言情境的處理方式。 此功能僅適用於一組組織 (有限可用性)。 若想取得存取權，請聯絡 Adobe 代表。[閱讀全文](../integrations/aem-fragments.md#aem-variations)

  推出日期： 2026年4月3日

* **製作時Adobe Experience Manager內容片段內容** — 當您在文字欄位和內容區塊之間移動時，您的內容片段選取範圍會保持作用中，因此您可以新增更多片段欄位，而不需每次重新開啟&#x200B;**開啟AEM內容警告器**。 此功能僅適用於一組組織 (有限可用性)。 若想取得存取權，請聯絡 Adobe 代表。[閱讀全文](../integrations/aem-fragments.md)

  推出日期： 2026年4月1日

#### WhatsApp

* **WhatsApp管道：內嵌註冊** - Adobe Journey Optimizer現在支援Meta的<strong>內嵌註冊</strong> WhatsApp管道設定流程。 此簡化上線體驗可讓您直接在AJO介面中連線您的<strong>WhatsApp商業帳戶</strong>和電話號碼，而不需導覽至<strong>Meta Business Manager</strong>，大幅縮短設定時間。 它也是移轉工具，可將現有電話號碼和<strong>WhatsApp商業帳戶(WABA)</strong>轉移到Adobe。

  檔案JIRA工作： [DOCAC-13386](https://jira.corp.adobe.com/browse/DOCAC-13386)

#### 設定

* **URL引數加密金鑰的特定許可權** — 若要存取和管理URL引數加密金鑰，已建立新許可權。 您現在必須授與&#x200B;**檢視機碼登入**&#x200B;和&#x200B;**管理機碼登入**&#x200B;許可權。

  檔案JIRA工作： [DOCAC-14490](https://jira.corp.adobe.com/browse/DOCAC-14490)

#### 協調的行銷活動

<!--* **Data Modeler enhancements** - The Data Modeler in Orchestrated Campaigns now supports enhanced <strong>composite relationship management</strong>. You can create and manage composite relationships directly in the UI, including linking a field to multiple tables of the same type. These enhancements build on the <strong>composite key</strong> and <strong>enumeration management</strong> capabilities introduced in the previous release.Documentation JIRA task: [DOCAC-14334](https://jira.corp.adobe.com/browse/DOCAC-14334)-->

* **協調行銷活動中的全域變數** — 協調行銷活動現在支援全域變數，這些變數只需定義一次，便可在工作流程內的所有活動中重複使用，可簡化設定，並確保動態值、運算式和內容個人化的一致性。

  檔案JIRA工作： [DOCAC-14113](https://jira.corp.adobe.com/browse/DOCAC-14113)

<!--
## March '26 pre-release notes {#march-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: March 24-25, 2026

### New capabilities {#march-26-features}

<table>
<thead>
<tr>
<th><strong>LLM email optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now optimize your email content for deliverability using large language model (LLM) technology. The LLM email optimizer analyzes your email content and provides actionable recommendations to improve sender reputation, avoid spam filters, and enhance overall deliverability performance.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14340">DOCAC-14340</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Convert images to email content templates</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now convert images into email content templates directly in Journey Optimizer. Use AI-powered analysis to automatically generate structured HTML templates from visual references, significantly reducing email design time.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14324">DOCAC-14324</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Incremental query activity in Orchestrated Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Incremental query</strong> activity is now available in Orchestrated Campaigns. This activity queries only new or updated records since the last workflow execution, significantly reducing processing time and improving efficiency for recurring campaigns targeting large datasets.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14262">DOCAC-14262</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Transactional category in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Orchestrated campaigns, you can now set a channel activity to the <strong>Transactional</strong> category using the <strong>Category</strong> field. This applies transactional channel configurations to that activity and bypasses business rules for it.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14233">DOCAC-14233</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Test activity in Orchestrated Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Test</strong> activity is now available in Orchestrated Campaigns. This activity routes workflow execution to different branches based on defined conditions, enabling you to validate campaign logic and configurations before activating live deliveries.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14115">DOCAC-14115</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom forms in landing pages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create <strong>custom forms</strong> in landing pages to collect specific subscriber data beyond standard opt-in fields. Define your own form fields, validation rules, and submission behaviors to support a wider range of subscription and profile enrichment use cases.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13963">DOCAC-13963</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Create Orchestrated Campaign use case</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey Agent</strong>, powered by Adobe Experience Platform Agent Orchestrator, can now create complete <strong>Orchestrated Campaign</strong> use cases through a natural language interface. Describe your campaign goal and requirements in plain language, and Journey Agent configures the campaign structure, activities, and targeting for you.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13768">DOCAC-13768</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New profile acquisition in landing pages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Landing pages now support <strong>new profile acquisition</strong> workflows, enabling you to capture and onboard new audience members directly from your landing page experiences. Configure acquisition forms to collect profile data and automatically provision new profiles in Adobe Experience Platform.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13757">DOCAC-13757</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey path optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey path optimization</strong> uses AI to analyze historical journey performance and automatically select the best path for each customer, maximizing conversion and engagement outcomes.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13492">DOCAC-13492</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use <strong>Decisioning</strong> to personalize and optimize the content of your email messages. Leverage Priority Scores, Formulas, or AI Models to display the most relevant offers and content to each recipient.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability). With this General Availability release, mirror pages are now supported.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13182">DOCAC-13182</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Message inbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Message Inbox</strong> is now available in Adobe Journey Optimizer, providing a centralized view of received in-app, push, and SMS messages. Recipients can access and interact with all their messages in one place, enabling richer engagement and re-engagement scenarios.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-11382">DOCAC-11382</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Native channel action activities deprecated</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Following the General Availability of the <strong>Action activity</strong> in February 2026, legacy native channel action activities (Email, SMS, Push, In-App, etc.) in the journey canvas are now deprecated. Existing journeys using legacy channel activities continue to function without any changes or migration required.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14144">DOCAC-14144</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Dataset lookup support in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new activity in journeys, Dataset lookup, allows you to to dynamically retrieve data from Adobe Experience Platform record datasets during runtime. By leveraging this capability, you can access data that may not reside in the profile or event payload, ensuring your customer interactions are both relevant and timely. Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14351">DOCAC-14351</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Trigger orchestrated campaigns using API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now trigger an orchestrated campaign via API. Configure the target campaign as "Triggered by a signal" and publish it. Then use an API call to fire the campaign. The API call can include parameters that will be available as variables in the triggered campaign.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14030">DOCAC-14030</a></p>
</td>
</tr>
</tbody>
</table>

### Improvements {#march-26-improv}

Improvements coming with this release are listed below.

#### Journeys

* **Journey Arbitration - AI Models** - In addition to ranking formulas, AI models can now be used with Journey Arbitration to automatically rank and prioritize journey entry for customers, using machine learning to determine the most relevant journey for each profile based on historical behavior and contextual signals. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

  Documentation JIRA task: [DOCAC-14295](https://jira.corp.adobe.com/browse/DOCAC-14295)

#### Reporting

* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.
  Documentation JIRA task: [DOCAC-14354](https://jira.corp.adobe.com/browse/DOCAC-14354)

* **Send-Time Optimization: updated controls location and new lift report** - Send-Time Optimization (STO) controls have been relocated to the Action configuration menu. Additionally, a new lift report is now available in Journeys reports to measure the impact of STO on your campaign performance metrics.

  Documentation JIRA task: [DOCAC-14335](https://jira.corp.adobe.com/browse/DOCAC-14335)

#### Email Designer

* **Open-time personalization using Dynamic Media (Beta)** - You can now personalize email content at open time using Adobe Dynamic Media assets, enabling real-time, recipient-specific images and visuals that are generated dynamically based on each recipient's attributes at the moment of email opening. This capability is currently in Beta.
  Documentation JIRA task: [DOCAC-14353](https://jira.corp.adobe.com/browse/DOCAC-14353)

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.
  Documentation JIRA task: [DOCAC-14254](https://jira.corp.adobe.com/browse/DOCAC-14254)

* **Text mode support in fragments** - Fragments now support text mode editing, allowing you to create and manage plain text versions of your content fragments for use in text-based email workflows and multi-channel scenarios.
  Documentation JIRA task: [DOCAC-14204](https://jira.corp.adobe.com/browse/DOCAC-14204)

#### Decisioning

* **Expression Fragment Reference change feed support in Edge Decisioning** - This enhancement allows changes in fragment references to automatically be reflected in all items that reference fragments, without needing to refresh anything manually (republishing the campaign or decision policy).
  Documentation JIRA task: [DOCAC-14350](https://jira.corp.adobe.com/browse/DOCAC-14350)

* **Optional fragments in decision items** - Fragments attached to decision items can now be configured as optional, providing greater flexibility in content composition when not all decision item renderings require a specific fragment.
  Documentation JIRA task: [DOCAC-14309](https://jira.corp.adobe.com/browse/DOCAC-14309)

#### Configuration

* **URL parameters encryption** - URL parameters in tracking links and landing pages can now be encrypted, providing an additional layer of security for sensitive parameter data. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.
  Documentation JIRA task: [DOCAC-14349](https://jira.corp.adobe.com/browse/DOCAC-14349)

* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.
  Documentation JIRA task: [DOCAC-14038](https://jira.corp.adobe.com/browse/DOCAC-14038)

#### Orchestrated campaigns

* **Target dimension simplification in Orchestrated Campaigns** - You can now easily select or automatically deduce the right targeting and secondary dimensions in Orchestrated campaigns for accurate, efficient audience activation.
  Documentation JIRA task: [DOCAC-13554](https://jira.corp.adobe.com/browse/DOCAC-13554)
-->

<!--
## February '26 pre-release notes {#feb-26-01-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: February 17, 2026

### New capabilities {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>Wave sending of outbound messages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can schedule outbound messages from <strong>campaigns</strong> or <strong>journeys</strong> to be delivered in controlled <strong>batches</strong> over time.</p>
<p>Wave sending offers the following benefits:</p>
<ul>
<li>Better <strong>deliverability</strong> – Spread sends over time to help maintain a strong <strong>sender reputation</strong> and reduce the risk of being flagged as spam.</li>
<li><strong>Load control</strong> – Avoid overwhelming downstream systems (e.g. call centers, landing pages) by limiting how many messages go out at once.</li>
<li>High-volume and time-sensitive use cases – Suited to large audiences or when you need to control timing (e.g. call center capacity, ramp-up, or time-bound offers).</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey arbitration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use <strong>formulas</strong> and <strong>AI models</strong> to automatically boost <strong>journey priority scores</strong> based on customer profile attributes and contextual factors, ensuring customers enter the most relevant journeys.</p>
<p>This capability is only available for a set of organizations (<strong>Limited Availability</strong>). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Channel Content Create</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Powered by <strong>Adobe Experience Platform Agent Orchestrator</strong>, <strong>Journey Agent</strong> is available in Journey Optimizer and enables you to analyze journeys through a <strong>natural language interface</strong>. You can now also generate and manage channel-specific content directly in Journey Agent, creating content for channels such as email and push, applying and previewing templates, refining tone and style through prompts, and opening content in <strong>Content Designer</strong> for in-context editing.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mobile Live Activities</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Live Activities</strong> provide <strong>real-time updates</strong> and interactive experiences within mobile apps, allowing users to stay informed about ongoing events or tasks directly on their device's screen. This feature enhances engagement by delivering live information, such as progress tracking, event updates, or interactive content, without requiring users to open the app.</p>
<p>Previously released in beta, this capability is now available to all environments (<strong>General Availability</strong>).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Action activity in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supports a new generic <strong>Action activity</strong> that enables you to configure both single actions and <strong>multi-action inbound action groups</strong>, allowing for streamlined action configuration within the <strong>journey canvas</strong>. In particular, this new feature allows for:</p>
<ul>
<li>A simplified native action configuration within the journey canvas.</li>
<li>The capacity to create multi-action inbound action groups.</li>
<li>The ability to add <strong>optimization</strong> to any built-in channel action.</li>
<li>The ability to add both <strong>experimentation</strong> and <strong>multilingual</strong> options to any action.</li>
</ul>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same <strong>authoring workflows</strong> and <strong>targeting capabilities</strong> already available for mobile push.</p>
<p>Previously released in beta, this capability is now available to all environments (<strong>General Availability</strong>).</p>
<p>Availability date: February 13, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Content decision activity</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Content decision activity</strong> is now available in the <strong>journey canvas</strong> for integrating <strong>personalized offers</strong> directly into your customer journeys. This activity enables you to deliver decision-based content and reference those offers throughout your journey—in conditions for creating eligibility-based branching, in custom actions for passing offer data to external systems, and in other activities for building fully personalized customer experiences.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (<strong>General Availability</strong>).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>For more information, refer to the <a href="../building-journeys/content-decision.md">detailed documentation</a>.</p>
<p>Availability date: February 11, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Self-service migration tooling APIs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Migration tooling APIs</strong> are now available to programmatically migrate <strong>Decision management</strong> entities to <strong>Decisioning</strong>, featuring:</p>
<ul>
<li>Flexible migration scopes (<strong>sandbox</strong>, <strong>offer</strong>, or <strong>decision</strong> level)</li>
<li>Automated <strong>dependency analysis</strong> and validation</li>
<li><strong>Rollback support</strong> for completed migrations</li>
<li>Detailed migration reports with object mappings</li>
</ul>
<p>For more information, refer to the <a href="../experience-decisioning/decisioning-migration-api.md">detailed documentation</a>.</p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gain deeper insight into the health and performance of your <strong>custom action endpoints</strong> with a new <strong>monitoring dashboard</strong> and enriched <strong>journey step event data</strong>. Track successful calls, errors, throughput, response times, and queue wait times to quickly understand when, where, and why anomalies occur.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (<strong>General Availability</strong>).</p>
<p>For more information, refer to the <a href="../action/reporting.md">detailed documentation</a>.</p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in SMS channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now personalize and optimize the content of your <strong>SMS messages</strong> with <strong>Decisioning</strong>. Use <strong>Priority Scores</strong>, <strong>Formulas</strong>, or <strong>AI Models</strong> to display the best content to your customers.</p>
<p>For more information, refer to the <a href="../experience-decisioning/create-decision.md">detailed documentation</a>.</p>
<p>Availability date: February 2, 2026</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#feb-26-01-improv}

Improvements coming with this release are listed below.

#### Configuration

* **Experience event usage in journey expressions** - Starting April 1, 2026, the use of experience event attributes in journey expressions will no longer be supported for organizations that have not used this capability in the last 90 days. This capability has already been unavailable for new customer organizations since July 8, 2025. For alternatives, see [Experience event lookup in journeys](../building-journeys/exp-event-lookup.md).


* **Subdomain delegation method switching** - You can now switch from one <strong>subdomain delegation</strong> method to another. This enables you to migrate domains using the <strong>CNAME delegation</strong> mode to the <strong>custom delegation</strong> method to adhere to your company's security policies.

  **Note**: This capability is only available for a set of organizations (<strong>Limited Availability</strong>). To gain access, contact your Adobe representative.


#### Email Designer

* **Use a brand theme to convert an image to an email template** - When converting an image to an email template in Journey Optimizer, you can now use a <strong>theme</strong> as input so the generated HTML follows your <strong>brand parameters</strong>. Styling such as background color, button color, fonts, line spacing, margins, and padding is applied automatically, reducing manual design work and delivering a template that is ready to use with minimal edits.


* **Update brands with new color tab** - <strong>Brand guidelines</strong> help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors section</strong> defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity.


#### AI

* **Integration of custom Firefly models and third-party image generation models** - Enable seamless integration of standard and custom <strong>Firefly models</strong>, along with approved <strong>third-party image models</strong> (e.g., NanoBanana), to provide greater flexibility, control, and brand alignment when generating images. This allows you to select the best model for each use case: standard Firefly for general needs, custom Firefly for on-brand generation, or approved third-party models for specialized or experimental scenarios.


#### Experience Decisioning

* **Edge inbound support for using Adobe Experience Platform data in Decisioning** - Decisioning support of <strong>Experience Platform data lookup</strong> now includes <strong>edge inbound</strong> channel use cases. The capability remains in Limited Availability; General Availability of the underlying data lookup feature is not yet announced (AEP/product dependency).

  **Note**: This capability is only available for a set of organizations (<strong>Limited Availability</strong>). To gain access, contact your Adobe representative.


* **Experience Decisioning preview in Code-based Experience channel** - You can now preview <strong>decision items</strong> when configuring <strong>Experience Decisioning</strong> with the <strong>Code-based Experience</strong> channel. Preview is available directly in the authoring interface before going live.


* **Offer Ranking AI Model Observability** - Journey Optimizer now allows you to monitor the <strong>health</strong>, <strong>training status</strong>, and <strong>performance</strong> of your <strong>AI models</strong> in Decisioning—so you can verify training success, troubleshoot failures, and understand impact on your outcomes. This capability is available for personalized optimization models only (not auto-optimization).


* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to <strong>decision items</strong> which can be leveraged in code-based experience campaigns through <strong>decision policies</strong>.

  **Note**: Previously released in Limited Availability, this capability is now available to all environments (General Availability).

  Availability date: February 12, 2026.


#### Journeys

* **Multiple inbound actions in journeys** - To simplify your journey orchestration, you can now define several <strong>inbound actions</strong> in a single journey. Previously available in campaigns, this capability enables you to deliver multiple <strong>code-based experiences</strong>, <strong>in-app messages</strong>, <strong>content cards</strong>, or <strong>web actions</strong> to different locations at the same time, each action containing specific content.

  **Note**: Previously released in Limited Availability, this capability is now available to all environments (General Availability).


* **SMS Webhooks** - <strong>Webhooks</strong> are now supported across all SMS providers. You can configure each webhook based on its intended purpose: <strong>Inbound webhooks</strong> to capture incoming messages and <strong>Feedback webhooks</strong> to receive delivery receipts, status updates, and other message-related events. [Read more](../sms/sms-webhook.md)

  Availability date: February 2, 2026.
-->
<!--
## January '26 pre-release notes {#jan-26-01-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: January 27, 2026

### New capabilities {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Action activity in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supports a new generic <strong>Action activity</strong> that enables you to configure both single actions and <strong>multi-action inbound action groups</strong>, allowing for streamlined action configuration within the journey canvas. In particular, this new feature allows for:</p>
<ul>
<li>A simplified native action configuration within the journey canvas.</li>
<li>The capacity to create multi-action inbound action groups.</li>
<li>The ability to add optimization to any built-in channel action.</li>
<li>The ability to add both experimentation and multi-lingual options to any action.</li>
</ul>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gain deeper insight into the health and performance of your custom action endpoints with a new <strong>monitoring dashboard</strong> and enriched journey step event data. Track successful calls, errors, throughput, response times, and queue wait times to quickly understand when, where, and why anomalies occur.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-126869">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Quiet Hours / Time Based Exclusions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Quiet hours let you define <strong>time-based exclusions</strong> for Email, SMS, Push, and WhatsApp channels. They ensure that no messages are sent during specific periods of time, helping you respect customer preferences and compliance requirements. You can apply quiet hours through <strong>rule sets</strong>, which can be assigned to individual actions in campaigns or journeys for precise control.</p>
<p>Previously released in Limited Availability, this feature is now available to all environments. With this General Availability release, the feature now includes the ability for customer to queue a campaign action until the completion of Quiet Hours, and the ability to preview the activated Quiet Hours rule.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-63912">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, the <strong>Direct Mail channel</strong> is now available on the <strong>journey canvas</strong>, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-38399">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-37866">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in Push and SMS channels</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add <strong>Decision policies</strong> into push and SMS journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-55817">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55818">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The <strong>Direct mail activity</strong> facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the <strong>extraction file</strong> required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-82584">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New <strong>source connectors</strong> are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Message Export</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Message Export</strong> capability is now available for email and SMS channels. This feature allows you to automatically export sent message content to a dedicated Experience Platform dataset, enabling you to:</p>
<ul>
<li>Meet regulatory compliance requirements (such as HIPAA)</li>
<li>Archive messages for legal claims and customer care inquiries</li>
<li>Retain copies of personalized content sent to individuals</li>
</ul>
<p>Records are retained in the AJO Message Export Dataset for <strong>7 calendar days from ingestion</strong>. During this retention period, you can export the data to your own storage via Experience Platform destinations. The feature is enabled at the channel configuration level, giving you granular control over which messages are exported.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-105313">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - Create a Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Create Agent enables Journey Optimizer users to build and configure marketing journeys using a natural language interface. With Journey Create Agent, practitioners can quickly create journeys by describing their requirements in conversational prompts. The agent streamlines journey creation, allowing marketers to focus on strategy rather than technical configuration.</p>
<p><a href="https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">Learn more</a></p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-95142">Link to PRODUCT JIRA task</a></p>
<p>Availability date: January 12, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Journey Optimizer API</strong> is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-96195">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 24, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New journey alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Three new <strong>journey alerts</strong> are now available to help you monitor and track journey lifecycle events and custom action performance:</p>
<ul>
<li><strong>Journey Published</strong>: Receive notifications when a journey is published by a practitioner in the journey canvas.</li>
<li><strong>Journey Finished</strong>: Get alerts when a journey has finished, with specific definitions based on journey type (Read Audience or Event-triggered).</li>
<li><strong>Custom Action Capping Triggered</strong>: Be notified when capping is activated on a custom action endpoint.</li>
</ul>
<p>These alerts can be subscribed to at the organization level or for specific journeys.</p>
<p>For more information, refer to the <a href="../reports/alerts.md#journey-alerts">detailed documentation</a>.</p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Themes in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply <strong>pre-approved themes</strong> to ensure brand consistency across all emails, speed up your campaign creation process, and independently produce high-quality emails while reducing dependency on design teams.</p>
<p>Previously released in beta version, this capability is now available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/NEO-88838">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#jan-26-01-improv}

Improvements coming with this release are listed below.

#### AI

* **AI Assistant Content Quality Checks** - In addition to brand alignment, you can now evaluate overall <strong>content quality</strong> to uncover potential issues with readability, cohesiveness, and effectiveness, independent of your brand guidelines. These automated checks help identify unclear messaging, inconsistent tone, or structural gaps.
  <a href="https://jira.corp.adobe.com/browse/CJM-103238">Link to PRODUCT JIRA task</a>
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors section</strong> defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity.
  <a href="https://jira.corp.adobe.com/browse/CJM-121183">Link to PRODUCT JIRA task</a>

#### Campaigns

* **Schedule Campaign using Profile Time Zone** - Campaign scheduling can now use each profile's <strong>time zone</strong> to deliver messages at the intended local time.

  **Note**: This improvement is only available for a set of organizations (Limited Availability).
  <a href="https://jira.corp.adobe.com/browse/CJM-43782">Link to PRODUCT JIRA task</a>

#### Channels

* **SMS Webhooks: Phase II** - Description to be provided.
  <a href="https://jira.corp.adobe.com/browse/CJM-93914">Link to PRODUCT JIRA task</a>

#### Email Designer

* **In-place corrections in the Email designer** - <strong>AI-powered automatic content suggestions</strong> are now available in the Email Designer when violations are detected during content validation. If content is flagged as misaligned with brand guidelines or fails quality criteria, the system proactively generates corrected alternatives that can be reviewed and applied inline, improving compliance and accelerating production.
  <a href="https://jira.corp.adobe.com/browse/CJM-95365">Link to PRODUCT JIRA task</a>

#### Experience Decisioning

* **Self-service migration tooling APIs** - A new set of <strong>migration tooling APIs</strong> is available to migrate Offer management entities to Experience Decisioning. The tooling enables seamless migration between sandboxes with dependency resolution and rollback capabilities.
  <a href="https://jira.corp.adobe.com/browse/CJM-109695">Link to PRODUCT JIRA task</a>

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to decision items which can be leveraged in code-based experience campaigns through decision policies.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/CJM-110282">Link to PRODUCT JIRA task</a>

#### Journeys

* **Leverage a failure response payload in journey Custom Actions** - You can now define an optional <strong>error response payload</strong> for custom actions. When a call fails, the error payload is exposed in the journey context and is available in the timeout/error branch to support richer fallback logic and debugging.
  <a href="https://jira.corp.adobe.com/browse/CJM-113125">Link to PRODUCT JIRA task</a>

* **Combine native and Adobe Campaign message actions** - Journey Optimizer now lets you combine Adobe Campaign v7/v8 message actions with native channel actions in the same journey.
  <a href="https://jira.corp.adobe.com/browse/CJM-113103">Link to PRODUCT JIRA task</a>

* **Journey payload size validation in journeys** - Journey Optimizer now provides <strong>payload size validation</strong> to help ensure optimal performance and system stability. When building or publishing journeys, you receive clear warnings and errors if payload sizes approach or exceed recommended limits, along with actionable guidance to optimize your journey configuration. This proactive validation helps you identify potential issues early and maintain journey performance.
  <a href="https://jira.corp.adobe.com/browse/CJM-122236">Link to PRODUCT JIRA task</a>

* **Multiple inbound actions in journeys** - To simplify your journey orchestration, you can now define <strong>multiple inbound actions</strong> in a single journey. Previously available in campaigns, this capability enables you to deliver multiple code-based experiences, In-app messages, Content Cards or web actions to different locations at the same time, each action containing a specific content.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a>

#### Orchestrated campaigns

* **Select attributes and copy distribution values** - You can now select or copy values directly from the distribution of values view in orchestrated campaigns.
  <a href="https://jira.corp.adobe.com/browse/CJM-105244">Link to PRODUCT JIRA task</a>

* **Data usage label inheritance for audiences** - <strong>Data usage labels</strong> applied in Adobe Experience Platform now automatically carry over when saving audiences in orchestrated campaigns, reducing manual DULE tagging.
  <a href="https://jira.corp.adobe.com/browse/CJM-120769">Link to PRODUCT JIRA task</a>

* **Predefined retargeting filters** - To support easier retargeting for orchestrated campaign use cases, this release introduces new <strong>retargeting filters</strong>. These filters let you directly target audiences based on message engagement, such as sent, opened only, opened or clicked, or opened and clicked, and select the specific campaign or in-transition campaign you want to retarget.
  <a href="https://jira.corp.adobe.com/browse/CJM-116701">Link to PRODUCT JIRA task</a>

* **Predefined filters with parameters** - You can now create <strong>filters with parameters</strong> in orchestrated campaigns for reusable, editable rules.
  <a href="https://jira.corp.adobe.com/browse/CJM-115431">Link to PRODUCT JIRA task</a>

* **Message confirmation before send** - A <strong>confirmation step</strong> is now enabled by default before sending orchestrated campaigns to reduce accidental sends.
  <a href="https://jira.corp.adobe.com/browse/CJM-87219">Link to PRODUCT JIRA task</a>

* **User-generated metadata support** - The <strong>executionMetadata helper function</strong> is now available in the personalization editor for Orchestrated Campaigns, enabling you to attach contextual information to any native action and store it in a dataset for export to external systems.
  <a href="https://jira.corp.adobe.com/browse/CJM-112697">Link to PRODUCT JIRA task</a>

* **Restart button** - Orchestrated campaigns now include a <strong>restart button</strong> so you can quickly re-launch runs when needed before publishing the campaign.
  <a href="https://jira.corp.adobe.com/browse/CJM-106020">Link to PRODUCT JIRA task</a>

* **Rate control support** - Orchestrated campaigns now support <strong>rate control</strong> to help you pace deliveries and align with volume constraints.
  <a href="https://jira.corp.adobe.com/browse/CJM-113254">Link to PRODUCT JIRA task</a>

#### Permissions

* **Prevent self-approval for journeys and campaigns** - You can now require that creators cannot approve their own journeys or campaigns, improving <strong>separation of duties</strong> in approval workflows.
  <a href="https://jira.corp.adobe.com/browse/CJM-99957">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95676">Link to PRODUCT JIRA task</a>

## Coming soon {#jan-26-01-coming-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

<table>
<thead>
<tr>
<th><strong>Content generation within Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Powered by Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> is available in Journey Optimizer and enables you to analyze journeys through a natural language interface. You can now also generate and manage channel-specific content directly in Journey Agent, creating content for channels such as email and push, applying and previewing templates, refining tone and style through prompts, and opening content in Content Designer for in-context editing.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-111882">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 2, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Content decision activity</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now include <strong>personalized offers</strong> in your journeys through a dedicated Content decision activity in the journey canvas, and use them in journey activities, including conditions and custom actions.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-99223">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->
