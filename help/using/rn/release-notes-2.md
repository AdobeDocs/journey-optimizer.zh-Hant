---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 發行說明
hide: true
source-git-commit: 6f67786674f995422a5add1600d7f0dbfe915067
workflow-type: tm+mt
source-wordcount: '2835'
ht-degree: 18%

---


<!-- DRAFT — Topic-based layout exploration. All content is identical to release-notes.md (May '26). The only change is the grouping axis: topic > type. -->

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="最新資訊"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能，並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer] 遵循持續傳遞模式，允許 Adobe 持續傳遞新功能、增強功能和修正。 此方法可讓您分階段推出可擴充的功能，以確保所有環境的效能和穩定性。 基於此模型，發行說明會在每月發行之間更新。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](releases.md)。

[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。 若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

>[!NOTE]
>
>這些發行說明中列出的功能包括&#x200B;**可用日期**，指出每個變更可在您的環境中存取的時間。 標示為&#x200B;**即將推出**&#x200B;的專案已排定在未來幾天或幾週發行。 這些區段中的資訊可能會有所變更。

## 2026年5月發行說明 {#may-26-rn}

### 歷程 {#may-26-journeys}

下列功能和改進專案已新增到此版本的歷程。 預計未來幾天或幾週也會有其他變更 — 請參閱下方的[即將推出](#may-26-journeys-coming-soon)區段。

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
<p>如需詳細資訊，請參閱<a href="../building-journeys/simulate-journey.md">詳細說明文件</a>。</p>
<p>推出日期： 2026年5月5日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程路徑最佳化 — 目標定位（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用新的<strong>最佳化</strong>節點來鎖定特定對象，以決定符合您以業務為中心的KPI的最佳途徑。</p>
<p>此工具可讓您開發更有效率的行銷活動，更可能在1:1層級引起共鳴、改善客戶的行銷個人化工作，並增強轉換和收入等重要的客戶參與KPI。</p>
<p>此功能先前在「有限可用性」中提供，現在可供所有環境使用。</p>
<p>推出日期： 2026年5月21日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程仲裁 — 排名公式（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用公式，根據客戶設定檔屬性和情境式因素自動提升歷程優先順序分數，確保客戶進入最相關的歷程。</p>
<p>此功能先前在「有限可用性」中提供，現在可供所有環境使用。</p>
<p>推出日期： 2026年5月21日</p>
</td>
</tr>
</tbody>
</table>

#### 即將推出 {#may-26-journeys-coming-soon}

未來幾天或幾週預計會有以下歷程功能。 **下列資訊可能會變更。**

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
<!--<p><img src="assets/do-not-localize/expression-assistant.gif"></p>-->
<p>推出日期： 2026年5月22日</p>
</td>
</tr>
</tbody>
</table>

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
<p>推出日期： 2026年6月1日</p>
</td>
</tr>
</tbody>
</table>

* **非循環讀取對象歷程的自動完成** — 非循環&#x200B;**讀取對象**&#x200B;歷程現在會在最後一個作用中設定檔退出後，自動轉換成&#x200B;**已停止**&#x200B;狀態。 以往，這些歷程會維持&#x200B;**即時**&#x200B;狀態，直到91天全域逾時到期 — 即使不再有設定檔流過。 透過這項改善，歷程狀態會在完成時反映實際執行狀態，讓您無需手動介入即可保持歷程詳細目錄準確。

  請注意，此行為不適用於包含導致等待期的節點的歷程，例如等待節點、反應節點或事件觸發的轉變。 這些歷程仍受標準91天全域逾時的約束。

  推出日期： 2026年5月21日

* **自訂動作中的憑證式自訂驗證** — 自訂動作現在支援憑證式自訂驗證。 將`subType: "certificateCredential"`新增至自訂授權設定後，Journey Optimizer會使用Adobe的Managed憑證來簽署JWT使用者端宣告，並將其交換為存取權杖 — 不需要使用者端密碼。 專為執行憑證式身分驗證的企業API （例如Azure Entra ID）而設計。

  推出日期： 2026年5月21日

* **關聯式資料以回圈為基礎的個人化** — 個人化編輯器現在支援在關聯式集合（例如訂單、帳戶或預訂）上重複執行的Loop區塊，並在單一電子郵件或簡訊中為每個記錄呈現一個內容區塊。 集合是使用個人化權杖透過資料選擇器設定，不需要撰寫運算式。

  推出日期： 2026年6月1日

* **外部對象的補充識別碼支援** — 歷程中的補充識別碼現在支援外部對象，包括從CSV檔案匯入的對象和使用Federated Audience Composition建立的對象。 您可以從對象中指定任何非身分屬性或非個人身分屬性作為補充ID — 不需要架構標籤。

  推出日期： 2026年6月1日

### 協調的行銷活動 {#may-26-oc}

下列功能和改善專案已新增至此版本中的協調行銷活動。 預計未來幾天或幾週也會有其他變更 — 請參閱下方的[即將推出](#may-26-oc-coming-soon)區段。

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
<p>如需詳細資訊，請參閱<a href="../orchestrated/trigger-orchestrated-campaign.md#signal-end">詳細說明文件</a>。</p>
<p>推出日期： 2026年5月20日</p>
</td>
</tr>
</tbody>
</table>

* **在擴充活動中新增連結** — 在協調行銷活動的擴充活動中現在可以使用新增連結功能。 這可讓您在工作表格資料與現有的資料庫表格之間建立直接關係。

  推出日期： 2026年5月20日

#### 即將推出 {#may-26-oc-coming-soon}

預計未來幾天或幾週內，將推出下列精心安排的行銷活動功能。 **下列資訊可能會變更。**

<table>
<thead>
<tr>
<th><strong>針對協調行銷活動的檔案式目標定位（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>協調的行銷活動現在支援直接將CSV或TXT檔案載入行銷活動畫布作為目標對象，而不先將檔案擷取到Adobe Experience Platform。 檔案資料會在執行時使用，不會儲存為Adobe Experience Platform資料集。 在檔案設定期間，您可以定義欄對應、資料型別、NULL處理和每欄錯誤原則。 這支援無法建立完整擷取管道的臨時傳送或合作夥伴清單行銷活動。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>推出日期： 2026年6月1日</p>
</td>
</tr>
</tbody>
</table>

### 行銷活動 {#may-26-campaigns}

#### 即將推出 {#may-26-campaigns-coming-soon}

預計未來幾天或幾週會有以下行銷活動改良專案。 **下列資訊可能會變更。**

* **促銷活動生命週期事件的客戶警示** — 新的系統警示現在會通知您動作和API觸發之促銷活動的重要生命週期事件。 在沙箱層級訂閱。

  推出日期： 2026年6月1日

* **覆寫行銷活動中的預設執行欄位** — 先前可在歷程層級使用，您現在可以覆寫行銷活動引數中電子郵件、簡訊和WhatsApp傳送的預設執行欄位全域設定。

  推出日期： 2026年6月1日

### 決策 {#may-26-decisioning}

下列功能和改進專案已新增至此版本中的Decisioning。 預計未來幾天或幾週也會有其他變更 — 請參閱下方的[即將推出](#may-26-decisioning-coming-soon)區段。

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

* **決定移轉工作流程API** — 建立相依性分析和移轉工作流程的API合約已更新：在要求URL （`sandbox`、`offer`或`decision`）上傳遞&#x200B;**`request-level`**&#x200B;作為&#x200B;**查詢引數**。 JSON內文中不得再傳送請求層級。 [閱讀全文](../experience-decisioning/decisioning-migration-api.md)

  推出日期： 2026年5月6日

* **決策中的Adobe Experience Manager內容片段** — 您現在可以將Adobe Experience Manager內容片段對應至決策中的決策專案，並在決策政策內運用這些片段，以便在適當的時間將適當的片段提供給適當的客戶。 [閱讀全文](../integrations/aem-fragments.md#aem-decisioning)

  此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。

  推出日期： 2026年5月20日

#### 即將推出 {#may-26-decisioning-coming-soon}

預計未來幾天或幾週內，將會有以下決策功能。 **下列資訊可能會變更。**

<table>
<thead>
<tr>
<th><strong>直接郵件通道中的決策支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將決定政策新增到直接郵件歷程和行銷活動中。 決策原則是優惠方案的容器，可運用決策引擎以動態方式傳回每個對象成員的最佳內容。 直接郵件決定也支援批次決定使用案例，讓您為特定Adobe Experience Platform對象中的每個設定檔匯出對應的優惠專案。</p>
<!--<p><img src="assets/do-not-localize/exd-dm.gif"></p>-->
<p>推出日期： 2026年6月1日</p>
</td>
</tr>
</tbody>
</table>

### 電子郵件頻道 {#may-26-email}

下列功能和改進專案已新增到此版本的電子郵件通道。 預計未來幾天或幾週也會有其他變更 — 請參閱下方的[即將推出](#may-26-email-coming-soon)區段。

<table>
<thead>
<tr>
<th><strong>電子郵件設計工具中的深層連結</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以透過電子郵件設計工具中的專用選項，將深層連結新增至您的電子郵件內容。 這可確保使用者直接導向至正確的應用程式內內容，而非重新導向至瀏覽器或應用程式商店，以保留內容與參與度。</p>
<p><img src="assets/do-not-localize/deeplinks.gif"></p>
<p>如需詳細資訊，請參閱<a href="../email/deeplinks.md">詳細說明文件</a>。</p>
<p>推出日期： 2026年5月12日</p>
</td>
</tr>
</tbody>
</table>

#### 即將推出 {#may-26-email-coming-soon}

未來幾天或幾週內，預計將會有以下電子郵件管道的改善。 **下列資訊可能會變更。**

* **個人化每個收件者和行銷活動的電子郵件寄件者詳細資料** — 協調的行銷活動現在支援使用設定檔屬性或關聯資料，個人化電子郵件標題欄位，包括寄件者名稱、寄件者地址和回覆對象。 如此可讓寄件者詳細資料反映每個收件者的相關顧問、位置或分支，而非透過單一公司地址路由傳送所有傳送。

  可在管道層級設定標題值，並使用內容相關資料覆寫每個行銷活動，以獲得更精確的控制。

  推出日期： 2026年6月1日

* **可編輯片段欄位中的RTF文字** — 您現在可以新增RTF文字至您的電子郵件內容中所使用的可自訂片段。 例如，使用文字元件作為電子郵件Designer中的可編輯欄位時，您可以直接格式化內容（例如粗體和斜體）並插入超連結。

  推出日期： 2026年6月1日

* **限製片段中的繼承中斷** — 現在當您建立或編輯片段時，可以選擇在電子郵件中使用時是否可修改片段。 鎖定片段可確保片段在出現的所有地方都保持同步，避免進行可能違反品牌標準或法規遵循要求的本機編輯。 此設定稍後可更新，並套用至未來的用途。

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

* **字元計數** — 您現在可以使用字元計數即時監視SMS訊息的長度。 它可協助您檢視訊息何時將分割成多個區段，以更好地管理格式並避免傳送成本意外增加。 [閱讀全文](../mobile/create-mobile-message.md)

* **簡訊傳入至自訂資料集** - 在&#x200B;**簡訊 API 認證**&#x200B;中，將&#x200B;**傳入簡訊**&#x200B;路由至您選取的&#x200B;**自訂、已啟用輪廓的體驗事件資料集**，而非僅預設追蹤資料集。 [閱讀全文](../mobile/mobile-webhook.md)

* **Webhook 介面增強功能** - 在設定簡訊 Webhook 時，使用者介面現在包含內建的設定指南，其中包含實用的範例，可讓您更輕鬆地調整提供者裝載並疑難排解問題，而無需離開設定流程。 [閱讀全文](../mobile/mobile-webhook.md)

### WhatsApp 頻道 {#may-26-whatsapp}

下列改良功能已新增至此版本的WhatsApp管道。

* **WhatsApp按鈕支援和追蹤** - WhatsApp範本現在支援&#x200B;**快速回覆**、**Call to action - URL**&#x200B;和&#x200B;**Call to action -**，不支援&#x200B;**複製代碼**。 Journey Optimizer會傳送支援的按鈕並追蹤與其他管道報表的互動。

* **WhatsApp頻道內容資料** - Journey Optimizer現在會擷取從WhatsApp頻道傳回的其他互動資料，並將其儲存在`whatsAppChannelContext`欄位群組下的&#x200B;**AJO EmailTrackingExperienceEvent資料集**。

  +++ 為WhatsApp對象建立和參與分析擷取的欄位

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
<li><strong>瀏覽、搜尋和篩選所有資產和片段</strong>。</li>
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
<th><strong>整合（全面發佈）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><b>整合</b>功能可讓您直接將第三方資料來源連線至 Adobe Journey Optimizer。 透過簡化您提取外部資料和<b>可撰寫內容</b>的方式，此功能可讓您更輕鬆地跨所有管道提供個人化的動態訊息。</p>
<p>此功能先前在Beta中發行，現在可供所有環境使用。</p>
<p>如需詳細資訊，請參閱<a href="../integrations/integrations.md">詳細文件</a>。</p>
<p>推出日期： 2026年5月4日</p>
</td>
</tr>
</tbody>
</table>

* **Assets選擇器中的跨組織存放庫存取** — 您現在可以直接在Adobe Experience Manager資產選擇器中，順暢地從多個組織的存放庫中選擇資產。

### 管理 {#may-26-admin}

#### 即將推出 {#may-26-admin-coming-soon}

未來幾天或幾週預計會有以下管理改善專案。 **下列資訊可能會變更。**

* **歷程和行銷活動的資料夾** — 您現在可以將歷程和行銷活動整理到資料夾中，以改善介面中的導覽和管理。

  推出日期： 2026年5月21日

* **訊息回饋事件資料集正移至批次擷取** - `AJO Message Feedback Event Dataset`正在從串流模式轉換為批次擷取模式。 這項變更可確保資料擷取不超過串流擷取限制。 如果您在Customer Journey Analytics報表中使用此資料集，或對其執行查詢，預計未來最多2小時的資料延遲會增加。

  推出日期： 2026年6月1日

### 報告 {#may-26-reporting}

#### 即將推出 {#may-26-reporting-coming-soon}

預計未來幾天或幾週將有以下報告改進。 **下列資訊可能會變更。**

* **排除電子郵件和簡訊報告的機器人點按** — 現在提供新的預估量度，以協助篩選出電子郵件和簡訊報告中的非人類（機器人）互動。 這些包括預估點按率、點進率(CTR)和點進開啟率(CTOR)，提供更準確真實客戶參與情況的檢視。 現有量度維持不變，這些新量度可與目前報表搭配使用，以改善分析。

  推出日期： 2026年6月1日
