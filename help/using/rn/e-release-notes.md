---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 86bd616a9331c5225c78ccf52c5d26a063fa8654
workflow-type: tm+mt
source-wordcount: '2080'
ht-degree: 29%

---

# 搶鮮版發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能增強並修正錯誤。所有變更都會在每月底整合於[發行說明](release-notes.md)。


## 2026年1月發行前備註 {#jan-26-01-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。連結、畫面及更新的文件會在發行當日發佈於發行說明。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**：2026年1月26日

### 全新功能 {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>歷程中的動作活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 支援一個新的通用 <strong>動作活動</strong> ，讓你能配置單一動作與 <strong>多行動的入站動作群組</strong>，讓行程畫布內的動作配置更為精簡。 尤其是這項新功能允許：</p>
<ul>
<li>簡化歷程畫布中的原生動作設定。</li>
<li>容量用來建立多動作傳入動作群組。</li>
<li>能夠將最佳化新增至任何內建管道動作。</li>
<li>能夠將實驗與多語言選項新增至任何動作。</li>
</ul>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自訂動作監控</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過全新 <strong>監控儀表板</strong> 與豐富的旅程步驟事件資料，深入了解您的客製化行動端點的健康狀況與效能。 追蹤成功通話、錯誤、吞吐量、回應時間及佇列等待時間，快速了解異常發生的時間、地點及原因。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>勿打擾時間/不接收訊息的時間</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>安靜時段讓你可以為電子郵件、簡訊、推播和 WhatsApp 頻道定義 <strong>基於時間的排除</strong> 。 他們確保在特定時段內不會發送任何訊息，幫助你尊重客戶偏好與合規要求。 你可以透過 <strong>規則套</strong>用安靜時間，這些規則可以分配到戰役或旅程中的個別行動，以便精確掌控。</p>
<p>此功能先前僅以有限可用性形式推出，現在已適用於所有環境。 隨著這次正式上市釋出，該功能現在包含客戶可以排隊執行活動直到安靜時段結束，以及預覽已啟用的安靜時段規則。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>旅程中的直郵管道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>過去僅限於活動的直郵管道<strong>，</strong>現在已在旅程畫布<strong>上開放</strong>，讓你能將直郵融入你的行程中。直郵現在可用於批次及1：1旅程情境，並支援檔案擷取設定及基於時間的頻率設定。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web Push 通知頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 現在支援 <strong>網頁推播通知</strong>，將推播管道擴展至行動裝置之外。 你可以無縫地將通知傳送到行動與桌面瀏覽器，讓你能直接在客戶的裝置上觸及他們，無需應用程式。 此增強功能可讓您運用行動推播中現有的相同製作工作流程和目標定位功能，透過即時的個人化訊息與使用者互動。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>RCS 基本訊息</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>隨著新的 <strong>RCS Basic 附加</strong> 元件，您現在可以在 Journey Optimizer 中傳送基本的豐富通訊服務（RCS）訊息，並依照供應商與電信業者的支援，實現以下增強的訊息功能：</p>
<ul>
<li>有品牌、已驗證寄件者支援：使用具有品牌化元素（標誌、寄件者名稱等）的已驗證企業檔案，可以用來來傳送訊息。</li>
<li>訊息傳遞洞察力：接收包括訊息狀態更新（例如已傳送、已傳遞、已讀取）等詳細傳遞報告。</li>
<li>連結追蹤：請在 RCS 訊息中內嵌、追蹤網址，以便進行參與分析。</li>
<li>遞補簡訊：當設定檔的裝置暫不支援 RCS，或是暫時無法透過 RCS 連線時，系統會自動回覆簡訊。</li>
<li>基本訊息組成：發送基本的文字 RCS 訊息。</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>推送與簡訊通道中的決策支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>你現在可以在推送和簡訊行程及活動中新增 <strong>決策政策</strong> 。 決策原則是優惠方案的容器，可運用決策引擎以動態方式傳回最佳內容，傳送給每個對象成員。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>編排廣告活動中的直郵管道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>直郵管道現已可透過協調活動使用。 <strong>直郵活動</strong>促進了在你的協調活動中發送直郵，無論是一次性訊息還是重複訊息。它用來自動化產生 <strong>直郵服務所需擷取檔案</strong> 的流程。 您可以將管道活動與協調式行銷活動版面結合，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。</p>
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
<p>有了 Journey Optimizer，你現在可以透過著陸頁擷取 <strong>個人檔案屬性</strong> 。 根據特定資料集，根據你的需求建立、設計並管理 <strong>客製化表單</strong> 。 然後，您可以在登陸頁面中善用自訂表單，將選擇的設定檔屬性新增至為每個表單定義的資料集。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>忠誠度應用程式的新來源連接器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，Adobe <strong>Experience Platform 已提供 Talon.One、Capillary 及 Kobie 忠誠應用程式的新原始碼連接器</strong> 。 這些連接器可讓您將忠誠度資料順暢地串流至 Adobe Experience Platform，並在 Journey Optimizer 中利用這些資料。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>訊息匯出</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在可以 <strong>將已送出的</strong> 配送資料匯出到特定資料集，以便歸檔及合規。 此容量不僅適用於電子郵件，也可用於其他管道如簡訊。 訊息匯出資料集的資料保留期限現為 <strong>7 天</strong>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>用於擷取動作行銷活動的新 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>全新 Journey Optimizer API</strong> 現已推出，讓您能以程式化方式檢索與活動相關的資料，如詳細資料、版本與設定。</p>
<p>如需詳細資訊，請參閱<a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">詳細文件</a>。</p>
<p>推出日期：2025 年 11 月 24 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>新歷程警示</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在新增了三個 <strong>行程提醒</strong> ，幫助你監控與追蹤旅程生命週期事件及自訂行動表現：</p>
<ul>
<li><strong>歷程已發佈</strong>：當操作者歷程版面中發佈歷程時，會收到通知。</li>
<li><strong>歷程已完成</strong>：歷程完成時收到警示，並根據歷程類型有特定定義 (讀取客群或事件觸發)。</li>
<li><strong>自訂動作上限已觸發</strong>：在自訂動作端點上啟用上限時，會收到通知。</li>
</ul>
<p>這些警示可在組織層級訂閱或針對特定歷程訂閱。</p>
<p>如需詳細資訊，請參閱<a href="../reports/alerts.md#journey-alerts">詳細文件</a>。</p>
<p>推出日期：2025 年 11 月 5 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件設計工具中的主題</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>你現在可以快速套用 <strong>預先核准的主題</strong> ，確保所有電子郵件的品牌一致性，加快活動製作流程，並獨立產出高品質電子郵件，同時減少對設計團隊的依賴。</p>
<p>此功能先前以 Beta 版發行，現在可供部分組織使用 (有限可用性)。若想取得存取權，請聯絡您的 Adobe 代表。</p>
<img src="assets/do-not-localize/themes.gif">
<p>如需詳細資訊，請參閱<a href="../email/apply-email-themes.md">詳細文件</a>。</p>
<p>推出日期：2025 年 11 月 5 日</p>
</td>
</tr>
</tbody>
</table>

### 改善 {#jan-26-01-improv}

以下列舉部分發布內容附上的改良功能。

#### 人工智慧

* **AI 助理內容品質檢查** ——除了品牌一致性外，您現在還能評估整體 <strong>內容品質</strong> ，發現可讀性、連貫性與有效性等潛在問題，這不依賴品牌指引。 這些自動檢查有助於識別訊息不明確、語氣不一致或結構性缺口。
* **更新品牌新增色彩標籤** ——品牌指引有助於確保品牌在所有接觸點都能一致呈現。 新的 <strong>「色彩」部分</strong> 定義了品牌色彩系統的標準，說明色彩的選擇、組織與應用方式。 它確保統一使用主色、次色、點綴色及中性色，以支持統一、易於親近且易於辨識的品牌識別。

#### 行銷活動

* **使用設定檔時區** 排程活動 - 活動排程現在可以利用每個設定檔的 <strong>時區</strong> ，在預定的當地時間發送訊息。

  **注意**：此改進僅適用於部分組織（有限可用性）。

#### 管道

* **SMS Webhooks：第二** 階段 - 說明待提供。

* **WhatsApp 轉售優惠** - 說明待提供。

#### 電子郵件 Designer

* **電子郵件設計器** 中的原地修正—— <strong>當內容驗證中偵測到違規時，AI 驅動的自動內容建議</strong> 現在可在郵件設計器中提供。 若內容被標記為與品牌指引不符或品質標準不符，系統會主動產生修正後的替代方案，可即時審查並應用，提升合規性並加速生產。

#### 體驗決策

* **行程仲裁** ——你現在 <strong>可以使用公式和 AI 模型</strong> ，根據客戶檔案屬性和情境因素自動提升行程優先權分數，確保顧客輸入最相關的行程。

  **注意**：此改進僅適用於部分組織（有限可用性）。

* **EXD 沙盒工具文件 - 更新** - 說明待提供。

* **自助遷移工具 API——** 新增一組 <strong>遷移工具 API</strong> ，可將優惠管理實體遷移至 Experience Decisioning。 此工具能實現沙盒間無縫遷移，並具備相依性解析與回滾功能。

* **將片段附加到決策項目**——Journey Optimizer 現在提供將片段<strong>附加</strong>到決策項目的功能，這可透過決策政策在程式碼體驗活動中加以利用。

  **注意**：此改進先前為有限可用性版本，現已開放至所有環境（正式可用）。

#### 歷程

* **在旅程中利用失敗回應有效載荷自訂動作** ——你現在可以為自訂動作定義一個可選 <strong>的錯誤回應有效載荷</strong> 。 當呼叫失敗時，錯誤有效載荷會暴露在旅程上下文中，並可於逾時/錯誤分支中提供，以支援更豐富的備援邏輯與除錯。

* **將原生訊息與 Adobe Campaign 訊息動作** 合併——Journey Optimizer 現在允許你在同一旅程中將 Adobe Campaign v7/v8 訊息動作與原生管道動作合併。

* **旅程有效載荷大小驗證——** Journey Optimizer 現在提供 <strong>有效載荷大小驗證</strong> ，以協助確保最佳效能與系統穩定性。 在建立或發布行程時，若有效載荷尺寸接近或超過建議限制，您將獲得明確警告與錯誤，並提供可行的指引以優化行程配置。 這種主動驗證能幫助你及早發現潛在問題並維持旅程表現。

* **旅程中的** 多個入站動作 - 為了簡化行程協調，你現在可以在單一旅程中定義 <strong>多個入站行動</strong> 。 此功能先前在活動中提供，讓你能同時向不同地點傳送多個程式碼體驗、應用程式內訊息、內容卡或網頁行動，每個動作包含特定內容。

  **注意**：此改進先前為有限可用性版本，現已開放至所有環境（正式可用）。

#### 協調的行銷活動

* **選擇屬性並複製分配值** - 你現在可以直接從編排式廣告活動中的值分配檢視中選取或複製值。

* **受眾** 的資料使用標籤繼承—— <strong>Adobe Experience Platform 中套用的資料使用標籤</strong> ，現在在協調式活動中儲存受眾時會自動轉移，減少手動 DULE 標籤。

* **預定義重定向篩選器** - 為了支援更簡單的重定向，適合協調式活動使用情境，本版本引入了新的 <strong>重定向篩選器</strong>。 這些篩選器讓你能根據訊息互動直接鎖定受眾，例如已發送、僅開啟、已開啟或點擊，或開啟再點擊，並選擇你想要重新行銷的特定活動或過渡中活動。

* **預先定義的參數** 篩選器——你現在可以在編排的活動中建立 <strong>帶有參數</strong> 的篩選器，以實現可重複使用且可編輯的規則。

* **發送** 前確認訊息 - <strong>現在預設在發送協調活動前啟用確認步驟</strong> ，以減少誤送。

* **使用者產生的元資料支援** - <strong>執行元資料協助</strong> 功能現已在編排活動的個人化編輯器中提供，讓您能將情境資訊附加於任何原生行動，並儲存在資料集中以匯出至外部系統。

* **重新啟動按鈕** ——編排式戰役現在包含 <strong>重新啟動按鈕</strong> ，讓你在發布戰役前能快速重新啟動遊戲。

* **速率控制支援** - 協調式廣告活動現在支援 <strong>速率控制</strong> ，幫助您控制配送節奏並符合數量限制。

#### 權限

* **防止行程與活動** 自我審核——你現在可以要求創作者不能自行批准旅程或活動，改善 <strong>審核流程中職責的分離</strong> 。

## 即將推出 {#jan-26-01-coming-soon}

下列功能和增強功能已排定在未來幾天發行。**資訊可能會有變更**。這些更新在生產環境上線後，更新的連結、畫面和文件將會共用。

<table>
<thead>
<tr>
<th><strong>Journey Agent 內的內容產生</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent<strong> 由 Adobe Experience Platform Agent Orchestrator </strong>提供，並可在 Journey Optimizer 中使用，讓你能透過自然語言介面分析旅程。你現在也能直接在 Journey Agent 中產生和管理專屬通路內容，為電子郵件和推播等通路創建內容，套用與預覽範本，透過提示精煉語氣與風格，並在 Content Designer 中開啟內容以便上下文編輯。</p>
<p>上市日期：2026年2月2日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>內容決策活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>你現在可以透過旅程畫布中專門的內容決策活動，將個人化優惠<strong>納入</strong>旅程中，並在旅程活動中使用，包括條件和自訂動作。</p>
<p>上市日期：2026年2月2日</p>
</td>
</tr>
</tbody>
</table>
