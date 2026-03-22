---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0563bf02ecdd0229cc24e9d463af9c496faaa0a2
workflow-type: tm+mt
source-wordcount: '2984'
ht-degree: 26%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="最新資訊"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer] 遵循持續傳遞模式，允許 Adobe 持續傳遞新功能、增強功能和修正。此方法可讓您分階段推出可擴充的功能，以確保所有環境的效能和穩定性。

基於此模型，發行說明會在每月發行之間更新。如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](releases.md)。

[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2026年3月發行前注意事項 {#march-26-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。連結、畫面及更新的文件會在發行當日發佈於發行說明。

另請參閱[Adobe Experience Platform發行前說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**：2026 年 3 月 24-25 日

### 新功能 {#march-26-features}



<table>
<thead>
<tr>
<th><strong>協調行銷活動中的交易式訊息</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>協調的行銷活動現在支援<strong>交易式訊息</strong>，讓您能夠直接在行銷活動工作流程中觸發即時、事件導向的訊息，例如訂單確認、預訂通知和帳戶更新。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用API觸發協調的行銷活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以透過API觸發協調的行銷活動。 將目標行銷活動設定為「由訊號觸發」並發佈。 然後使用API呼叫來引發行銷活動。 API呼叫可包含引數，這些引數將在觸發的行銷活動中作為變數使用。</p>
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
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>URL引數加密</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>追蹤連結和登入頁面中的URL引數現在可以加密，為敏感引數資料提供額外的安全層。</p>
<ul>
<li>在專用的<strong>管理</strong>登入中登入及管理加密金鑰。</li>
<li>使用運算式中新的加密協助程式，針對您要在轉譯時保護的查詢引數，加密追蹤連結和登陸頁面URL中的敏感資料。</li>
</ul>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
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
<p>使用新的「最佳化」節點來鎖定特定對象，或執行A/B測試，以決定符合以業務為中心的KPI的最佳途徑。
此工具可讓您測試並變更內容，以及自訂通訊、排序和時機，以便最有效地觸及客戶。
</p>
<p>先前以「有限可用性」發行，現在此功能可用於所有環境（一般可用性）。 <a href="../building-journeys/optimize.md">了解更多</a></p>
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
<p>歷程中的新活動，資料集查詢，可讓您在執行階段動態擷取Adobe Experience Platform記錄資料集中的資料。 透過運用此功能，您可以存取輪廓或事件裝載內容中可能未駐留的資料，確保客戶互動相關且及時。先前以「有限可用性」發行，現在此功能可用於所有環境（一般可用性）。 如需詳細資訊，請參閱<a href="../building-journeys/dataset-lookup.md">詳細說明文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>原生管道動作活動已棄用</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在2026年2月<strong>動作活動</strong>正式發行後，歷程畫布中的舊版原生頻道活動（電子郵件、推播、簡訊、應用程式內、網頁、程式碼型體驗和內容卡）現已棄用。</p>
<p>您現在使用單一<strong>動作活動</strong>來設定所有通道動作，取代個別通道特定節點的需求。</p>
使用舊版管道活動的現有歷程將繼續正常運作，不會進行任何變更或需要進行移轉。
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-action.md">詳細說明文件</a>。</p>
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
<p>先前以「有限可用性」發行，現在此功能可用於所有環境（一般可用性）。 在此「一般可用性」版本中，現在支援映象頁面。</p>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/create-decision-policy.md">詳細說明文件</a>。</p>
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
<p>先前以「有限可用性」發行，現在此功能可用於所有環境（一般可用性）。 <a href="../content-management/image-to-html.md">了解更多</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>訊息收件匣</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer現在提供新的<strong>訊息收件匣</strong>，以集中檢視收到的應用程式內訊息、推播訊息和簡訊。 收件者可以在一個位置存取及互動所有訊息，實現更豐富的參與及重新參與情境。</p>
<p>推出日期： 2026年3月31日</p>
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
<p>如需詳細資訊，請參閱<a href="../content-management/email-template-expert-mode.md">詳細說明文件</a>。</p>
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
<p>可緊密整合標準與自訂Firefly模型，以及經核准的協力廠商影像模型，以便在產生影像時提供更大的彈性、控制力及品牌一致性。</p>
<p>選擇符合您需求的正確模式：</p>
<ul><li> <strong>Adobe模型</strong> （由Firefly Image Model 4提供技術支援）可立即產生影像，無需額外設定</li><li> <strong>合作夥伴機型</strong> （由Gemini 2.5 Flash提供），提供專門的功能</li><li><strong>自訂模型</strong> （在您自己的資產上訓練的品牌特定模型），用於品牌上產生，完全符合您的品牌識別、風格和視覺准則。</li></ul>
<p>如需詳細資訊，請參閱<a href="../content-management/generative-models.md">詳細說明文件</a>。</p>
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
<p>透過Adobe Journey Optimizer中的iOS即時活動，直接將即時體驗帶入客戶的「鎖定Screens」和「動態島嶼」 。 提供即時更新，從訂單追蹤和航班狀態到事件倒計時、即時分數和傳送進度，而不需要使用者開啟您的應用程式。 讓您的對象保持知情並在正確的時間參與，就在他們所在的位置。</p>
<p>此功能先前以Beta版發佈，現已開放所有環境使用（全面發佈）。</p>
<p>如需詳細資訊，請參閱<a href="../mobile-live/get-started-mobile-live.md">詳細說明文件</a>。</p>
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
<p>如需詳細資訊，請參閱<a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html">詳細說明文件</a>。</p>
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
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/ranking/ai-model-observability.md">詳細說明文件</a>。</p>
<p>推出日期： 2026年3月9日</p>
</td>
</tr>
</tbody>
</table>


### 改善 {#march-26-improv}

以下列舉部分發布內容附上的改良功能。


#### 報告

* **排除電子郵件和簡訊報告的機器人點按** — 電子郵件和簡訊報告現在會自動從點按量度中篩選出機器人點按，提供更精確的參與資料，並防止自動流量誇大您的效能數字。

* **傳送時間最佳化：更新的控制項位置和新的提升度報告** — 傳送時間最佳化(STO)控制項已重新放置到[動作]設定功能表。 此外，歷程報表現在提供新的提升度報表，以測量STO對行銷活動效能量度的影響。

#### 電子郵件設計工具

* **電子郵件Designer顯示在Unified Shell中** — 電子郵件Designer現在顯示在Unified Shell體驗中，提供與其他Adobe應用程式一致的一致導覽和標題體驗。

* **片段中的文字模式支援** — 若要支援文字型電子郵件工作流程，您現在可以建立和管理視覺化片段的文字版本，以便在包含該片段的純文字版電子郵件中最佳使用。

  **警告：**&#x200B;使用目前版本之前建立的片段時，片段文字版本可能會錯誤轉譯，包括在Designer電子郵件和傳送給收件者的最終電子郵件中。 為了對較舊的片段產生最佳結果，請編輯、儲存並重新發佈每個片段。

#### 決策

* **Edge Decisioning中的運算式片段參考變更摘要** — 此增強功能可讓片段參考的變更自動反映在參考片段的所有專案中，而不需要手動重新整理任何專案（重新發佈行銷活動或決定原則）。

* **決策專案中的選用片段** — 在決策專案中使用片段時，您現在可以將片段設為選用，如此一來，如果Edge上暫時無法使用該片段，則會略過該片段，而歷程或行銷活動會繼續呈現，而非失敗。

#### 設定

* **歷程與行銷活動的資料夾** — 您現在可以將歷程與行銷活動整理到資料夾中，讓團隊處理大量內容時可以進行結構化導覽及更輕鬆的管理。 此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。

* **AJO次要收件者意見反應事件資料集重新命名** - `AJO Email BCC Feedback Event`資料集已重新命名為`AJO Secondary Recipient Feedback Event`資料集。 其影響會依您的情況而有所不同：

   * **現有使用者**：只更新顯示名稱。 基礎資料表名稱保持不變。
   * **新使用者和沙箱**：顯示名稱和表格名稱都會反映新名稱。
   * **具有新沙箱的現有使用者**：顯示名稱和表格名稱都會更新為新名稱。

  推出日期： 2026年3月2日

#### 協調的行銷活動

* **協調行銷活動中的全域變數** — 協調行銷活動現在支援全域變數，這些變數只需定義一次，便可在工作流程內的所有活動中重複使用，可簡化設定，並確保動態值、運算式和內容個人化的一致性。

* **協調行銷活動中的目標維度簡化** — 您現在可以輕鬆選取或自動推斷協調行銷活動中的正確目標定位和次要維度，以實現準確、有效的受眾啟用。

#### 歷程

* **在歷程中傳送傳出訊息的波次** — 您現在可以排程來自Journey Optimizer歷程的訊息，以控管批次方式傳送一段期間。 [了解更多](../building-journeys/send-using-waves.md)

  此功能先前以「有限可用性」發佈，以供歷程使用，現在則可用於所有環境（一般可用性）。

  推出日期： 2026年3月16日

* **歷程技術詳細資料中的暫停和繼續詳細資訊** — 歷程&#x200B;**技術詳細資訊**&#x200B;現在包含額外的暫停和繼續資訊：上次暫停和繼續的日期和時間、執行每個動作之使用者的顯示名稱和內部識別碼，以及整套暫停的歷程設定，例如暫停行為、最長暫停期間和自動繼續狀態。 [了解更多](../building-journeys/journey-properties.md)

  推出日期： 2026年3月2日


## 2026年2月發行說明 {#feb-26-01-rn}

[新功能](#feb-26-01-features)和[改進](#feb-26-01-improv)區段已涵蓋可用的功能。<!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in February.-->

<!--**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

<!--**Release date**: February 17-18, 2026-->

### 新功能 {#feb-26-01-features}


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
<p>在<strong>行銷活動</strong>中，此功能適用於所有環境（一般可用性）。 如需詳細資訊，請參閱<a href="../campaigns/send-using-waves.md">詳細說明文件</a>。</p>

<p>在<strong>歷程</strong>中，此功能僅適用於一組組織（可用性限制） — 若要取得存取權，請聯絡您的Adobe代表。 如需詳細資訊，請參閱<a href="../building-journeys/send-using-waves.md">詳細說明文件</a>。</p>
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
<p>如需詳細資訊，請參閱<a href="../push/push-configuration-web.md">詳細說明文件</a>。</p>
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


* **將片段附加至決策項目** - Journey Optimizer 現在提供將片段附加至決策項目的功能，而決策項目可透過決策原則用於程式碼型體驗行銷活動。[閱讀全文](../experience-decisioning/fragments-decision-policies.md)

  此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。

  推出日期：2026年2月12日。

#### 個人化

* **執行中繼資料協助程式** - `executionMetadata`協助程式函式現在可供所有Journey Optimizer客戶使用。 使用此外掛程式來動態附加內容資訊至任何原生動作，並在資料集中擷取該資訊，以匯出至外部系統。 [閱讀全文](../personalization/functions/helpers.md#execution-metadata)

  此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。

  推出日期：2026年2月20日。

#### 簡訊

* **SMS Webhook** — 所有SMS提供者現在都支援Webhook。 您可以根據每個Webhook的預期用途進行設定：傳入Webhook以擷取傳入訊息，反饋Webhook以接收傳遞回條、狀態更新和其他訊息相關事件。 [閱讀全文](../sms/sms-webhook.md)

  推出日期：2026年2月2日。

<!--## Coming soon {#coming-soon}

The features and improvements below are planned for release later in February. Release dates and scope may change without prior notice.

### Improvements {#coming-soon-improv}

* **Decisioning preview in Code-based Experience channel** - You can now preview decision items when configuring Decisioning with the Code-based Experience channel. Preview is available directly in the authoring interface before going live.

  Availability date: February 18, 2026
-->

