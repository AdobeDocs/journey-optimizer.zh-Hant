---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ea2753bd9ce7372e53fefc7816d19a7a3c73b87d
workflow-type: tm+mt
source-wordcount: '2545'
ht-degree: 18%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="最新資訊"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能，並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]遵循持續傳遞模式，允許Adobe持續提供新功能、增強功能和修正。 此方法可讓您分階段推出可擴充的功能，以確保所有環境的效能和穩定性。

基於此模型，發行說明會在每月發行之間更新。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](releases.md)。

[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。 若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2026年5月更新 {#may-26-rn}

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
<p>此功能以有限可用性的形式提供給所有客戶，並具備基本功能。</p>
<p><img src="assets/do-not-localize/simulate-user.gif"></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/simulate-journey.md">詳細說明文件</a>。</p>
<p>推出日期： 2026年5月5日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>決策規則和排名公式AI最佳化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] 現在使用AI來偵測可以簡化的決定規則和排名公式。 在詳細目錄中，紅色指示器會出現在AI已識別最佳化機會的任何規則上。 按一下指示器會顯示原始運算式以及AI建議的版本。 從那裡，您可以下載檔案以檢視每個版本評估模擬設定檔的方式，並確認其行為相同，然後以最佳化的設定檔取代運算式。</p>
<p>如需詳細資訊，請參閱<a href="../start/ai-features.md#decisioning-optimization">詳細說明文件</a>。</p>
<p>推出日期： 2026年5月5日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>整合</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><b>整合</b>功能可讓您直接將協力廠商資料來源連線至Adobe Journey Optimizer。 透過簡化您提取外部資料和<b>可撰寫內容</b>的方式，此功能可讓您更輕鬆地跨所有管道提供個人化的動態訊息。</p>
<p>之前以 Beta 版本發行，目前此功能所有環境都適用 (一般可用性)。</p>
<p>如需詳細資訊，請參閱<a href="../integrations/integrations.md">詳細文件</a>。</p>
<p>推出日期： 2026年5月4日</p>
</td>
</tr>
</tbody>
</table>

### 改善 {#may-26-improv}

#### 決策

* **決定移轉工作流程API** — 建立相依性分析和移轉工作流程的API合約已更新：在要求URL （`sandbox`、`offer`或`decision`）上傳遞&#x200B;**`request-level`**&#x200B;作為&#x200B;**查詢引數**。 JSON內文中不得再傳送請求層級。 [閱讀全文](../experience-decisioning/decisioning-migration-api.md)

  推出日期： 2026年5月6日

#### 簡訊

<!--
* **Opt-out and consent at phone number and sender** - For SMS, Journey Optimizer now records marketing consent and opt-out at the level of both the profile's phone number and short code. 

  This capability is currently only available for Sinch SMS configurations. [Read more](../sms/sms-configuration-sinch.md)
-->

* **字元計數** — 在Adobe Journey Optimizer中，您現在可以使用字元計數即時監視SMS訊息的長度。 它可協助您檢視訊息何時將分割成多個區段，以更好地管理格式並避免傳送成本意外增加。 [閱讀全文](../sms/create-sms.md)

* **SMS內嵌至自訂資料集** — 在&#x200B;**SMS API認證**&#x200B;中，將&#x200B;**傳入SMS**&#x200B;路由至您選取的&#x200B;**自訂、啟用設定檔的體驗事件資料集**，而非僅預設追蹤資料集。 [閱讀全文](../sms/sms-webhook.md)

* **Webhook介面增強功能** — 在設定SMS Webhook時，使用者介面現在包含內建的設定指南，其中包含實用的範例，可讓您更輕鬆地對齊提供者裝載並疑難排解問題，而不需離開設定流程。 [閱讀全文](../sms/sms-webhook.md)

#### WhatsApp

* **WhatsApp按鈕支援和追蹤** - WhatsApp範本現在支援&#x200B;**快速回覆**、**Call to action - URL**&#x200B;和&#x200B;**Call to action -**，不支援&#x200B;**複製代碼**。 Journey Optimizer會傳送支援的按鈕並追蹤與其他管道報表的互動。

## 即將推出 {#coming-soon}

下列功能和增強功能預計於未來幾天發行。 **資訊可能會有變更**。 這些更新在生產環境上線後，更新的連結、畫面和文件將會共用。

### 新功能 {#comming-soon-features}

<table>
<thead>
<tr>
<th><strong>電子郵件Designer中的深層連結</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以透過電子郵件Designer中的專用選項，將深層連結新增至您的電子郵件內容。</p><p>這可確保使用者直接導向至正確的應用程式內內容，而非重新導向至瀏覽器或應用程式商店，以保留內容與參與度。</p>
<!--<p><img src="assets/do-not-localize/forms.gif"></p>-->
<p>如需詳細資訊，請參閱<a href="../email/message-tracking.md">詳細說明文件</a>。</p>
<p>推出日期： 2026年5月7日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程片段</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在Adobe Journey Optimizer中建立<strong>歷程片段</strong>。 歷程片段是可重複使用的歷程節點集合，您可以只建置一次，然後放入您的沙箱的任何歷程中。 無論是資格檢查、偏好的管道路由邏輯或歡迎順序，片段都有助於團隊更快移動並保持一致，而不會每次從頭開始重建相同的邏輯。</p>
<p>建立後，片段會儲存在專用的<strong>片段詳細目錄</strong>中，並可使用<strong>歷程片段</strong>活動插入任何歷程。</p>
<!--<p><img src="assets/do-not-localize/journey-fragments.gif"></p>-->
<p>此功能僅適用於一組組織（可用性限制）。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<!--p>For more information, refer to the <a href="../building-journeys/journey-fragments.md">detailed documentation</a>.</p-->
<p>推出日期： 2026年5月12日</p>
</td>
</tr>
</tbody>
</table>

## 2026年4月發行說明 {#april-26-rn}

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

四月初發佈的新功能和改進專案會隨推出日期一併公佈。

**發行日期**： 2026年4月28至29日

### 新功能 {#april-26-features}

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
<p>如需詳細資訊，請參閱<a href="../orchestrated/activities/incremental-query.md#incremental-query-configuration">詳細文件</a>。</p>
<p>推出日期： 2026年4月30日</p>
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
<p><img src="assets/do-not-localize/sender-headers.gif"></p>
<p>如需詳細資訊，請參閱<a href="../email/header-parameters.md#sender-header">詳細說明文件</a>。</p>
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
<p><img src="../configuration/assets/email-config-cc.png"></p>
<p>如需詳細資訊，請參閱<a href="../configuration/cc-email-field.md">詳細說明文件</a>。</p>
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
<p><img src="assets/do-not-localize/oc-sandbox.gif"></p>
<p>如需詳細資訊，請參閱<a href="../configuration/copy-objects-to-sandbox.md">詳細說明文件</a>。</p>
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
<p>Adobe Journey Optimizer現在提供<strong>MCP （模型內容通訊協定）伺服器</strong>，直接在任何MCP相容應用程式中呈現行銷活動、管道設定和沙箱作業。 透過這項整合，不同的角色可以圍繞相同的協調流程資料共同作業。 您可以對話式描述您的意圖，讓LLM叫用適當的MCP工具，而不需針對Adobe Journey Optimizer REST API撰寫查詢或導覽多個UI畫面。 此功能目前在Claude Web和Desktop中提供。</p>
<p>此功能適用於公開Beta中的所有客戶。</p>
<p>如需詳細資訊，請參閱<a href="../integrations/ajo-mcp.md">詳細文件</a>。</p>
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
<p><img src="assets/do-not-localize/journey-arbitration-ai-models.gif"></p>
<p>如需詳細資訊，請參閱<a href="../conflict-prioritization/journey-ai-models.md">詳細說明文件</a>。</p>
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
<p>如需詳細資訊，請參閱<a href="../integrations/express.md">詳細說明文件</a>。</p>
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
<p>[!DNL Adobe Journey Optimizer] 現在在個人化編輯器中直接包含<strong>AI助理</strong>，以及可將自然語言提示轉換為有效個人化運算式和條件邏輯的電子郵件Designer，不需要語法專業知識。 描述您想要實現的個人化，而AI會產生現成的程式碼，您可以立即套用或透過後續提示進行調整。</p>
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
<p>如需詳細資訊，請參閱<a href="../building-journeys/path-experimentation.md">詳細說明文件</a>。</p>
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
<p>如需詳細資訊，請參閱<a href="../inbox/inbox-gs.md">詳細說明文件</a>。</p>
<p>推出日期： 2026年4月7日</p>
</td>
</tr>
</tbody>
</table>

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
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/create-decision-policy.md">詳細說明文件</a>。</p>
<p>推出日期： 2026年4月6日</p>
</td>
</tr>
</tbody>
</table>

### 改善 {#april-26-improv}

#### AI

<!--
* **Brand alignment score in Campaign dashboard** - You can now assess your brand alignment score directly within your Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.
-->

* **提示助理增強功能** — 提示助理可以即時分析使用者提示，並找出清晰度、完整度和內容之間的差距，藉此增強AI內容的產生能力。 它建議改善重寫，並提供可操作的指引，以利用對象、膚色和意圖等關鍵詳細資訊豐富提示。 功能也會要求目標明確的澄清問題，以協助使用者在產生之前調整其輸入。 如此一來，可減少反複專案數，進而提供更精確、高品質的輸出。 [了解更多](../content-management/ai-assistant-prompting-guide.md#prompt-assistant)

  推出日期： 2026年5月5日

#### 推播

* **在通道設定中個人化應用程式ID** — 在推播通道設定中，您現在可以個人化&#x200B;**應用程式ID**&#x200B;欄位，讓每位收件者都能根據其設定檔資訊，從適當的品牌接收推播通知。 [閱讀全文](../push/push-configuration.md#app-id-personalization)

#### 決策

* **決定移轉工作流程API** — 建立相依性分析和移轉工作流程的API合約已更新：在要求URL （`sandbox`、`offer`或`decision`）上傳遞&#x200B;**`request-level`**&#x200B;作為&#x200B;**查詢引數**。 JSON內文中不得再傳送請求層級。 [閱讀全文](../experience-decisioning/decisioning-migration-api.md)

  推出日期： 2026年5月6日

* **將片段附加至決定專案** - Journey Optimizer現在提供將片段附加至決定專案的功能，而決定專案可透過決定原則，在程式碼型體驗和電子郵件行銷活動中運用。 [閱讀全文](../experience-decisioning/fragments-decision-policies.md)

  此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。

* **已略過暫時無法使用的片段** — 在決定專案中使用片段時，如果Edge上暫時無法使用片段，則會略過該片段，而且歷程或行銷活動會繼續轉譯而不是失敗。 [閱讀全文](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  推出日期： 2026年4月14日

#### Adobe Experience Manager整合

* **Adobe Experience Manager內容片段變數支援** — 您可以在插入Adobe Experience Manager內容片段時選取&#x200B;**內容片段變數** （例如語言或頻道變數），以改良地區設定和多語言情境的處理方式。 [閱讀全文](../integrations/aem-fragments.md#aem-variations)

  此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。

* **製作時Adobe Experience Manager內容片段內容** — 當您在文字欄位和內容區塊之間移動時，您的內容片段選取範圍會保持作用中，因此您可以新增更多片段欄位，而不需每次重新開啟&#x200B;**開啟AEM內容警告器**。 [閱讀全文](../integrations/aem-fragments.md)

  此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。

#### 電子郵件設計

* **電子郵件內容的進階HTML編輯器** — 進階HTML模式可讓您在電子郵件Designer中編輯內容的HTML來源、在來源中新增進階運算式（例如條件），以及在HTML檢視和案頭檢視之間切換，而不會遺失您的變更。

  此功能先前僅可用於電子郵件內容範本，現在已部署至電子郵件Designer中的&#x200B;**電子郵件**&#x200B;內容（例如，在歷程及行銷活動中撰寫的電子郵件）以及電子郵件內容範本。 目前處於「有限可用性」 — 請聯絡您的Adobe代表以取得存取權。 [閱讀全文](../email/email-expert-mode.md)

  推出日期： 2026年4月9日

#### 歷程路徑最佳化

* **實驗型別** — 您現在可以在設定路徑實驗時選擇A/B實驗（開始時固定分割）或多臂吃角子老虎機（每週更新權重的自動分割）。 [閱讀全文](../building-journeys/path-experimentation.md)

  推出日期： 2026年4月7日

* **路徑實驗：縮放成功者** — 您現在可以自動或手動將實驗的成功路徑轉出給完整受眾。 一旦確定獲勝者，您就可以擴大其觸及範圍和有效性，而無需持續監控實驗。 [閱讀全文](../building-journeys/path-experimentation.md#scale-winner)

  此功能僅適用於單一歷程（事件觸發和受眾資格）。 它不適用於讀取對象歷程。

  推出日期： 2026年4月7日

* **條件** - [最佳化](../building-journeys/optimize.md)活動是在歷程中建立條件路徑的新工具。 它取代了先前的&#x200B;**條件**&#x200B;活動，此活動已從UI中移除。 所有條件式邏輯都會保留，現在會透過&#x200B;**最佳化**&#x200B;活動的條件來處理。 [閱讀全文](../building-journeys/conditions.md)

  此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。

  推出日期： 2026年4月7日

#### 協調的行銷活動

* **協調行銷活動中的全域變數** — 協調行銷活動現在支援全域變數，這些變數只需定義一次，便可在工作流程內的所有活動中重複使用，可簡化設定，並確保動態值、運算式和內容個人化的一致性。 [閱讀全文](../orchestrated/global-variables.md)
* **資料Modeler增強功能** — 協調的關聯式結構描述現在支援跨多個欄位的複合索引鍵。 從DDL檔案載入綱要也會產生分項清單，而從DDL或Excel檔案載入會自動建立表格之間的複合關係。 在實體關係檢視中，複合連結現在會在檔案上傳後，顯示表格之間的完整欄位配對集。 [閱讀全文](../orchestrated/gs-schemas.md)
