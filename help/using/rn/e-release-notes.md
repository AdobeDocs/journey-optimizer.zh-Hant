---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: fcf7ea6d5d6ceaa02490e8cbaf807b9f670c63cc
workflow-type: tm+mt
source-wordcount: 2157
ht-degree: 20%

---


# 搶鮮版發行說明 {#e-release-notes}

Adobe Journey Optimizer 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

## 2026年8月發行前注意事項 {#august-26-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。 連結、畫面和更新的文件會在變更上線生產時發佈。 雖然大多數變更會在發行日期提供，但有些可能會稍後推出。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**： 2026年8月18至19日

### 入門 {#august-26-onboarding}

下列功能已新增至此版本的上線。

<table>
<thead>
<tr>
<th><strong>入門電子郵件和歷程的引導功能（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過引導式功能，協助您將現有電子郵件內容和歷程移至Journey Optimizer，讓從其他行銷平台轉換至Adobe Journey Optimizer變得更輕鬆。 專屬的工作區可讓您重複使用現有工作，而非從頭重建。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15330">DOCAC-15330</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 歷程 {#august-26-journeys}

下列功能和改進功能已新增到此版本的歷程。

<table>
<thead>
<tr>
<th><strong>歷程層級保留</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以直接從歷程屬性設定歷程的保留群組。 保留是目標受眾中可設定的百分比，會排除在進入歷程之外且不會收到任何通訊。 將保留設定檔與Customer Journey Analytics報告中的作用中設定檔進行比較，即可測量歷程帶來的增量提升度（實際影響）。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15162">DOCAC-15162</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **在歷程運算式編輯器中加入新的dateDiff函式** — 歷程運算式編輯器現在包含`dateDiff`函式，該函式會以天數計算兩個日期之間的差異。 此函式適用於以時間為基礎的邏輯，例如建立截止日期、計算客戶生命週期持續時間或在歷程條件中建立倒數計時器。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15293">DOCAC-15293</a> <!-- Documentation link: TBD -->

* **歷程標題中的開始和結束日期** — 當在歷程上設定開始和/或結束日期時，它們現在會出現在狀態徽章旁邊的歷程標題中。 顯示的標籤會根據每個日期是即將到來或是已過去而調整。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">DOCAC-14702</a> <!-- Documentation link: TBD -->

### 行銷活動 {#august-26-camp}

下列功能和改善專案已新增至此版本中的行銷活動。

<table>
<thead>
<tr>
<th><strong>Action行銷活動中的傳入體驗模擬</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在上線前在「動作」行銷活動中模擬傳入頻道動作。 使用模擬模式透過模擬使用者測試您的設定並預覽呈現的體驗，包括產生的URL和QR碼，因此您可以端對端驗證規則、決策和內容呈現。</p>
<p>此功能目前為私人測試版，僅供有限的組織使用。 請聯絡您的 Adobe 代表以取得更多資訊。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15166">DOCAC-15166</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **行銷活動的資料夾** — 您現在可以將行銷活動整理到資料夾中，以改善介面中的導覽和管理。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15098">DOCAC-15098</a> <!-- Documentation link: TBD -->

* **行銷活動儀表板中的品牌一致性分數** - 您現在可以直接在行銷活動儀表板中評估您的品牌一致性分數，以確保內容符合品牌形象。 這可讓您快速驗證指引，而無需開啟內容設計工具。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14516">DOCAC-14516</a> <!-- Documentation link: TBD -->

* **覆寫行銷活動中的預設執行欄位** - 先前可在歷程層級使用，您現在可以在全域覆寫行銷活動參數中電子郵件、簡訊和 WhatsApp 傳送的預設執行欄位集。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">DOCAC-14718</a> <!-- Documentation link: TBD -->

### 協調的行銷活動 {#august-26-oc}

下列功能和改進功能已新增到此版本的協調行銷活動。

<table>
<thead>
<tr>
<th><strong>針對協調的行銷活動提供無訊息工作時間支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將無訊息時間套用至協調行銷活動。 無訊息小時可讓您定義以時間為基礎的排除，以防止在特定期間傳送訊息，協助您在行銷活動協調使用案例中遵守客戶偏好設定和合規性要求。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14054">DOCAC-14054</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **管理設定檔目標維度的功能** — 您現在可以刪除設定檔目標Dimension，或編輯並交換其設定的身分名稱空間，讓您對資料設定有更優異的控制權和彈性。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15018">DOCAC-15018</a> <!-- Documentation link: TBD -->

* **支援Line （可用性限制）** — 您現在可以直接將LINE動作新增至您的協調行銷活動中。 這項新活動可讓您建立及提供高度個人化的內容，包括文字、貼圖、影像、影片、位置資料和豐富的Flex訊息，以便在LINE平台上順暢地吸引您的客戶。 此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14905">DOCAC-14905</a> <!-- Documentation link: TBD -->

* **新協調行銷活動公開API** — 現已為協調行銷活動提供新API規格。 這些API可讓您以程式設計方式建立、管理和觸發協調的行銷活動，實現與外部系統和自動化管道的更深層整合。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14308">DOCAC-14308</a> <!-- Documentation link: TBD -->

* **個人化每個收件者和行銷活動的電子郵件寄件者詳細資料** — 協調的行銷活動現在支援使用設定檔屬性或關聯資料，個人化電子郵件標題欄位，包括寄件者名稱、寄件者地址和回覆對象。 如此一來，寄件者詳細資料就能反映每個收件者的相關顧問、位置或分支，而非透過單一公司地址路由所有傳送。 可在管道層級設定標頭值，並使用內容資料覆寫每個行銷活動，以獲得更精確的控制。 <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">DOCAC-13761</a> <!-- Documentation link: TBD -->

* **協調行銷活動中的目標維度簡化** — 作用中目標維度現在會顯示在工作流程畫布上，因此您可以檢視頻道活動使用的維度。 多實體區段流程較簡單，因為您不再需要個別的「變更維度」活動。 此外，您現在可以明確選擇訊息是在設定檔層級還是在次要維度層級傳送。 <a href="https://jira.corp.adobe.com/browse/DOCAC-13554">DOCAC-13554</a> <!-- Documentation link: TBD -->

* **在協調的行銷活動中使用波段傳送** — 您現在可以排程來自協調行銷活動的輸出訊息，以控管批次方式隨時間傳送。 波次傳送也支援更好的傳遞能力，並降低被標籤為垃圾訊息的風險，有助於維持強大的寄件者信譽，是高流量或時間敏感型行銷活動的理想選擇。 <a href="https://jira.corp.adobe.com/browse/DOCAC-13990">DOCAC-13990</a> <!-- Documentation link: TBD -->

### 管道 {#august-26-channels}

下列功能和改進專案已新增到此版本中的管道。

<table>
<thead>
<tr>
<th><strong>Web Channel中的決策支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning現在可用於Web管道。 您可以直接在網頁視覺化編輯器中使用決定原則，將最相關的選件傳送給每位訪客。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11548">DOCAC-11548</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API觸發的電子郵件中的個人化PDF附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在支援在API觸發的行銷活動中，每封電子郵件最多附加5個收件者特定PDF。 PDF檔案會安全地從資料登陸區域擷取並在傳送時附加，每個檔案的位置都直接在API裝載中傳遞。 這可讓現有的上游檔案產生系統維持原狀，由Journey Optimizer處理傳送。</p>
<p>支援的使用案例包括發票、對帳單、票證、合約、出貨標籤，以及依收件者而異的類似檔案。 個人化PDF附件僅適用於API觸發的行銷活動，在歷程或協調的行銷活動中不支援。</p>
<p>PDF附件附加元件支援較大的附件數量與大小；如需詳細資訊，請聯絡您的Adobe代表。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15186">DOCAC-15186</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **LINE 管道 - 製作變更** - LINE 管道 UI 已升級進階訊息製作功能。 此發行版本引入對多種訊息格式的支援，包括文字、影像、影像地圖、輪播和Flex （JSON編輯器），以及即時裝置預覽。 使用者現在可以管理最多五個已排序訊息的群組訊息 (包含新增、移除和重新排序控制項)，並利用整合的個人化編輯器進行驗證的動態傳訊。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">DOCAC-14869</a> <!-- Documentation link: TBD -->

* **輸送量的效能附加元件 — 推播** — 在API觸發的行銷活動中提供新的高輸送量異動訊息模式。 此模式專為大規模即時交易型傳訊而設計，最高可支援每秒 5,000 筆交易，而且可用性更高。 此功能先前僅適用於電子郵件頻道，現在也可用於推播頻道，適用於已購買Adobe高輸送量異動訊息附加元件產品的組織。 請聯絡您的 Adobe 代表以取得更多資訊。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14717">DOCAC-14717</a> <!-- Documentation link: TBD -->

### 決策 {#august-26-decisioning}

下列改善專案已新增至此版本中的決策。

* **決策中的版位層級頻率上限** — 決策中的頻率上限規則現在可以將範圍限定於個別版位，讓您更能掌控優惠方案在指定介面中的顯示頻率。 有兩種模式可供使用：版位特定上限，定義只適用於所選版位中顯示優惠方案的上限；以及每次版位上限，會針對出現優惠方案的每個版位獨立套用上限，因此每個版位都會維持其自己的上限計數器。 請注意，與位置相關的上限不適用於使用以Adobe Experience Platform資料為基礎的規則來設定上限的優惠方案。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14980">DOCAC-14980</a> <!-- Documentation link: TBD -->

### 電子郵件設計工具 {#august-26-email}

此版本的電子郵件Designer已新增下列改善專案。

* **電子郵件Designer中的新表格元件** — 電子郵件Designer現在包含內建的表格元件，可讓您直接在電子郵件中建構列和欄的內容。 將元件拖放至畫布上、自訂列和欄數，並獨立設定每個儲存格的樣式，以建立清晰、有組織的版面配置，而不依賴自訂HTML。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15093">DOCAC-15093</a> <!-- Documentation link: TBD -->

### 管理 {#august-26-administration}

下列改善專案已新增至此版本的管理中。

* **自訂子網域的Feedback Loop OTP程式** — 直接在產品UI中顯示Yahoo寄件者中心一次性密碼(OTP)，已改善Feedback Loop (FBL)自訂子網域設定程式。 使用者現在可以自動擷取及顯示Yahoo寄件者中心網域擁有權驗證期間產生的OTP。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">DOCAC-14815</a> <!-- Documentation link: TBD -->

### 可用性改進功能 {#august-26-usability}

已針對此版本的使用性新增下列改善專案。

* **內容變體的新內容模擬體驗** - **模擬內容**&#x200B;工作流程引入重新設計的體驗：所有變體現在都會在單一可捲動格線（並排、棧疊或包裝版面）中一起呈現，取代一次一個變體的檢視。 單一底部動作列可整合測試變體之間的導覽、縮放、檢視區切換（案頭/行動裝置）、地區設定切換、新增範例輸入、使用AI產生變體、挑選並儲存模擬使用者，以及匯入或匯出變體。 移除左側邊欄並收合額外的頁首圖層可大幅增加預覽的空間。 下方動作列中的&#x200B;**切換為傳統體驗**&#x200B;選項可讓您隨時還原成先前的體驗。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15285">DOCAC-15285</a> <!-- Documentation link: TBD -->

* **歷程詳細目錄中的大量作業** — 您現在可以直接從歷程詳細目錄清單執行新的大量動作，以便更快速地一次管理多個歷程。 選取數個歷程，並在單一步驟中套用下列任何新動作：新增至封裝、刪除、移至資料夾、編輯標籤或管理存取權。 這降低了一次一個歷程重複相同動作的需求，並簡化了處理大量歷程的團隊的歷程管理。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15358">DOCAC-15358</a> <!-- Documentation link: TBD -->

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## 2026年7月發行前注意事項 {#july-26-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。 連結、畫面和更新的文件會在變更上線生產時發佈。 雖然大多數變更會在發行日期提供，但有些可能會稍後推出。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**： 2026年7月28至29日

<!--

### Onboarding {#july-26-onboarding}

Journey Optimizer introduces the Onboarding Assistant, a new capability in this release.

<table>
<thead>
<tr>
<th><strong>Onboarding Assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### 歷程 {#july-26-journeys}

下列改善專案已新增至此版本中的歷程。


### 行銷活動 {#july-26-campaigns}

下列功能和改善專案已新增至此版本中的行銷活動。

<!--
<table>
<thead>
<tr>
<th><strong>Inbound experience simulation in Action campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now simulate inbound channel actions in Action campaigns before going live. Use simulation mode to test your configuration with simulated users and preview the rendered experience, including a generated URL and QR code, so you can validate rules, decisioning, and content rendering end-to-end.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>
-->

### 協調的行銷活動 {#july-26-oc}

下列改善專案已新增至此版本中的協調行銷活動。

<!--

<table>
<thead>
<tr>
<th><strong>Quiet Hours support for orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now apply quiet hours to Orchestrated campaigns. Quiet hours let you define time-based exclusions to prevent messages from being sent during specific periods, helping you respect customer preferences and compliance requirements across campaign orchestration use cases.</p>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **Ability to Manage Profile Target Dimensions** - You can now delete a Profile Target Dimension or edit and swap its configured identity namespace, providing greater control and flexibility over your data setups.

* **Support for Line** - You can now add LINE actions directly into your Orchestrated campaigns. This new activity allows you to build and deliver highly personalized content, including text, stickers, images, videos, location data, and rich Flex Messages, to engage your customers seamlessly on the LINE platform. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

* **New Orchestrated campaigns public APIs** - New API specifications are now available for Orchestrated campaigns. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines.

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address. Header values can be set at the channel level and overridden per campaign using contextual data for more precise control. Documentation link: TBD

* **Target dimension simplification in Orchestrated campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.

* **Send messages in waves** - You can now schedule outbound messages from orchestrated campaigns to be delivered in controlled batches over time. Ideal for high-volume or time-sensitive campaigns, wave sending also supports better deliverability and helps maintain a strong sender reputation by reducing the risk of being flagged as spam.

-->

### 管道 {#july-26-channels}

下列功能和改進專案已新增到此版本中的管道。

### 決策 {#july-26-decisioning}

下列改善專案已新增至此版本中的決策。

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### 內容管理 {#july-26-content}

下列改善專案已新增至此版本的內容管理。

<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### 個人化 {#july-26-personalization}

下列改善專案已新增至此版本中的個人化。


### 電子郵件設計工具 {#july-26-email}

下列功能已新增至此版本的電子郵件通道。


### 管理 {#july-26-administration}

下列功能已新增至此版本的管理中。


### 可用性改進功能 {#july-26-usability}

此版本即將推出下列可用性改善。

* 內容範本中SMS、推播、應用程式內和程式碼基底頻道的&#x200B;**快速啟動捷徑** — 「內容範本」清單中的&#x200B;**更多動作**&#x200B;按鈕現在提供其他頻道特定捷徑。 對於SMS範本，請快速編輯訊息或檢查字元計數/區段。 對於推播範本，請編輯標題、本文或媒體。 針對應用程式內範本，請編輯訊息標頭、訊息本文或媒體URL。 對於程式碼基底通道範本，請直接編輯程式碼。 這些捷徑可擴充現有的電子郵件頻道快速啟動捷徑。<!-- Documentation link: TBD -->
