---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 7284814029465a8806b78640b8ffe6c44ad030a7
workflow-type: tm+mt
source-wordcount: '3902'
ht-degree: 17%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="最新資訊"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能，並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]遵循持續傳遞模式，允許Adobe持續提供新功能、增強功能和修正。 此方法可讓您分階段推出可擴充的功能，以確保所有環境的效能和穩定性。

基於此模型，發行說明會在每月發行之間更新。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](releases.md)。

[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。 若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2026年4月搶鮮版發行說明 {#april-26-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。 連結、畫面及更新的文件會在發行當日發佈於發行說明。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

四月初發佈的新功能和改進專案會隨推出日期一併公佈。

**發行日期**： 2026年4月28至29日

### 新功能 {#april-26-features}

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
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件標頭中的寄件者引數</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過Journey Optimizer，您現在可以在傳輸實體（寄件者）與編寫實體（寄件者）不同的情況下傳送電子郵件。 支援此功能的電子郵件使用者端通常會將其轉譯為「代表寄件者的寄件者」或顯示「透過」指標。 填寫電子郵件通道設定中的選擇性<strong>寄件者標題</strong>欄位，以設定此功能。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件通道設定中的「副本」欄位</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在電子郵件通道設定中設定選用的CC （副本）欄位。 不同於密件副本，副本收件者對主要收件者可見，可啟用透明通訊和更清晰的擁有權。</p>
<p>這可讓您自動複製每則訊息上正確的利害關係人，例如關係經理或帳戶擁有者，同時確保客戶知道要聯絡誰以進行後續追蹤。</p>
<p>CC欄位支援個人化，因此單一設定可根據設定檔資料動態路由副本，使其可在多個使用案例中擴充，而無需其他設定。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件Designer中的深層連結</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以透過電子郵件Designer中的專用選項，將深層連結新增至您的電子郵件內容。 這可確保使用者直接導向至正確的應用程式內內容，而非重新導向至瀏覽器或應用程式商店，以保留內容與參與度。</p>
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
<p>Adobe Journey Optimizer現在提供<strong>MCP （模型內容通訊協定）伺服器</strong>，直接在任何MCP相容應用程式中呈現行銷活動、忠誠度、管道設定和沙箱作業。 透過這項整合，不同的角色可以圍繞相同的協調流程資料共同作業。 您可以對話式描述您的意圖，讓LLM叫用適當的MCP工具，而不需針對Adobe Journey Optimizer REST API撰寫查詢或導覽多個UI畫面。 此功能目前在Claude Web和Desktop中提供。</p>
<p>此功能適用於公開Beta中的所有客戶。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>跨沙箱複製協調的行銷活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>沙箱工具現在支援將協調的行銷活動從一個沙箱封裝和複製到另一個沙箱。 如此一來，您就不需要在每個環境中手動重建行銷活動。 封裝行銷活動時，會自動包含其核心相依物件，例如合併原則、訊息，以便匯入的行銷活動到達時便能進行設定和驗證。 為了保護生產環境，所有匯入的行銷活動都會以草稿狀態在目標沙箱中著陸，在任何行銷活動上線之前為團隊提供審查和核准步驟。</p>
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
<p><strong>協調的行銷活動</strong>現在支援<strong>增量查詢</strong>活動，其目標僅是自上次執行以來新符合資格的設定檔或事件。

這可讓週期性行銷活動專注於全新受眾（新註冊、新合格的忠誠度會員和類似區段），同時減少查詢工作量，並避免隨著時間推移而出現的重複傳送。</p>
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
<p>您現在可以在排名公式中使用<strong>AI模型</strong>，以根據客戶設定檔屬性和內容因素自動提升歷程優先順序分數，確保客戶進入最相關的歷程。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Express 整合</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer中的<b>Adobe Express整合</b>可讓您在內容建立期間直接使用Adobe Express的編輯工具，讓您調整大小、移除背景、裁切，以及將資產轉換為JPEG或PNG。
</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><img src="assets/do-not-localize/express_resize.gif"></p>
<p>如需詳細資訊，請參閱<a href="../integrations/express.md">詳細文件</a>。</p>
<p>推出日期： 2026年4月23日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>針對AI收件匣最佳化電子郵件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer現在包含新功能，可確保您的電子郵件結構最佳化，以便用於Gmail中的Apple Intelligence和Google Gemini等AI支援收件匣。</p>
<p>隨著AI助理日益控制收件者讀取和操作電子郵件的方式，此功能可幫助您產生和創作可在下游AI工作（包括摘要、分類、優先順序設定和意圖擷取）中妥善執行的內容。</p>
<p><img src="assets/do-not-localize/optimize-for-ai.gif"></p>
<p>如需詳細資訊，請參閱<a href="../email/llm-email-optimizer.md">最佳化AI收件匣的電子郵件</a>。</p>
<p>推出日期： 2026年4月17日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Personalization運算式的AI助理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] 現在在個人化編輯器中直接包含<strong>AI助理</strong>，此編輯器可將自然語言提示轉換為有效的個人化運算式和條件式邏輯，不需要語法專業知識。 描述您想要實現的個人化，而AI會產生現成的程式碼，您可以立即套用或透過後續提示進行調整。</p>
<p>助理也會反向運作。 選取任何現有的運算式，並要求其說明邏輯、識別問題或提出改進建議。 這可讓此工具不僅適合用於撰寫新運算式，也適合用於檢閱及偵錯團隊中的現有運算式。</p>
<p><img src="assets/do-not-localize/assistant-perso.gif"></p>
<p>如需詳細資訊，請參閱<a href="../content-management/generative-personalization-expressions.md">Personalization運算式的AI小幫手</a>。</p>
<p>推出日期： 2026年4月13日</p>
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
<p>使用新的<strong>最佳化</strong>節點來執行A/B測試或多臂吃角子老虎機實驗，以決定符合您以企業為中心的KPI的最佳途徑。 此工具可讓您測試並變更內容，以及自訂通訊、排序和時機，以便最有效地觸及客戶。
</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p>作為「一般可用性」的一部分，此版本引入<strong>實驗型別</strong>選擇（A/B或多臂吃角子老虎機）和<strong>縮放單一歷程的獲勝者</strong>。</p>
<p><img src="assets/do-not-localize/optimize-experiment.gif"></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/path-experimentation.md">詳細文件</a>。</p>
<p>推出日期： 2026年4月7日</p>
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
<p><strong>收件匣</strong>是一項行動功能，可搭配內容卡使用，讓客戶在應用程式或網站中建立集中式位置，以顯示傳送給使用者的訊息。 這可延長行銷通訊的存留期，確保即使在訊息關閉後，仍可存取訊息。</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../inbox/inbox-gs.md">詳細文件</a>。</p>
<p>推出日期： 2026年4月7日</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Optimize email text for AI inboxes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now includes a new capability that ensures your emails are optimally structured for AI-powered inboxes such as Apple Intelligence and Google Gemini in Gmail.</p>
<p>As AI assistants increasingly control how recipients read and act on email, this feature helps you author content that performs well across downstream AI tasks including summarization, triage, prioritization, and intent extraction.</p>
<p><img src="assets/do-not-localize/text-optimizer.gif"></p>
<p>For more information, refer to <a href="../email/llm-email-optimizer.md">Optimize email text for AI inboxes</a>.</p>
<p>Availability date: April 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>電子郵件頻道中的決策支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用<strong>決策</strong>來個人化及最佳化您的電子郵件內容。 利用優先順序分數、公式或AI模型，向每位收件者顯示最相關的優惠和內容。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。 在此「一般可用性」版本中，現在支援映象頁面。</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/create-decision-policy.md">詳細文件</a>。</p>
<p>推出日期： 2026年4月6日</p>
</td>
</tr>
</tbody>
</table>

### 改善 {#april-26-improv}

#### AI

* **行銷活動儀表板中的品牌一致性分數** — 您現在可以直接在行銷活動儀表板中評估您的品牌一致性分數，以確保內容保持在品牌上。 這可讓您快速驗證指引，而不需開啟內容設計工具。

* **提示助理增強功能** — 當提示不明確、不完整或混用多個目標時，**提示助理現在可以詢問重點澄清問題，或在產生請求前建議更清楚的重寫請求，協助您在助理回應之前先釘選所需的內容，這樣可改善一致性並減少重試次數。**&#x200B;[了解更多](../content-management/ai-assistant-prompting-guide.md)

#### 決策

* **將片段附加至決定專案** - Journey Optimizer現在提供將片段附加至決定專案的功能，而決定專案可透過決定原則，在程式碼型體驗和電子郵件行銷活動中運用。 此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。

* **已略過暫時無法使用的片段** — 在決定專案中使用片段時，如果Edge上暫時無法使用片段，則會略過該片段，而且歷程或行銷活動會繼續轉譯而不是失敗。 [閱讀全文](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  推出日期： 2026年4月14日

#### 推播

* **在通道設定中個人化應用程式ID** — 在推播通道設定中，您現在可以個人化&#x200B;**應用程式ID**&#x200B;欄位，讓每位收件者都能根據其設定檔資訊，從適當的品牌接收推播通知。

#### 簡訊

* **字元計數** — 在Adobe Journey Optimizer中，您現在可以使用字元計數即時監視SMS訊息的長度。 它可協助您檢視訊息何時將分割成多個區段，以更好地管理格式並避免傳送成本意外增加。 [閱讀全文](../sms/create-sms.md)

* **在電話號碼和寄件者處選擇退出和同意** — 對於簡訊，Journey Optimizer現在會在設定檔的電話號碼和短代碼層級記錄行銷同意和選擇退出。

  此功能目前僅適用於Sinch SMS設定。 [閱讀全文](../sms/sms-configuration-sinch.md)

* **SMS內嵌至自訂資料集** — 在&#x200B;**SMS API認證**&#x200B;中，將&#x200B;**傳入SMS**&#x200B;路由至您選取的&#x200B;**自訂、啟用設定檔的體驗事件資料集**，而非僅預設追蹤資料集。 [閱讀全文](../sms/sms-webhook.md)

* **Webhook介面增強功能** — 在設定SMS Webhook時，使用者介面現在包含內建的設定指南，其中包含實用的範例，可讓您更輕鬆地對齊提供者裝載並疑難排解問題，而不需離開設定流程。 [閱讀全文](../sms/sms-webhook.md)

#### WhatsApp

* **WhatsApp互動按鈕與追蹤** - Journey Optimizer中的WhatsApp現在支援範本與使用案例所需的互動按鈕，以及內建的互動追蹤，因此您可以測量參與度，並搭配其他管道報表分析效能。

#### Adobe Experience Manager整合

* **Adobe Experience Manager內容片段變數支援** — 您可以在插入Adobe Experience Manager內容片段時選取&#x200B;**內容片段變數** （例如語言或頻道變數），以改良地區設定和多語言情境的處理方式。 [閱讀全文](../integrations/aem-fragments.md#aem-variations)

  此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。

  推出日期： 2026年4月3日

* **製作時Adobe Experience Manager內容片段內容** — 當您在文字欄位和內容區塊之間移動時，您的內容片段選取範圍會保持作用中，因此您可以新增更多片段欄位，而不需每次重新開啟&#x200B;**開啟AEM內容警告器**。 [閱讀全文](../integrations/aem-fragments.md)

  此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。

  推出日期： 2026年4月1日

#### 設定

* **URL引數加密金鑰的特定許可權** — 若要存取和管理URL引數加密金鑰，已建立新許可權。 您現在必須授與&#x200B;**檢視機碼登入**&#x200B;和&#x200B;**管理機碼登入**&#x200B;許可權。

#### 協調的行銷活動

* **資料Modeler增強功能** — 協調的關聯式結構描述現在支援跨多個欄位的複合索引鍵。 從DDL檔案載入綱要也會產生分項清單，而從DDL或Excel檔案載入會自動建立表格之間的複合關係。 在實體關係檢視中，複合連結現在會在檔案上傳後，顯示表格之間的完整欄位配對集。

* **協調行銷活動中的全域變數** — 協調行銷活動現在支援全域變數，這些變數只需定義一次，便可在工作流程內的所有活動中重複使用，可簡化設定，並確保動態值、運算式和內容個人化的一致性。

#### 電子郵件設計

* **電子郵件內容的進階HTML編輯器** — 進階HTML模式可讓您在電子郵件Designer中編輯內容的HTML來源、在來源中新增進階運算式（例如條件），以及在HTML檢視和案頭檢視之間切換，而不會遺失您的變更。

  此功能先前僅可用於電子郵件內容範本，現在已部署至電子郵件Designer中的&#x200B;**電子郵件**&#x200B;內容（例如，在歷程及行銷活動中撰寫的電子郵件）以及電子郵件內容範本。 目前處於「有限可用性」 — 請聯絡您的Adobe代表以取得存取權。 [閱讀全文](../email/email-expert-mode.md)

  推出日期： 2026年4月9日

* **電子郵件Designer中個人化運算式的AI Assistant** — 在電子郵件Designer中，選取元件並在內容工具列中使用&#x200B;**新增運算式**&#x200B;以純語言描述您需要的個人化、檢閱產生的運算式，並在不離開設計工具的情況下插入它。 [了解更多](../content-management/generative-personalization-expressions.md#generate-email-designer)

  推出日期： 2026年4月15日

#### 歷程路徑最佳化

* **實驗型別** — 您現在可以在設定路徑實驗時選擇A/B實驗（開始時固定分割）或多臂吃角子老虎機（每週更新權重的自動分割）。 [閱讀全文](../building-journeys/path-experimentation.md)

  推出日期： 2026年4月7日

* **路徑實驗：縮放成功者** — 您現在可以自動或手動將實驗的成功路徑轉出給完整受眾。 一旦確定獲勝者，您就可以擴大其觸及範圍和有效性，而無需持續監控實驗。 [閱讀全文](../building-journeys/path-experimentation.md#scale-winner)

  此功能僅適用於單一歷程（事件觸發和受眾資格）。 它不適用於讀取對象歷程。

  推出日期： 2026年4月7日

* **條件** - [最佳化](../building-journeys/optimize.md)活動是在歷程中建立條件路徑的新工具。 它取代了先前的&#x200B;**條件**&#x200B;活動，此活動已從UI中移除。 所有條件式邏輯都會保留，現在會透過&#x200B;**最佳化**&#x200B;活動的條件來處理。 [閱讀全文](../building-journeys/conditions.md)

  此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。

  推出日期： 2026年4月7日


## 2026年3月發行說明 {#march-26-rn}

[新功能](#march-26-features)和[改進](#march-26-improv)區段已涵蓋可用的功能。<!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in March.-->

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

**發行日期**： 2026年3月24至25日

### 新功能 {#march-26-features}

<table>
<thead>
<tr>
<th><strong>URL引數加密</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>追蹤和登陸頁面連結中的URL引數（已新增至您的電子郵件訊息）現在可以加密，為敏感引數資料提供額外的安全層。</p>
<ul>
<li>在專用的<strong>管理</strong>登入中登入及管理加密金鑰。</li>
<li>在運算式中使用新的「Encrypt」協助程式函式，針對您要在轉譯時保護的查詢引數，加密URL中的敏感資料。</li>
</ul>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p><img src="assets/do-not-localize/encrypt-helper.gif"></p>
<p>如需詳細資訊，請參閱<a href="../personalization/url-parameter-encryption.md">詳細文件</a>。</p>
<p>推出日期： 2026年3月31日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>將影像轉換為電子郵件內容範本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以直接在Journey Optimizer中將影像轉換為電子郵件內容範本。 使用AI支援的分析，從視覺參考自動產生結構化HTML範本，大幅縮短電子郵件設計時間。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><img src="assets/do-not-localize/image-converter.gif"></p>
<p>如需詳細資訊，請參閱<a href="../content-management/image-to-html.md">詳細文件</a>。</p>
<p>推出日期： 2026年3月31日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>登陸頁面自訂表單</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過[!DNL Journey Optimizer]，您可以透過登入頁面擷取設定檔屬性。</p>
<p>根據特定資料集，建立、設計和管理為您的需求量身打造的自訂表單。 然後，您可以在登陸頁面中善用自訂表單，將選擇的設定檔屬性新增至為每個表單定義的資料集。</p>
<p>此功能先前以「有限可用性」發佈，以供美國和澳洲的客戶使用，而現在則可用於所有環境（一般可用性）。</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../landing-pages/lp-forms.md">詳細文件</a>。</p>
<p>推出日期：2026年3月26日。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在協調的行銷活動中測試活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>新的<strong>測試</strong>活動現在可在協調的行銷活動中使用。 此活動會根據定義的條件，將工作流程執行路由至不同的分支，讓您在啟用即時傳遞之前，先驗證行銷活動邏輯和設定。</p>
<p><img src="../orchestrated/assets/test-1.png"></p>
<p>如需詳細資訊，請參閱<a href="../orchestrated/activities/test.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程中的資料集查詢支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程中的新<strong>資料集查詢</strong>活動可讓您在執行階段動態擷取Adobe Experience Platform記錄資料集的資料，讓您存取不屬於設定檔或事件裝載的資訊，讓客戶互動保持相關且即時。</p>
<p>先前以「有限可用性」發行給一組有限組織，現在所有有權使用[資料集查詢](../data/lookup-aep-data.md)的客戶都可以使用歷程中的資料集查詢活動，同時仍以「有限可用性」發行。</p>
<p><img src="../building-journeys/assets/aep-data-activity.png"></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/dataset-lookup.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>動作活動會取代頻道特定的歷程活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在2026年2月<strong>動作活動</strong>正式發行後，歷程畫布中的舊版原生頻道活動（電子郵件、推播、簡訊、應用程式內、網頁、程式碼型體驗和內容卡）現已棄用。</p>
<p>您現在必須使用單一「動作」活動來設定所有管道動作，取代需要個別的管道專用節點。</p>
<p>使用舊版管道活動的現有歷程仍可繼續運作，無需任何變更或移轉。</p>
<p><img src="assets/do-not-localize/action-activity.gif"></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-action.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件範本的高階HTML編輯器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>電子郵件內容範本的進階HTML模式可讓您在電子郵件Designer中編輯內容的HTML來源、在來源中新增進階運算式（例如條件），以及在HTML檢視和案頭檢視之間切換，而不會遺失您的變更。</p>
<p>此功能僅適用於電子郵件通道的內容範本。 目前處於「有限可用性」 — 請聯絡您的Adobe代表以取得存取權。</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../email/email-expert-mode.md">詳細文件</a>。</p>
<p>推出日期： 2026年3月10日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>整合自訂Firefly模型與協力廠商影像產生模型</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>啟用標準與自訂 Firefly 模型，以及經核准的第三方影像模型的緊密整合，以便在生成影像時提供更大的彈性、控制力及品牌一致性。</p>
<p>選擇符合您需求的正確模式：</p>
<ul><li> <strong>Adobe模型</strong> （由Firefly Image Model 4提供技術支援）可立即產生影像，無需額外設定</li><li> <strong>合作夥伴機型</strong> （由Gemini 2.5 Flash提供），提供專門的功能</li><li><strong>自訂模型</strong> （在您自己的資產上訓練的品牌特定模型），用於品牌上產生，完全符合您的品牌識別、風格和視覺准則。</li></ul>
<p>如需詳細資訊，請參閱<a href="../content-management/generative-models.md">詳細文件</a>。</p>
<p>推出日期： 2026年3月2日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>iOS的已上線活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過Adobe Journey Optimizer中的<strong>iOS上線活動</strong>，直接將即時體驗帶入客戶的Lock Screens和Dynamic Island。 提供即時更新，從訂單追蹤和航班狀態到事件倒計時、即時分數和傳送進度，而不需要使用者開啟您的應用程式。 讓您的對象保持知情並在正確的時間參與，就在他們所在的位置。</p>
<p>此功能先前以Beta版發佈，現已開放所有環境使用（全面發佈）。</p>
<p>如需詳細資訊，請參閱<a href="../mobile-live/get-started-mobile-live.md">詳細文件</a>。</p>
<p>推出日期： 2026年3月3日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent：頻道內容建立</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>由<strong>Adobe Experience Platform Agent Orchestrator</strong>提供技術支援的<strong>Journey Agent</strong>可在Journey Optimizer中使用，並可讓您透過自然語言介面分析歷程。 您現在也可以直接在Journey Agent中產生和管理頻道特定內容、建立電子郵件和推播之類的頻道內容、套用和預覽範本、透過提示調整色調和風格，以及在<strong>內容Designer</strong>中開啟內容以進行內容內編輯。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>如需詳細資訊，請參閱<a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html" target="_blank">詳細文件</a>。</p>
<p>推出日期： 2026年3月4日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI模型監視</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在可讓您監視決策AI模型的健全狀態、培訓狀態和效能。 這可讓您驗證培訓成功、疑難排解失敗，並瞭解對您結果的影響，以便使用AI為每個客戶選取最佳選件。 請注意，此功能僅適用於<strong>決策</strong> （不適用於舊版決策管理模型）。</p>
<p>此功能目前僅適用於<strong>個人化最佳化</strong>模型（非自動最佳化）。</p>
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/ranking/ai-model-observability.md">詳細文件</a>。</p>
<p>推出日期： 2026年3月9日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用訊號觸發協調的行銷活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在可以透過<strong>API訊號</strong>觸發協調的行銷活動。 若要進行此設定，請將目標行銷活動設定為<strong>由訊號</strong>觸發，發佈，然後使用API呼叫引發它。 API呼叫中包含的任何引數都可在執行的行銷活動中作為變數使用。 請注意，訊號觸發的協調行銷活動仍為<strong>批次</strong>行銷活動，與API觸發的行銷活動不同。</p>
<p><img src="assets/do-not-localize/oc-triggered.gif"></p>
<p>如需詳細資訊，請參閱<a href="../orchestrated/trigger-orchestrated-campaign.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>協調行銷活動中的交易式類別</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在協調的行銷活動中，您現在可以將管道活動設定為<strong>異動</strong>類別。 這會將異動管道設定套用至該活動，並在業務規則不應套用或客戶不需要選擇加入時很有用。</p>
<p><img src="assets/do-not-localize/oc-transactional.gif"></p>
<p>如需詳細資訊，請參閱<a href="../orchestrated/activities/channels.md#add">詳細文件</a>。</p>
<p>此功能將在未來幾天內逐步向所有區域推出。</p>
</td>
</tr>
</tbody>
</table>

### 改善 {#march-26-improv}

以下列舉部分發布內容附上的改良功能。

#### 個人化

* **完整/基本URL個人化** — 您可以使用設定檔屬性（例如網域或路徑）個人化目的地URL。 若要啟用此功能，請向Adobe提供您接受的網域清單。 [閱讀全文](../personalization/personalization-build-expressions.md#where)

  此功能先前以「有限可用性」發佈，以供歷程使用，現在則可用於所有環境（一般可用性）。

  推出日期： 2026年4月1日

#### 報告

* **傳送時間最佳化：更新的控制項位置和新的提升度報告** — 傳送時間最佳化(STO)控制項已重新放置到[動作]設定功能表。 此外，歷程報表現在提供新的提升度報表，以測量STO對行銷活動效能量度的影響。 [閱讀全文](../reports/channel-report-cja.md#optimization-models)

  推出日期： 2026年3月27日

<!--
* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.

#### Email Designer

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.

* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment.

  **Caution:** When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered—both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.
-->

#### 設定

<!--* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.-->

* **AJO網域憑證更新失敗** — 您現在可以透過電子郵件或在Journey Optimizer通知中心訂閱接收系統警示，當用於電子郵件傳遞的網域憑證接近到期或已過期時。 [閱讀全文](../reports/alerts.md#alert-certificates-renewal-unsuccessful)

  推出日期： 2026年3月26日

* **AJO次要收件者意見反應事件資料集重新命名** - `AJO Email BCC Feedback Event`資料集已重新命名為`AJO Secondary Recipient Feedback Event`資料集。 其影響會依您的情況而有所不同：

   * **現有使用者**：只更新顯示名稱。 基礎資料表名稱保持不變。
   * **新使用者和沙箱**：顯示名稱和表格名稱都會反映新名稱。
   * **具有新沙箱的現有使用者**：顯示名稱和表格名稱都會更新為新名稱。

  >[!NOTE]
  >
  >新資料集會立即顯示新名稱。 對於較舊的資料集名稱，回填和對帳會逐步進行，並且可能需要幾週的時間才能完成。

  推出日期： 2026年3月2日


#### 歷程

* **更新設定檔動作：支援多個設定檔屬性** - **更新設定檔**&#x200B;動作活動現在支援在單一節點中最多更新五個設定檔屬性。 以前，每個動作一次只能更新一個屬性，而需要多個節點更新多個屬性。 使用新的&#x200B;**更新其他欄位**&#x200B;按鈕來新增其他欄位/值組，減少畫布複雜性並改善效能。 [了解更多](../building-journeys/update-profiles.md)

* **在歷程中傳送傳出訊息的波次** — 您現在可以排程來自Journey Optimizer歷程的訊息，以控管批次方式傳送一段期間。 [了解更多](../building-journeys/send-using-waves.md)

  此功能先前以「有限可用性」發佈，以供歷程使用，現在則可用於所有環境（一般可用性）。

  推出日期： 2026年3月16日

* **歷程技術詳細資料中的暫停和繼續詳細資訊** — 歷程&#x200B;**技術詳細資訊**&#x200B;現在包含額外的暫停和繼續資訊：上次暫停和繼續的日期和時間、執行每個動作之使用者的顯示名稱和內部識別碼，以及整套暫停的歷程設定，例如暫停行為、最長暫停期間和自動繼續狀態。 [了解更多](../building-journeys/journey-properties.md)

  推出日期： 2026年3月2日

#### 決策

* **決策移轉 — 選件與內容屬性** — 移轉API實體對應現在會列出&#x200B;**選件屬性** （個人化選件專案結構描述上的`migratedofferattributes`）與&#x200B;**內容屬性** （移轉資料集結構描述上的`migratedcontextattributes`）。 [閱讀全文](../experience-decisioning/decisioning-migration-api.md#entity-mapping)

  推出日期： 2026年3月31日

<!--
## Coming soon {#coming-soon}

The features and improvements below are planned for release later in March/early April. Release dates and scope are **subject to change without prior notice**.


WAITING RELEASE DATE CONFIRMATION * **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.


WAITING RELEASE DATE CONFIRMATION
* **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->
