---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: eaf35e2c75bde0c8ce613b10fd7945cb707e1c7a
workflow-type: tm+mt
source-wordcount: '1839'
ht-degree: 19%

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

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### 新功能 {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>網頁推播通知頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer現在支援<strong>網頁推播通知</strong>，將推播頻道擴展至行動裝置以外。 您可以順暢地傳送通知給<strong>行動與案頭瀏覽器</strong>，讓您直接在他們的裝置上聯絡客戶，而不需要應用程式。 此增強功能可讓您運用行動推播中現有的相同製作工作流程和目標定位功能，透過即時的個人化訊息與使用者互動。</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>之前以 Beta 版本發行，目前此功能所有環境都適用 (一般可用性)。</p>
<p>如需詳細資訊，請參閱<a href="../push/push-configuration-web.md">詳細文件</a>。</p>
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
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../orchestrated/activities/channels.md#channel">詳細文件</a>。</p>
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
<p>Journey Agent現在提供建立功能，可讓Journey Optimizer使用者透過<strong>自然語言介面</strong>建置及設定行銷歷程。 使用這些新的技能，從業人員只需在<strong>對話提示</strong>中描述他們的需求，即可快速建立歷程。 這項創新簡化了歷程建立流程，讓行銷人員能夠專注於策略而非技術設定。</p>
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
<p>現在有新的Journey Optimizer API可供使用，可讓您以程式設計方式擷取及檢查<strong>促銷活動相關資料</strong>，例如詳細資料、版本和設定。</p>
<p>如需詳細資訊，請參閱<a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">詳細文件</a>。</p>
<p>推出日期：2025 年 11 月 24 日</p>
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
<p>您現在可以快速套用<strong>預先核准的主題</strong>，以確保所有電子郵件中的<strong>品牌一致性</strong>、加快行銷活動建立流程，以及獨立產生高品質電子郵件，同時減少對設計團隊的依賴。</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>此功能先前以 Beta 版發行，現在可供部分組織使用 (有限可用性)。若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>如需詳細資訊，請參閱<a href="../email/apply-email-themes.md">詳細文件</a>。</p>
<p>推出日期：2025 年 11 月 5 日</p>
</td>
</tr>
</tbody>
</table>

### 改進 {#jan-26-01-improv}

#### AI

* **AI助理內容品質檢查** — 除了品牌一致性之外，您現在還可以評估整體的<strong>內容品質</strong>，以找出潛在的<strong>可讀性</strong>、一致性和效能問題，不受品牌准則影響。 這些自動化檢查有助於識別不清楚的訊息、不一致的語調或結構性缺口。 [瞭解詳情](../content-management/brands-score.md#validate-quality)。 [在視訊中探索此功能](https://video.tv.adobe.com/v/3470557/?captions=chi_hant&learn=on)。

#### 體驗決策

* **將片段附加至決定專案** - Journey Optimizer現在提供將<strong>片段</strong>附加至<strong>決定專案</strong>的功能，這些功能可在透過決定原則的程式碼式體驗行銷活動中運用。 [閱讀全文](../experience-decisioning/items.md)

  **注意**：先前以「有限可用性」發行，現在所有環境都可以使用此改善功能（一般可用性）。

#### 歷程

* **結合原生和Adobe Campaign訊息動作** - Journey Optimizer現在可讓您在同一歷程中結合<strong>Adobe Campaign v7/v8</strong>訊息動作和<strong>原生頻道動作</strong>。 [閱讀全文](../building-journeys/using-adobe-campaign-v7-v8.md)

* **自訂動作錯誤回應承載** — 您現在可以為自訂動作定義選用的<strong>錯誤回應承載</strong>。 呼叫失敗時，錯誤裝載會公開於歷程內容（在動作的errorResponse節點下），並可與<strong>一併提供於</strong>逾時/錯誤分支`jo_status_code`，以支援更豐富的遞補邏輯和偵錯。 [閱讀全文](../action/action-response.md)

* **歷程中的歷程裝載大小驗證** - Journey Optimizer現在會驗證<strong>裝載大小</strong>，以協助確保最佳效能和系統穩定性。 當建置或發佈歷程時，如果裝載大小接近或超過建議的限制，您會收到明確的<strong>警告和錯誤</strong>，並提供可操作的指引，以最佳化您的歷程設定。 此主動式驗證可幫助您儘早識別潛在問題並維護歷程績效。 [閱讀全文](../start/guardrails.md#journey-payload-size)

* **歷程警示** — 有新的<strong>預先設定的警示</strong>可供歷程使用。
   * <strong>超過設定檔捨棄率</strong> — 超過臨界值的最後5分鐘內，捨棄設定檔與輸入設定檔的比率
   * <strong>超出自訂動作錯誤率</strong> — 過去5分鐘超出臨界值的自訂動作錯誤與成功HTTP呼叫的比率
   * <strong>超過的設定檔錯誤率</strong> — 在過去5分鐘超過臨界值的設定檔錯誤率

  如需詳細資訊，請參閱[詳細文件](../reports/alerts.md)。

  推出日期：2025年10月14日。

#### 協調的行銷活動

* **對象的資料使用標籤繼承** — 現在，在協調的行銷活動中儲存<strong>對象</strong>時，Adobe Experience Platform中套用的標籤會自動延續，減少手動<strong>DULE標籤</strong>。 [閱讀全文](../orchestrated/activities/save-audience.md)

* **含引數的預先定義篩選器** — 您現在可以在協調的行銷活動中建立<strong>含</strong>引數<strong>的預先定義篩選器</strong>，以取得可重複使用、可編輯的規則。 [閱讀全文](../orchestrated/predefined-filters.md)

* **選取屬性並複製發佈值** — 您現在可以直接從協調行銷活動中的<strong>值分佈</strong>檢視<strong>選取或複製值</strong>。 [閱讀全文](../orchestrated/build-query.md)

* **傳送前的訊息確認** — 現在預設會在傳送協調的行銷活動前啟用<strong>確認步驟</strong>，以減少意外傳送。 [閱讀全文](../orchestrated/activities/channels.md#confirm-message-sending)

* **預先定義的重新目標定位篩選器** — 為了支援更輕鬆地針對協調的行銷活動使用案例重新目標定位，此版本引進了新的<strong>行銷活動意見定位篩選器</strong>。 這些篩選器可讓您根據<strong>訊息參與</strong> （例如已傳送、僅開啟、已開啟或已按一下，或已開啟或已按一下）直接鎖定對象，並選取您要重新鎖定目標的特定行銷活動或轉換中行銷活動。 [閱讀全文](../orchestrated/retarget.md)

* **速率控制支援** — 協調的行銷活動現在支援<strong>速率控制</strong>，協助您加速傳遞並符合<strong>數量限制</strong>。 [閱讀全文](../orchestrated/activities/channels.md#rate-control)

* **重新啟動按鈕** — 協調的行銷活動現在包含<strong>重新啟動按鈕</strong>，因此您可以在發佈行銷活動之前，視需要快速<strong>重新啟動執行</strong>。 [閱讀全文](../orchestrated/start-monitor-campaigns.md)

* **使用者產生的中繼資料支援** - <strong>executionMetadata協助程式函式</strong>現在可在協調行銷活動的個人化編輯器中使用，可讓您將內容相關資訊附加至任何原生動作，並將其儲存在資料集中，以匯出至外部系統。 [閱讀全文](../personalization/functions/helpers.md#execution-metadata)

#### 權限

* **防止自我核准歷程與行銷活動** — 新增建立或設定<strong>核准原則</strong>時的選項，以防止歷程或行銷活動建立者將<strong>核准自己的物件</strong>。 [閱讀全文](../test-approve/approval-policies.md)

## 即將推出 {#jan-26-01-coming-soon}

下列功能和增強功能已排定在未來幾天發行。**資訊可能會有變更**。這些更新在生產環境上線後，更新的連結、畫面和文件將會共用。

### 功能

<table>
<thead>
<tr>
<th><strong>歷程中的直接郵件頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>以前僅限於行銷活動，現在歷程畫布上提供<strong>直接郵件</strong>頻道，可讓您將直接郵件合併到歷程中。 直接郵件現在可同時用於<strong>批次和1:1歷程案例</strong>，並支援檔案擷取設定和時間頻率設定。</p>
<p>先前以「有限可用性」發行，此功能將適用於所有環境（一般可用性）。</p>
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
<p><strong>無訊息時數</strong>可讓您定義電子郵件、簡訊、推播和WhatsApp頻道的時間型排除專案。 它們可確保在特定時段內不會傳送任何訊息，協助您遵守客戶偏好設定和合規性要求。 您可以透過<strong>規則集</strong>套用無訊息時數，這些規則集可指派給行銷活動或歷程中的個別動作，以進行精確控制。</p>
<p>此功能先前以「有限可用性」發行，現在可供所有環境使用。 在此「一般可用性」版本中，功能現在包括讓客戶將行銷活動動作排入佇列直到完成「無訊息時數」的能力，以及預覽啟用「無訊息時數」規則的能力。</p>
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
<p><strong>移轉工具API</strong>現在可用於以程式設計方式將決定管理實體移轉到Decisioning，功能：</p>
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
<th><strong>自訂動作監視</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過新的監視儀表板和豐富的歷程步驟事件資料，更深入瞭解insight在<strong>自訂動作端點</strong>的健全狀況和效能。 追蹤成功的呼叫、錯誤、輸送量、回應時間和佇列等待時間，以快速瞭解異常發生的時間、地點和原因。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p>推出日期： 2026年1月28日</p>
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
<p>記錄會保留在AJO訊息匯出資料集中7天之久，從內嵌開始算起。 在此保留期間，您可以透過Experience Platform目的地將資料匯出至您自己的儲存空間。 此功能已在通道設定層級啟用，可讓您對要匯出的訊息進行<strong>精細控制</strong>。</p>
<p>此功能僅適用於電子郵件和簡訊頻道，以及已購買訊息匯出附加元件的組織。 如需詳細資訊，請聯絡您的 Adobe 代表。</p>
<p>推出日期：2026年1月30日</p>
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
<p>由Adobe Experience Platform Agent Orchestrator提供技術支援，<strong>Journey Agent</strong>可在Journey Optimizer中使用，並可讓您透過自然語言介面分析歷程。 您現在也可以直接在Journey Agent中<strong>產生和管理內容</strong>、建立電子郵件和推播之類的管道內容、套用和預覽範本、透過提示調整色調和風格，以及在內容Designer中開啟內容以進行內容內編輯。</p>
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
<p>您現在可以使用<strong>決策</strong>個人化並最佳化<strong>推播和SMS</strong>訊息的內容。 使用優先順序分數、公式或AI模型，向客戶顯示最佳內容。</p>
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
<p>歷程畫布現在提供新的<strong>內容決定活動</strong>，以便將<strong>個人化優惠</strong>直接整合至您的客戶歷程。 此活動可讓您提供決策型內容，並在整個歷程中參考這些優惠方案 — 在建立資格型分支的條件、在自訂動作中將優惠方案資料傳遞至外部系統，以及在其他活動中建立完全個人化的客戶體驗。</p>
<p>此功能將適用於所有環境（一般可用性）。</p>
<p>推出日期： 2026年2月3日</p>
</td>
</tr>
</tbody>
</table>

### 改進

* **使用設定檔時區排程行銷活動** — 行銷活動排程現在可以使用每個設定檔的<strong>時區</strong>，在預期的當地時間傳送訊息。

  **注意**：此改善功能僅適用於一組組織（可用性限制）。

  推出日期：2026年1月29日。

* 所有SMS提供者現在都支援&#x200B;**SMS Webhook** - <strong>Webhook</strong>。 您可以根據每個Webhook的預期用途、入站Webhook來設定以擷取傳入訊息，以及回饋Webhook來接收傳遞回條、狀態更新和其他訊息相關事件。

  推出日期：2026年1月28日。
