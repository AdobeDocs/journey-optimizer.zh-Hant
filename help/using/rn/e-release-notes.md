---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 61447b6400b65e29a9187790e74be47b09764c4a
workflow-type: tm+mt
source-wordcount: '1967'
ht-degree: 100%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

**至發行日期之前，下方早期發行說明如有變更，恕不另行通知**。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024 年 10 月搶先發行說明 {#e-2024}

**發行日期**：2024 年 10 月 29-30 日

### 全新功能 {#e-features}

此發行版本提供下列詳細介紹的新功能。

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
<!--p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>歷程與行銷活動 (一般可用性) 通過核准</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>待政策通過核准，您就可以立即在 Journey Optimizer 中設定核准程序，允許行銷團隊使用，以確保行銷活動和歷程在正式上線之前，會先由合適的利害關係人負責審核，並完成簽核。</p>
<p>之前可用於一組組織 (LA)，目前所有使用者 (GA) 都可以使用核准原則。</p>
<p>如需詳細資訊，請參閱<a href="../test-approve/gs-approval.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>電子郵件組態個人化 (一般可用性)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您在建立電子郵件管道設定時，可以馬上定義動態子網域和個人化標題參數，就能提高電子郵件設定彈性，更能夠掌握得當。</p><p>在行銷活動或歷程中使用個人化設定，讓您可以預覽電子郵件內容，以便使用定義好的動態設定，檢查潛在錯誤。</p>
<p>之前可用於一組組織 (LA)，目前所有使用者 (GA) 都可以使用電子郵件組態個人化。</p>
<p>如需詳細資訊，請參閱<a href="../email/surface-personalization.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>使用範例輸入資料 (測試版) 來測試內容</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 目前讓您可以預覽電子郵件內容，還能使用從 CSV 檔案上傳，或是手動新增的範例輸入資料，傳送校樣，以便測試電子郵件內容的不同變體。 系統會自動偵測您在內容中使用到的所有設定檔屬性，以便進行個人化，以上屬性可應用到測試上，即可建立多個變體。</p>
<p>此功能目前有提供測試版。</p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>衝突與優先順序管理 (可用性限制)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在 Journey Optimizer 中，管理行銷活動和歷程的數量和時機，正是避免客戶因互動次數過於頻繁而感到不知所措的重要關鍵。 Journey Optimizer 目前有提供多種衝突管理和排定優先順序工具。</p><p><ul><li><b>歷程頻率上限</b>：您目前可以建立規則集，以便套用至歷程中，讓您可以為設定檔限制每日、每週或每月的歷程次數，還能控制同時執行的並行歷程次數。</li>
<li><b>優先順序分數</b>：您目前可以將優先順序分數指派給行銷活動，或是歷程，分數由 0 到100 分起跳。 分數越高則表示優先順序越高。 當有兩種行銷活動同時使用到相同的管道設定時，Journey Optimizer 就會選取優先順序分數最高的行銷活動。如果行銷活動的分數一樣，就會選擇最近才修改過的行銷活動。</li>
<li><b>檢視潛在衝突</b>：歷程和行銷活動中的最新「檢視潛在衝突」按鈕目前可以讓您識別與其他歷程，或是行銷活動之間的重疊程度，例如開始日期、目標對象，或是選取的管道設定。</li>
<li><b>歷程仲裁</b>：這項新功能讓您可以找出最重要的歷程優先順序，再提供給客戶使用。 您可以建立規則，以便在客戶符合即將進入的優先順序較高的歷程資格時，阻止對方進入優先順序較低的歷程。</li></ul></p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>指定客戶群組可在限量中，使用衝突和優先順序管理功能。 請注意，未來將會向更多使用者逐步推出以上功能。 如果您有興趣加入上述功能的等候名單，請洽詢客戶團隊。</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>網頁設計工具的非視覺化編輯模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>作為 Journey Optimizer 網頁設計工具的替代方案，您目前可以使用非視覺化編輯器，將修改版本新增至自己的網站。 這項工具讓您可以手動輸入變更，不用在視覺編輯器中開啟頁面。
如果您無法安裝瀏覽器擴充功能，例如 Adobe Experience Cloud Visual Helper，這種非視覺化編輯模式可以算是相當實用，只要在網頁設計工具中載入頁面，就會需要用到這種擴充功能。</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程中的內容實驗 (一般可用性)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 現在支援歷程的實驗，行銷活動已提供此功能。實驗是在線上測試的情境下進行的隨機試驗，意即某些隨機選取的使用者會接觸到訊息的指定變化，而另一組隨機選取的使用者則會接觸到一些其他處理方式。 接觸到後，您就可以測量感興趣的結果量度，例如電子郵件開啟、訂閱或購買數。</p>
<p>之前開放給一整組組織 (LA) 使用，目前所有使用者 (GA) 都可以使用歷程中的實驗。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Decisioning (一般可用性)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning 之前開放給一整組組織 (LA) 使用，又稱為體驗決策，目前開放給所有使用者 (GA) 使用。Decisioning 會透過提供集中行銷優惠目錄，又稱為「決策項目」，還有複雜的決策引擎，設法簡化個人化。 此引擎會運用規則與排名標準來選取，並呈現出最相關的決定項目給每個人。這些決策項目會透過新的程式碼型體驗頻道，無縫整合入廣泛的傳入介面。</p>

<p>目前，Decisioning 不適用於已購買 Adobe Health Shield 和 Privacy and Security Shield 附加產品的組織。</p>

<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>規則集 (可用性限制)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您可以馬上建立精細的頻率上限規則，再透過規則集，將這些規則套用至訊息或是歷程上。 這項新功能讓您可以透過設定跨頻道規則，控制對象接收訊息的頻率，以上規則會自動從訊息和動作中排除過度請求的設定檔。</p><p>這項新功能讓您可以限制每日、每週或每月的歷程次數，還能控制同時執行的並行歷程次數。</p>
<p>特定客戶群組可在限量中使用規則集。 請注意，未來將會向更多使用者逐步推出以上功能。 如果您有興趣加入以上功能的等候名單，請洽詢客戶團隊。</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>歷程與行銷活動的多語言訊息 (一般可用性)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在單一行銷活動或歷程中，輕鬆建立多種語言的內容。透過此功能，您可以在編輯行銷活動或歷程時切換語言、簡化整個編輯流程，並提高有效管理多種語言內容的能力。</p>
<p>只要使用一般可用性，目前在所有管道上都可使用多語言內容。 </p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>將 Movable Ink 整合入 Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您目前可以將 Movable Ink Da Vinci 整合入 Adobe Journey Optimizer。 透過這項新的整合，您可以做到以下幾點： </p>
<p><ul><li>善用 Movable Ink Da Vinci 產品中的強大功能，將批次行銷活動的電子郵件變化版本加以組合並進行個人化</li>
<li>使用 Da Vinci 進行製作，利用 AJO 進行最佳化和服務傳遞，為 Journey Optimizer 的客戶，加速從業人員的工作流程</li>
<li>使用 Adobe 資料，將 Da Vinci 模型最佳化。</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>已更新報告體驗 (一般可用性)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>自 2024 年 10 月 16 日起開放使用</p>
<p>Journey Optimizer 報告功能目前開放給一般人使用 (GA)，改良後的版本擁有互通性，能使用 Customer Journey Analytics 功能，可將兩邊平台之間的報告標準化，改善資料一致性與可靠性。Journey Optimizer 與 Customer Journey Analytics 之間緊密整合，讓您可以更清楚地檢視效能量度，讓使用者能做出更睿智的決策。</p>
<p>推廣一般可用性之後，會引進四種新功能：可以建立簡易量度，建立並發佈對象，使用 Insight Builder 臨時提出問題，將排程報表流程自動化，寫封電子郵件寄給主要收件者。</p>
<p>如需詳細資訊，請參閱<a href="../reports/report-cja-manage.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>重要提醒：目前的報告體驗將於推出 2025 年 1 月份版本後，正式終止服務。過了上述日期，新的報告體驗就會成為標準版。建議您先自己熟悉一下新的功能，以確保能順利轉換服務。<a href="../reports/report-gs-cja.md">了解如何開始使用 Journey Optimizer 的新報告介面</a></p>
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
<p>自 2024 年 10 月 1 日起開放使用</p>
<p>透過程式碼型體驗管道，Adobe Journey Optimizer 可讓您針對任何傳入屬性進行進階個人化及測試，跨不同接觸點 (例如網頁應用程式、行動應用程式、桌面應用程式、視訊主控台、電視連結的裝置、智慧型電視、資訊站、ATM、IoT 裝置等) 達成量身打造的無縫傳遞體驗。程式碼型體驗管道現可在歷程版面中使用。</p>
<p>如需詳細資訊，請參閱<a href="../code-based/create-code-based.md">詳細文件</a>。</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程中的網頁體驗</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>自 2024 年 10 月 1 日起開放使用</p>
<p>有了網頁管道，Adobe Journey Optimizer 可讓您將透過傳入網頁歷程向客戶提供的網站體驗個人化。網頁管道現可在歷程版面中使用。</p>
<p>如需詳細資訊，請參閱<a href="../web/create-web.md">詳細文件</a>。</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

### 改進項目 {#e-improvements}

此發行版本隨附下列改進項目。

**簡訊頻道**

>[!AVAILABILITY]
>
>下列增強功能只適用於 Sinch 和 Infobip 提供者。

已引進簡訊增強功能，改善傳送訊息功能：

* 您可以定義並管理簡訊行銷活動，還有歷程的唯一關鍵字，啟用更個人化、有效率的通訊服務。

* 當無法辨識關鍵字時，您可以先建立並傳遞預設簡訊。

* 目前您可以編輯或刪除簡訊 API 管道設定。

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**資料集**

* **存留時間護欄**：自 2024 年 11 月 1 日起，將在新沙箱和新組織中，向 Journey Optimizer 系統產生的資料集，開放使用存留時間 (TTL) 護欄功能，如下所示：

   * 輪廓存放區中的資料為 90 天
   * 資料湖中的資料為 13 個月

  將在第二階段，開放現有客戶沙箱使用這項變更。 

  此外，自 11 月 1 日起，串流細分將不再支援使用追蹤與意見資料集中的傳送和開啟事件。屆時就會將此變更套用至所有客戶沙箱和組織中。 [了解更多](../data/datasets-ttl.md)

* **自訂動作中的參數** (可用日期：2024 年 10 月 3 日)：自訂動作目前有支援無效和選用參數。[了解更多](../action/about-custom-action-configuration.md#define-the-message-parameters)

**報告**

* **Decisioning 報告**&#x200B;現已開放使用，可提供基本深入分析，告訴訪客如何與體驗互動。

**資料治理與同意原則** - 推出日期：2024 年 10 月 7 日

* 已在 Journey Optimizer 的所有管道中強制執行&#x200B;**資料治理原則**。對於已在 Adobe Experience Platform 中建立原則的客戶，這些原則會在設定管道設定時套用至行銷動作。使用設定建立內容時，系統會檢查所有個人化欄位是否有任何資料治理違規。如果發現違規，將無法發佈歷程或行銷活動。[了解更多](../action/action-privacy.md)

* **自訂同意原則**&#x200B;現在適用於所有Journey Optimizer 管道。在傳送訊息或提供傳入體驗之前強制執行時，系統會檢查使用者是否已同意在將收到的內容中使用個人化欄位。如果未予以同意，則不會顯示該體驗。[了解更多](../action/consent.md)

  >[!NOTE]
  >
  >同意原則目前僅適用已購買 Adobe **Healthcare Shield** 與&#x200B;**隱私權與安全性防護**&#x200B;附加產品的組織。

**對象** - 推出日期： 2024 年 10 月 8 日

* 當鎖定目標的 CSV 檔案對象時，您現在可於個人化編輯器與在行銷活動和歷程規則產生器，使用檔案中的屬性。[了解更多](../audience/about-audiences.md)

* 現在可以使用自訂上傳 (CSV 檔案) 中的對象與屬性，來與 Healthcare Shield 或 Privacy and Security Shield 搭配使用

**程式碼型頻道**

* 目前有提供內容範本。 您可以從開發人員建立的內容範本開始使用，加速完成程式碼型體驗的製作。 使用內容範本，讓行銷人員只要修改某些數值或欄位，而不用構成整體 HTML 或 JSON 內容裝載。

**Decisioning**

[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hant) 使用者目前可以選擇在決定中設定 AI 模型時，將 AI 模型最佳化 (之前又稱為體驗決策)。 舉例來說，這讓您可以將自訂「購買」表格最佳化，而非受到轉換率等定義的限制。
