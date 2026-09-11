---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
hide: true
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
source-git-commit: 445bfb155d5e14ebbc84ef70036cde64662dc938
workflow-type: tm+mt
source-wordcount: 2506
ht-degree: 14%

---


# 搶鮮版發行說明 {#e-release-notes}

Adobe Journey Optimizer 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

## 2026年9月發行前注意事項 {#sep-26-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。 連結、畫面和更新的文件會在變更上線生產時發佈。 雖然大多數變更會在發行日期提供，但有些可能會稍後推出。如需詳細資訊，請參閱每個項目所列的推出日期。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**： 2026年9月22至23日

### 內容管理 {#sep-26-content-management}

以下功能即將推出此版本的內容管理。

<table>
<thead>
<tr>
<th><strong>CX Co-worker中的訊息複製與電子郵件設計外掛程式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Co-worker現在提供兩種新的外掛程式，可簡化您從策略到部署的<strong>訊息和電子郵件工作流程</strong>：</p>
<p><strong>訊息複製外掛程式</strong>：</p>
<ul>
<li>擷取行銷活動簡報，並定義訊息地圖、敘述弧和頻道角色。</li>
<li>建立跨管道、接觸點、地區、對象和變體量身打造的多維度內容矩陣。</li>
<li>產生全新副本，並運用Adobe Firefly來產生、裁切及調整行銷活動視覺效果。</li>
<li>允許就地內容評估，並直接將核准的資產同步回Journey Optimizer、Adobe Campaign V8和Marketo。</li>
</ul>
<p><strong>電子郵件設計外掛程式</strong>：</p>
<ul>
<li>將行銷目標、參考熒幕擷取畫面或Figma設計連結轉換為自訂版面配置計畫和生產就緒電子郵件HTML。</li>
<li>管理可重複使用的品牌資產、設計權杖和結構化電子郵件範本。</li>
<li>稽核針對企業法規遵循、視覺設計品質和WCAG 2.1 AA協助工具標準而組裝的電子郵件程式碼。</li>
<li>將核准的HTML直接匯出至Adobe Journey Optimizer和Adobe Campaign。</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15642" target="_blank">DOCAC-15642</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 忠誠度 {#sep-26-loyalty}

此版本中的「忠誠度」提供下列功能和改善功能。

<table>
<thead>
<tr>
<th><strong>挑戰機會</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>忠誠度績效選單現在包含<strong>機會標籤</strong>，其中會顯示AI偵測到的趨勢和差距，例如層級進展摩擦或挑戰任務流失，每個都具有預計的影響，以及按一下「使用AI建立」動作以產生可解決它的挑戰。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15563" target="_blank">DOCAC-15563</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15661" target="_blank">DOCAC-15661</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **CX同事忠誠度建議技能** — 行銷人員現在可以在CX同事的對話介面中直接要求&#x200B;**挑戰機會**，根據真正的忠誠度計畫趨勢獲得實際的挑戰想法，並在不離開聊天室的情況下將其轉換為即時挑戰。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15565" target="_blank">DOCAC-15565</a> <!-- Documentation link: TBD -->

### 入門 {#sep-26-onboarding}

以下功能即將在此版本中上線。

<table>
<thead>
<tr>
<th><strong>入門電子郵件和歷程的引導功能（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過引導式功能，您可以更輕鬆地從其他行銷平台轉換至 Adobe Journey Optimizer，將現有電子郵件內容和歷程移至 Journey Optimizer。 <strong>專屬工作區</strong>可讓您重複使用現有工作，而非從頭重建。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15330" target="_blank">DOCAC-15330</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 歷程 {#sep-26-journeys}

下列功能和改進功能將新增到此版本的歷程。

<table>
<thead>
<tr>
<th><strong>CX Co-worker中的歷程模擬（MCP與聊天）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Co-worker中的<strong>歷程模擬技能</strong>可自動進行端對端歷程驗證，讓您輕鬆解讀結果。 請注意，此功能目前僅支援快速模擬流程，不會完全取代Journey Optimizer手動模擬體驗。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15374" target="_blank">DOCAC-15374</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* 歷程模擬中的&#x200B;**決策路徑實驗** - **路徑實驗** （決策中最佳化活動的一部分）現在支援歷程模擬。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15641" target="_blank">DOCAC-15641</a> <!-- Documentation link: TBD -->

* **歷程模擬中的補充ID支援** - **歷程模擬現在支援Supplemental ID**，可讓您針對讀取對象和事件觸發的歷程測試複雜的使用者案例。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15448" target="_blank">DOCAC-15448</a> <!-- Documentation link: TBD -->

<table>
<thead>
<tr>
<th><strong>從CX同事邊欄建立歷程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>使用AI建立歷程</strong>現在可直接從CX Co-worker右側邊欄取得，將先前的AI Assistant體驗取代為品牌重塑的整合式進入點，以產生歷程。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14898" target="_blank">DOCAC-14898</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **已改良批次對象評估等待邏輯** — 在&#x200B;**讀取對象活動**&#x200B;中，歷程中的「批次對象評估後觸發」選項現在會等待任何正在進行中的批次分段完成，確保歷程使用執行中的資料，而不是退回至較舊的快照。 如果沒有正在進行的批次細分，歷程會使用最新可用的對象資料立即引發。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15465" target="_blank">DOCAC-15465</a> <!-- Documentation link: TBD -->

* **與CX Coworker比較歷程版本** — 現在，檢閱兩個歷程版本之間的變更內容時，需要在Journey Optimizer節點內逐個節點手動比較 — 沒有結構化的差異，這會導致變更檢閱、稽核和預先發佈檢查緩慢且容易出錯，尤其是當歷程越來越複雜時。 此功能可讓客戶或AI代理程式透過CX Coworker Chat比較歷程的任意兩個版本，在不開啟Journey Optimizer的情況下，恢復完整保真&#x200B;**結構化diff** — 新增/移除/修改/移動具有欄位層級詳細資訊、變更連線、歷程層級屬性變更和統計計數的節點。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15297" target="_blank">DOCAC-15297</a> <!-- Documentation link: TBD -->

* **歷程畫布中的內容預覽** — 今天檢閱管道內容需要一次開啟一個節點，個別開啟每個節點 — 在具有多個管道節點的歷程中緩慢且容易出錯，尤其是當個人化需要檢查每個節點的多個處理或變體時。 **內容預覽**&#x200B;透過直接在畫布中為每個管道節點呈現內容縮圖，以全熒幕模式檢查並在處理與變體之間切換，來移除該摩擦。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15456" target="_blank">DOCAC-15456</a> <!-- Documentation link: TBD -->

### 管道 {#sep-26-channels}

此版本中的管道即將推出下列功能和改善。

<table>
<thead>
<tr>
<th><strong>Android Live Updates的已上線活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在將<strong>即時活動支援擴充至Android</strong>，以擴充其即時行動個人化功能。 您可以直接將即時進度更新傳送給使用者，例如訂單追蹤、航班狀態、即時活動更新和即時運動分數。</p>
<p>除了支援iOS Live活動以外，Journey Optimizer現在還管理其平台設定中Android Live更新的暫時推送代號。 它使用API觸發的行銷活動和Headless API來支援廣播和交易式更新流程。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15510" target="_blank">DOCAC-15510</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自訂傳出頻道（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>自訂傳出頻道</strong>可讓管理員透過無程式碼的Channel Builder，將任何傳出以HTTP為基礎的訊息頻道（例如WeChat、Kakao Talk、Messenger或專屬提供者）直接帶入Journey Optimizer。 設定之後，便可在各種行銷活動、歷程和精心安排的行銷活動中使用自訂管道，並提供與原生管道相同的完整功能集：使用運算式編輯器進行個人化、內容實驗、預覽和校樣、現成可用的報告，以及同意與治理強制執行。</p>
<p>在此版本中，自訂傳出頻道也獲得幾個新功能：</p>
<ul>
<li>透過Journey Optimizer編輯器在自訂管道裝載中使用Personalization Decisioning，與程式碼型體驗中的方式相同。</li>
<li>套用商業規則至自訂管道，就像您在原生管道上所做的那樣。</li>
<li>在管道清單中選取API觸發行銷活動的自訂管道，這在之前是不可能的。</li>
<li>為自訂管道定義報表webhook並將其附加至管道設定，以便您可以透過互動事件豐富Journey Optimizer報表。</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14037" target="_blank">DOCAC-14037</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>覆寫電子郵件通道組態設定</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>建立您的歷程和行銷活動時，您現在可以直接在歷程或行銷活動動作層級覆寫從所選管道設定衍生的電子郵件引數。</p>
<p>這可讓您個人化電子郵件標題欄位（<strong>來自名稱</strong>、<strong>來自電子郵件前置詞</strong>、<strong>回覆名稱</strong>和<strong>回覆電子郵件</strong>）、執行位址和清單取消訂閱值，使用設定檔屬性或內容資料以取得更精確的控制權。 特別是，這允許寄件者詳細資料反映每個收件者的相關顧問、位置或分支，而不是透過單一公司地址路由傳送所有傳送。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14718" target="_blank">DOCAC-14718</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **自訂SMS BYOP驗證彈性** — 您現在可以在連線您的SMS提供者的OAuth設定時，設定&#x200B;**自訂驗證標頭**，包括權杖在傳出訊息中的放置位置以及權杖請求本身的格式。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15638" target="_blank">DOCAC-15638</a> <!-- Documentation link: TBD -->

### 協調的行銷活動 {#sep-26-oc}

下列功能和改進功能將新增到此版本的協調行銷活動。

<table>
<thead>
<tr>
<th><strong>或是加入協調行銷活動的活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在協調的行銷活動中，<strong>加入活動</strong>現在支援AND和OR加入條件。 使用OR邏輯時，完成任一上游分支（而非全部）的設定檔會沿著單一共用下游路徑繼續。 如此一來，就可以直接在畫布上建立「如果A、B或C，則執行此動作」的模式，而不需跨不同分支重複下游步驟。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15020" target="_blank">DOCAC-15020</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>協調行銷活動的警報</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>協調的行銷活動現在透過在歷程及行銷活動中使用的相同警報架構，支援<strong>自動警報</strong>。 當行銷活動執行失敗、逾時或需要確認時會觸發警報，每個警報包括所發生的情況、時間、地點以及監控檢視的直接連結，並按嚴重程度分類，以便團隊無需手動UI檢查即可優先排序。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14886" target="_blank">DOCAC-14886</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* 協調行銷活動的&#x200B;**LINE頻道** - LINE現在可做為協調行銷活動的原生傳出頻道，連同電子郵件、簡訊和推播。 您可以直接從行銷活動畫布建立及傳送LINE訊息，包括文字、貼圖、影像、影片、位置資料和Flex訊息，在日本和APAC等以LINE為主的市場支援促銷、交易和持續參與使用案例。 此功能先前以「有限可用性」發行，現已正式推出。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15102" target="_blank">DOCAC-15102</a> <!-- Documentation link: TBD -->

* **新的協調行銷活動監控API** — 新的&#x200B;**API規格**&#x200B;現在可用於協調行銷活動，可讓您以程式設計方式建立、管理和觸發協調行銷活動，與外部系統和自動化管道進行更深入的整合。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14308" target="_blank">DOCAC-14308</a> <!-- Documentation link: TBD -->

* **直接加入UX改良功能** — 從相關集合新增屬性時，您現在可以在三種加入模式（新預設值，警告您卡式產品對效能的潛在影響，加上現有的彙總和進階模式）之間選擇，讓您更容易在建置查詢之前瞭解查詢的取捨。

### 行銷活動 {#sep-26-campaigns}

此版本中的行銷活動推出下列功能和改善。

<table>
<thead>
<tr>
<th><strong>Action Campaigns (Beta)中的傳入體驗模擬</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以於上線前，在動作行銷活動中模擬傳入管道動作。 使用模擬模式，透過模擬使用者測試您的設定並預覽呈現的體驗 (包括產生的 URL 和 QR 碼)，讓您可以端到端驗證規則、決策機制與內容呈現。</p>
<p>此功能目前為 Private Beta 版本，僅供特定組織使用。 請聯絡您的 Adobe 代表以取得更多資訊。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15166" target="_blank">DOCAC-15166</a></p>
</td>
</tr>
</tbody>
</table>

* **行銷活動的資料夾** — 您現在可以將行銷活動整理到&#x200B;**資料夾**&#x200B;中，以改善介面中的導覽和管理。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15098" target="_blank">DOCAC-15098</a> <!-- Documentation link: TBD -->

### 決策 {#sep-26-decisioning}

下列功能和改進功能將新增到此版本的決策。

<table>
<thead>
<tr>
<th><strong>Web Channel中的決策支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>決策功能現在可用於網頁管道。 您可以直接在網頁視覺化編輯器中使用決策原則，將最相關的產品建議傳送給每位訪客。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11548" target="_blank">DOCAC-11548</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **從CX Co-worker產生決策規則** — 先前透過右邊欄提供的&#x200B;**AI輔助決策規則產生**&#x200B;體驗現在可透過CX Co-worker存取，以取代右邊欄，作為使用AI建立規則的方式。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15290" target="_blank">DOCAC-15290</a> <!-- Documentation link: TBD -->

### 直接郵件 {#sep-26-direct-mail}

此版本中的Direct Mail即將提供下列功能和改善。

* **自動分割大型檔案** — 現在，直接郵件檔案在大約超過20 GB時，可以自動分割成多個部分，或在檔案路由設定中選擇目標檔案大小時手動分割。 選用的JSON資訊清單檔案說明了所有產生的部分。

* **提高對象上限** — 直接郵件管道對象上限已從300萬個設定檔提升至1億個，讓您可將目標鎖定在較大對象上，而不會出現檔案建立錯誤。

### 電子郵件設計工具 {#sep-26-email-designer}

此版本中的電子郵件Designer即將提供下列功能和改善。

<table>
<thead>
<tr>
<th><strong>電子郵件主題變體的獨立深色模式樣式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>電子郵件主題現在支援深色模式的獨立樣式。 在佈景主題產生器中，您可以為特定變體開啟深色模式，以產生專用深色模式樣式表，讓您從淺色模式樣式中單獨編輯該樣式表 — 在一種模式中所做的變更不再覆寫另一種模式。 在電子郵件和範本編輯器中，案頭和行動檢視選項旁新的預覽切換可讓您以深色模式預覽內容。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15663" target="_blank">DOCAC-15663</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>直接在電子郵件Designer中從PSD檔案匯入Dynamic Media範本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>電子郵件Designer的Dynamic Media元件現在可讓您在瀏覽現有Dynamic Media範本之外，直接匯入Photoshop (PSD)檔案為新範本。 將PSD檔案拖放至元件中，Adobe Journey Optimizer會自動將其轉換為儲存在Dynamic Media中的動態媒體範本，不需要手動轉換或穿過Adobe Experience Manager來迴轉換。 匯入後，您可使用內建的Dynamic Media編輯器編輯範本，這與電子郵件Designer中的Adobe Express內容使用相同的體驗。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15664" target="_blank">DOCAC-15664</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件Designer中的新表格元件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>電子郵件Designer現在包含內建<strong>表格元件</strong>，可讓您直接在電子郵件中建構列和欄的內容。 將元件拖放至畫布上、自訂列和欄數，並獨立設定每個儲存格的樣式，以建立清晰、有組織的版面配置，而不依賴自訂HTML。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15093" target="_blank">DOCAC-15093</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **電子郵件主題中自訂字型的遞補字型** — 您現在可以為任何透過電子郵件主題套用的自訂(Web)字型定義遞補字型。 如果訂閱者的電子郵件使用者端不支援自訂字型，Adobe Journey Optimizer會自動顯示指定的遞補字型，而不會將選項保留給電子郵件使用者端的預設值。 這可讓電子郵件印刷樣式更貼近您的品牌方針，並減少電子郵件使用者端間的字型轉譯不一致問題。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15662" target="_blank">DOCAC-15662</a> <!-- Documentation link: TBD -->

### 可用性改進功能 {#sep-26-usability}

* **內容模擬體驗中的可用性改善** — 新的內容模擬體驗現在可讓您命名並組織變體以便輕鬆比較、直接從每個卡片複製或刪除變體詳細資料、依需求檢視完整屬性路徑和每個卡片管道設定，以及從更顯眼的上傳按鈕上傳您自己的CSV、JSON或JSONL設定檔。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15570" target="_blank">DOCAC-15570</a>


