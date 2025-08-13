---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: dc4c512ba48ab7de45ad9719eeb87056ee757dd6
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 35%

---

# 搶鮮版發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能增強並修正錯誤。所有變更都會在每月底整合於[發行說明](release-notes.md)。


## 2025年8月發行前注意事項 {#25-8-rn}

**在發行日期**&#x200B;之前，下列發行前附註可能會有所變更，恕不另行通知。 連結、畫面和更新檔案會在發行日期的發行說明中發佈。

另請參閱 [Adobe Experience Platform 搶鮮版發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**：2025 年 8 月 19 日


### 全新功能 {#Aug-25-8-features}

<table>
<thead>
<tr>
<th><strong>暫停並繼續歷程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您立即可以暫停，繼續歷程。在不中斷客戶體驗的情況下，此功能可讓歷程從業人員暫時暫停即時歷程，藉此提供更大控制力，帶來更多彈性。 暫停時，系統就不會傳送任何通訊，設定檔會維持在暫停狀態，直到繼續歷程為止。</p>
<p>您只能暫停並繼續單一歷程，或可執行大量暫停，然後繼續另一組歷程操作。</p>
<p>此外，您還可以將全域篩選器套用至已暫停歷程，即可根據屬性排除設定檔。</p>
<p><!--img src="assets/do-not-localize/PauseResume.gif"/>--></p>
<p>之前以「限量」的名義發行，目前此功能所有環境都適用 (一般可用性)。</p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-pause.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>行事曆檢視</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程和行銷活動清單中，目前只有提供行事曆視圖。 行事曆視圖讓您可以透過視覺化方式，呈現個別清單中的所有歷程，同時啟用行銷活動。</p>
<p>此功能之前以「限量」的名義發行，目前所有環境都可以使用。在此「一般可用性」版本中，功能包括：</p>
<ul>
<li>日期中導覽的設計改善，</li>
<li>能夠檢視草稿行銷活動（如果您已設定開始和結束日期），</li>
<li>隱藏和顯示長時間執行行事曆專案的新設定。</li>
</ul>
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>使用 Adobe Experience Platform 資料進行個人化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>善用在個人化編輯器中的 Adobe Experience Platform 資料，將內容個人化。 若想這樣做，就必須先透過 API 呼叫，啟用查詢個人化所需的資料集。 一旦完成，您就可以使用這些資料，將內容個人化，改成[!DNL Journey Optimizer]。</p>
<p>此功能之前以 [限量] 的名義發行，目前所有環境都可以使用。 已在此一般可用性版本中，引進以下增強功能：</p>
<ul>
<li>支援傳入頻道、</li>
<li>「datasetLookup」協助程式函式現在可用於運算式和視覺片段中，以使用Adobe Experience Platform資料集中的資料進行個人化內容。</li>
<li>資料集中的選項現在可讓您啟用資料集以進行查詢個人化，而無需執行API呼叫。</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Use Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><img src="assets/do-not-localize/FILE.gif"/></p>
<p><For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>歷程路徑最佳化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在可讓您運用人工智慧和實驗架構，最佳化您的歷程，同時確保條件與最佳化功能之間的無縫可用性及差異。</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
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
<p>Journey Optimizer支援新的通用動作活動，可讓您設定單一動作和多管道傳出動作，進而簡化歷程畫布中的動作設定。 透過此新活動，您還能將目標最佳化、實驗和多語言變體新增到任何內建頻道動作。</p>
<p>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
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
<p>Journey Optimizer現在可讓您建立自訂表單，並在登入頁面中運用自訂表單，將設定檔屬性擷取至為每個表單定義的資料集中。</p>
<p>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。</p>
<p><!--This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.--></p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>


### 改良功能 {#Aug-25-8-improv}

以下列舉部分發布內容附上的改良功能。

* **管理**

   * **頻道設定監視警示** — 您現在可以透過電子郵件或在Journey Optimizer通知中心訂閱接收系統警示，以防發生頻道設定失敗或遺失DNS記錄。

* **行銷活動**

   * **傳出行銷活動的速率控制** — 您現在可以為傳出行銷活動（電子郵件、簡訊、推播通知）啟用節流速率控制，讓您防止下游系統（例如登陸頁面或客戶服務平台）上的超載。

   * **動作行銷活動排程** — 已更新行銷活動每日、每週和每月排程器，以改善詳細程度。 例如，您現在可以設定排程之間的周數/月數、定義要執行的日期，以及決定在特定發生次數後或特定日期停止。

* **頻道 — 推播**

   * **推播通知到期日** — 您現在可以為每個推播通知指定到期日，以防止在特定日期之後傳送對時間敏感的訊息（例如黑色星期五特賣），從而避免給您的客戶帶來不佳的體驗。

* **頻道 — 電子郵件**

   * **電子郵件的PDF附件** — 您現在可以將靜態PDF檔案附加至透過Journey Optimizer傳送的電子郵件訊息。

* **頻道 — SMS**

   * **模糊選擇退出** — 啟用時，**模糊選擇退出**&#x200B;選項會偵測與定義的選擇退出關鍵字（例如「CANCIL」）非常相似的傳入訊息，並自動傳送確認回覆以驗證使用者的取消訂閱意圖。 如果使用者透過定義的提示確認，則取消訂閱他們。

* **設定**

   * **動態網域支援** - Journey Optimizer現在支援在管道設定層級所列之預先定義網域的追蹤URL中的個人化。

   * **一鍵取消訂閱URL的自訂屬性支援** — 使用Journey Optimizer，如果您在Adobe外部管理同意，則可以在電子郵件設定中定義您自己的一鍵取消訂閱連結，以設定外部自訂端點。 當您的收件者按一下取消訂閱連結時，Journey Optimizer會將一些預設的設定檔特定引數附加至同意更新事件。

     若要進一步個人化您的一鍵式取消訂閱連結，您現在可以定義將附加至同意事件的自訂屬性。

* **歷程**

   * **歷程大量作業** — 您現在可以從歷程清單中選取多個專案。 選取後，您一次最多可以暫停或恢復10個歷程。
