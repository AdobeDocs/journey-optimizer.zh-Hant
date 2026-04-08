---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明2026年
description: Journey Optimizer 2026 年發行說明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 65ca94cf-8e17-4a25-90f3-238083f81477
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '2525'
ht-degree: 62%

---

# 發行說明 2026 年 {#release-notes-2026}

此頁面列出了於 2026 年發行的所有 [!DNL Journey Optimizer] 功能和改善。



## 2026年2月發行說明 {#feb-26-01-rn}

### 全新功能 {#feb-26-01-features}


<table>
<thead>
<tr>
<th><strong>歷程仲裁</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用<strong>排名公式</strong>，根據客戶設定檔屬性和內容因素，自動提升歷程優先順序分數，確保客戶進入最相關的歷程。</p>
<p><img src="assets/do-not-localize/journey-arbitration-formulas.gif"/></p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>如需詳細資訊，請參閱<a href="../conflict-prioritization/journey-ranking-formulas.md">詳細文件</a>。</p>
<p>推出日期： 2026年2月24日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程中的動作活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer支援新的通用<strong>動作活動</strong>，可讓您設定單一動作和多動作傳入動作群組，以簡化歷程畫布中的動作設定。 尤其是這項新功能允許：</p>
<ul>
<li>簡化歷程畫布中的原生動作設定。</li>
<li>容量用來建立多動作傳入動作群組。</li>
<li>能夠將最佳化新增至任何內建管道動作。</li>
<li>能夠新增實驗和多語言選項至任何動作。</li>
</ul>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-action.md">詳細文件</a>。</p>
<p>推出日期：2026年2月20日</p>
<p><strong>注意：</strong>所有原生頻道現在都可透過動作歷程活動存取。 舊版原生管道活動將在3月版本中停用。 包含舊版動作的現有歷程仍可繼續正常運作，無需移轉。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>傳出訊息的波動傳送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以排程來自Journey Optimizer行銷活動或歷程的訊息，以控管批次方式隨時間傳遞。</p>
<p>波次傳送提供下列優點：</p>
<ul>
<li>更好的可遞送性 — 隨著時間推移分散式傳送，以協助維持強大的傳送者信譽，並降低被標籤為垃圾訊息的風險。</li>
<li>載入控制 — 透過限制同時傳出的訊息數量，避免讓下游系統（例如呼叫中心、登陸頁面）不堪重負。</li>
<li>大量且有時效性的使用案例 — 適合大型對象，或您需要控制時機時（例如客服中心容量、加電或有時限的選件）。</li>
</ul>
<p><img src="assets/do-not-localize/waves.gif"/></p>
<p>在<strong>行銷活動</strong>中，此功能適用於所有環境（一般可用性）。 如需詳細資訊，請參閱<a href="../campaigns/send-using-waves.md">詳細文件</a>。</p>

<p>在<strong>歷程</strong>中，此功能僅適用於一組組織（可用性限制） — 若要取得存取權，請聯絡您的Adobe代表。 如需詳細資訊，請參閱<a href="../building-journeys/send-using-waves.md">詳細文件</a>。</p>
<p>推出日期： 2026年2月19日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>將子網域移轉至自訂委派</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以從介面使用CNAME委派模式將子網域移轉至自訂委派，這樣您就可以符合公司指引的更嚴格安全性原則，而無需重新建立通道設定。</p>
<p><img src="assets/do-not-localize/subdomain-migration.gif"/></p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/custom-subdomain-migration.md">詳細文件</a>。</p>
<p>推出日期： 2026年2月19日</p>
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
<p>Adobe Journey Optimizer現在支援<strong>網頁推播通知</strong>，將推播通道擴充至行動裝置以外。 您可以順暢地將通知傳送至<strong>行動瀏覽器和桌面瀏覽器</strong>，讓您無需應用程式即可直接在其裝置上聯絡客戶。此增強功能可讓您運用行動推播中現有的相同製作工作流程和目標定位功能，透過即時的個人化訊息與使用者互動。</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>此功能先前在Beta中發行，現在可供所有環境使用（全面發佈）。</p>
<p>如需詳細資訊，請參閱<a href="../push/push-configuration-web.md">詳細文件</a>。</p>
<p>推出日期： 2026年2月13日</p>
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
<p>歷程畫布現在提供新的<strong>內容決定活動</strong>，可將個人化優惠直接整合至您的客戶歷程。 此活動可讓您提供決策型內容，並在整個歷程中參考這些優惠方案 — 在建立資格型分支的條件、在自訂動作中將優惠方案資料傳遞至外部系統，以及在其他活動中建立完全個人化的客戶體驗。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/content-decision.md">詳細文件</a>。</p>
<p>推出日期：2026年2月10日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自助移轉工具 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>移轉工具API現在可用於以程式設計方式將<strong>決定管理</strong>實體移轉到<strong>決定</strong>，其功能：</p>
<ul>
<li>彈性的移轉範圍 (沙箱、產品建議或決策層級)</li>
<li>自動化相依性分析和驗證</li>
<li>已完成移轉的復原支援</li>
<li>包含物件對應的詳細移轉報表</li>
</ul>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/decisioning-migration-api.md">詳細文件</a>。</p>
<p>推出日期：2026 年 2 月 3 日</p>
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
<p>透過新的監視儀表板和豐富的歷程步驟事件資料，更深入瞭解insight的健康狀況和效能，讓您瞭解自訂動作端點。 追蹤成功的呼叫、錯誤、輸送量、回應時間和佇列等待時間，以快速瞭解異常情況發生的時間、地點和原因。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p>如需詳細資訊，請參閱<a href="../action/reporting.md">詳細文件</a>。</p>
<p>推出日期：2026 年 2 月 3 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>簡訊頻道中的決策支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用Decisioning個人化及最佳化SMS訊息內容。 使用優先順序分數、公式或 AI 模型，向客戶顯示最佳內容。</p>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/create-decision.md">詳細文件</a>。</p>
<p>推出日期：2026 年 2 月 2 日</p>
</td>
</tr>
</tbody>
</table>

### 改善 {#feb-26-01-improv}

以下列舉部分發布內容附上的改良功能。

#### 設定

* **歷程運算式中的體驗事件使用方式** — 自2026年4月1日起，過去90天內未使用此功能的組織將不再支援在歷程運算式中使用體驗事件屬性。 自2025年7月8日起，新客戶組織已無法使用此功能。 如需其他選擇，請參閱歷程中的[體驗事件查閱](../building-journeys/exp-event-lookup.md)。

#### 內容管理

<!--
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors</strong> section defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity. [Read more](../content-management/brands.md)
-->

* **使用主題將影像轉換為電子郵件範本** — 在Journey Optimizer中將影像轉換為電子郵件範本時，您現在可以使用主題作為輸入，讓產生的HTML遵循您的品牌引數。 系統會自動套用背景顏色、按鈕顏色、字型、行距、邊界及邊框間距等樣式，減少手動設計工作，並提供可立即使用且只需少量編輯的範本。 [閱讀全文](../content-management/image-to-html.md)

  推出日期：2026年2月17日。

<!--* **Text mode for fragments** - You can now create and manage text versions of your fragments, supporting workflows that rely on plain text content and providing the same flexibility as in email content. [Read more](../content-management/create-fragments.md)-->

#### 電子郵件設計工具

* **文字縮排** — 您現在可以直接從屬性面板將可自訂的左縮排套用至文字元件中的第一行段落。 <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. -->這可以改善長篇內容（例如編輯和文章）的可讀性。 [閱讀全文](../email/get-started-email-style.md)

  推出日期：2026年2月18日。

#### 決策

* **在決定中使用Adobe Experience Platform資料的Edge傳入支援** — 在決定中使用Adobe Experience Platform資料時，除了歷程中的電子郵件和自訂動作之外，現在還能支援邊緣傳入使用案例。 [閱讀全文](../experience-decisioning/aep-data-exd.md)

  此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。

* **程式碼型體驗管道中的決策預覽** — 您現在可以在使用程式碼型體驗管道設定決策時預覽決策專案。 上線之前，可以直接在編寫介面中使用預覽。 [閱讀全文](../code-based/test-code-based.md#preview-code-based)

  推出日期： 2026年2月18日

<!--
THIS WAS FINALLY NOT RELEASED IN FEBRUARY

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach fragments to decision items which can be leveraged in code-based experience campaigns through decision policies. [Read more](../experience-decisioning/fragments-decision-policies.md)

  Previously released in Limited Availability, this capability is now available to all environments (General Availability).

  Availability date: February 12, 2026.
-->

#### 個人化

* **執行中繼資料協助程式** - `executionMetadata`協助程式函式現在可供所有Journey Optimizer客戶使用。 使用此外掛程式來動態附加內容資訊至任何原生動作，並在資料集中擷取該資訊，以匯出至外部系統。 [閱讀全文](../personalization/functions/helpers.md#execution-metadata)

  此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。

  推出日期：2026年2月20日。

#### 簡訊

* **SMS Webhook** — 所有SMS提供者現在都支援Webhook。 您可以根據每個Webhook的預期用途進行設定：傳入Webhook以擷取傳入訊息，反饋Webhook以接收傳遞回條、狀態更新和其他訊息相關事件。 [閱讀全文](../sms/sms-webhook.md)

  推出日期：2026年2月2日。



## 2026 年 1 月發行說明 {#jan-26-rn}

<!--**Release date**: January 27-28, 2026-->

### 全新功能 {#jan-26-01-features}


<table>
<thead>
<tr>
<th><strong>推播頻道中的決策支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用<strong>決策</strong>個人化和最佳化<strong>推播通知</strong>的內容。 使用優先順序分數、公式或 AI 模型，向客戶顯示最佳內容。</p>
<p>具有推播通知的Experience Decisioning需要特定版本的Mobile SDK。 在實作此功能之前，請檢查<a href="https://developer.adobe.com/client-sdks/home/release-notes/" target="_blank">發行說明</a>以識別所需的版本，並確定您已相應地升級。 您也可以在<a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions/" target="_blank">本節</a>中檢視您平台的所有可用SDK版本。</p>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/create-decision.md">詳細文件</a>。</p>
<p>推出日期：2026 年 1 月 30 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程中的直接郵件管道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>以前僅限於行銷活動，現在歷程畫布上也提供<strong>直接郵件</strong>管道，可讓您將直接郵件整合到歷程中。直接郵件現在可同時用於<strong>批次和 1:1 歷程案例</strong>，並支援檔案擷取設定和時間頻率設定。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><img src="assets/do-not-localize/dm-journey.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../direct-mail/get-started-direct-mail.md">詳細文件</a>。</p>
<p>推出日期： 2026年1月29日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>勿打擾時間 (不接收訊息的時間)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>勿打擾時間</strong>可讓您定義不接收電子郵件、簡訊、推播和 WhatsApp 管道訊息的時間。此功能可確保在特定時段內不會傳送任何訊息，協助您遵守客戶偏好設定和合規性要求。您可以透過<strong>規則集</strong>套用勿打擾時間，這些規則集可指派給行銷活動或歷程中的個別動作，以進行精確控制。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都可以使用。在此「一般可用性」版本中，功能現在包括讓客戶將行銷活動動作排入佇列直到完成勿打擾時間，以及預覽啟用的勿打擾時間規則。</p>
<p><img src="assets/do-not-localize/quiet-hour-ga.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../conflict-prioritization/quiet-hours.md">詳細文件</a>。</p>
<p>推出日期： 2026年1月29日</p>
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
<p>新的<strong>訊息匯出</strong>功能現在可用於電子郵件和簡訊管道。此功能可讓您將傳送的訊息內容自動匯出至專用的 Experience Platform 資料集，讓您能夠：</p>
<ul>
<li>符合法規合規性要求 (例如 HIPAA)</li>
<li>封存法律索償和客戶服務查詢的訊息</li>
<li>保留傳送給個人的個人化內容複本</li>
</ul>
<p>從擷取之日起，記錄會在 AJO 訊息匯出資料集中保留 7 天。在此保留期間，您可以透過Experience Platform目標將其匯出至您自己的儲存空間。 此功能已在管道設定層級啟用，可讓您對要匯出的訊息進行<strong>精細控制</strong>。</p>
<p>此功能僅適用於電子郵件和簡訊管道，以及已購買訊息匯出附加產品的組織。如需詳細資訊，請聯絡您的 Adobe 代表。</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../configuration/message-export.md#message-export">詳細文件</a>。</p>
<p>推出日期：2026 年 1 月 28 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>協調行銷活動中的直接郵件管道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>協調行銷活動現在提供直接郵件管道。<strong>直接郵件活動</strong>讓您在協調的行銷活動中傳送直接郵件更加方便，單次訊息和定期訊息皆適用。此類活動可用於將直接郵件提供者所需之<strong>摘取檔案</strong>產生流程自動化。您可以將管道活動與協調行銷活動畫布結合，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../orchestrated/activities/channels.md#channel">詳細文件</a>。</p>
<p>推出日期：2026 年 1 月 28 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey 代理 - 建立歷程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey 代理現在提供建立功能，可讓 Journey Optimizer 使用者透過<strong>自然語言介面</strong>建立及設定行銷歷程。透過這些新的技能，從業人員只需在<strong>對話提示</strong>中描述他們的需求，即可快速建立歷程。這項創新簡化了歷程建立流程，讓行銷人員能夠專注於策略而非技術設定。</p>
<p>如需詳細資訊，請參閱<a href="../start/ai-features.md#journey-agent">詳細文件</a>。</p>
<p>推出日期：2026 年 1 月 12 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>動作行銷活動擷取 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現已提供新的 Journey Optimizer API，可讓您以程式設計方式擷取及檢查<strong>行銷活動相關資料</strong>，例如詳細資訊、版本和設定。</p>
<p>如需詳細資訊，請參閱<a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">詳細文件</a>。</p>
<p>推出日期：2025 年 11 月 24 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件設計工具主題</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>目前您可以快速套用<strong>事先核准的主題</strong>，以便確保所有電子郵件的<strong>品牌都有保持一致性</strong>，加快行銷活動的建立流程，個別製作高品質的電子郵件，同時減少對設計團隊的依賴。</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>此功能先前以 Beta 版發行，現在可供部分組織使用 (有限可用性)。若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>如需詳細資訊，請參閱<a href="../email/apply-email-themes.md">詳細文件</a>。</p>
<p>推出日期：2025 年 11 月 5 日</p>
</td>
</tr>
</tbody>
</table>

### 改善 {#jan-26-01-improv}

#### AI

* **AI 助理內容品質檢查** - 除了品牌一致性之外，您現在還可以評估整體的<strong>內容品質</strong>，以找出潛在的<strong>可讀性</strong>、一致性和效能問題，不受品牌准則影響。這些自動化檢查有助於識別不清楚的訊息、不一致的語調或結構性缺口。[閱讀全文](../content-management/brands-score.md#validate-quality)。

  [在影片中探索此功能](https://video.tv.adobe.com/v/3470544/?learn=on)。

#### 歷程

* **結合原生和 Adobe Campaign 訊息動作** - Journey Optimizer 現在可讓您在同一歷程中結合 <strong>Adobe Campaign v7/v8</strong> 訊息動作和<strong>原生管道動作</strong>。[閱讀全文](../building-journeys/using-adobe-campaign-v7-v8.md)

  推出日期：2026年1月27日。

* **自訂動作錯誤回應承載** - 您現在可以為自訂動作定義選用的<strong>錯誤回應承載</strong>。呼叫失敗時，歷程內容會公開錯誤承載 (在動作的 errorResponse 節點下)，並可`jo_status_code`一併在<strong>逾時/錯誤分支</strong>中提供，以支援更豐富的遞補邏輯和偵錯。[閱讀全文](../action/about-custom-action-configuration.md#define-the-message-parameters)

  推出日期：2026年1月27日。

* **歷程中的歷程承載大小驗證** - Journey Optimizer 現在會驗證<strong>承載大小</strong>，以協助確保最佳績效和系統穩定性。當建立或發佈歷程時，如果承載大小接近或超過建議的限制，您會收到明確的<strong>警告和錯誤</strong>，並提供可操作的指引，以最佳化您的歷程設定。此主動式驗證可幫助您儘早識別潛在問題並維護歷程績效。[閱讀全文](../start/guardrails.md#journey-payload-size)

  推出日期：2026年1月27日。


* **歷程警示** - 新的<strong>預先設定警示</strong>可供歷程使用。
   * <strong>超過輪廓捨棄率</strong>：過去 5 分鐘超過臨界值的輪廓捨棄與輸入輪廓的比率
   * <strong>超過自訂動作錯誤率</strong>：過去 5 分鐘超出臨界值的自訂動作錯誤與成功 HTTP 呼叫的比率
   * <strong>超過輪廓錯誤率</strong>：過去 5 分鐘超過臨界值的輪廓出錯與輸入輪廓的比率

  如需詳細資訊，請參閱[詳細文件](../reports/alerts.md)。

  推出日期：2025 年 10 月 14 日。

#### 協調的行銷活動

* **客群的資料使用標籤繼承** - 現在，在協調的行銷活動中儲存<strong>客群</strong>時，Adobe Experience Platform 中套用的標籤會自動延續，減少手動 <strong>DULE 標記</strong>。[閱讀全文](../orchestrated/activities/save-audience.md)

* **含參數的預先定義篩選器** - 您現在可以在協調的行銷活動中建立含<strong>參數</strong>的<strong>預先定義篩選器</strong>，以取得可重複使用、可編輯的規則。[閱讀全文](../orchestrated/predefined-filters.md)

* **選取屬性並複製分佈值** - 您現在可以直接從協調行銷活動的<strong>值分佈</strong>檢視中<strong>選取或複製值</strong>。[閱讀全文](../orchestrated/build-query.md)

* **傳送前的訊息確認** - 現在預設會在傳送協調的行銷活動前啟用<strong>確認步驟</strong>，以減少意外傳送。[閱讀全文](../orchestrated/activities/channels.md#confirm-message-sending)

* **預先定義的重定向篩選器** - 為了支援更輕鬆地針對協調的行銷活動使用案例進行重定向，此版本引進了新的<strong>行銷活動意見回饋篩選器</strong>。這些篩選器可讓您根據<strong>訊息參與</strong> (例如已傳送、僅開啟、已開啟或已按一下，或已開啟和已按一下) 直接鎖定客群，並選取您要重定向的特定行銷活動或轉換中行銷活動。[閱讀全文](../orchestrated/retarget.md)

* **速率控制支援** - 協調的行銷活動現在支援<strong>速率控制</strong>，協助您加速傳遞並符合<strong>數量限制</strong>。[閱讀全文](../orchestrated/activities/channels.md#rate-control)

* **重新啟動按鈕** - 協調的行銷活動現在包含<strong>重新啟動按鈕</strong>，因此您可以在發佈行銷活動之前，視需要快速<strong>重新啟動執行</strong>。[閱讀全文](../orchestrated/start-monitor-campaigns.md)

* **使用者產生的中繼資料支援** - <strong>executionMetadata 協助程式函式</strong>現在可在協調行銷活動的個人化編輯器中使用，可讓您將內容相關資訊附加至任何原生動作，並將其儲存在資料集中，以匯出至外部系統。[閱讀全文](../personalization/functions/helpers.md#execution-metadata)

  推出日期：2026年1月27日。

* **將即時行銷活動還原為草稿狀態** — 您現在可以在行銷活動發生執行錯誤或您需要修改排程的行銷活動才能開始執行時，將即時協調的行銷活動還原為草稿狀態。 在傳送第一則訊息之前，此選項均可用。 [閱讀全文](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### 行銷活動

* **使用設定檔時區排程行銷活動** — 行銷活動排程現在可以使用每個設定檔的<strong>時區</strong>，在預期的當地時間傳送訊息。 [閱讀全文](../campaigns/campaign-schedule.md)

  **注意**：這項改善僅適用於一組組織（可用性限制）。

  推出日期：2026年1月27日。

#### 權限

* **防止自我核准歷程與行銷活動** - 新增建立或設定<strong>核准原則</strong>時的選項，以防止歷程或行銷活動建立者<strong>核准自己的物件</strong>。[閱讀全文](../test-approve/approval-policies.md)

  推出日期：2026年1月27日。
