---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: be07b0dfec31d23f741bfc2a9f89fe1a7891ef0b
workflow-type: tm+mt
source-wordcount: '1783'
ht-degree: 43%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="有哪幾種新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會整合到每月最後一週的發行說明一起發表。[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2025年9月發行說明 {#25-9-rn}

**發行日期**：2025 年 9 月 23-24 日

### 全新功能 {#sept-25-9-features}

<!-- table>
<thead>
<tr>
<th><strong>Public API to retrieve journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new Journey Optimizer API is now available to retrieve journeys and their associated objects such as campaigns and surfaces.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">detailed documentation</a></p>
<p>Availability date: Sept 25, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer Experimentation Accelerator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator是AI優先的產品，旨在將您的實驗提升到新的境界。 此產品專為Adobe Journey Optimizer和Adobe Target使用者打造，可整合實驗管理、提供AI支援的深入分析和機會，並推出新的實驗代理程式。</p>
<p>您可以期待：</p>
<ul>
<li><strong>整合實驗詳細目錄：</strong>在一個中央工作區中快速檢視、篩選及管理Adobe Journey Optimizer和Adobe Target的所有實驗。</li>
<li><strong>AI實驗見解和機會：</strong>使用GenAI驅動的見解和推薦，超越統計讀數。 現在，每個實驗都會顯示可操作的機會，以及完整的支援理由，讓團隊可以更自信地決定下一個要測試的內容。</li>
<li>Journey Optimizer中的<strong>多臂吃角子老虎機(MAB)支援：</strong>透過多臂吃角子老虎機實驗，最大化影響，同時減少浪費的流量。 MAB不會平均分割對象，而是會即時自動為更多訪客分配表現最佳的變數，這樣您就能為更多客戶提供更好的體驗，同時仍會瞭解哪些變數有效。</li></ul>
<p><img src="assets/do-not-localize/experimentation-accelerator.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../content-management/experiment-accelerator.md">詳細文件</a></p>
<p>推出日期：2025 年 9 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent已推出！</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent由<a href="https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator" target="_blank">Adobe Experience Platform Agent Orchestrator</a>提供技術支援，可在Journey Optimizer中使用。 它可讓您透過自然語言介面分析歷程。 代理程式會偵測歷程中的對象或排程衝突與設定檔流失，協助您採取步驟解決衝突。 不久，您將能夠使用代理支援建立歷程。</p>
<p>如需詳細資訊，請參閱<a href="https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze" target="_blank">詳細文件</a></p>
<p>推出日期：2025 年 9 月 24 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件設計工具中的深色模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 電子郵件設計工具現在提供切換到深色模式視圖的功能，您可以在此處額外定義特定的自訂設定，該設定將僅對在深色模式下讀取其電子郵件的收件者顯示。</p>
<p>請注意下列事項：</p>
<ul>
<li>深色模式的最終呈現可能會有所不同，取決於收件者的電子郵件用戶端。</li>
<li>並非所有電子郵件用戶端都支援自訂深色模式。此外，某些電子郵件用戶端只會對收到的所有電子郵件套用自己的預設深色模式。在這兩種情況下，系統無法呈現您在電子郵件設計工具中定義的自訂設定。</li>
</ul>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../email/dark-mode.md">詳細文件</a></p>
 <p>推出日期：2025 年 9 月 16 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程路徑最佳化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用新的「最佳化」節點，鎖定特定客群或執行 A/B 測試，以判斷達到以業務為中心的 KPI 所需的最佳途徑。</p>
<p>此工具可讓您測試並變更內容，以及自訂通訊、排序和時機，以便最有效地觸及客戶。</p>
<p>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/optimize.md">詳細文件</a></p>
<p>推出日期：2025 年 9 月 4 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>子網域的自訂委派方法</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了完全委派和 CNAME 方法之外，目前還有提供一種新的子網域設定方法：自訂委派方法可讓您能完全掌控並維護傳遞、呈現，還有追蹤訊息所需的 DNS 各大層面。</p>
<p>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。</p>
<p><img src="assets/do-not-localize/custom-delegation.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../configuration/delegate-custom-subdomain.md">詳細文件</a></p>
<p>推出日期：2025 年 9 月 4 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用 Adobe Experience Platform 資料進行個人化與決策</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此功能先前於公開測試版發佈，現在可供所有環境使用。 已在此版本中，引進以下增強功能：</p>
<ul><li>支援傳入頻道中的資料集查詢個人化。</li>
<li>「datasetLookup」協助程式函式現在可用於運算式片段中。目前，此功能僅供有限的一組客戶使用。若想取得存取權，請聯絡您的 Adobe 代表。</li>
<li>資料集管理介面中的選項現在可讓您啟用記錄型資料集以進行查詢個人化，而無需執行 API 呼叫。</li>
<li>增強的監視功能，可追蹤資料擷取狀態，並了解資料集何時準備好進行查詢。</li>
<li>更新使用指南和護欄，確保最佳績效和可靠性。</li>
<li>現在可以在決策上限規則中利用 Adobe Experience Platform 資料集。</li></ul></p>
<p>如需詳細資訊，請參閱<a href="../data/lookup-aep-data.md">詳細文件</a></p>
<p>推出日期：2025 年 9 月 1 日</p>
</td>
</tr>
</tbody>
</table>


### 改善 {#sept-25-9-improvements}

* **API觸發的行銷活動的Webhook支援**\
  API觸發的行銷活動現在支援Webhook。 設定webhook URL以接收每則訊息的即時狀態更新，進而改善可觀察性，並實現順暢的監控和自動化。 [閱讀全文](../configuration/feedback-webhooks.md)

  推出日期：2025 年 9 月 29 日

* **核准原則許可權**
在建立或設定核准原則時，新增選項以防止歷程/行銷活動建立者核准自己的物件。 [瞭解詳情](../test-approve/approval-policies.md) — 推出日期： 2025年9月23日

* SMS頻道&#x200B;**的**&#x200B;mTLS支援
設定自訂SMS提供者時，您現在可以選擇啟用雙向TLS (mTLS)驗證，這要求使用者端和伺服器在建立安全連線之前確認彼此的身分。 [瞭解詳情](../sms/sms-configuration-custom.md) — 推出日期： 2025年9月23日

* **以模型為基礎的結構描述**\
  現在可以使用以模型為基礎的結構描述，來支援在「協調的行銷活動」中的關聯式模型需求。 [瞭解詳情](../orchestrated/gs-schemas.md) — 推出日期： 2025年9月23日

* **歷程中的資料集查詢支援**\
  歷程中的新活動&#x200B;**資料集查詢**&#x200B;可讓您在執行階段從Adobe Experience Platform記錄資料集中動態擷取資料。 運用此功能，您可以存取設定檔或事件裝載中可能未駐留的資料，確保客戶互動相關且及時。 [瞭解詳情](../building-journeys/dataset-lookup.md) — 推出日期： 2025年9月23日

  此活動僅適用於一組組織（可用性限制）。 若想取得存取權，請聯絡您的 Adobe 代表。

* 歷程自訂動作中的&#x200B;**重新導向支援**\
  歷程自訂動作現在支援重新導向(302)。  — 推出日期： 2025年9月23日

* **管道設定監視警示** - 您現在可以透過電子郵件或在 Journey Optimizer 通知中心訂閱接收系統警示，以防發生使用自訂子網域委派類型的電子郵件管道設定錯誤。[瞭解詳情](../reports/alerts.md#alert-channel-config-failure) — 推出日期： 2025年9月23日

* **一鍵取消訂閱要求** — 我們已匯入改善功能，進一步加強Adobe Managed下所設定一鍵取消訂閱要求的處理能力，確保處理可靠且一致。  — 推出日期： 2025年9月23日

* **自訂驗證現在支援巢狀JSON內文引數**\
  設定自訂動作的自訂驗證時，現在支援巢狀JSON物件（例如`bodyParams`內的子物件）。 [瞭解詳情](../datasource/external-data-sources.md#custom-authentication-mode) — 推出日期： 2025年9月18日

* **每小時重設上限頻率** - 您目前可以將每小時上限套用至頻道規則集。此功能以前稱為「有限可用性」，現在可供所有環境使用，並可讓您選擇1小時（之前為3小時）。 [瞭解詳情](../conflict-prioritization/channel-capping.md) — 推出日期： 2025年9月17日

* **模擬所有傳入頻道的內容變化**\
  先前僅可用於電子郵件、簡訊和推播通知頻道，模擬內容變數現在也適用於所有傳入頻道。 [瞭解詳情](../test-approve/simulate-sample-input.md) — 推出日期： 2025年9月17日

* **決策上限規則的運算式** - 您現在可以建立自己的運算式，以定義決策項目的上限規則臨界值。[瞭解詳情](../experience-decisioning/items.md#capping) — 推出日期： 2025年9月16日

* **動態網域支援** - Journey Optimizer 現在支援 Adobe 所接受的預先定義網域的完整/基底 URL 個人化。[瞭解詳情](../personalization/personalization-build-expressions.md#where) — 推出日期： 2025年9月12日

  此功能以有限可用性提供給一組客戶。



### 即將推出 {#sept-25-9-soon}

下列功能和增強功能已排定在未來幾天發行。 **資訊可能會變更**。 這些更新上線生產後，更新的連結、畫面和檔案將會共用。

<table>
<thead>
<tr>
<th><strong>新增Web推播通知頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer現在支援Web推播通知，將推播頻道擴展至行動裝置以外。 您可以順暢地將通知傳送至行動瀏覽器和案頭瀏覽器，讓您無需應用程式即可直接在其裝置上聯絡客戶。</p>
<p>此增強功能可讓您運用行動推送中現有的相同撰寫工作流程和目標定位功能，即時與使用者互動並提供個人化訊息。</p>
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自訂動作監控和報告</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>自訂動作監控和報告功能現已可用。 此功能可讓您更清楚瞭解歷程健康狀況和執行，包括生命週期狀態和效能警示。 您現在可以快速瞭解自訂動作中發生異常狀況的時間、地點和原因。</p>
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p-->
</td>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary, and Kobie loyalty apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>登陸頁面自訂表單</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在使用 [!DNL Journey Optimizer]，可以透過登入頁面擷取設定檔屬性。</p>
<p>根據特定資料集，建立、設計和管理為您的需求量身打造的自訂表單。 然後，您可以在登陸頁面中善用自訂表單，將選擇的設定檔屬性新增至為每個表單定義的資料集。</p>
<p>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<!--p>For more information, refer to the <a href="../landing-pages/lp-forms.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件的 PDF 附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以對透過 Journey Optimizer 傳送的電子郵件訊息附加靜態 PDF 檔案。</p>
<ul>
<li>您每年最多可以為每個設定檔傳送 6 封含有 PDF 附件的訊息。</li>
<li>每個附件允許的大小上限為 5 MB。</li>
<li>如需任何額外大小或容量，您可以購買PDF附件附加元件。 如需詳細資訊，請聯絡您的 Adobe 代表。</li>
</ul>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<!--p>For more information, refer to the <a href="../email/pdf-attachments.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p-->
</td>
</tr>
</tbody>
</table>



* **新歷程警示**\
  新的預先設定警示可供歷程使用：

   * 超過設定檔捨棄率：過去5分鐘超過臨界值的設定檔捨棄與輸入設定檔的比率。
   * 超出自訂動作錯誤率：過去5分鐘超出臨界值的自訂動作錯誤與成功HTTP呼叫的比率。
   * 超過設定檔錯誤率：過去5分鐘超過臨界值的設定檔出錯與輸入設定檔的比率。
<!--
  * [Profile Discard Rate Exceeded](../reports/alerts.md#profile-discard-rate-exceeded): Ratio of profile discards to entered profiles over the last 5 mins exceeded threshold.  
  * [Custom Action Error Rate Exceeded](../reports/alerts.md#custom-action-error-rate-exceeded): Ratio of custom action errors to successful HTTP calls over the last 5 mins exceeded threshold.  
  * [Profile Error Rate Exceeded](../reports/alerts.md#profile-error-rate-exceeded): Ratio of profiles-in-error to entered profiles over the last 5 mins exceeded threshold.-->

您可以修改臨界值，並訂閱個別歷程層級警報與全域警報。

<!-- Availability date: Sept XX, 2025-->


* **一鍵取消訂閱URL的自訂屬性支援**\
  透過Journey Optimizer，如果您在Adobe之外管理同意，則可在電子郵件設定中定義您自己的一鍵式取消訂閱連結，以設定外部自訂端點。 當您的收件者按一下取消訂閱連結時，Journey Optimizer 會將一些預設的設定檔特定參數附加至同意更新事件。

  若要進一步個人化取消訂閱電子郵件地址，您現在可以定義將附加至同意事件的自訂屬性。 自8月25日發行以來，此功能已可用於自訂的一鍵式取消訂閱連結。

  <!-- Availability date: Sept XX, 2025-->


* **API觸發的電子郵件行銷活動的高輸送量模式**\
  API觸發的行銷活動現在提供新的高輸送量模式。 此模式專為大規模即時傳訊（每秒最多5000筆交易）而設計，可提供更高的可用性並降低延遲。\
  此功能僅適用於電子郵件管道，以及已購買Adobe高輸送量交易訊息附加產品的組織。 如需詳細資訊，請聯絡您的Adobe代表。

  <!-- Availability date: Sept XX, 2025-->
