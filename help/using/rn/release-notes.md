---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b6f0174b31b4ef317c18644a93a4ae38a712fb36
workflow-type: tm+mt
source-wordcount: '2175'
ht-degree: 89%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="有哪幾種新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會整合到每月最後一週的發行說明一起發表。[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2025年9月更新 {#sep-updates}

### 全新功能 {#Sep-25-features}

<table>
<thead>
<tr>
<th><strong>電子郵件設計工具中的深色模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 電子郵件設計工具現在提供切換到深色模式視圖的功能，您可以在此處額外定義特定的自訂設定，該設定將僅對在深色模式下讀取其電子郵件的收件者顯示。</p>
<p>請注意下列事項：</p>
<ul>
<li>深色模式的最終呈現可能會有所不同，取決於收件者的電子郵件用戶端。</li>
<li>並非所有電子郵件用戶端都支援自訂深色模式。此外，某些電子郵件用戶端只會對收到的所有電子郵件套用自己的預設深色模式。在這兩種情況下，系統無法呈現您在電子郵件設計工具中定義的自訂設定。</li>
</ul>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../email/dark-mode.md">詳細文件</a></p>
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
<p>使用新的「最佳化」節點，鎖定特定客群或執行 A/B 測試，以判斷達到以業務為中心的 KPI 所需的最佳途徑。</p>
<p>此工具可讓您測試並變更內容，以及自訂通訊、排序和時機，以便最有效地觸及客戶。</p>
<p>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/optimize.md">詳細文件</a></p>
<p>推出日期：2025 年 9 月 4 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>子網域的自訂委派方法</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了完全委派和 CNAME 方法之外，目前還有提供一種新的子網域設定方法：自訂委派方法可讓您能完全掌控並維護傳遞、呈現，還有追蹤訊息所需的 DNS 各大層面。</p>
<p>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/delegate-custom-subdomain.md">詳細文件</a></p>
<p>推出日期：2025 年 9 月 4 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用Adobe Experience Platform資料進行個人化和決策 — 可用性限制</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此功能先前於公開測試版發佈，現在僅供有限可用狀態的所有環境使用。 已在此版本中，引進以下增強功能：</p>
<ul><li>支援傳入頻道中的資料集查詢個人化。</li>
<li>「datasetLookup」協助程式函式現在可用於運算式片段中。 目前，此功能僅供有限的客戶使用。 若想取得存取權，請聯絡您的 Adobe 代表。</li>
<li>資料集管理介面中的選項現在可讓您啟用以記錄為基礎的資料集，以進行查詢個人化，而無需執行API呼叫。</li>
<li>增強的監控功能，可追蹤資料擷取狀態，並瞭解資料集何時準備好進行查詢。</li>
<li>更新使用指南和護欄，確保最佳效能和可靠性。</li>
<li>現在可以在決策上限規則中利用Adobe Experience Platform資料集。</li></ul></p>
<p>如需詳細資訊，請參閱<a href="../data/lookup-aep-data.md">詳細文件</a></p>
<p>推出日期：2025 年 9 月 1 日</p>
</td>
</tr>
</tbody>
</table>

### 功能改善 {#Sep-25-improv}

* **動態網域支援** - Journey Optimizer現在支援Adobe所接受的預先定義網域的完整/基本URL個人化。 [閱讀更多資訊](../personalization/personalization-build-expressions.md#where) <!--Availability date: September 12-->

  >[!NOTE]
  >
  >此功能在有限可用性的情況下提供給一組客戶。

* **決策上限規則的運算式** — 您現在可以建立自己的運算式，以定義決策專案的上限規則臨界值。 [閱讀全文](../experience-decisioning/items.md#capping)

  >[!NOTE]
  >
  >此功能目前以有限可用性的形式提供給所有使用者。

* **頻道設定監視警示** — 您現在可以透過電子郵件或在Journey Optimizer通知中心訂閱接收系統警示，以防止發生使用自訂子網域委派型別的電子郵件頻道設定錯誤。 [閱讀全文](../reports/alerts.md#alert-dns-record-missing)

## 2025 年 8 月發行說明 {#25-8-rn}

**發行日期**：2025 年 8 月 19 日

### 全新功能 {#Aug-25-8-features}

此版本隨附的新功能詳述如下。

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
<p><img src="assets/do-not-localize/PauseResume.gif"/></p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-pause.md">詳細文件</a></p>
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
<li>日期中導覽的設計改善；</li>
<li>能夠檢視草稿行銷活動 (如果您已設定開始和結束日期)；</li>
<li>隱藏和顯示長時間執行行事曆項目的新設定。</li>
</ul>
<p><img src="assets/do-not-localize/calendar.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-ui.md#calendar">詳細文件</a></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from [!DNL Adobe Experience Platform] in the personalization editor to personalize your content and decision attributes. In particular, this allows you to extend the definition of your attributes to additional data in datasets for bulk updates that change periodically without having to manually update the attributes one at a time.</p>
<p>With this release, the following enhancements have been introduced:</p>
<ul>
<li>Support of inbound channels,</li>
<li>The "datasetLookup" helper function can now be used within expression and visual fragments to personalize content using data from Adobe Experience Platform datasets,</li>
<li>An option in the dataset now allows you to enable datasets for lookup personalization, without having to perform an API call.</li>
</ul>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p>For more information, refer to the <a href="../personalization/aep-data-perso.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

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
<th><strong>歷程中的動作活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 支援新的一般動作活動，可讓您設定單一動作和多動作的傳入動作群組，進而簡化歷程畫布中的動作設定。尤其是這項新功能允許：</p>
<ul>
<li>簡化歷程畫布中的原生動作設定。</li>
<li>容量用來建立多動作傳入動作群組。</li>
<li>能夠將最佳化新增至任何內建管道動作。</li>
<li>能夠將實驗與多語言選項新增至任何動作。</li>
</ul>
<p>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。</p>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-action.md">詳細文件</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件的 PDF 附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以對透過 Journey Optimizer 傳送的電子郵件訊息附加靜態 PDF 檔案。</p>
<ul>
<li>您每年最多可以為每個設定檔傳送 6 封含有 PDF 附件的訊息。</li>
<li>每個附件允許的大小上限為 5 MB。</li>
<li>如需其他大小或流量，您可以購買附件套組附加元件。 如需詳細資訊，請聯絡您的 Adobe 代表。</li>
</ul>
<p>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>如需詳細資訊，請參閱<a href="../email/pdf-attachments.md">詳細文件</a></p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>行銷活動中的最佳化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 現在可讓您使用工具，為客群提供個人化和最佳化內容，讓您執行內容實驗、建立規則型目標定位，以及使用兩者的進階組合，從而最大化行銷活動和歷程的有效性。</p>
<p>使用最佳化時，您可以：</p>
<ul>
<li>測試多種內容變化，以確定出最有效的傳訊。</li>
<li>根據使用者屬性和內容資料提供個人化內容。</li>
<li>針對進階策略結合目標定位和實驗。</li>
<li>篩選出不符合變體條件的使用者。</li>
<li>確保遞補機制以維持使用者參與。</li>
</ul>
<P>歷程或行銷活動上線後，會根據定義的條件評估輪廓，並根據比對條件，提供輪廓和適當的體驗或內容。</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>先前於 8 月 8 日僅在行銷活動中發行，現在自 8 月 22 日期起，此容量也可在歷程中使用。</p>
<p>如需詳細資訊，請參閱<a href="../campaigns/campaigns-message-optimization.md">詳細文件</a></p>
</td>
</tr>
</tbody>
</table>

### 改良功能 {#Aug-25-8-improv}

以下列舉部分發布內容附上的改良功能。

* **管理**

   * **管道設定監視警示** - 您現在可以透過電子郵件或在 Journey Optimizer 通知中心訂閱接收系統警示，以防<!--a channel configuration failure happens or if -->遺失 DNS 記錄。[閱讀全文](../reports/alerts.md#alert-dns-record-missing)

* **AI 助理**

   * **以多種語言產生內容** - 現在可以法文、西班牙文、德文、義大利文、日文、瑞典文、荷蘭文和挪威文產生內容。[閱讀全文](../content-management/generative-uc.md#languages)

     推出日期：8 月 25 日


* **行銷活動**

   * **傳出行銷活動的速率控制** - 您現在可以為傳出行銷活動 (電子郵件、簡訊、推播通知) 啟用速率控制，讓您防止下游系統 (例如登陸頁面或客戶服務平台) 上的超載。[閱讀全文](../campaigns/campaign-schedule.md#rate-control)

   * **動作行銷活動排程** - 行銷活動每日、每週和每月排程器已更新，為定期排程提供更詳細控制：

      * **每週重複**：您現在可以選擇每週或每兩週重複一次行銷活動，以及選擇應該在一週中的哪一天進行。

      * **每月重複**：您現在可以選擇每個月或每隔一個月重複一次行銷活動，以及選擇應在該月的哪一天進行。

      * **每日、每週或每月排程**：您可以指定是否應在特定日期停止定期排程，或在進行特定次數後停止。

   * **排程交易動作行銷活動** - 排程交易動作行銷活動現在可用於透過電子郵件、簡訊和推播管道傳送批次、以客群為基礎的交易型通訊。

* **頻道 - 內容卡**

   * **內容卡版面配置範本** - 內容卡管道現在提供 OOTB 訊息版面配置，可簡化您的體驗製作流程。此版本包含小型影像、大型影像和僅限影像版面配置範本。[閱讀全文](../content-card/design-content-card.md)

* **管道 - 推播**

   * **推播通知過期日期** - 您現在可以為每個推播通知指定過期日期，以防止在特定日期之後傳送對時間敏感的訊息 (例如黑色星期五特賣)，從而避免使客戶體驗不佳。

* **管道 - 簡訊**

   * **模糊選擇退出** - 啟用時，**模糊選擇退出**&#x200B;選項會偵測與定義的選擇退出關鍵字 (例如「CANCIL」) 非常相似的傳入訊息，並自動傳送確認回覆以驗證使用者的取消訂閱意圖。如果使用者透過定義的提示確認，則可以取消訂閱。[閱讀全文](../sms/sms-configuration-sinch.md)

     >[!NOTE]
     >
     >**模糊選擇退出**&#x200B;僅適用於 Sinch 與 Infobip。

   * **驗證簡訊連線** - 您現在可以將範例訊息傳送至指定裝置，在 Adobe Journey Optimizer 中輕鬆測試和驗證簡訊 API 認證。[閱讀全文](../sms/sms-configuration-sinch.md)

* **設定**

   * **一鍵取消訂閱 URL 的自訂屬性支援** - 使用 Journey Optimizer，如果您在 Adobe 外部管理同意，則可以在電子郵件設定中定義您自己的一鍵取消訂閱連結，以設定外部自訂端點。當您的收件者按一下取消訂閱連結時，Journey Optimizer 會將一些預設的設定檔特定參數附加至同意更新事件。

     若要進一步個人化一鍵取消訂閱連結，您現在可以定義將要同時附加至同意事件的自訂屬性。[閱讀全文](../email/list-unsubscribe.md#custom-attributes)

* **資料集**

   * **體驗決策物件存放庫 - 個人化產品建議項目** - 內建的匯出資料集現在會擷取所有產品建議屬性與生命週期狀態，啟用完整的個人化及報告功能。[閱讀全文](../data/export-datasets.md)

   * 已透過 `etag` 欄位引入版本檢查，以改善一致性並追蹤變更，進而更可靠地提供項目。

* **決策**

   * **將片段附加至決策項目** - Journey Optimizer 現在提供將片段附加至決策項目的功能，而決策項目可透過決策原則用於程式碼型體驗行銷活動。此功能為有限可用性，僅提供給一組客戶。[閱讀全文](../experience-decisioning/create-decision.md#fragments)

* **歷程**

   * **歷程大量作業** - 您現在可以從歷程清單中選取多個項目。選取後，您一次最多可以暫停或恢復 10 個歷程。

   * **自訂動作中的重新導向 (302) 支援** - 自訂動作現在可以根據每個要求處理 HTTP 302 重新導向。 如此一來，歷程便可整合 API，將請求重新導向至本地化或區域特定的 URL。 系統會自動遵循重新導向，確保提供正確內容而不需要額外設定。

   * **歷程中有多個傳入動作** - 為簡化歷程協調，您現在可以在單一歷程中定義數個傳入動作。此功能先前僅供行銷活動使用，可讓您同時向不同位置提供多個程式碼型體驗、應用程式內訊息、內容卡或網頁動作，每個動作都包含特定內容。[閱讀全文](../building-journeys/journey-action.md#multi-action)

## 行銷活動協調

**推出日期**：2025 年 8 月 4 日

Journey Optimizer 現在包含&#x200B;**行銷活動協調**，這是專為品牌啟動的批次行銷活動而建置的新功能。此發行版本推出行銷活動協調畫布和增強型資料模型，共同讓行銷人員規劃、鎖定目標及提供個人化的跨頻道行銷活動。

>[!IMPORTANT]
>
>若要存取行銷活動協調，您的授權必須包含 **Journey Optimizer - 行銷活動和歷程**&#x200B;或 **Journey Optimizer - 行銷活動**&#x200B;套件。請聯絡您的 Adobe 代表以確認您的授權並在需要時進行更新。

![行銷活動協調 GIF](assets/do-not-localize/release.gif)

它包含[關聯式結構描述與資料集](#oc-relational)和[行銷活動畫布](#oc-canvas)。這兩項創新加在一起，在 Journey Optimizer 中開啟了協調批次行銷活動的新標準。主要功能列於下方。

### 主要功能 {#oc-capabilities}

* **多步驟工作流程**

  使用專門建置的全新行銷活動協調畫布，推進複雜的多頻道批次行銷活動。

* **隨選對象**

  隨選區段對象以立即啟用。

* **多實體細分**

  使用產品、商店、續約、預留等商業內容 (非人員維度) 來建立對象。

* **預先傳送可見度**

  在推出之前和行銷活動執行期間，檢閱、調整及最佳化對象和行銷活動

### 行銷活動畫布 {#oc-canvas}

專為批次行銷活動建置的全新視覺協調介面。此畫布能夠實現：

* 多步驟、多頻道行銷活動流程的視覺化規劃

* 支援從關聯式查詢建立的隨選對象

* 進階對象分割、等待和條件式邏輯

* 套用商業規則和篩選器後的精確預先傳送計數

### 關聯式結構描述和資料集 {#oc-relational}

Adobe Journey Optimizer 現在支援連結至以人員為基礎的輪廓的關聯式實體 (例如產品、商店、預訂、合約)。這允許跨多維度資料結構的細分和個人化，啟用如下的使用案例：

* 每個預訂、訂閱或合約有一則訊息

* 根據相關實體屬性 (例如產品類別或商店位置) 細分

* 增強可尋址能力 (例如，傳送給與實體繫結的所有已知聯絡人)

### 為何這項能力很重要

此版本讓行銷人員可完全控制品牌啟動、以對象為基礎的批次行銷，結合彈性的資料建模與特意建置的協調體驗。它專為即時歷程的批次行銷活動協調而設計，同時提供進階的個人化與擴充性。

### 了解更多

閱讀[行銷活動協調文件](../orchestrated/gs-orchestrated-campaigns.md)並深入了解。


