---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: ee485d872299b592e27cf40cd3cde9b362bc85d2
workflow-type: tm+mt
source-wordcount: 2694
ht-degree: 21%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="最新資訊"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能，並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer] 遵循持續傳遞模式，允許 Adobe 持續傳遞新功能、增強功能和修正。 此方法可讓您分階段推出可擴充的功能，以確保所有環境的效能和穩定性。 基於此模型，發行說明會在每月發行之間更新。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](releases.md)。

[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。 若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

>[!NOTE]
>
>這些發行說明中列出的功能包括&#x200B;**可用日期**，指出每個變更可在您的環境中存取的時間。 **即將推出**&#x200B;摺疊式功能表中的專案預計將在未來幾天或幾週內推出。 這些區段中的資訊可能會有所變更。


## 2026年6月更新 {#june-26-updates}

<table>
<thead>
<tr>
<th><strong>歷程片段（正式發行）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在Adobe Journey Optimizer中建立<strong>歷程片段</strong>。 歷程片段是可重複使用的歷程節點集合，您可以只建置一次，然後放入您的沙箱的任何歷程中。 無論是資格檢查、偏好的管道路由邏輯或歡迎順序，片段都有助於團隊更快移動並保持一致，而不會每次從頭開始重建相同的邏輯。</p>
<p>建立後，片段會儲存在專用的<strong>片段詳細目錄</strong>中，並可使用<strong>歷程片段</strong>活動插入任何歷程。</p>
<p>先前此功能以「有限可用性」提供，現已開放所有客戶使用。 歷程片段也支援<strong>沙箱工具</strong>，可讓您跨沙箱封裝及匯出片段。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-fragments.md">詳細文件</a>。</p>
<p>推出日期： 2026年6月9日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>直接郵件通道中的決策支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將決定政策新增到直接郵件歷程和行銷活動中。 決策原則是優惠方案的容器，可運用決策引擎以動態方式傳回每個對象成員的最佳內容。 直接郵件決定也支援批次決定使用案例，讓您為特定Adobe Experience Platform對象中的每個設定檔匯出對應的優惠專案。 </p>
<p><img src="assets/do-not-localize/exd-dm.gif"></p>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/use-decision-policy.md">詳細文件</a>。</p>
<p>推出日期： 2026年6月3日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程運算式的AI助理（公開Beta）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI Assistant現在會在歷程進階運算式編輯器中運作，將自然語言提示轉換為有效的運算式和條件式邏輯。 描述您要建置的運算式，AI Assistant會產生可立即套用的程式碼，或透過後續提示進行調整。</p>
<p>此功能以公用Beta的形式提供給所有客戶。</p>
<p><img src="assets/do-not-localize/expression-assistant.gif"></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/expression/expression-agent.md">詳細文件</a>。</p>
<p>推出日期： 2026年6月3日</p> 
</td>
</tr>
</tbody>
</table>


* **自訂動作中的憑證式自訂驗證** — 自訂動作現在支援憑證式自訂驗證。 將`subType: "certificateCredential"`新增至自訂授權設定後，Journey Optimizer會使用Adobe的Managed憑證來簽署JWT使用者端宣告，並將其交換為存取權杖 — 不需要使用者端密碼。 專為執行憑證式身分驗證的企業API （例如Microsoft Entra ID）而設計。 [了解更多](../datasource/external-data-sources.md#certificate-credential)

  推出日期： 2026年6月4日



## 2026年5月發行說明 {#may-26-rn}

### 歷程 {#may-26-journeys}

下列功能和改進專案已新增到此版本的歷程。 預計未來幾天或幾週也會有其他變更。

<table>
<thead>
<tr>
<th><strong>歷程片段（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在Adobe Journey Optimizer中建立<strong>歷程片段</strong>。 歷程片段是可重複使用的歷程節點集合，您可以只建置一次，然後放入您的沙箱的任何歷程中。 無論是資格檢查、偏好的管道路由邏輯或歡迎順序，片段都有助於團隊更快移動並保持一致，而不會每次從頭開始重建相同的邏輯。</p>
<p>建立後，片段會儲存在專用的<strong>片段詳細目錄</strong>中，並可使用<strong>歷程片段</strong>活動插入任何歷程。</p>
<!--<p><img src="assets/do-not-localize/journey-fragments.gif"></p>-->
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-fragments.md">詳細說明文件</a>。</p>
<p>推出日期： 2026年5月13日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程模擬（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將歷程設定為<strong>模擬</strong>。 此模式可讓您使用<strong>模擬的使用者</strong>來驗證您的邏輯。 這些是專為模擬建立的臨時輪廓，可讓您自由測試，而無需在 Adobe Experience Platform 中管理持續的測試輪廓。</p>
<p>此功能以有限可用性的形式提供給所有客戶，並具備基本功能。</p>
<p><img src="assets/do-not-localize/simulate-user.gif"></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/simulate-journey.md">詳細文件</a>。</p>
<p>推出日期： 2026年5月5日</p>
</td>
</tr>
</tbody>
</table>

+++ 即將推出 — **下列資訊可能會變更。**

未來幾天或幾週預計會有以下歷程功能。

<!--
<table>
<thead>
<tr>
<th><strong>Journey path optimization – Targeting (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use the new <strong>Optimize</strong> node to target specific audiences to determine the best path to meet your business-centric KPIs.</p>
<p>This tool allows you to develop more effective marketing campaigns that are more likely to resonate at the 1:1 level, improve marketing personalization efforts for customers and enhance critical customer engagement KPIs, such as conversions and revenue.</p>
<p>Previously available in Limited Availability, this capability is now available to all environments.</p>
<p>Availability date: June 1, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Arbitration – ranking formulas (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use formulas to automatically boost journey priority scores based on customer profile attributes and contextual factors, ensuring customers enter the most relevant journeys.</p>
<p>Previously available in Limited Availability, this capability is now available to all environments.</p>
<p>Availability date: June 1, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>歷程模擬（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>先前在「有限可用性」中發行的「歷程模擬」現在可供所有環境使用。 透過此一般可用性版本，您現在可以使用Journey Agent直接在模擬功能表中產生模擬使用者和事件。</p>
<p>推出日期：2026年6月初</p>
</td>
</tr>
</tbody>
</table>

* **非循環讀取對象歷程的自動完成** — 非循環&#x200B;**讀取對象**&#x200B;歷程現在會在最後一個作用中設定檔退出後，自動轉換成&#x200B;**已停止**&#x200B;狀態。 以往，這些歷程會維持&#x200B;**即時**&#x200B;狀態，直到91天全域逾時到期 — 即使不再有設定檔流過。 透過這項改善，歷程狀態會在完成時反映實際執行狀態，讓您無需手動介入即可保持歷程詳細目錄準確。

  請注意，此行為不適用於包含導致等待期的節點的歷程，例如等待節點、反應節點或事件觸發的轉變。 這些歷程仍受標準91天全域逾時的約束。

  推出日期：2026年6月初

* **外部對象的補充識別碼支援** — 歷程中的補充識別碼現在支援外部對象，包括從CSV檔案匯入的對象和使用Federated Audience Composition建立的對象。 您可以從對象中指定任何非身分屬性或非個人身分屬性作為補充ID，不需要架構標籤。

  推出日期：2026年6月初

+++

### 協調的行銷活動 {#may-26-oc}

下列功能和改善專案已新增至此版本中的協調行銷活動。 預計未來幾天或幾週也會有其他變更。

<table>
<thead>
<tr>
<th><strong>鏈結協調的行銷活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，只要直接從其他協調行銷活動的<strong>結束活動</strong>觸發協調的行銷活動，即可將協調的行銷活動連結在一起。</p>
<p>這可讓您將複雜的協調流程邏輯分解成更小且可重複使用的流程，以便從多個上層行銷活動呼叫，而非每次都重新建置。 在執行階段傳遞的裝載可用於下遊行銷活動中的細分和個人化，因此每個連結的行銷活動都可以根據其收到的內容採取行動。</p>
<p><img src="assets/do-not-localize/oc-trigger.gif"></p>
<p>如需詳細資訊，請參閱<a href="../orchestrated/trigger-orchestrated-campaign.md#signal-end">詳細文件</a>。</p>
<p>推出日期： 2026年5月20日</p>
</td>
</tr>
</tbody>
</table>

* **在擴充活動中新增連結** — 在協調行銷活動的擴充活動中現在可以使用新增連結功能。 這可讓您在工作表格資料與現有的資料庫表格之間建立直接關係。

  推出日期： 2026年5月20日

<!--
+++ Coming soon — **Information below is subject to change.**

The following orchestrated campaign capability is expected in the upcoming days or weeks.

<table>
<thead>
<tr>
<th><strong>File-based targeting for orchestrated campaigns (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Orchestrated campaigns now support loading a CSV or TXT file directly into the campaign canvas as the targeting audience, without first ingesting the file into Adobe Experience Platform. The file data is consumed at execution time and is not persisted as an Adobe Experience Platform dataset. During file setup, you can define column mappings, data types, NULL handling, and per-column error policies. This supports ad-hoc sends or partner list campaigns where building a full ingestion pipeline is not practical.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>Availability date: June 1, 2026</p>
</td>
</tr>
</tbody>
</table>

* **Loop-based personalization for relational data** - The personalization editor now supports a Loop block that iterates over relational collections, such as orders, accounts, or bookings, and renders one content block per record inside a single email or SMS. Collections are configured through the data picker using personalization tokens, with no expression writing required.

  Availability date: Early June, 2026

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address.

  Header values can be set at the channel level and overridden per campaign using contextual data for more precise control.

  Availability date: Early June, 2026

+++
-->

### 行銷活動 {#may-26-campaigns}

* **促銷活動生命週期事件的客戶警示** — 新的系統警示現在會通知您動作和API觸發之促銷活動的重要生命週期事件。 在沙箱層級訂閱。 [閱讀更多](../reports/alerts.md)

  推出日期： 2026年6月1日

<!--
+++ Coming soon — **Information below is subject to change.**

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default execution field set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.

  Availability date: Early June, 2026

+++
-->

### 決策 {#may-26-decisioning}

下列功能和改進專案已新增至此版本中的Decisioning。 預計未來幾天或幾週也會有其他變更。

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
<p><img src="assets/do-not-localize/rule-ai.gif"></p>
<p>如需詳細資訊，請參閱<a href="../start/ai-features.md#decisioning-optimization">詳細說明文件</a>。</p>
<p>推出日期： 2026年5月5日</p>
</td>
</tr>
</tbody>
</table>

* **決策中的Adobe Experience Manager內容片段** — 您現在可以將Adobe Experience Manager內容片段對應至決策中的決策專案，並在決策政策內運用這些片段，以便在適當的時間將適當的片段提供給適當的客戶。 [閱讀全文](../integrations/aem-fragments.md#aem-decisioning)

  此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。

  推出日期： 2026年5月20日

* **來自行銷活動摘要的決策原則詳細資訊** — 您現在可以從行銷活動摘要頁面檢閱每個決策原則的完整結構，包括選擇策略、決策專案和遞補優惠，而不需要複製或編輯行銷活動。 您也可以將JSON摘要複製到剪貼簿，以便透過Adobe支援或您的工程團隊進行疑難排解。 [閱讀更多](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

  推出日期： 2026年5月20日

* **決定移轉工作流程API** — 建立相依性分析和移轉工作流程的API合約已更新：在要求URL （`sandbox`、`offer`或`decision`）上傳遞&#x200B;**`request-level`**&#x200B;作為&#x200B;**查詢引數**。 JSON內文中不得再傳送請求層級。 [閱讀全文](../experience-decisioning/decisioning-migration-api.md)

  推出日期： 2026年5月6日

### 電子郵件頻道 {#may-26-email}

下列功能和改進專案已新增到此版本的電子郵件通道。 預計未來幾天或幾週也會有其他變更。

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
<p>請注意，雖然「深層連結」選項可供所有客戶使用，但深層連結只有在您已完成必要設定和行動應用程式實施步驟時才有效。</p>
<p><img src="assets/do-not-localize/deeplinks.gif"></p>
<p>如需詳細資訊，請參閱<a href="../email/deeplinks.md">詳細文件</a>。</p>
<p>推出日期： 2026年5月12日</p>
</td>
</tr>
</tbody>
</table>

* **限製片段中的繼承中斷** — 現在當您建立或編輯片段時，可以選擇在電子郵件中使用時是否可修改片段。 鎖定片段可確保片段在出現的所有地方都保持同步，避免進行可能違反品牌標準或法規遵循要求的本機編輯。 此設定稍後可更新，並套用至未來的用途。 [閱讀更多](../content-management/create-fragments.md#lock-visual-fragment)

  推出日期： 2026年5月21日

### 行動裝置訊息（簡訊、多媒體簡訊服務與RCS） {#may-26-mobile}

下列功能和改進專案已新增至此版本的行動傳訊。

<table>
<thead>
<tr>
<th><strong>新的行動訊息頻道和增強的RCS訊息</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>SMS、MMS和RCS現在整合在Adobe Journey Optimizer中的單一<strong>行動訊息</strong>動作下，因此更易從單一位置管理所有行動訊息型別。 在此更新中，您現在可以透過新的原生撰寫體驗，直接在Journey Optimizer中撰寫豐富媒體RCS訊息，包括影像、輪播和建議的動作。</p>
<p>如需詳細資訊，請參閱<a href="../mobile/get-started-mobile.md">詳細說明文件</a>。</p>
<p>推出日期： 2026年5月20日</p>
</td>
</tr>
</tbody>
</table>

* **字元計數** - 在 Adobe Journey Optimizer 中，您現在可以使用字元計數，即時監視簡訊的長度。 它可協助您檢視訊息何時將分割成多個區段，以更好地管理格式並避免傳送成本意外增加。 [閱讀全文](../mobile/create-mobile-message.md)

* **簡訊傳入至自訂資料集** - 在&#x200B;**簡訊 API 認證**&#x200B;中，將&#x200B;**傳入簡訊**&#x200B;路由至您選取的&#x200B;**自訂、已啟用輪廓的體驗事件資料集**，而非僅預設追蹤資料集。 [閱讀全文](../mobile/mobile-webhook.md)

* **Webhook 介面增強功能** - 在設定簡訊 Webhook 時，使用者介面現在包含內建的設定指南，其中包含實用的範例，可讓您更輕鬆地調整提供者裝載並疑難排解問題，而無需離開設定流程。 [閱讀更多](../mobile/mobile-webhook.md)

* **SMS內容中的深層連結** — 現在可以使用Url協助程式函式將深層連結新增到您的SMS內容。 這可確保直接將收件者導向至預期的應用程式內內容，無需透過網頁瀏覽器或應用程式商店路由，前提是您已完成必要的設定和行動應用程式實施步驟。 [閱讀更多](../email/deeplinks.md)

### WhatsApp 頻道 {#may-26-whatsapp}

下列改良功能已新增至此版本的WhatsApp管道。

* **WhatsApp按鈕支援和追蹤** - WhatsApp範本現在支援&#x200B;**快速回覆**、**Call to action - URL**&#x200B;和&#x200B;**Call to action -**，不支援&#x200B;**複製代碼**。 Journey Optimizer會傳送支援的按鈕並追蹤與其他管道報表的互動。

* **WhatsApp頻道內容資料** - Journey Optimizer現在會擷取從WhatsApp頻道傳回的其他互動資料，並將其儲存在`whatsAppChannelContext`欄位群組下的&#x200B;**AJO EmailTrackingExperienceEvent資料集**。 [閱讀更多](../whatsapp/send-whatsapp.md#whatsapp-channel-context)

  +++ 系統會擷取下列欄位，用於建立對象和分析WhatsApp參與度

   * **`messageType`** - WhatsApp訊息型別（例如`templateBased`、`response`）
   * **`inboundMessage`** — 傳入回覆內容（例如`stop`、`start`、`subscribe`）
   * **`inboundNumber`** — 收到傳入訊息的寄件者識別碼
   * **`channelType`** — 頻道類別（`Utility`、`Marketing`或`Promotional`）
   * **`profileNumber`** — 接收傳入訊息的電話號碼
   * **`origTimestamp`** - Meta / WhatsApp的原始時間戳記
   * **`status`** — 傳遞狀態包含標準化的提供者意見回應（`sent`、`delivered`、`bounce`、`error`、`delay`、`duplicate`、`denylist`、`exclude`或`unknown`）以及原始提供者狀態訊息
   * **`reactionEvent`** — 使用者回應的內容：回應的表情符號，或特定訊息的回覆文字
   * **`reactionMessageID`** — 正在回應的原始郵件識別碼
   * **`reactionActionName`** — 回應動作的型別（`react`、`unreact`或`reply`）
   * **`interactiveSelectedTitle`** — 使用者從WhatsApp互動式訊息中選取的標題
   * **`interactiveType`** — 互動式訊息型別（`list reply`、`button reply`或`button`）
   * **`interactiveSelectedDescription`** — 所選WhatsApp互動式選項的說明
   * **`interactiveSelectedID`** — 從WhatsApp選取選項的ID

  +++

### 內容與整合 {#may-26-content}

下列功能和改善專案已新增至此版本的內容管理和整合。

<table>
<thead>
<tr>
<th><strong>內容警告器選擇器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在使用<strong>內容警告器選取器</strong>，此統一強制回應視窗可同時選取Experience Manager Assets和內容片段。 新的選取器包括：</p>
<ul>
<li><strong>瀏覽、搜尋和篩選所有資產和片段的</strong>。</li>
<li><strong>AI語意搜尋</strong>：以簡單的語言描述您需要的內容，例如「山中的咖啡」，以根據含義和內容呈現內容相關的資產，而不只是文字相符。 也支援多語言查詢。</li>
<li><strong>簡短上傳</strong>：上傳行銷簡報，以根據其內容和需求自動呈現符合行銷活動內容的資產。</li>
<li><strong>Dynamic Media轉譯</strong>：挑選並套用動態資產的影像轉譯，而不需離開選取器。</li>
</ul>
<p>如需詳細資訊，請參閱<a href="../integrations/aem-content-advisor.md">詳細說明文件</a>。</p>
<p>推出日期： 2026年5月19日</p>
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
<p><b>整合</b>功能可讓您直接將第三方資料來源連線至 Adobe Journey Optimizer。 透過簡化您提取外部資料和<b>可撰寫內容</b>的方式，此功能可讓您更輕鬆地跨所有管道提供個人化的動態訊息。</p>
<p>之前以 Beta 版本發行，目前此功能所有環境都適用 (一般可用性)。</p>
<p>如需詳細資訊，請參閱<a href="../integrations/integrations.md">詳細文件</a>。</p>
<p>推出日期： 2026年5月4日</p>
</td>
</tr>
</tbody>
</table>

* **Assets選擇器中的跨組織存放庫存取** — 您現在可以直接在Adobe Experience Manager資產選擇器中，順暢地從多個組織的存放庫中選擇資產。

### 管理 {#may-26-admin}

* **URL引數加密** — 您現在可以加密追蹤中的URL引數，以及新增至您電子郵件訊息的登陸頁面連結。 這為敏感引數資料提供額外的安全層。 此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。 [閱讀更多](../personalization/url-parameter-encryption.md)

  推出日期： 2026年6月1日

* **金鑰登入的新許可權** — 現在需要兩個新許可權，才能存取和管理URL引數加密所需的金鑰： **管理金鑰登入**&#x200B;和&#x200B;**檢視金鑰登入**。 [閱讀更多](../administration/high-low-permissions.md#administration-permissions)

  推出日期： 2026年6月1日

<!--
+++ Coming soon — **Information below is subject to change.**

* **Message Feedback Event Dataset moving to batch ingestion** - The `AJO Message Feedback Event Dataset` is transitioning from streaming to batch ingestion mode. This change ensures that data ingestion does not exceed streaming ingestion limits. If you use this dataset in Customer Journey Analytics reports or run queries against it, expect an increase in data latency of up to 2 hours going forward.

  Availability date: June 1, 2026

+++
-->

### 可用性改善 {#may-26-usability}

以下可用性改良功能也於2026年5月發行。

#### 清單

* **大量動作** — 您現在可以在&#x200B;**行銷活動**、**片段**&#x200B;和&#x200B;**範本**&#x200B;清單中一次選取多個專案，並從單一動作列執行大量作業，包括新增專案至封裝、將其移至資料夾、編輯標籤、管理存取權，以及封存或刪除專案。 [了解更多](../start/search-filter-categorize.md#bulk-actions)

  ![](../start/assets/bulk-actions-campaigns.png)

* **排序和調整欄大小** - **行銷活動**、**片段**&#x200B;和&#x200B;**範本**&#x200B;清單現在支援按一下任何欄標題來排序。 在「行銷活動」資料夾檢視中，也可依&#x200B;**[!UICONTROL 優先順序]**&#x200B;和&#x200B;**[!UICONTROL 頻道設定]**&#x200B;進行排序和篩選。 **片段**&#x200B;和&#x200B;**範本**&#x200B;清單中的資料行寬度也是可調整大小的 — 拖曳資料行邊界以符合您最關心的資料。 [了解更多](../start/search-filter-categorize.md#filter-lists)

#### 內容製作

* **內嵌設定檔屬性編輯** — 電子郵件Designer中的內嵌設定檔屬性編輯最初於4月發行。 在5月發行版本中，此功能已從AI助理分離出來，並延伸至推播通道編輯器。 [了解更多](../personalization/personalize.md#inline-personalization)

  ![](../personalization/assets/inline-profile-attributes.png)

* **推播通道編輯器中的連結URL工具提示** — 當任何連結或媒體欄位中的URL太長而無法顯示時，該欄位旁邊永遠會顯示工具提示圖示 — 將滑鼠游標停留在該欄位上可檢視完整的URL。 [了解更多](../push/design-push.md#on-click-behavior)

  ![](../rn/assets/do-not-localize/push-link-tooltip.png)

<!--
#### Simulation & Preview

* **Redesigned preview experience** - The content preview screen has been redesigned with a side-by-side layout that lets you compare how your content renders across multiple profiles at a glance, enabling quicker and more confident reviews before sending. [Learn more](../test-approve/simulate-sample-input.md#preview)

  ![](../test-approve/assets/simulation-preview-redesign.png)
-->

+++ 即將推出 — **下列資訊可能會變更。**

* **歷程和行銷活動的資料夾** — 您現在可以將歷程和行銷活動整理到資料夾中，以改善介面中的導覽和管理。

  推出日期：2026年6月初

+++

