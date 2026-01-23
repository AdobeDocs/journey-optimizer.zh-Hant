---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 21231a10389a6238cff6d71966ce2bab8379ea59
workflow-type: tm+mt
source-wordcount: '2096'
ht-degree: 27%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="有哪幾種新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer] 遵循持續傳遞模式，允許 Adobe 持續傳遞新功能、增強功能和修正。此方法可讓您分階段推出可擴充的功能，以確保所有環境的效能和穩定性。

基於此模型，發行說明會在每月發行之間更新。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](releases.md)。

[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2026年1月發行前注意事項 {#latest-rn}

**發行日期**： 2026年1月27日

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。連結、畫面及更新的文件會在發行當日發佈於發行說明。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

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
<p><strong>注意</strong>：協調的行銷活動不支援無訊息時間。</p>
<p>此功能先前以「有限可用性」發行，現在可供所有環境使用。 在此「一般可用性」版本中，功能現在包括讓客戶將行銷活動動作排入佇列直到完成「無訊息時數」的能力，以及預覽啟用「無訊息時數」規則的能力。</p>
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
<p><strong>附註</strong>：尚未支援Web推播通知的靜音通知。</p>
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
<p>新的<strong>訊息匯出</strong>功能現在可用於電子郵件和簡訊頻道。 此功能可讓您將傳送的訊息內容自動匯出至專用的Experience Platform資料集，讓您能夠：</p>
<ul>
<li>符合法規合規性要求（例如HIPAA）</li>
<li>封存法律索償和客戶服務查詢的訊息</li>
<li>保留傳送給個人的個人化內容復本</li>
</ul>
<p>記錄會保留在AJO訊息匯出資料集中<strong>從內嵌</strong>起的7個日曆日。 在此保留期間，您可以透過Experience Platform目的地將資料匯出至您自己的儲存空間。 此功能會在通道設定層級啟用，讓您精確控制要匯出哪些訊息。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent — 建立歷程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Create Agent可讓Journey Optimizer使用者使用自然語言介面來建立和設定行銷歷程。 使用Journey Create Agent，從業人員可以在對話式提示中描述其需求，以快速建立歷程。 此代理程式可簡化歷程建立，讓行銷人員聚焦於策略而非技術設定。</p>
<p><a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">了解更多</a></p>
<p>推出日期： 2026年1月12日</p>
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
<p>推出日期：2025 年 11 月 5 日</p>
</td>
</tr>
</tbody>
</table>

### 改善 {#jan-26-01-improv}

以下列舉部分發布內容附上的改良功能。

#### AI

* **AI Assistant內容品質檢查** — 除了品牌一致性之外，您現在還可以評估整體<strong>內容品質</strong>，以找出可讀性、連貫性和有效性的潛在問題，不受品牌准則影響。 這些自動化檢查有助於識別不清楚的訊息、不一致的語調或結構性缺口。

* **使用新的顏色標籤更新品牌** — 品牌指引有助於確保您的品牌在所有接觸點上呈現一致。 新的<strong>色彩區段</strong>定義了您品牌色彩系統的標準，概述如何跨體驗選擇、組織和套用色彩。 它可確保主色、次色、輔色和中性色的一致使用，以支援有凝聚力、可存取且可辨識的品牌識別。

#### 行銷活動

* **使用設定檔時區排程行銷活動** — 行銷活動排程現在可以使用每個設定檔的<strong>時區</strong>，在預期的當地時間傳送訊息。 電子郵件、推播、簡訊、WhatsApp和LINE頻道都可使用設定檔時區進行排程。

  **注意**：這項改善僅適用於一組組織（可用性限制）。

#### 管道

* **SMS Webhooks：階段II** — 將提供的說明。

#### 電子郵件 Designer

* **在電子郵件設計工具中就地更正** — 使用您的品牌指引管理內容時，在內容驗證期間偵測到違規時，現在可以使用<strong>AI支援的自動內容建議</strong>。 如果內容標示為不符合品牌指導方針或品質標準，系統會主動產生修正的替代方案，以供線上檢閱和套用，進而改善法規遵循並加快生產速度。

#### 體驗決策

* **自助移轉工具API** — 提供一組新的<strong>移轉工具API</strong>，可將Offer Management實體移轉至Experience Decisioning。 此工具可讓您在沙箱之間無縫移轉，並具備相依性解析和復原功能。

* **將片段附加至決定專案** - Journey Optimizer現在提供將<strong>片段</strong>附加至決定專案的功能，這些決定專案可在程式碼型體驗行銷活動中透過決定原則運用。

  **注意**：先前以「有限可用性」發行，現在所有環境都可以使用此改善功能（一般可用性）。

#### 歷程

* **在歷程自訂動作中善用失敗回應承載** — 您現在可以為自訂動作定義選用的<strong>錯誤回應承載</strong>。 呼叫失敗時，錯誤裝載會公開於歷程內容中，並可在逾時/錯誤分支中使用，以支援更豐富的遞補邏輯和偵錯。

* **結合原生和Adobe Campaign訊息動作** - Journey Optimizer現在可讓您在同一歷程中結合Adobe Campaign v7/v8訊息動作和原生頻道動作。

* **歷程中的歷程裝載大小驗證** - Journey Optimizer現在提供<strong>裝載大小驗證</strong>，以協助確保最佳效能和系統穩定性。 當建置或發佈歷程時，如果裝載大小接近或超過建議的限制，您會收到明確的警告和錯誤，以及最佳化歷程設定的可操作指引。 此主動式驗證可幫助您儘早識別潛在問題並維護歷程績效。

* **歷程中的多個輸入動作** — 為簡化歷程協調，您現在可以在單一歷程中定義<strong>多個輸入動作</strong>。 此功能先前可用於行銷活動，可讓您同時向不同位置提供多個程式碼型體驗、應用程式內訊息、內容卡片或網頁動作，每個動作都包含特定內容。

  **注意**：先前以「有限可用性」發行，現在所有環境都可以使用此改善功能（一般可用性）。

#### 協調的行銷活動

* **選取屬性並複製發佈值** — 您現在可以直接從協調行銷活動的值發佈檢視中選取或複製值。

* **對象的資料使用標籤繼承** - <strong>在Adobe Experience Platform中套用的資料使用標籤</strong>現在會在將對象儲存在精心安排的行銷活動中時自動延續，減少手動DULE標籤。

* **預先定義的重新目標定位篩選器** — 為了支援更輕鬆地針對協調的行銷活動使用案例重新目標定位，此版本引進了新的<strong>重新目標定位篩選器</strong>。 這些篩選器可讓您根據訊息參與度（例如，已傳送、已開啟、已開啟或已按一下，或已開啟或已按一下）直接鎖定對象，以及選取您要重新鎖定目標的特定行銷活動或轉換中行銷活動。

* **具有引數的預先定義篩選器** — 您現在可以在協調的行銷活動中建立具有引數<strong>的</strong>篩選器，以供可重複使用、可編輯的規則使用。

* **傳送前的訊息確認** — 現在預設會在傳送協調的行銷活動前啟用<strong>確認步驟</strong>，以減少意外傳送。

* **使用者產生的中繼資料支援** - <strong>executionMetadata協助程式函式</strong>現在可在「協調的行銷活動」的個人化編輯器中使用，可讓您將內容相關資訊附加至任何原生動作，並將其儲存在資料集中，以匯出至外部系統。

* **重新啟動按鈕** — 協調的行銷活動現在包含<strong>重新啟動按鈕</strong>，您可以在發佈行銷活動之前，視需要快速重新啟動執行。

* **速率控制支援** — 協調的行銷活動現在支援<strong>速率控制</strong>，以協助您加速傳遞並符合數量限制。

#### 權限

* **防止自我核准歷程與行銷活動** — 您現在可以要求建立者無法核准自己的歷程或行銷活動，以改善<strong>核准工作流程中的職責分離</strong>。

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
<p>此功能將適用於所有環境（一般可用性）。</p>
<p>推出日期： 2026年2月3日</p>
</td>
</tr>
</tbody>
</table>
