---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 94ac5fda2d10beb1fd016f41aa298a82694043c3
workflow-type: tm+mt
source-wordcount: '1904'
ht-degree: 39%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都將在每個月最後一週的發行說明中合併。 [!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2024年10月發行 {#24-10-rn}

**發行日期**： 2024年10月29至30日

### 新功能 {#24-10-features}

此版本提供下列詳細的新功能：

<table>
<thead>
<tr>
<th><strong>鎖定電子郵件內容</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 現在允許您透過鎖定整個範本，或是特定結構和元件，鎖定電子郵件範本中的內容。這樣做讓您可以防止無意間不小心編輯內容，或將內容刪除，讓您更能掌控範本自訂，進而提高電子郵件行銷活動的效率和可靠性。</p>
<p>如需詳細資訊，請參閱<a href="../content-management/content-locking.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
<p>自2024年10月24日起提供</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程中的程式碼型體驗</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過程式碼型體驗管道，Adobe Journey Optimizer 可讓您針對任何傳入屬性進行進階個人化及測試，跨不同接觸點 (例如網頁應用程式、行動應用程式、桌面應用程式、視訊主控台、電視連結的裝置、智慧型電視、資訊站、ATM、IoT 裝置等) 達成量身打造的無縫傳遞體驗。程式碼型體驗管道現可在歷程版面中使用。</p>
<p>如需詳細資訊，請參閱<a href="../code-based/create-code-based.md">詳細文件</a>。</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>自2024年10月1日起提供</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程中的網站體驗</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>有了網頁管道，Adobe Journey Optimizer 可讓您將透過傳入網頁歷程向客戶提供的網站體驗個人化。網頁管道現可在歷程版面中使用。</p>
<p>如需詳細資訊，請參閱<a href="../web/create-web.md">詳細文件</a>。</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>自2024年10月1日起提供</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>衝突與優先順序管理（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在Journey Optimizer中，管理行銷活動和歷程的數量和時機是避免客戶因太多互動而感到不知所措的關鍵。 Journey Optimizer現在提供數種衝突管理和優先順序的工具。 <p>如需詳細資訊，請參閱<a href="../conflict-prioritization/gs-conflict-prioritization.md">詳細文件</a>。</p></p><p><ul><li><b>歷程頻率上限</b>：您現在可以建立規則集以套用至您的歷程，讓您限制設定檔每日、每週或每月的歷程次數，並控制同時執行的並行歷程次數。</li>
<li><b>優先順序分數</b>：您現在可以指派優先順序分數至行銷活動或歷程，範圍從0到100。 數字越高表示優先順序越高。 當兩個行銷活動或歷程動作使用相同的管道設定時，Journey Optimizer會選取優先順序分數最高的行銷活動。 如果行銷活動具有相同的分數，將會選擇最近修改最低的行銷活動。</li>
<li><b>檢視潛在衝突</b>：歷程和行銷活動中的新「檢視潛在衝突」按鈕現在可讓您識別與其他歷程或行銷活動的重疊，例如開始日期、目標對象或選取的頻道設定。</li>
<li><b>歷程仲裁</b>：這項新功能可讓您為客戶提供最重要的歷程優先順序。 您可以建立規則，以在客戶符合即將進入的較高優先順序歷程的資格時，抑制進入較低優先順序歷程。</li>
<li><b>依通訊型別設定頻率上限： </b>使用規則集，您現在可以依通訊型別（例如「銷售」、「促銷」）設定精細規則，以防止訊息相似的客戶超載。 您可以跨多個管道控制頻率，自動排除過度請求的設定檔，以確保更好的客戶體驗。</li></ul>

<p>特定客戶群組可在「有限可用性」中使用衝突和優先順序管理功能。 請注意，這些功能將在未來逐步向更多使用者推出。 如果您有興趣新增至這些功能的輪候表，請洽詢您的客戶團隊。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Mobile Ink與Adobe Journey Optimizer整合</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以整合Mobile Ink Da Vinci與Adobe Journey Optimizer。 透過這項新整合，您可以： </p>
<p><ul><li>利用Mobile Ink的Da Vinci產品中的強大功能，為批次行銷活動組合和個人化電子郵件變體</li>
<li>使用Da Vinci進行製作和Adobe Journey Optimizer進行最佳化和交付的Journey Optimizer客戶，加速從業者工作流程</li>
<li>使用Adobe資料最佳化達文西模型。</li></ul></p>
<p>如需詳細資訊，請參閱<a href="https://movableink.com/adobe-and-movable-ink">Movable Ink Da Vinci檔案</a>。</p>
</tr>
</tbody>
</table>

先前可供一組組織(LA)使用，現在所有使用者(GA)都可使用下列功能：

<table>
<thead>
<tr>
<th><strong>電子郵件設定個人化（全面發佈） </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>為提升彈性並控制電子郵件設定，您可以在建立電子郵件通道設定時定義動態子網域和個人化的標題引數。
</p>
<p>如需詳細資訊，請參閱<a href="../email/surface-personalization.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>自2024年10月23日起提供</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>歷程與行銷活動中的核准（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>待政策通過核准，您就可以立即在 Journey Optimizer 中設定核准程序，允許行銷團隊使用，以確保行銷活動和歷程在正式上線之前，會先由合適的利害關係人負責審核並簽核。</p>
<p>如需詳細資訊，請參閱<a href="../test-approve/gs-approval.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/approval.gif"/>
<p>自2024年10月22日起提供</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>歷程中的內容實驗（全面發佈）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 現在支援歷程的實驗，行銷活動已提供此功能。實驗是在線上測試的情境下進行的隨機試驗，意即某些隨機選取的使用者會接觸到訊息的指定變化，而另一組隨機選取的使用者則會接觸到一些其他處理方式。 接觸到後，您就可以測量感興趣的結果量度，例如電子郵件開啟、訂閱或購買數。</p>
<p>如需詳細資訊，請參閱<a href="../content-management/content-experiment.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Decisioning (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning, previously available for a set of organizations (LA) and known as Experience Decisioning, is now available to all users (GA), including organizations that have purchased the Adobe Healthcare Shield or Privacy and Security Shield add-on offerings.</p><p>Decisioning simplifies personalization by offering a centralized catalog of marketing offers known as 'decision items' and a sophisticated decision engine. This engine leverages rules and ranking criteria to select and present the most relevant decision items to each individual. These decision items are seamlessly integrated into a wide range of inbound surfaces through the code-based experience channel.</p>
<p>For more information, refer to the <a href="../experience-decisioning/gs-experience-decisioning.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>歷程與行銷活動中的多語言訊息（全面發佈）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在單一行銷活動或歷程中，輕鬆建立多種語言的內容。透過此功能，您可以在編輯行銷活動或歷程時切換語言、簡化整個編輯流程，並提高有效管理多種語言內容的能力。</p>
<p>如需詳細資訊，請參閱<a href="../content-management/multilingual-gs.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/multilingual.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>更新的報告體驗（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer報告功能現已正式推出(GA)，且與Customer Journey Analytics功能的互通性也得以改善，將兩個平台的報告標準化，並改善資料一致性和可靠性。 Journey Optimizer 與 Customer Journey Analytics 之間的緊密整合可讓您更清楚檢視績效量度，讓使用者能做出更明智的決策。</p>
<p>正式發行中引進了四項新功能：建立簡易量度、建立和發佈對象、使用Insight Builder提出臨時問題，以及排程報表自動以電子郵件傳送給主要收件者。</p>
<p>如需詳細資訊，請參閱<a href="../reports/report-cja-manage.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>重要：目前的報告體驗將於2025年1月淘汰。 在此日期之後，新的報告體驗將成為標準體驗。建議您熟悉新功能，以確保順利轉換。 <a href="../reports/report-gs-cja.md">了解如何開始使用 Journey Optimizer 的新報表介面</a></p>
<p>自2024年10月16日起提供</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用範例輸入資料測試您的內容(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在可讓您透過預覽內容並使用從檔案上傳或手動新增的範例輸入資料傳送校樣來測試內容的不同變體。 系統會自動偵測您在內容中用於個人化的所有設定檔屬性，這些屬性可用於測試，以建立多個變體。</p>
<p>此功能目前以公開測試版的形式提供給所有客戶用於電子郵件、簡訊和推播通知頻道。</p>
<p>如需詳細資訊，請參閱<a href="../test-approve/simulate-sample-input.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--The following capabilities are available to all customers in public beta:

<!--<table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from Adobe Experience Platform in the personalization editor to personalize your content. To do this, datasets needed for lookup personalization must first be enabled through an API call. Once done, you can use their data to personalize your content into [!DNL Journey Optimizer].</p>
<p>This capability is currently available to all customers as a public beta.</p>
<p>For more information, refer to the <a href="../personalization/lookup-aep-data.md"</a>.</p>
</td>
</tr>
</tbody>
</table>-->

### 改進項目 {#24-10-improvements}

此發行版本隨附下列改進項目。

**簡訊頻道**

已引進簡訊增強功能來改善您的傳訊功能：

* 您可以定義和管理簡訊行銷活動和歷程的唯一關鍵字，以實現更個人化且有效率的通訊。

* 當關鍵字無法辨識時，您可以建立並傳遞預設簡訊。

* 您現在可以編輯或刪除SMS API頻道設定。

在[Infobip](../sms/sms-configuration-infobip.md)和[Sinch](../sms/sms-configuration-sinch.md)的SMS設定檔案中進一步瞭解這些改善。

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!—* **即時歷程的最大數量** - Journey Optimizer在生產沙箱上現在具有500個即時歷程的護欄，而不是100個。 即時歷程的數量會顯示在歷程畫布中。<!-- DOCAC-10977-->

**網路頻道**

* **網頁設計工具的非視覺化編輯模式** — 作為Journey Optimizer網頁設計工具的替代方案，您現在可以使用非視覺化編輯器對您的網站新增修改。 它可讓您手動輸入變更，而不需在視覺編輯器中開啟頁面。 如果您無法安裝瀏覽器擴充功能(例如Adobe Experience Cloud Visual Helper)，這種非視覺化編輯模式相當實用；在Web設計工具中載入頁面需要此擴充功能。 [了解更多](../web/web-non-visual-editor.md)


**資料集**

* **傳送並開啟事件** — 自2024年11月1日起，串流區段將不再支援使用Journey Optimizer追蹤和意見反應資料集中的傳送和開啟事件。 此變更將套用至所有客戶沙箱和組織。 [了解更多](../data/datasets-ttl.md#segmentation-update)

* **資料集存留時間(TTL)** — 從2025年2月開始，將在新沙箱和新組織中向Journey Optimizer系統產生的資料集推出存留時間(TTL)護欄，如下所示：

   * 輪廓存放區中的資料為 90 天
   * 資料湖中的資料為 13 個月

  此變更將在後續階段中推出至現有客戶沙箱。 [了解更多](../data/datasets-ttl.md#ttl)

* **自訂動作中的引數** （使用日期：2024年10月3日） — 自訂動作現在支援NULL和選用引數。 [了解更多](../action/about-custom-action-configuration.md#define-the-message-parameters)

**報告**

* **Experience Decisioning報告**&#x200B;現已可用，可提供訪客如何與您的體驗互動的基本深入分析。 [了解更多](../reports/campaign-global-report-cja-code.md##decisioning-kpis)

**資料治理與同意原則** - 推出日期：2024 年 10 月 7 日

* 已在 Journey Optimizer 的所有管道中強制執行&#x200B;**資料治理原則**。對於已在Adobe Experience Platform中建立原則的客戶，這些原則會套用至行銷動作，作為管道設定的一部分。 使用設定建立內容時，系統會檢查所有個人化欄位是否有任何資料治理違規。如果發現違規，將無法發佈歷程或行銷活動。[了解更多](../action/action-privacy.md)

* **自訂同意原則**&#x200B;現在適用於所有Journey Optimizer 管道。在傳送訊息或提供傳入體驗之前強制執行時，系統會檢查使用者是否已同意在將收到的內容中使用個人化欄位。如果未予以同意，則不會顯示該體驗。[了解更多](../action/consent.md)

  >[!NOTE]
  >
  >同意原則目前僅適用已購買 Adobe **Healthcare Shield** 與&#x200B;**隱私權與安全性防護**&#x200B;附加產品的組織。

**對象** - 推出日期： 2024 年 10 月 8 日

* 當鎖定目標的 CSV 檔案對象時，您現在可於個人化編輯器與在行銷活動和歷程規則產生器，使用檔案中的屬性。[了解更多](../audience/about-audiences.md)

* 現在可以使用自訂上傳 (CSV 檔案) 中的對象與屬性，來與 Healthcare Shield 或 Privacy and Security Shield 搭配使用

**組態** — 推出日期： 2024年10月23日

* 在行銷活動或歷程中使用個人化設定時，您現在可以預覽電子郵件內容，以使用您定義的動態設定檢查潛在錯誤。 [了解更多](../email/surface-personalization.md#check-configuration)

**程式碼型管道**

* 現在提供內容範本。 您可以從開發人員建立的內容範本開始，加速程式碼型體驗的撰寫作業。 使用內容範本可讓行銷人員僅修改某些值或欄位，而不是構成整個HTML或JSON內容裝載。 [了解更多](../content-management/content-templates.md)

**決策**

<!--* [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) users can now choose custom models to optimize on when setting up an AI model in Decisioning (formerly known as Experience Decisioning). This allows you, for example, to optimize on a custom "purchases" table rather than defined constraints such as clickthrough rate."-->

* 將決定策略新增到具有體驗決定的程式碼型行銷活動時，您現在除了選取策略之外，還可以手動選取單一決定專案。 此外，您現在可以選取多個遞補優惠。 這可保證會傳回一定數量的決定專案。 [了解更多](../experience-decisioning/create-decision.md)
