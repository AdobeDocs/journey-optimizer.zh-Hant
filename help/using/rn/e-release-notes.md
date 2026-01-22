---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 3d9316e3a42696c4e944ec23b0300e56b07142c2
workflow-type: tm+mt
source-wordcount: '2342'
ht-degree: 21%

---

# 搶鮮版發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能增強並修正錯誤。所有變更都會在每月底整合於[發行說明](release-notes.md)。


## 2026年1月發行前注意事項 {#jan-26-01-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。連結、畫面及更新的文件會在發行當日發佈於發行說明。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**： 2026年1月26日

### 全新功能 {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>歷程中的動作活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer支援新的通用<strong>動作活動</strong>，可讓您設定單一動作和<strong>多重動作傳入動作群組</strong>，以簡化歷程畫布中的動作設定。 尤其是這項新功能允許：</p>
<ul>
<li>簡化歷程畫布中的原生動作設定。</li>
<li>容量用來建立多動作傳入動作群組。</li>
<li>能夠將最佳化新增至任何內建管道動作。</li>
<li>能夠將實驗與多語言選項新增至任何動作。</li>
</ul>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13290">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">產品JIRA工作的連結</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自訂動作監視</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過新的<strong>監控儀表板</strong>和豐富的歷程步驟事件資料，更深入瞭解insight的健康狀況和效能，讓您瞭解自訂動作端點。 追蹤成功的呼叫、錯誤、輸送量、回應時間和佇列等待時間，以快速瞭解異常發生的時間、地點和原因。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13981">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-126869">產品JIRA工作的連結</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>勿打擾時間/不接收訊息的時間</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>無訊息小時可讓您定義電子郵件、簡訊、推播和WhatsApp頻道的<strong>時間型排除</strong>。 它們可確保在特定時段內不會傳送任何訊息，協助您遵守客戶偏好設定和合規性要求。 您可以透過<strong>規則集</strong>套用無訊息時數，這些規則集可指派給行銷活動或歷程中的個別動作，以進行精確控制。</p>
<p>此功能先前以「有限可用性」發行，現在可供所有環境使用。 在此「一般可用性」版本中，功能現在包括讓客戶將行銷活動動作排入佇列直到完成「無訊息時數」的能力，以及預覽啟用「無訊息時數」規則的能力。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13986">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-63912">產品JIRA工作的連結</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程中的直接郵件頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>以前僅限行銷活動使用<strong>直接郵件頻道</strong>，現在可在<strong>歷程畫布</strong>上使用，讓您將直接郵件合併到歷程中。 直接郵件現在可用於批次和1:1歷程情境，並支援檔案擷取設定和時間型頻率設定。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13543">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-38399">產品JIRA工作的連結</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>網頁推播通知頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer現在支援<strong>網頁推播通知</strong>，將推播頻道擴展至行動裝置以外。 您可以順暢地將通知傳送至行動瀏覽器和案頭瀏覽器，讓您無需應用程式即可直接在其裝置上聯絡客戶。 此增強功能可讓您運用行動推播中現有的相同製作工作流程和目標定位功能，透過即時的個人化訊息與使用者互動。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13581">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-37866">產品JIRA工作的連結</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>推播和簡訊通道中的決策支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將<strong>決定原則</strong>新增至推播和SMS歷程與行銷活動中。 決策原則是優惠方案的容器，可運用決策引擎以動態方式傳回最佳內容，傳送給每個對象成員。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13426">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/DOCAC-13425">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55817">產品JIRA工作的連結</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55818">產品JIRA工作的連結</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>協調行銷活動中的直接郵件頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，直接郵件頻道可用於協調的行銷活動。 <strong>直接郵件活動</strong>可促進直接郵件在協調的行銷活動內傳送，一次性和循環性的郵件。 它用於自動化產生直接郵件提供者所需的<strong>擷取檔案</strong>的程式。 您可以將管道活動與協調式行銷活動版面結合，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13379">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-82584">產品JIRA工作的連結</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>忠誠度應用程式的新來源連接器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform現在提供新的<strong>來源聯結器</strong>，適用於Talon.One、Chariceline和Kobie忠誠度應用程式。 這些連接器可讓您將忠誠度資料順暢地串流至 Adobe Experience Platform，並在 Journey Optimizer 中利用這些資料。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13372">連結到DOCAC JIRA任務</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>訊息匯出</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在可以<strong>將已傳送的傳遞</strong>匯出至特定資料集，以用於封存和法規遵循目的。 此容量不僅適用於電子郵件，也適用於其他管道，例如簡訊。 訊息匯出資料集的資料保留期現在為<strong>7天</strong>。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12915">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105313">產品JIRA工作的連結</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>用於擷取動作行銷活動的新 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現已提供新的<strong>Journey Optimizer API</strong>，可讓您以程式設計方式擷取及檢查行銷活動相關資料，例如詳細資料、版本和設定。</p>
<p>如需詳細資訊，請參閱<a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">詳細文件</a>。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13506">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-96195">產品JIRA工作的連結</a></p>
<p>推出日期：2025 年 11 月 24 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>新歷程警示</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>三個新的<strong>歷程警示</strong>現在可供協助您監視及追蹤歷程生命週期事件和自訂動作效能：</p>
<ul>
<li><strong>歷程已發佈</strong>：當操作者歷程版面中發佈歷程時，會收到通知。</li>
<li><strong>歷程已完成</strong>：歷程完成時收到警示，並根據歷程類型有特定定義 (讀取客群或事件觸發)。</li>
<li><strong>自訂動作上限已觸發</strong>：在自訂動作端點上啟用上限時，會收到通知。</li>
</ul>
<p>這些警示可在組織層級訂閱或針對特定歷程訂閱。</p>
<p>如需詳細資訊，請參閱<a href="../reports/alerts.md#journey-alerts">詳細文件</a>。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13465">連結到DOCAC JIRA任務</a></p>
<p>推出日期：2025 年 11 月 5 日</p>
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
<p>您現在可以快速套用<strong>預先核准的主題</strong>，以確保所有電子郵件中的品牌一致性、加快行銷活動建立流程，以及獨立產生高品質電子郵件，同時減少對設計團隊的依賴。</p>
<p>此功能先前以 Beta 版發行，現在可供部分組織使用 (有限可用性)。若想取得存取權，請聯絡您的 Adobe 代表。</p>
<img src="assets/do-not-localize/themes.gif">
<p>如需詳細資訊，請參閱<a href="../email/apply-email-themes.md">詳細文件</a>。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12941">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/NEO-88838">產品JIRA工作的連結</a></p>
<p>推出日期：2025 年 11 月 5 日</p>
</td>
</tr>
</tbody>
</table>

### 改善 {#jan-26-01-improv}

以下列舉部分發布內容附上的改良功能。

#### AI

* **AI Assistant內容品質檢查** — 除了品牌一致性之外，您現在還可以評估整體<strong>內容品質</strong>，以找出可讀性、連貫性和有效性的潛在問題，不受品牌准則影響。 這些自動化檢查有助於識別不清楚的訊息、不一致的語調或結構性缺口。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13917">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-103238">產品JIRA工作的連結</a>
* **使用新的顏色標籤更新品牌** — 品牌指引有助於確保您的品牌在所有接觸點上呈現一致。 新的<strong>色彩區段</strong>定義了您品牌色彩系統的標準，概述如何跨體驗選擇、組織和套用色彩。 它可確保主色、次色、輔色和中性色的一致使用，以支援有凝聚力、可存取且可辨識的品牌識別。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13811">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-121183">產品JIRA工作的連結</a>

#### 行銷活動

* **使用設定檔時區排程行銷活動** — 行銷活動排程現在可以使用每個設定檔的<strong>時區</strong>，在預期的當地時間傳送訊息。

  **注意**：這項改善僅適用於一組組織（可用性限制）。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-11534">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-43782">產品JIRA工作的連結</a>

#### 管道

* **SMS Webhooks：階段II** — 將提供的說明。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13978">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-93914">產品JIRA工作的連結</a>

* **WhatsApp轉售選件** — 提供說明。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13669">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-86420">產品JIRA工作的連結</a>

#### 電子郵件 Designer

* **電子郵件設計工具中的就地更正** - <strong>AI支援的自動內容建議</strong>現在可在電子郵件Designer中在內容驗證期間偵測到違規時取得。 如果內容標示為不符合品牌指導方針或品質標準，系統會主動產生修正的替代方案，以供線上檢閱和套用，進而改善法規遵循並加快生產速度。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13979">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95365">產品JIRA工作的連結</a>

#### 體驗決策

* **歷程仲裁** — 您現在可以使用<strong>公式和AI模型</strong>，根據客戶設定檔屬性和情境因素自動提升歷程優先順序分數，確保客戶進入最相關的歷程。

  **注意**：這項改善僅適用於一組組織（可用性限制）。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13976">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-78932">產品JIRA工作的連結</a>

* **exd沙箱工具檔案 — 更新** — 提供說明。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13596">連結到DOCAC JIRA工作</a>

* **自助移轉工具API** — 提供一組新的<strong>移轉工具API</strong>，可將Offer Management實體移轉至Experience Decisioning。 此工具可讓您在沙箱之間無縫移轉，並具備相依性解析和復原功能。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13837">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-109695">產品JIRA工作的連結</a>

* **將片段附加至決定專案** - Journey Optimizer現在提供將<strong>片段</strong>附加至決定專案的功能，這些決定專案可在程式碼型體驗行銷活動中透過決定原則運用。

  **注意**：先前以「有限可用性」發行，現在所有環境都可以使用此改善功能（一般可用性）。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13418">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-110282">產品JIRA工作的連結</a>

#### 歷程

* **在歷程自訂動作中善用失敗回應承載** — 您現在可以為自訂動作定義選用的<strong>錯誤回應承載</strong>。 呼叫失敗時，錯誤裝載會公開於歷程內容中，並可在逾時/錯誤分支中使用，以支援更豐富的遞補邏輯和偵錯。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13977">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113125">產品JIRA工作的連結</a>

* **結合原生和Adobe Campaign訊息動作** - Journey Optimizer現在可讓您在同一歷程中結合Adobe Campaign v7/v8訊息動作和原生頻道動作。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13974">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113103">產品JIRA工作的連結</a>

* **歷程中的歷程裝載大小驗證** - Journey Optimizer現在提供<strong>裝載大小驗證</strong>，以協助確保最佳效能和系統穩定性。 當建置或發佈歷程時，如果裝載大小接近或超過建議的限制，您會收到明確的警告和錯誤，以及最佳化歷程設定的可操作指引。 此主動式驗證可幫助您儘早識別潛在問題並維護歷程績效。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13840">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-122236">產品JIRA工作的連結</a>

* **歷程中的多個輸入動作** — 為簡化歷程協調，您現在可以在單一歷程中定義<strong>多個輸入動作</strong>。 此功能先前可用於行銷活動，可讓您同時向不同位置提供多個程式碼型體驗、應用程式內訊息、內容卡片或網頁動作，每個動作都包含特定內容。

  **注意**：先前以「有限可用性」發行，現在所有環境都可以使用此改善功能（一般可用性）。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13453">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">產品JIRA工作的連結</a>

#### 協調的行銷活動

* **選取屬性並複製發佈值** — 您現在可以直接從協調行銷活動的值發佈檢視中選取或複製值。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13973">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105244">產品JIRA工作的連結</a>

* **對象的資料使用標籤繼承** - <strong>在Adobe Experience Platform中套用的資料使用標籤</strong>現在會在將對象儲存在精心安排的行銷活動中時自動延續，減少手動DULE標籤。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13972">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-120769">產品JIRA工作的連結</a>

* **預先定義的重新目標定位篩選器** — 為了支援更輕鬆地針對協調的行銷活動使用案例重新目標定位，此版本引進了新的<strong>重新目標定位篩選器</strong>。 這些篩選器可讓您根據訊息參與度（例如，已傳送、已開啟、已開啟或已按一下，或已開啟或已按一下）直接鎖定對象，以及選取您要重新鎖定目標的特定行銷活動或轉換中行銷活動。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13971">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-116701">產品JIRA工作的連結</a>

* **具有引數的預先定義篩選器** — 您現在可以在協調的行銷活動中建立具有引數<strong>的</strong>篩選器，以供可重複使用、可編輯的規則使用。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13970">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-115431">產品JIRA工作的連結</a>

* **傳送前的訊息確認** — 現在預設會在傳送協調的行銷活動前啟用<strong>確認步驟</strong>，以減少意外傳送。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13927">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-87219">產品JIRA工作的連結</a>

* **使用者產生的中繼資料支援** - <strong>executionMetadata協助程式函式</strong>現在可在「協調的行銷活動」的個人化編輯器中使用，可讓您將內容相關資訊附加至任何原生動作，並將其儲存在資料集中，以匯出至外部系統。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13923">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-112697">產品JIRA工作的連結</a>

* **重新啟動按鈕** — 協調的行銷活動現在包含<strong>重新啟動按鈕</strong>，您可以在發佈行銷活動之前，視需要快速重新啟動執行。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13920">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-106020">產品JIRA工作的連結</a>

* **速率控制支援** — 協調的行銷活動現在支援<strong>速率控制</strong>，以協助您加速傳遞並符合數量限制。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13764">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113254">產品JIRA工作的連結</a>

#### 權限

* **防止自我核准歷程與行銷活動** — 您現在可以要求建立者無法核准自己的歷程或行銷活動，以改善<strong>核准工作流程中的職責分離</strong>。
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13472">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99957">產品JIRA工作的連結</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95676">產品JIRA工作的連結</a>

## 即將推出 {#jan-26-01-coming-soon}

下列功能和增強功能已排定在未來幾天發行。**資訊可能會有變更**。這些更新在生產環境上線後，更新的連結、畫面和文件將會共用。

<table>
<thead>
<tr>
<th><strong>在Journey Agent中產生內容</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>由Adobe Experience Platform Agent Orchestrator提供技術支援，<strong>Journey Agent</strong>可在Journey Optimizer中使用，並可讓您透過自然語言介面分析歷程。 您現在也可以直接在Journey Agent中產生和管理管道專用內容，為電子郵件和推播等管道建立內容，套用和預覽範本，透過提示調整色調和風格，以及在內容Designer中開啟內容以進行內容內嵌編輯。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13980">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111882">產品JIRA工作的連結</a></p>
<p>推出日期：2026年2月2日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>內容決定活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以透過歷程畫布中的專屬內容決定活動，在歷程中加入<strong>個人化優惠</strong>，並在歷程活動（包括條件和自訂動作）中使用這些優惠。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12902">連結到DOCAC JIRA工作</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99223">產品JIRA工作的連結</a></p>
<p>推出日期：2026年2月2日</p>
</td>
</tr>
</tbody>
</table>
