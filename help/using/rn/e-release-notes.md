---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: a2257f19ea46aaf4bcf45580a0e6cf0d207be355
workflow-type: tm+mt
source-wordcount: 1876
ht-degree: 5%

---


# 搶鮮版發行說明 {#e-release-notes}

Adobe Journey Optimizer持續提供新功能、現有功能的增強功能，以及錯誤修正。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

## 2026年6月發行前注意事項 {#june-26-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。 連結、畫面和更新的檔案會在變更上線生產時發佈。 雖然大多數變更會在發行日期提供，但有些可能會稍後推出 — 如需詳細資訊，請參閱每個專案所列的「推出日期」。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**： 2026年6月16至17日

### 歷程 {#june-26-journeys}

以下功能和改進即將在此版本中推出。

* **提高即時歷程限制與新護欄** — 您現在最多可以有&#x200B;**200個使用中歷程**，比先前的100個限制有所增加。

* **歷程標題中的開始和結束日期** — 當即時歷程設定開始和/或結束日期時，它們現在會出現在即時狀態徽章旁邊的&#x200B;**歷程標題**&#x200B;中。 顯示的標籤會根據每個日期是近期到來或已過去而調整。

* **直接停止或關閉暫停的歷程** — 您現在可以&#x200B;**直接從**&#x200B;暫停&#x200B;**狀態停止歷程或將其關閉到新入口**。 之前，暫停的歷程必須恢復為上線，然後才能停止或關閉。

### 協調的行銷活動 {#june-26-oc}

此版本中的協調行銷活動推出以下功能和改善。

<table>
<thead>
<tr>
<th><strong>協調行銷活動中的檔案型目標定位</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>協調的行銷活動現在支援直接將<strong>CSV或TXT檔案</strong>載入行銷活動畫布，作為目標對象，而不先將檔案擷取到Adobe Experience Platform。 檔案資料會在執行時使用，不會儲存為Adobe Experience Platform資料集。 在檔案設定期間，您可以定義欄對應、資料型別、NULL處理和每欄錯誤原則。 未通過驗證的列會在行銷活動執行前遭到拒絕並記錄，讓對象保持乾淨，無需手動預先處理。 這尤其適合在無法建立完整擷取管道的臨時傳送或合作夥伴清單行銷活動。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
</td>
</tr>
</tbody>
</table>

* **在協調的行銷活動中關聯資料以回圈為基礎的個人化** — 個人化編輯器現在支援&#x200B;**回圈區塊**，可在關聯式集合（例如訂單、帳戶或預訂）上反複運算，並在單一電子郵件或簡訊中為每個記錄呈現一個內容區塊。 集合是使用個人化權杖透過資料選擇器設定，不需要撰寫運算式。 您可以在行銷活動上線之前，預覽循環區塊針對範例資料呈現的方式，包括處理空白集合。

* **個人化每個收件者和行銷活動的電子郵件寄件者詳細資料** — 協調的行銷活動現在支援使用設定檔屬性或關聯資料，個人化&#x200B;**電子郵件標題欄位**，包括寄件者名稱、寄件者地址和回覆對象。 如此可讓寄件者詳細資料反映每個收件者的相關顧問、位置或分支，而非透過單一公司地址路由傳送所有傳送。 可在管道層級設定標題值，並使用內容相關資料覆寫每個行銷活動，以獲得更精確的控制。

<!--
* **Target dimension simplification in Orchestrated campaigns** - The active **targeting dimension** is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->

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
</td>
</tr>
</tbody>
</table>

* **動態優惠屬性** - Decisioning中的優惠屬性現在可以在傳送時使用設定檔、情境和對象資料進行個人化。 如此一來，行銷人員就不需要針對次要內容變數維持重複的優惠方案，而能夠管理較少、較靈活的決策專案。

* **決策中的版位層級頻率上限** — 決策中的頻率上限規則現在可以將範圍限定於個別版位，讓您更能掌控優惠方案在指定介面中的顯示頻率。 提供兩種模式：

   * 位置專用上限：定義上限值，此上限值僅在優惠方案顯示在所選位置時適用。
   * 每次刊登的上限：將上限獨立套用至選件出現的每個刊登版位，讓每個刊登版位維持其專屬的上限計數器。

### 電子郵件 {#june-26-email}

此版本的電子郵件頻道即將提供下列功能和改善。

<table>
<thead>
<tr>
<th><strong>電子郵件Designer中的內容品質檢查</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在在電子郵件Designer中直接納入內容品質評分，在啟動前可跨三個維度分析您的電子郵件：拼字、文法和標點符號；可讀性和語調，包括長句標籤、被動語態和行話；以及主題行和CTA有效性，針對清晰度、急迫性和結構評分。 每個檢查都會顯示可操作的建議，讓團隊在不離開編寫介面的情況下捕捉和解決問題。</p>
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
<p>Journey Optimizer現在包含一個選項，可移除不必要的空格、評論和重複程式碼，進而縮小電子郵件的HTML大小，而不會影響電子郵件的呈現方式。 這可避免某些電子郵件提供者用來標幟或拒絕訊息的大小臨界值，且可縮短收件者的載入時間，藉此改善傳遞能力。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>片段可編輯欄位中的RTF文字</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以新增RTF文字至您的電子郵件內容中所使用的可自訂片段。 例如，使用文字元件作為電子郵件Designer中的可編輯欄位時，您可以直接格式化內容（例如粗體和斜體）並插入超連結。</p>
</td>
</tr>
</tbody>
</table>

* **增強影像至HTML轉換工具** — 現已提供新版本的影像至HTML轉換工具功能，可提高HTML產生的正確性。 此更新利用較高層級的LLM模型，從影像輸入提供更精確且可靠的HTML輸出。

+++ 即將推出 — **下列資訊可能會變更**

<table>
<thead>
<tr>
<th><strong>電子郵件Designer中的模組</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>電子郵件Designer現在包含現成可用的版面模組（例如頁首、產品卡、資訊區塊和頁尾）資料庫，您可以將這些模組直接拖放到電子郵件畫布中。</p>
<p>每個模組都預先設定了可編輯的屬性（影像、標題、文字、按鈕、連結），並可透過WYSIWYG介面完全自訂，因此無需您從頭開始建立結構，即可加速電子郵件的建立。</p>
<p>推出日期： 2026年6月22日</p>
</td>
</tr>
</tbody>
</table>

+++

### 行動裝置訊息（SMS、MMS、RCS和LINE） {#june-26-mobile}

此版本即將對行動裝置傳訊功能進行下列改進。

* **SMS報告的不重複點按** — 新的&#x200B;**不重複點按**&#x200B;模組已引入SMS報告，對目前可用於電子郵件報告的SMS提供相同層級的精細效能追蹤。

* **LINE Channel — 編寫變更** - LINE Channel UI已升級為進階訊息編寫功能。 此發行版本引入對&#x200B;**多種訊息格式**&#x200B;的支援，包括文字、影像、影像地圖、轉盤和Flex （JSON編輯器），以及即時裝置預覽。 使用者現在可以管理最多五個已排序訊息的群組訊息（包含新增、移除和重新排序控制項），並利用整合的個人化編輯器進行驗證的動態傳訊。

* **簡訊 — 顯示使用量度** — 針對直接透過Adobe Journey Optimizer購買簡訊的客戶，已引入新的&#x200B;**簡訊使用儀表板**。 您現在可以檢視及追蹤最近90天的訊息傳送量度，並依「行動原始」(MO)和「行動已終止」(MT)訊息進行分類。 此資料也可透過CSV下載，讓您更清楚掌握和控制簡訊支出。

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
</td>
</tr>
</tbody>
</table>

<!--
### Campaigns {#june-26-campaigns}

The following improvement is coming to campaigns in this release.

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default **execution field** set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.
-->

### 報表 {#june-26-reporting}

此版本的報告功能即將提供下列改善專案。

* **電子郵件和簡訊報告的預估點按次數** — 歷程、行銷活動和頻道報告中現在提供新的&#x200B;**預估點按次數**&#x200B;量度，以用於電子郵件和簡訊。 此量度不包括已識別的機器人和非人類互動(NHI)流量，以提供更清楚的真實客戶參與檢視。 現有的點按次數量度仍可使用，並繼續報告總點按次數。

+++ 即將推出 — **下列資訊可能會變更**

* **新的電子郵件和簡訊報告的預估點按量度** — 為了更準確地檢視實際客戶參與度，現在可以在歷程、行銷活動和頻道報告中使用新的預估量度。 這些量度有助於從報表資料中篩選掉非人類互動(NHI)和機器人點按：

   * 預估的CTR：相對於傳遞總數的預估點按次數。
   * 預估僅電子郵件的CTOR：與預估開啟次數相關的預估點按次數。

  推出日期：2026年6月底

+++

### 設定 {#june-26-configuration}

此版本的設定和管理功能即將改進以下內容。

* **從串流模式移至批次模式的資料集** - AJO訊息回饋事件資料集正在從串流模式轉換為&#x200B;**批次擷取模式**。 這項變更可確保資料擷取不超過串流擷取限制。 如果您在Customer Journey Analytics報表中使用此資料集，或對其執行查詢，預計未來最多2小時的資料延遲會增加。

+++ 即將推出 — **下列資訊可能會變更**

* **Web應用程式防火牆(WAF) IP白名單** - Adobe Journey Optimizer現在支援登陸頁面的Web應用程式防火牆(WAF) IP白名單，可讓組織強制所有傳入要求都透過其設定的WAF基礎架構專門路由。 透過這項增強功能，客戶可設定Journey Optimizer以拒絕任何略過WAF層的直接請求，確保一致套用Imperva等工具中定義的安全性原則。 此功能可加強具有嚴格網路存取需求之企業的安全狀況，讓企業能夠完全控制其AJO託管登陸頁面的流量。

  推出日期：2026年6月底

+++

### 可用性改善 {#june-26-usability}

此版本即將推出下列可用性改善。

* **歷程與行銷活動的資料夾** — 您現在可以將歷程與行銷活動整理到&#x200B;**資料夾**，以改善介面中的導覽和管理。
