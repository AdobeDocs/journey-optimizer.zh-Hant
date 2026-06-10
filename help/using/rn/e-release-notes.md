---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 1ff42f25705112ec5c841b0cbd2a74cd5bf8c68a
workflow-type: tm+mt
source-wordcount: 1838
ht-degree: 10%

---


# 搶鮮版發行說明 {#e-release-notes}

Adobe Journey Optimizer持續提供新功能、現有功能的增強功能，以及錯誤修正。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

## 2026年6月發行前注意事項 {#june-26-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。 連結、畫面和更新的檔案會在變更上線生產時發佈。 雖然大多數變更會在發行日期提供，但有些可能會稍後推出 — 如需詳細資訊，請參閱每個專案所列的「推出日期」。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**： 2026年6月16至17日


### 歷程 {#june-26-journeys}

以下功能和改進即將在此版本中推出。

<table>
<thead>
<tr>
<th><strong>歷程仲裁 — 公式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用<strong>公式</strong>，根據客戶設定檔屬性和內容因素自動<strong>排定歷程的優先順序及仲裁順序</strong>，確保客戶進入最相關的歷程。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14719">DOCAC JIRA 任務連結</a></p>
</td>
</tr>
</tbody>
</table>

* **提高即時歷程限制與新護欄** — 您現在最多可以有&#x200B;**200個使用中歷程**，比先前的100個限制有所增加。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14826">連結到DOCAC JIRA工作</a>

* **歷程標題中的開始和結束日期** — 當即時歷程設定開始和/或結束日期時，它們現在會出現在即時狀態徽章旁邊的&#x200B;**歷程標題**&#x200B;中。顯示的標籤會根據每個日期是近期到來或已過去而調整。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">連結到DOCAC JIRA工作</a>

* **直接停止或關閉暫停的歷程** — 您現在可以&#x200B;**直接從**&#x200B;暫停&#x200B;**狀態停止歷程或將其關閉到新入口**。之前，暫停的歷程必須恢復為上線，然後才能停止或關閉。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14229">連結到DOCAC JIRA工作</a>

* **外部對象的補充識別碼支援** — 歷程中的補充識別碼現在支援外部對象，包括從CSV檔案匯入的對象和使用Federated Audience Composition建立的對象。您可以從對象中指定任何非身分屬性或非個人身分屬性作為補充ID，不需要架構標籤。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14541">連結到DOCAC JIRA工作</a>

### 協調的行銷活動 {#june-26-oc}

此版本中的協調行銷活動推出以下功能和改善。

<table>
<thead>
<tr>
<th><strong>在協調的行銷活動中載入檔案活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>協調的行銷活動現在支援直接將<strong>CSV或TXT檔案</strong>載入行銷活動畫布，作為目標對象，而不先將檔案擷取到Adobe Experience Platform。 檔案資料會在執行時使用，不會儲存為Adobe Experience Platform資料集。 在檔案設定期間，您可以定義欄對應、資料型別、NULL處理和每欄錯誤原則。 這支援無法建立完整擷取管道的臨時傳送或合作夥伴清單行銷活動。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14704">DOCAC JIRA 任務連結</a></p>
</td>
</tr>
</tbody>
</table>

* **在協調的行銷活動中關聯資料以回圈為基礎的個人化** — 個人化編輯器現在支援&#x200B;**回圈區塊**，可在關聯式集合（例如訂單、帳戶或預訂）上反複運算，並在單一電子郵件或簡訊中為每個記錄呈現一個內容區塊。集合是使用個人化權杖透過資料選擇器設定，不需要撰寫運算式。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14703">連結到DOCAC JIRA工作</a>

* **個人化每個收件者和行銷活動的電子郵件寄件者詳細資料** — 協調的行銷活動現在支援使用設定檔屬性或關聯資料，個人化&#x200B;**電子郵件標題欄位**，包括寄件者名稱、寄件者地址和回覆對象。如此可讓寄件者詳細資料反映每個收件者的相關顧問、位置或分支，而非透過單一公司地址路由傳送所有傳送。可在管道層級設定標題值，並使用內容相關資料覆寫每個行銷活動，以獲得更精確的控制。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">連結到DOCAC JIRA工作</a>

* **協調行銷活動中的目標維度簡化** — 作用中的&#x200B;**目標維度**&#x200B;現在會顯示在工作流程畫布上，以便您檢視頻道活動使用的維度。多實體區段流程較簡單，因為您不再需要個別的「變更維度」活動。此外，您現在可以明確選擇訊息是在設定檔層級還是在次要維度層級傳送。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13554">連結到DOCAC JIRA工作</a>

### 決策 {#june-26-decisioning}

以下功能即將在此版本中推出Decisioning。

<table>
<thead>
<tr>
<th><strong>在Decisioning中利用Adobe Experience Manager內容片段</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在決定中將<strong>Adobe Experience Manager內容片段</strong>對應至<strong>決定專案</strong>，並在決定原則中運用這些片段，以便在適當的時間將適當的片段提供給適當的客戶。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14885">DOCAC JIRA 任務連結</a></p>
</td>
</tr>
</tbody>
</table>

### 管道 {#june-26-channels}

此發行版本引進了以下功能。

<table>
<thead>
<tr>
<th><strong>自訂傳出頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在推出<strong>自訂頻道</strong>，這項新功能可讓管理員透過無程式碼頻道產生器，將任何外寄HTTP式訊息頻道（例如WeChat、Kakao Talk、Messenger或專屬提供者）直接帶入Journey Optimizer。</p>
<p>設定之後，便可在各種行銷活動、歷程和精心安排的行銷活動中使用自訂管道，並提供與原生管道相同的完整功能集：使用運算式編輯器進行個人化、內容實驗、預覽和校樣、現成可用的報告，以及同意和治理實施。 這填補了先前由自訂動作填補的空白，這些動作僅限於歷程，且缺乏專屬的內容製作。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11381">DOCAC JIRA 任務連結</a></p>
</td>
</tr>
</tbody>
</table>

### 電子郵件 {#june-26-email}

此版本的電子郵件頻道即將提供下列功能和改善。

<!--
<table>
<thead>
<tr>
<th><strong>Advanced Components</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Email Designer now includes a library of ready-to-use layout components — such as Headers, Product Cards (1, 2, or 3 columns), Information blocks, and Footers — that you can drag and drop directly into your email canvas. Each component comes pre-configured with editable properties (image, title, text, button, links) and can be fully customized through the WYSIWYG interface, speeding up email creation without requiring you to build structures from scratch.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14877">Link to DOCAC JIRA task</a></p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>電子郵件Designer中的內容檢查</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在可讓使用者直接在電子郵件Designer介面中驗證其<strong>電子郵件內容品質</strong> （包括可讀性、有效性和內容一致性）。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14870">DOCAC JIRA 任務連結</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>啟用電子郵件大小縮減</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>這個新選項可讓您<strong>減少電子郵件中HTML</strong>的大小（移除不必要的空白字元、註解及多餘的程式碼），而不變更電子郵件的外觀。 這有助於改善傳遞能力（有些電子郵件提供者會拒絕或標幟超大電子郵件），並可加快收件者的載入時間。</p>
<p>推出日期： 2026年6月10日</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14777">DOCAC JIRA 任務連結</a></p>
</td>
</tr>
</tbody>
</table>

* **片段可編輯欄位中的RTF文字** — 您現在可以新增RTF文字至您的電子郵件內容中所使用的可自訂片段。例如，使用文字元件作為電子郵件Designer中的可編輯欄位時，您可以直接格式化內容（例如粗體和斜體）並插入超連結。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14715">連結到DOCAC JIRA工作</a>

* **片段中的文字模式支援** — 若要支援文字型電子郵件工作流程，您現在可以建立和管理視覺化片段的文字版本，以便在包含該片段的純文字版電子郵件中最佳使用。使用目前版本之前建立的片段時，片段文字版本可能會錯誤轉譯 — 在電子郵件Designer和傳遞給收件者的最終電子郵件中皆然。為了對較舊的片段產生最佳結果，請編輯、儲存並重新發佈每個片段。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14204">連結到DOCAC JIRA工作</a>

### 行動裝置訊息（SMS、MMS、RCS和LINE） {#june-26-mobile}

此版本即將對行動裝置傳訊功能進行下列改進。

* **SMS報告的不重複點按** — 新的&#x200B;**不重複點按**&#x200B;模組已引入SMS報告，對目前可用於電子郵件報告的SMS提供相同層級的精細效能追蹤。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14895">連結到DOCAC JIRA工作</a>

* **LINE Channel — 編寫變更** - LINE Channel UI已升級為進階訊息編寫功能。此發行版本引入對&#x200B;**多種訊息格式**&#x200B;的支援，包括文字、影像、影像地圖、轉盤和Flex （JSON編輯器），以及即時裝置預覽。使用者現在可以管理最多五個已排序訊息的群組訊息（包含新增、移除和重新排序控制項），並利用整合的個人化編輯器進行驗證的動態傳訊。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">連結到DOCAC JIRA工作</a>

* **簡訊 — 顯示使用量度** — 針對直接透過Adobe Journey Optimizer購買簡訊的客戶，已引入新的&#x200B;**簡訊使用儀表板**。您現在可以檢視及追蹤最近90天的訊息傳送量度，並依「行動原始」(MO)和「行動已終止」(MT)訊息進行分類。此資料也可透過CSV下載，讓您更清楚掌握和控制簡訊支出。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14345">連結到DOCAC JIRA工作</a>

### 內容與整合 {#june-26-content}

此版本即將推出下列功能和改善專案以進行內容管理和整合。

<table>
<thead>
<tr>
<th><strong>Journey Optimizer中Adobe Experience Manager內容片段的改進</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此版本提供數項增強功能，使<strong>Adobe Experience Manager內容片段</strong>在Journey Optimizer編寫工作流程中更實用、更易於控管，且更易於投入生產：</p>
<ul>
<li>Journey Optimizer現在支援從多個Adobe Experience Manager設定擷取內容片段，包括作者、發佈和已驗證的發佈階層。</li>
<li>選取片段後，其內容會保留在訊息中，讓作者可以跨內容區塊重複使用片段欄位，而不需要重新選取。</li>
<li>Journey Optimizer已引入新的專用內容片段清單頁面，以改進生命週期管理；使用者可以識別不同步的片段，並觸發手動同步以保持最新狀態。</li>
<li>地區設定和變數支援現在可讓行銷人員更刻意使用相同內容片段的替代版本。</li>
<li>現在，Adobe Journey Optimizer存取Adobe Experience Manager內容的方式有了彈性。 此發行版本引進了針對您的歷程與行銷活動中使用的內容片段<strong>切換來源存放庫</strong>的功能。</li>
<li>現在與<b>Managed Services</b>相容，您可以直接在Journey Optimizer中檢視、存取及使用Adobe Experience Manager內容片段，以進行個人化。 只需在組態設定中新增Adobe Experience Manager Managed Services存放庫URL，作為一次性設定即可。</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14686">DOCAC JIRA 任務連結</a></p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14821">DOCAC JIRA 任務連結</a></p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14684">DOCAC JIRA 任務連結</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI助理與Adobe Experience Manager Asset Essentials整合</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI助理現在會在產生電子郵件、網頁和推播通知時，直接從您的Adobe Experience Manager Assets自動擷取<b>品牌核准的影像</b>。 如此一來，您就不需要手動搜尋Assets或仰賴一般AI遞補功能，確保每個視覺效果都完全正確且符合品牌規範。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14761">DOCAC JIRA 任務連結</a></p>
</td>
</tr>
</tbody>
</table>

### 行銷活動 {#june-26-campaigns}

此版本中的行銷活動即將進行下列改進。

* **覆寫行銷活動中的預設執行欄位** — 您現在可以覆寫行銷活動引數中電子郵件、簡訊和WhatsApp傳遞設定的全域預設&#x200B;**執行欄位**。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">連結到DOCAC JIRA工作</a>

### 報表 {#june-26-reporting}

此版本的報告功能即將提供下列改善專案。

* **新的電子郵件和簡訊報告的預估點按量度** — 為了更準確地檢視實際客戶參與度，現在可以在歷程、行銷活動和頻道報告中使用新的預估量度。 這些量度有助於從報表資料中篩選掉非人類互動(NHI)和機器人點按：
   * 預估點按次數：移除已識別的機器人和非人類流量後計算的總點按次數。
   * 預估的CTR：相對於傳遞總數的預估點按次數。
   * 預估僅電子郵件的CTOR：與預估開啟次數相關的預估點按次數。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14354">連結到DOCAC JIRA工作</a>

### 設定 {#june-26-configuration}

此版本的設定和管理功能即將改進以下內容。

* **Web應用程式防火牆(WAF) IP白名單** - Adobe Journey Optimizer現在支援登陸頁面的WAF IP白名單，讓組織能夠強制所有傳入要求都透過其設定的WAF基礎架構專門路由。透過這項增強功能，客戶可設定Journey Optimizer以拒絕任何略過WAF層的直接請求，確保一致套用Imperva等工具中定義的安全性原則。此功能可加強具有嚴格網路存取需求之企業的安全狀況，讓企業能夠完全控制其Journey Optimizer託管登陸頁面的流量。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14814">連結到DOCAC JIRA工作</a>

* **自訂子網域的Feedback Loop OTP程式** - Feedback Loop (FBL)自訂子網域設定程式已改善，直接在產品UI中顯示Yahoo寄件者中心&#x200B;**一次性密碼(OTP)**。使用者現在可以自動擷取及顯示Yahoo寄件者中心網域擁有權驗證期間產生的OTP。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">連結到DOCAC JIRA工作</a>

* **已更新針對客戶情境的批次結束輸送量基準** - Adobe Journey Optimizer的批次傳送輸送量基準已更新，以反映多個個人化情境的生產等級效能 — 從基本傳送到具有條件式邏輯的複雜動態內容。更新後的量度現在可於產品說明中取得，以協助客戶準確規劃其傳訊量。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14816">連結到DOCAC JIRA工作</a>

* **從串流模式移至批次模式的資料集** - AJO訊息回饋事件資料集正在從串流模式轉換為&#x200B;**批次擷取模式**。這項變更可確保資料擷取不超過串流擷取限制。如果您在Customer Journey Analytics報表中使用此資料集，或對其執行查詢，預計未來最多2小時的資料延遲會增加。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14771">連結到DOCAC JIRA工作</a>

### 可用性改善 {#june-26-usability}

此版本即將推出下列可用性改善。

* **歷程與行銷活動的資料夾** — 您現在可以將歷程與行銷活動整理到&#x200B;**資料夾**，以改善介面中的導覽和管理。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">連結到DOCAC JIRA工作</a>

