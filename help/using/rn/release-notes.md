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
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 4f3312974e2533c97954e887b4371de6fc80595a
workflow-type: tm+mt
source-wordcount: '2079'
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
>這些發行說明中列出的功能包括&#x200B;**可用日期**，指出每個變更在您的環境中可用的時間。 **即將推出**&#x200B;摺疊式版面中的項目預計將在未來幾天或幾週內推出。 這些部分的資訊可能會有變更。

## 2026年9月發行說明 {#sep-26-updates}

### 內容管理 {#sep-26-content-management}

<table>
<thead>
<tr>
<th><strong>CX Coworker中的內容管理MCP工具</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Coworker現在有一組新的<strong>內容管理MCP工具</strong>，可讓您透過自然語言提示探索和管理Journey Optimizer內容資產。 要求其列出或擷取內容範本、片段、登陸頁面，以及歷程/行銷活動內嵌訊息內容。 此外也可以建立內容、更新範本，以及建立、更新、複製和發佈片段，並直接在歷程和行銷活動中更新內嵌頻道動作內容。</p>
<p>如需詳細資訊，請參閱<a href="../content-management/content-management-coworker-skills.md#content-management">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年9月3日</p>
</td>
</tr>
</tbody>
</table>

* **登陸頁面的強制同意核取方塊** — 您現在可以在登陸頁面表單元件中讓核取方塊成為強制性，要求訪客在提交表單前先選取該核取方塊（例如，提供同意）。 [了解更多](../landing-pages/lp-content.md#use-form-component)

  推出日期： 2026年9月4日

* **個人化語法中的其他保留關鍵字** - Profile Query Language (PQL)中的保留關鍵字清單已展開，以包含一般關鍵字、時間單位和布林值/邏輯運運算元。 如果您的XDM結構描述包含符合其中一個關鍵字的欄位名稱，請以反引號將其包住，以便在個人化運算式中參照。 [了解更多](../personalization/personalization-syntax.md#reserved-keywords)

  推出日期： 2026年9月1日

### 忠誠度 {#sep-26-loyalty}

<table>
<thead>
<tr>
<th><strong>熟客方案事件對應更新</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>建立或編輯事件對應現在使用新的&#x200B;**視覺對應產生器**：選取結構、從可搜尋的欄位選擇器挑選欄位、將每個欄位對應到具有每列連線狀態的忠誠度事件欄位，以及預覽自動產生的JSONata運算式，並可以選擇隨時切換為手動JSONata編輯。</p><p>此外，忠誠度管理員中的「事件定義」已重新命名為「事件對應」，而重新整理的清單檢視會顯示人類看得懂的體驗事件結構描述名稱。</p>
<p>如需詳細資訊，請參閱<a href="../loyalty-challenges/loyalty-admin.md#event-mappings">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年9月22日</p>
</td>
</tr>
</tbody>
</table>

* **「永遠」忠誠度挑戰** — 忠誠度挑戰現在可以無限期地執行。 設定排程時，將&#x200B;**挑戰結束**&#x200B;設為&#x200B;**無結束日期**，挑戰永不過期。 [了解更多](../loyalty-challenges/create-challenges.md#schedule)

  推出日期： 2026年9月1日

* **Healthcare Shield與Privacy and Security Shield客戶可使用Loyalty** - Healthcare Shield與Privacy and Security Shield客戶現在可使用Journey Optimizer Loyalty。 [了解更多](../loyalty-challenges/get-started.md)

  推出日期： 2026年9月15日

+++ 即將推出 — **下列資訊可能會有變更。**

* **每個成員忠誠度挑戰完成期限** — 忠誠度挑戰現在支援每個成員完成期限：在「完成要求」底下選擇「選擇加入後的數天內」，以便每個成員的截止日期根據其自己的選擇加入日期計算，而不是整個方案的固定結束日期。 如果挑戰結束日期及此選擇加入期間皆已設定，則每個成員的截止日期為第一個出現的日期。<!-- Documentation link: TBD -->

+++

### 歷程 {#sep-26-journeys}

<table>
<thead>
<tr>
<th><strong>同事中的歷程模擬</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Co-worker中的<strong>歷程模擬技能</strong>可自動進行端對端歷程驗證，並讓您輕鬆解讀結果。 請注意，此功能目前僅支援快速模擬流程，不會完全取代Journey Optimizer手動模擬體驗。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journeys-coworker-skills.md#journey-simulation">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年9月23日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程層級保留 (有限可用性)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以直接從歷程屬性設定歷程的保留群組。 保留群組是目標客群中可設定的百分比，這會被排除在歷程之外，且不會收到任何訊息。 將保留設定檔與 Customer Journey Analytics 報告中的現用設定檔進行比較，即可測量歷程帶來的增量提升度 (實際影響)。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。 如需發行週期與可用性階段的完整詳細資訊，請參閱 <a href="releases.md">Journey Optimizer 發行週期</a>。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-properties.md#performance-management">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年9月1日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在歷程中使用AI產生運算式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程進階運算式編輯器現在整合了AI支援的運算式產生：說明您要以自然語言建置的運算式，而編輯器產生您可以立即套用或通過後續提示調整的現成程式碼。</p>
<p>此功能先前以限額版本推出，現在已可在所有環境中使用 (正式版本)。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/expression/generate-expression.md">詳細文件</a>。</p>
<p>推出日期： 2026年9月1日</p>
</td>
</tr>
</tbody>
</table>


* **受眾資格歷程中的跳轉活動支援** — 您現在可以在以受眾資格節點開始的歷程中使用跳轉活動，以跳至事件型歷程。 此功能正在逐步推廣至組織。 如果您的環境中沒有看到此內容，可能是因為您仍在對象資格中使用批次對象。 [了解更多](../building-journeys/jump.md)

  推出日期：2026年9月22日。

* **批次對象評估後觸發** — 對於以批次對象為目標的週期性歷程，您可以在歷程執行前設定最多6小時的等待時間，以進行新的批次評估。 如果評估正在進行中，歷程會等待它完成；如果上次執行使用了最新的快照，則會等待較新的批次。 如果等候期間結束時沒有可用的新受眾，則會略過該事件。 [了解更多](../building-journeys/read-audience.md)

  推出日期： 2026年9月18日

* 歷程模擬中的&#x200B;**決策** — 模擬現在支援路徑實驗，作為&#x200B;**最佳化**&#x200B;活動的一部分。 路由是由Decisioning處理，而且每個模擬使用者是隨機且非確定性的。

  [了解更多](../building-journeys/simulate-journey-gs.md)

  推出日期： 2026年9月15日

* **偵測到新的歷程異常警報** — 現在，當即時歷程的每日流量在歷程登入、歷程退出和事件傳送之間偏離其歷史基準線，或意外降至零時，新的系統警報會警告您。 此警報目前僅可用於生產沙箱。

  [了解更多](../reports/alerts.md)

  推出日期： 2026年9月15日

* **歷程模擬中的決策** — 您現在可以模擬依賴決策的歷程，新增支援下列專案：

  * 「模擬」現在支援「內容決策」節點。
  * 「模擬」現在支援「最佳化」活動的目標定位規則方法。
  * 具有Adobe Journey Optimizer決策內容的動作（例如使用決策原則的電子郵件）現在可在模擬中支援。
  * 完全支援使用優惠資格，以及依規則、對象、優先順序或公式排名的決定原則。 依AI模型排名 — 也支援Personalization，不過傳回的優惠方案可能因執行而異。

  [了解更多](../building-journeys/simulate-journey-gs.md)

  推出日期： 2026年9月8日

* **分析歷程異常技能** - CX Coworker現在可以使用&#x200B;**分析歷程異常**&#x200B;技能，根據歷史基準線，偵測歷程進入、退出或訊息傳送計數中的非預期尖峰、下降或平線。 在確認真正的異常後，該技能會執行唯讀診斷，以找出可能的根本原因和建議。 [了解更多](../building-journeys/journeys-coworker-skills.md#journey-analyze)

  推出日期： 2026年9月2日

* **歷程運算式編輯器中的新dateDiff函式** — 歷程運算式編輯器現在包含`dateDiff`函式，以天數計算兩個日期之間的差異。 此函式適用於以時間為基礎的邏輯，例如建立截止日期、計算客戶生命週期持續時間或在歷程條件中建立倒數計時器。  [了解更多](../building-journeys/functions/date-functions.md#dateDiff)

  推出日期： 2026年9月1日

+++ 即將推出 — **下列資訊可能會有變更。**

<table>
<thead>
<tr>
<th><strong>歷程畫布中的內容預覽</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>今天檢閱管道內容需要一次一個地個別開啟每個活動 — 在包含許多管道活動的歷程中緩慢且容易出錯，尤其是當個人化表示檢查每個活動的多個處理或變體時。 <strong>內容預覽</strong>透過直接在畫布中顯示每個頻道活動的內容縮圖，以全熒幕模式檢查並在處理與變體之間切換，來移除該摩擦。</p>
<p>目標推出日期： 2026年9月28日</p>
</td>
</tr>
</tbody>
</table>

* **衛生分析技能** - CX Coworker現在可以掃描您的使用中歷程和草稿歷程，找出中斷的設定、無訊息失敗、過時或未使用的資產，例如過時的草稿歷程、孤立的資料來源和持續的自訂動作錯誤，並直接在聊天中呈現建議的修正。<!-- Documentation link: TBD -->

+++

### 行銷活動 {#sep-26-campaigns}

+++ 即將推出 — **下列資訊可能會有變更。**

* **動作行銷活動的資料夾** — 您現在可以將動作行銷活動整理到資料夾中，以改善介面中的導覽和管理。

* **覆寫動作行銷活動中的預設執行欄位** — 您現在可以覆寫動作行銷活動引數中針對電子郵件、簡訊和WhatsApp傳遞全域設定的預設執行欄位（先前可在歷程層級使用）。

+++

### 協調的行銷活動 {#sep-26-orchestrated-campaigns}

<table>
<thead>
<tr>
<th><strong>協調行銷活動的警報</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>協調的行銷活動現在透過在歷程及行銷活動中使用的相同警報架構，支援<strong>自動警報</strong>。 行銷活動執行失敗、逾時時時會觸發警報，每個警報都包含已發生的事件、發生時間、地點以及畫布的直接連結，以便檢視記錄檔中的進一步詳細資訊。</p>
<p>如需詳細資訊，請參閱<a href="../orchestrated/start-monitor-campaigns.md#alerting">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年9月22日</p>
</td>
</tr>
</tbody>
</table>

* **在協調的行銷活動中具有關聯資料的條件式內容** — 在電子郵件Designer中針對協調的行銷活動建立條件式內容時，您現在可以直接在關聯式資料（例如與設定檔相關聯的相關記錄）上建立條件，而不只是標準設定檔屬性。 [了解更多](../orchestrated/activities/channels.md#add-personalization)

  推出日期： 2026年9月22日

### 入門 {#sep-26-onboarding}

以下改進即將在此版本中推出。

<table>
<thead>
<tr>
<th><strong>入門電子郵件和歷程的引導功能</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>入門電子郵件和歷程的引導功能現在包括下列改進：</p>
<ul>
<li>當您移轉電子郵件時，[!DNL Journey Optimizer]會識別該電子郵件所參考的內容區塊，並將其顯示為行動專案，因此您可以隨電子郵件移轉內容區塊。</li>
<li>介面已經過改良，讓引導式入門更直覺。</li></ul>
<p>如需詳細資訊，請參閱<a href="../start/onboarding-hub.md">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年9月2日s3</p>
</td>
</tr>
</tbody>
</table>

### 個人化 {#sep-26-personalization}

* **使用AI修正語法** — 偵測到PQL語法驗證錯誤時，Personalization編輯器現在會提供「使用AI修正」選項，協助直接從編輯器解決問題。

  推出日期： 2026年9月22日

### 決策 {#sep-26-decisioning}

<table>
<thead>
<tr>
<th><strong>Web Channel中的決策支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>決策功能現在可用於網頁管道。 您可以直接在網頁視覺化編輯器中使用決策原則，將最相關的產品建議傳送給每位訪客。</p>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/use-decision-policy.md">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年9月22日</p>
</td>
</tr>
</tbody>
</table>

* **在規則和排名公式模擬中支援Adobe Experience Platform設定檔** — 模擬規則或排名公式時，您現在可以選取Adobe Experience Platform設定檔來自動填入測試資料變體的屬性，而不是手動輸入。 [了解更多](../experience-decisioning/ranking/ranking-formulas.md#simulate-ranking-formula)

  推出日期： 2026年9月22日

### 客群 {#sep-26-audiences}

以下提醒適用於此版本中的對象。

* **即將變更對象構成擴充對象** — 在10月發行（10月底）期間，Journey Optimizer將停止使用或參考來源資料集沒有&#x200B;**主要身分描述項**&#x200B;的對象構成對象的歷程和行銷活動。 此後，歷程和行銷活動僅支援使用主要身分描述項建立的對象構成對象。 如果您需要這些歷程或行銷活動才能保持作用中，請聯絡您的Adobe代表 — 我們的產品團隊可以協助您移轉。<!-- Documentation link: TBD -->

### 管理 {#sep-26-administration}

下列提醒適用於此版本中的管理。

* **資料集存留時間(TTL)護欄 — 現有的沙箱** — 從2026年10月1日起，Journey Optimizer系統產生的資料集的存留時間(TTL)護欄（設定檔存放區為90天，資料湖為13個月）將強制用於現有的客戶沙箱和組織。

### 可用性改進功能 {#sep-26-usability}

* **片段驗證警示中的AI總覽** — 片段驗證警示對話方塊現在包含AI總覽，其中總結並說明了驗證問題（例如格式錯誤的運算式、缺少設定檔欄位以及無效的JSON），讓使用者可以更快進行疑難排解。

  推出日期： 2026年9月22日

* **更輕鬆地在新的歷程畫布中分離及加入分支** — 您現在可以將分支從歷程的其餘部分分離而不刪除它，並稍後透過直接在畫布上選取符合資格的活動，或從已中斷連線或已使用分支的清單中選取它，在不同的時間點重新加入。 [了解更多](../building-journeys/using-the-journey-designer.md#join-and-detach-branches)

  推出日期： 2026年9月1日

