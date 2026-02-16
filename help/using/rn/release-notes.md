---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 9dbe9c4f6073f68bc7d01b2a72dc89c927870dcf
workflow-type: tm+mt
source-wordcount: '1552'
ht-degree: 38%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="最新資訊"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer] 遵循持續傳遞模式，允許 Adobe 持續傳遞新功能、增強功能和修正。此方法可讓您分階段推出可擴充的功能，以確保所有環境的效能和穩定性。

基於此模型，發行說明會在每月發行之間更新。如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](releases.md)。

[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2026年2月發行前注意事項 {#feb-26-01-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。連結、畫面及更新的文件會在發行當日發佈於發行說明。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**：2026 年 2 月 17-18 日

### 新功能 {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>傳出訊息的波動傳送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您可以排程來自<strong>行銷活動</strong>或<strong>歷程</strong>的傳出訊息，以控管的<strong>批次</strong>隨時間傳遞。</p>
<p>波次傳送提供下列優點：</p>
<ul>
<li>更好的<strong>傳遞能力</strong> — 隨著時間推移散佈傳送，以協助維持強大的寄件者信譽，並降低被標示為垃圾郵件的風險。</li>
<li><strong>載入控制項</strong> — 藉由限制一次傳出的訊息數目，避免造成下游系統（例如客服中心、登陸頁面）負擔過重。</li>
<li>大量且有時效性的使用案例 — 適合大型對象，或您需要控制時機時（例如客服中心容量、加電或有時限的選件）。</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程仲裁</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用<strong>公式</strong>和<strong>AI模型</strong>，根據客戶設定檔屬性和情境因素自動提升歷程優先順序分數，確保客戶進入最相關的歷程。</p>
<p>此功能僅適用於一組組織（<strong>有限可用性</strong>）。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent：建立管道內容</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>由<strong>Adobe Experience Platform Agent Orchestrator</strong>提供技術支援的<strong>Journey Agent</strong>可在Journey Optimizer中使用，並可讓您透過自然語言介面分析歷程。 您現在也可以直接在Journey Agent中產生和管理頻道特定內容、建立電子郵件和推播之類的頻道內容、套用和預覽範本、透過提示調整色調和風格，以及在<strong>內容Designer</strong>中開啟內容以進行內容內編輯。</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Mobile Live Activities</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Live Activities</strong> provide real-time updates and interactive experiences within mobile apps, allowing users to stay informed about ongoing events or tasks directly on their device's screen. This feature enhances engagement by delivering live information, such as progress tracking, event updates, or interactive content, without requiring users to open the app.</p>
<p>Previously released in beta, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>
-->

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
<li>將<strong>最佳化</strong>新增至任何內建頻道動作的功能。</li>
<li>能夠將<strong>experimentation</strong>和<strong>多語言</strong>選項新增至任何動作。</li>
</ul>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>網頁推播通知管道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 現在支援<strong>網頁推播通知</strong>，將推播管道擴展至行動裝置以外。您可以順暢地將通知傳送至行動瀏覽器和桌面瀏覽器，讓您無需應用程式即可直接在其裝置上聯絡客戶。此增強功能可讓您運用行動推播中現有的相同製作工作流程和目標定位功能，透過即時的個人化訊息與使用者互動。</p>
<p>此功能先前以Beta版發佈，現已開放所有環境使用（全面發佈）。</p>
<p>推出日期： 2026年2月13日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>網頁推播通知管道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 現在支援<strong>網頁推播通知</strong>，將推播管道擴展至行動裝置以外。您可以順暢地將通知傳送至<strong>行動瀏覽器和桌面瀏覽器</strong>，讓您無需應用程式即可直接在其裝置上聯絡客戶。此增強功能可讓您運用行動推播中現有的相同製作工作流程和目標定位功能，透過即時的個人化訊息與使用者互動。</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>此功能先前在Beta中發行，現在可供所有環境使用（全面發佈）。</p>
<p>如需詳細資訊，請參閱<a href="../push/push-configuration-web.md">詳細說明文件</a>。</p>
<p>推出日期： 2026年2月11日</p>
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
<p>推出日期： 2026年2月11日</p>
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
<p><strong>移轉工具API</strong>現在可用於以程式設計方式將<strong>決定管理</strong>實體移轉到<strong>決定</strong>，其功能：</p>
<ul>
<li>彈性移轉範圍（<strong>沙箱</strong>、<strong>選件</strong>或<strong>決定</strong>層級）</li>
<li>自動化<strong>相依性分析</strong>和驗證</li>
<li>已完成移轉的<strong>復原支援</strong></li>
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
<p>insight透過新的<strong>監視儀表板</strong>和豐富的<strong>歷程步驟事件資料</strong>，更深入瞭解<strong>自訂動作端點</strong>的健全狀況和效能。 追蹤成功的呼叫、錯誤、輸送量、回應時間和佇列等待時間，以快速瞭解異常情況發生的時間、地點和原因。</p>
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
<p>您現在可以使用<strong>決策</strong>個人化和最佳化<strong>簡訊訊息</strong>的內容。 使用<strong>優先順序分數</strong>、<strong>公式</strong>或<strong>AI模型</strong>向客戶顯示最佳內容。</p>
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


* **將子網域移轉至自訂委派** — 您現在可以使用CNAME委派模式，直接從介面將子網域移轉至自訂委派，這樣您就可以符合公司指引的更嚴格安全性原則，而不需要重新建立管道設定。

  **注意**：此功能僅適用於一組組織（<strong>有限可用性</strong>）。 若想取得存取權，請聯絡您的 Adobe 代表。


#### 電子郵件設計工具

* **使用品牌主題將影像轉換為電子郵件範本** — 在Journey Optimizer中將影像轉換為電子郵件範本時，您現在可以使用主題作為輸入，讓產生的HTML遵循您的品牌引數。 系統會自動套用背景顏色、按鈕顏色、字型、行距、邊界及邊框間距等樣式，減少手動設計工作，並提供可立即使用且只需少量編輯的範本。


* **使用新的顏色索引標籤更新品牌** - 品牌指引有助於確保您的品牌在所有接觸點上保持一致的呈現。新的色彩區段會定義您品牌色彩系統的標準，概述如何在體驗間選擇、組織及套用色彩。 它可確保主色、次色、輔色和中性色的一致使用，以支援一致、可存取且可辨識的品牌識別。


#### AI

* **整合自訂Firefly模型與協力廠商影像產生模型** — 可緊密整合標準與自訂Firefly模型，以及經核准的協力廠商影像模型（例如NanoBanana），以便在產生影像時提供更大的彈性、控制力及品牌一致性。 這可讓您為每個使用案例選取最佳模型：適用於一般需求的標準Firefly、適用於品牌內產生的自訂Firefly，或適用於特殊或實驗場景的已核准第三方模型。


#### 體驗決策

* **在決定中使用Adobe Experience Platform資料的Edge傳入支援** — 在決定中使用Adobe Experience Platform資料時，除了歷程中的電子郵件和自訂動作之外，現在還能支援邊緣傳入使用案例。

  **注意**：此功能僅適用於一組組織（<strong>有限可用性</strong>）。 若想取得存取權，請聯絡您的 Adobe 代表。


* **程式碼型體驗管道中的Experience Decisioning預覽** — 您現在可以在使用程式碼型體驗管道設定Experience Decisioning時預覽決定專案。 上線之前，可以直接在編寫介面中使用預覽。


* **優惠排名AI模型可觀察性** — 現在Journey Optimizer可讓您在Decisioning中監視AI模型的健康情況、訓練狀態和效能，以便您驗證訓練成功、疑難排解失敗，並瞭解對您結果的影響。 此功能僅適用於個人化最佳化模型（而非自動最佳化）。


* **將片段附加至決策項目** - Journey Optimizer 現在提供將片段附加至決策項目的功能，而決策項目可透過策定原則用於程式碼型體驗行銷活動。

  **注意**：此功能先前以「有限可用性」發行，現在可供所有環境使用（一般可用性）。

  推出日期：2026年2月12日。


#### 歷程

* **歷程中有多個傳入動作** - 為簡化歷程協調，您現在可以在單一歷程中定義數個傳入動作。此功能先前在行銷活動中提供，可讓您同時向不同位置提供多個程式碼型體驗、應用程式內訊息、內容卡片或網頁動作，每個動作都包含特定內容。

  **注意**：此功能先前以「有限可用性」發行，現在可供所有環境使用（一般可用性）。


* **簡訊 Webhook** - 所有簡訊提供者現在都支援 <strong>Webhook</strong>。您可以根據每個webhook的預定用途來設定每個webhook： <strong>傳入webhook</strong>以擷取傳入訊息，以及<strong>回饋webhook</strong>以接收傳遞回條、狀態更新和其他訊息相關事件。 [閱讀全文](../sms/sms-webhook.md)

  推出日期：2026年2月2日。