---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d819b559e335ed743e1835edb170bca6e6653a4d
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 12%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="有哪幾種新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer] 遵循持續傳遞模式，允許 Adobe 持續傳遞新功能、增強功能和修正。此方法可讓您分階段推出可擴充的功能，以確保所有環境的效能和穩定性。

基於此模型，發行說明會在每月發行之間更新。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](releases.md)。

[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2026年1月發行說明 {#latest-rn}

**發行日期**： 2026年1月27至28日

[功能](#jan-26-01-features)和[改進](#jan-26-01-improv)區段涵蓋已提供的功能，而[即將推出](#jan-26-01-coming-soon)列出排程在稍後推出日期的專案。

<!-- **The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date. 

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### 新功能 {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Journey Agent — 建立歷程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent現在提供建立功能，可讓Journey Optimizer使用者透過<strong>自然語言介面</strong>建置及設定行銷歷程。 從業人員可以在對話式提示中描述其需求，以快速建立歷程。 這會簡化歷程建立流程，讓行銷人員聚焦於策略而非技術設定。</p>
<p>如需詳細資訊，請參閱<a href="../start/ai-features.md#journey-agent">詳細文件</a>。</p>
<p>推出日期： 2026年1月12日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>動作行銷活動擷取API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>新的API可讓您擷取動作行銷活動，並依關鍵屬性加以篩選，以支援自動化和報告工作流程。</p>
<p>如需詳細資訊，請參閱<a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">詳細文件</a>。</p>
<p>推出日期：2025 年 11 月 24 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程警報</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>新的歷程警報可幫助您監控關鍵歷程健康訊號。 此版本針對設定檔捨棄率、自訂動作錯誤率和設定檔錯誤率，以及歷程詳細目錄的可設定臨界值和歷程層級警報訂閱引入警報型別。</p>
<p>所有歷程的臨界值均為全域值。</p>
<p>如需詳細資訊，請參閱<a href="../reports/alerts.md">詳細文件</a>。</p>
<p>推出日期：2025 年 10 月 14 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>傳送Designer主題的電子郵件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>建立電子郵件內容時，在電子郵件Designer中使用可重複使用的主題套用一致的樣式。</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../email/apply-email-themes.md">詳細文件</a>。</p>
<p>此功能適用於一組組織的「有限可用性」中。 請聯絡您的 Adobe 代表。</p>
<p>推出日期：2025 年 11 月 5 日</p>
</td>
</tr>
</tbody>
</table>

### 改進 {#jan-26-01-improv}

#### 體驗決策

* **將片段附加至決定專案** - Journey Optimizer現在提供將<strong>片段</strong>附加至決定專案的功能，這可在透過決定原則的程式碼型體驗行銷活動中使用。 [閱讀全文](../experience-decisioning/items.md)

  **注意**：先前以「有限可用性」發行，現在所有環境都可以使用此改善功能（一般可用性）。

#### 歷程

* **在歷程自訂動作中善用失敗回應承載** — 您現在可以為自訂動作定義選用的<strong>錯誤回應承載</strong>。 當呼叫失敗時，錯誤裝載會公開於歷程內容中，並可在逾時/錯誤分支中與`jo_status_code`一併取得，以支援更豐富的遞補邏輯和偵錯。 [閱讀全文](../action/action-response.md)

* **結合原生和Adobe Campaign訊息動作** - Journey Optimizer現在可讓您在同一歷程中結合Adobe Campaign v7/v8訊息動作和原生頻道動作。 [閱讀全文](../building-journeys/using-adobe-campaign-v7-v8.md)

* **歷程中的歷程裝載大小驗證** - Journey Optimizer現在會驗證歷程裝載大小，以協助確保最佳效能和系統穩定性。 當建置或發佈歷程時，如果裝載大小接近或超過建議的限制，您會收到明確的警告和錯誤，以及最佳化歷程設定的可操作指引。 此主動式驗證可幫助您儘早識別潛在問題並維護歷程績效。 [閱讀全文](../start/guardrails.md#message-content-size)

#### 協調的行銷活動

* **選取屬性並複製發佈值** — 您現在可以直接從協調行銷活動的值發佈檢視中選取或複製值。 [閱讀全文](../orchestrated/build-query.md)

* **對象的資料使用標籤繼承** — 現在，在協調的行銷活動中儲存對象時，Adobe Experience Platform中套用的標籤會自動延續，減少手動DULE標籤。 [閱讀全文](../orchestrated/activities/save-audience.md)

* **預先定義的重新目標定位篩選器** — 為了支援更輕鬆地針對協調的行銷活動使用案例重新目標定位，此版本引進了新的<strong>行銷活動意見定位篩選器</strong>。 這些篩選器可讓您根據訊息參與度（例如，已傳送、已開啟、已開啟或已按一下，或已開啟或已按一下）直接鎖定對象，以及選取您要重新鎖定目標的特定行銷活動或轉換中行銷活動。 [閱讀全文](../orchestrated/retarget.md)

* **具有引數的預先定義篩選器** — 您現在可以在協調的行銷活動中建立具有<strong>引數</strong>的預先定義篩選器，以取得可重複使用、可編輯的規則。 [閱讀全文](../orchestrated/predefined-filters.md)

* **傳送前的訊息確認** — 現在預設會在傳送協調的行銷活動前啟用<strong>確認步驟</strong>，以減少意外傳送。 [閱讀全文](../orchestrated/activities/channels.md#confirm-message-sending)

* **使用者產生的中繼資料支援** - <strong>executionMetadata協助程式函式</strong>現在可在個人化編輯器中用於協調的行銷活動，讓您將內容相關資訊附加至任何原生動作，並將其儲存在資料集中，以匯出至外部系統。 [閱讀全文](../personalization/functions/helpers.md#execution-metadata)

* **重新啟動按鈕** — 協調的行銷活動現在包含<strong>重新啟動按鈕</strong>，您可以在發佈行銷活動之前，視需要快速重新啟動執行。 [閱讀全文](../orchestrated/start-monitor-campaigns.md)

* **速率控制支援** — 協調的行銷活動現在支援<strong>速率控制</strong>，以協助您加速傳遞並符合數量限制。 [閱讀全文](../orchestrated/activities/channels.md#rate-control)

#### 權限

* **防止自我核准歷程和行銷活動** — 新增在建立或設定核准原則時防止歷程或行銷活動建立者核准其自己的物件的選項。 [閱讀全文](../test-approve/approval-policies.md)

## 即將推出 {#jan-26-01-coming-soon}

下列功能和增強功能已排定在未來幾天發行。**資訊可能會有變更**。這些更新在生產環境上線後，更新的連結、畫面和文件將會共用。

### 功能

<table>
<thead>
<tr>
<th><strong>訊息匯出</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>電子郵件和簡訊通道將可使用新的<strong>訊息匯出</strong>功能。 此功能可讓您將傳送的訊息內容自動匯出至專用的Experience Platform資料集，讓您能夠：</p>
<ul>
<li>符合法規合規性要求（例如HIPAA）</li>
<li>封存法律索償和客戶服務查詢的訊息</li>
<li>保留傳送給個人的個人化內容復本</li>
</ul>
<p>記錄會保留在AJO訊息匯出資料集中7天之久，從內嵌開始算起。 在此保留期間，您可以透過Experience Platform目的地將資料匯出至您自己的儲存空間。 此功能會在通道設定層級啟用，讓您精確控制要匯出哪些訊息。</p>
<p>此功能僅適用於電子郵件和簡訊頻道，以及已購買訊息匯出附加元件的組織。 如需詳細資訊，請聯絡您的 Adobe 代表。</p>
<p>推出日期： 2026年1月28日</p>
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
<p>Adobe Journey Optimizer將支援<strong>網頁推播通知</strong>，將推播頻道擴展至行動裝置以外。 您將能夠傳送通知給行動版和案頭版瀏覽器，讓您直接在他們的裝置上聯絡客戶，而不需要應用程式。 此增強功能將協助您即時吸引使用者使用即時的個人化訊息，運用行動推播的現有相同製作工作流程和目標定位功能。</p>
<p>此功能先前在Beta中發行，現在可供所有環境使用（全面發佈）。</p>
<p>推出日期： 2026年1月28日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自助移轉工具API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>移轉工具API</strong>將可用於以程式設計方式將決定管理實體移轉到Decisioning，其功能：</p>
<ul>
<li>彈性的移轉範圍（沙箱、選件或決定層級）</li>
<li>自動化相依性分析和驗證</li>
<li>已完成移轉的復原支援</li>
<li>包含物件對應的詳細移轉報表</li>
</ul>
<p>推出日期： 2026年1月28日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>無訊息時數（基於時間的排除）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>無訊息小時可讓您定義電子郵件、簡訊、推播和WhatsApp頻道的<strong>時間型排除</strong>。 它們可確保在特定期間不會傳送任何訊息，協助您遵守客戶偏好設定和合規性要求。 您可以透過<strong>規則集</strong>套用無訊息時數，這些規則集可指派給行銷活動或歷程中的個別動作，以進行精確控制。</p>
<p>先前以「有限可用性」發行，此功能將適用於所有環境（一般可用性）。 透過此「一般可用性」版本，功能還包括將行銷活動動作排入佇列直到完成「無訊息時數」的能力，以及預覽啟用「無訊息時數」規則的能力。</p>
<p>推出日期： 2026年1月28日</p>
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
<p>先前僅限於行銷活動，歷程畫布上將提供<strong>直接郵件頻道</strong>，讓您可將直接郵件合併到歷程中。 批次和1:1歷程案例均支援直接郵件，具有檔案擷取設定和時間型頻率設定。</p>
<p>先前以「有限可用性」發行，此功能將適用於所有環境（一般可用性）。</p>
<p>推出日期： 2026年1月28日</p>
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
<p>直接郵件頻道將可在協調的行銷活動中使用。 <strong>直接郵件活動</strong>將促進直接郵件在您協調的行銷活動中傳送，一次性和循環性的郵件。 它將自動產生直接郵件提供者所需的<strong>擷取檔案</strong>。 您將能夠將頻道活動結合到協調的行銷活動畫布中，以建立跨頻道行銷活動，這會根據客戶行為和資料觸發動作。</p>
<p>推出日期： 2026年1月28日</p>
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
<p>透過新的<strong>監視儀表板</strong>和豐富的歷程步驟事件資料，您將能夠更深入瞭解insight的健康狀況和效能，以及您的自訂動作端點。 追蹤成功的呼叫、錯誤、輸送量、回應時間和佇列等待時間，以快速瞭解異常發生的時間、地點和原因。</p>
<p>先前以「有限可用性」發行，此功能將適用於所有環境（一般可用性）。</p>
<p>推出日期： 2026年1月28日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在Journey Agent中產生內容</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>由Adobe Experience Platform Agent Orchestrator提供技術支援，<strong>Journey Agent</strong>將在Journey Optimizer中提供，並可讓您透過自然語言介面分析歷程。 您將能夠直接在Journey Agent中產生和管理頻道特定內容、建立電子郵件和推播之類的頻道內容、套用和預覽範本、透過提示調整音調和風格，以及在<strong>內容Designer</strong>中開啟內容以進行內容內編輯。</p>
<p>推出日期：2026年2月2日</p>
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
<p>您將會使用<strong>決策</strong>個人化並最佳化推播和簡訊的內容。 使用決定原則、<strong>優先順序分數</strong>、公式或AI模型，向客戶顯示最佳內容。</p>
<p>推出日期： 2026年2月3日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>內容決活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程畫布中將提供新的<strong>內容決定活動</strong>，用於將個人化優惠直接整合到您的客戶歷程中。 此活動可讓您在整個歷程中、在建立資格型分支的條件、在用於將優惠資料傳遞至外部系統的自訂動作中，以及在建立完全個人化客戶體驗的其他活動中，提供決策型內容並參考這些優惠方案。</p>
<p>此功能將適用於所有環境（一般可用性）。</p>
<p>推出日期： 2026年2月3日</p>
</td>
</tr>
</tbody>
</table>

### 改進

* **AI Assistant內容品質檢查** — 除了品牌一致性之外，您還能評估整體<strong>內容品質</strong>，以找出可讀性、連貫性和有效性的潛在問題，不受品牌准則影響。 這些自動檢查將有助於識別不清楚的訊息、不一致的語調或結構性缺口。 推出日期：2026年1月28日。

* **使用新的顏色標籤更新品牌** — 品牌指引可協助確保您的品牌在所有接觸點上呈現一致。 新的<strong>色彩區段</strong>將定義您品牌色彩系統的標準，概述如何在體驗間選擇、組織和套用色彩。 它將確保一致地使用主要、次要、輔色和中性顏色，以支援有凝聚力、可存取和可辨識的品牌識別。 推出日期：2026年1月28日。

* 所有SMS提供者將支援&#x200B;**SMS Webhooks** - <strong>Webhooks</strong>。 您將能夠根據預期目的設定每個Webhook：擷取傳入訊息的傳入Webhook和回饋Webhook，以接收傳遞回條、狀態更新和其他訊息相關事件。 推出日期：2026年1月28日。

* **使用設定檔時區排程行銷活動** — 行銷活動排程將能夠使用每個設定檔的<strong>時區</strong>，在預期的當地時間傳送訊息。 **注意**：此改善功能僅適用於一組組織（可用性限制）。 推出日期：2026年1月28日。
