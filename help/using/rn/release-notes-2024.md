---
solution: Journey Optimizer
product: journey optimizer
title: 2024 年發行說明
description: Journey Optimizer 2024 年發行說明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: bae533c5-1bfc-48bf-9f8d-1145383c040c
source-git-commit: 531662b7d5e2455a017d68d6037c44b6950cc894
workflow-type: tm+mt
source-wordcount: '2229'
ht-degree: 100%

---

# 發行說明 2024 年 {#release-notes-2024}

此頁面列出了於 2024 年發行的[!DNL Journey Optimizer]所有功能和改善。



## 2024 年 5 月發行說明 {#may-2024}

**發行日期**：2024 年 5 月 21 日至 22 日

### 新功能 {#e-features}

此發行版本提供下列詳細介紹的新功能。

<table>
<thead>
<tr>
<th><strong>體驗決策──有限可用性</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>體驗決策透過提供稱為「決策項目」的集中行銷優惠目錄與複雜的決策引擎來簡化個人化。 此引擎運用規則與排名標準來選取並呈現最相關的決定項目給每個人。</p>
<p>這些決策項目透過新的程式碼型體驗管道無縫整合到廣泛的傳入介面，現在可在 Journey Optimizer 行銷活動中存取。Experience Decisioning 決策原則僅可用於程式碼型的體驗活動。</p>
<p>體驗決策目前僅可適用於一組組織 (可用性限制)。 若要取得存取權，請和您的 Adobe 代表聯絡。</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/gs-experience-decisioning.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件介面個人化：開放限量使用</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您可以在建立電子郵件頻道介面時，馬上定義動態子網域和個人化標題參數，就能提高電子郵件設定彈性，更能夠掌握得當。</p>
<p>電子郵件介面個人化目前僅開放給某些組織使用 (開放限量使用)。 若要取得存取權，請和您的 Adobe 代表聯絡。</p>
<p>如需詳細資訊，請參閱<a href="../email/surface-personalization.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### 改進項目 {#e-improvements}

此發行版本隨附下列改進項目。

**體驗決策** (限量)

從 Beta 版到此版本，新增了以下改善：

* **體驗決策 + 程式碼型的體驗** ：您現在可以利用體驗決策功能在程式碼型的行銷活動中使用決策項目。 注意：程式碼型的體驗管道和體驗決策不適用於已購買 Adobe Healthcare Shield 以及 Privacy and Security Shield 附加產品的組織。[閱讀全文](../code-based/get-started-code-based.md)
* **內容資料** - 現在您可以在決策規則和排名公式中利用 Adobe Experience Platform 的內容資料。[閱讀全文](../experience-decisioning/context-data.md)
* **新權限** - 決策管理資源現在有新的「管理體驗決策」權限可用。 它可讓您管理與體驗決策相關的權限。[閱讀全文](../experience-decisioning/gs-experience-decisioning.md)
* **上限規則** - 您現在可以為體驗決策中的指定決策項目新增多個上限規則。 這可讓您針對活動內容傳送方式提高控制等級。[閱讀全文](../experience-decisioning/items.md#capping)
* **報告** - 現在您可以使用[!DNL Customer Journey Analytics]建立體驗決策活動的自訂報告儀表板。 [閱讀全文](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**電子郵件頻道**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **垃圾郵件評分** (Beta) - 您現在可以在專用的垃圾郵件報告中檢查您的內容垃圾郵件評分。 使用 SpamAssassin，Adobe Journey Optimizer 現在可以測試您的電子郵件內容並為其評分，以指出 ISP 或信箱提供者是否將其視為垃圾郵件。 [閱讀全文](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >此功能目前為 Beta 版本，僅供 Beta 版客戶使用。若要加入 Beta 版計畫，請聯絡 Adobe 代表。

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**歷程**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **mTLS 支援** - 自訂動作現在支援 mTLS 驗證。 自訂動作或歷程中不需要額外設定即可啟用 mTLS；當偵測到啟用 mTLS 的端點時，它會自動發生。 [閱讀全文](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **查詢事件中的表格** - 現在，當使用物件陣列內的屬性定義關聯性時，您可以運用查詢資料集中的資料。 查閱值將在歷程 (條件、自訂動作等) 以及訊息個人化中使用。 [閱讀全文](../event/experience-event-schema.md#relationships_limitations)
* **事件設定中的進階運算式編輯器** (LA) - 您現在可以在設定事件時運用進階運算式編輯器，讓您定義更複雜的運算式或在事件 ID 條件中使用函數。 此功能以「限量」形式向選定的客戶發布。[閱讀全文](../event/about-creating.md#adv-exp-editor)
* **合併原則** (LA) - 歷程使用的合併原則現在在整個歷程中可見且一致。 此功能以「限量」形式向選定的客戶發布。[閱讀全文](../building-journeys/journey-gs.md#merge-policies)

**全球化**

作為我們不斷努力提供統一使用者體驗的一部分，我們統一了 Adobe Experience Cloud 產品和應用程式中使用的術語。 這會影響德文術語「標題」，在與物件名稱相關時會變更為「標籤」。 這些變更將會逐步在使用者介面與檔案中逐步推出。




## 2024 年 4 月發行說明 {#apr-2024}

**發行日期**：2024 年 5 月 2 日

### 新功能 {#apr-features}

此發行版本提供下列詳細介紹的新功能。

<table>
<thead>
<tr>
<th><strong>多媒體訊息服務 (MMS) - 所有提供者</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過簡訊管道，您現在可以傳送多媒體訊息服務 (MMS) 訊息，來與客戶分享影像、GIF 或影片，藉此增強通訊交流。 MMS 最初僅適用 Sinch，現在也適用 Infobip 與 Twilio。</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>改善的歷程設計工具與即時報告</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此版本隨附改善的畫布使用者介面以供歷程使用，同時提供更直覺且有效率的使用者體驗。 活動更清晰明瞭，只需更少的點按次數就能在 Canvas 歷程上呈現更多資訊。</p>
<img src="assets/new-canvas3.gif"/>
<p>除改善歷程畫布設計外，我們也引進了直接在歷程畫布檢視過去 24 小時報告量度的功能。 </p>
<img src="assets/new-canvas6bis.png"/>
<p><strong>注意</strong>：這些變更將會從 4 月發布內容開始在所有環境逐步推出。</p>
<p>如需詳細資訊，請參閱<a href="new-canvas.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### 改進項目 {#apr-improvements}

此發行版本隨附下列改進項目。

<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**設定**

* 您現在可以在管道表面層級選取行銷動作。在介面使用時，會運用與該行銷動作相關的所有同意原則，以尊重客戶的偏好設定。[閱讀全文](../action/consent.md#surface-marketing-actions)
* 現在管道介面可以使用「物件層級存取控制」。[閱讀全文](../configuration/channel-surfaces.md#create-channel-surface)
* 在管道表面中啟用清單取消訂閱時，您現在可以定義同意級別，以與您管理所有其他來源的同意的方式保持一致。 [閱讀全文](../email/email-settings.md#list-unsubscribe)

**內容管理**

* 現在您可以模擬所有頻道的內容範本。 [閱讀全文](../content-management/content-templates.md#test-templates)

**個人化**

* 表達式編輯器中提供了新的 **toInt** 輔助函數。它允許您將任何類型 (數字、雙精度、整數、長整型、浮點型、短整型、位元組、布林型、字串) 轉換為整數。[閱讀全文](../personalization/functions/math.md#to-int)



## 2024 年 3 月發行說明 {#mar-2024}

**發行日期**： 2024 年 3 月 19 至 20 日

### 新功能 {#mar-features}

此發行版本提供的新功能詳述如下。

<table>
<thead>
<tr>
<th><strong>程式碼型體驗</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過新的程式碼型體驗管道，Adobe Journey Optimizer 可讓您針對任何傳入屬性進行進階個人化及測試，跨不同接觸點 (例如網頁應用程式、行動應用程式、桌面應用程式、視訊主控台、電視連結的裝置、智慧型電視、資訊站、ATM、IoT 裝置等) 達成量身打造的無縫傳遞體驗。</p>
<P>主要功能包括：</p>
<ul><li> 通用個人化：擴充所有接觸點的個人化體驗，確保一致且量身打造的使用者歷程</li>
<li>精細的編輯精確度：在應用程式或網頁內的個別位置編輯特定內容</li>
<li>多樣化實施：支援伺服器端、API 或 SDK 型實施方法，以便順暢整合您的開發環境。</li></ul></p>
<p>如需詳細資訊，請參閱<a href="../code-based/get-started-code-based.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/code-based.gif"> 
</tr>
</tbody>
</table>

### 改進項目 {#mar-improvements}

此發行版本隨附下列改進項目。

**內容範本**

* **縮圖** - **網格檢視**&#x200B;模式現可用於內容範本，展示縮圖以便改善視覺化存取。目前僅支援電子郵件 HTML 範本。 [了解更多](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >此功能以有限可用性 (LA) 形式向一小部分客戶發布。

**歷程**

歷程編寫生命週期已新增新中介狀態：

* **正在發佈**&#x200B;狀態介於&#x200B;**草稿**&#x200B;狀態與&#x200B;**即時**&#x200B;狀態之間
* **正在停止**&#x200B;狀態介於&#x200B;**即時**&#x200B;狀態與&#x200B;**已停止**&#x200B;狀態之間
* **正在啟用測試模式**&#x200B;或&#x200B;**正在停用測試模式**&#x200B;狀態介於&#x200B;**草稿**&#x200B;狀態與&#x200B;**草稿 (測試)**&#x200B;狀態

當歷程處於中介狀態時，其是唯讀。[了解更多](../building-journeys/journey-gs.md#filter)

## 2024 年 2 月發行說明 {#feb-2024}

**發行日期**：2024 年 2 月 21 日至 22 日

### 新功能{#feb-features}

此發行版本提供下列新功能。


<table>
<thead>
<tr>
<th><strong>網頁應用程式內傳訊</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在您可以使用新的網頁應用程式內訊息功能，透過模態疊加訊息直接在網站上顯示個人化內容。此功能可讓您有效地與網路訪客互動，從而增強使用者互動、保留率和轉換率。<br/><br/></p>
<p>如需詳細資訊，請參閱<a href="../in-app/create-in-app-web.md">詳細文件</a>。<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>多管道內容範本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了電子郵件，以下管道現在也提供內容範本：推播、應用程式內、簡訊與直接郵件，每個管道都有專用的範本類型。針對電子郵件，您現在可以選取內容類型，這可讓您將主旨行儲存為電子郵件範本的一部分。 <br/><br/></p>
<p>如需詳細資訊，請參閱<a href="../content-management/content-templates.md">詳細文件</a>。<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif"> 
</tr>
</tbody>
</table>


### 改進項目 {#feb-improvements}

此發行版本隨附下列改進項目。

**對象**

* **種子清單** - 使用&#x200B;**種子清單**&#x200B;時現在支援變體。種子地址會收到相同訊息的所有變體的副本 (例如內容實驗的不同處理方式)。[閱讀全文](../configuration/seed-lists.md)

以下改進之前以測試版形式提供，現在可供所有使用者使用：

* 您現在可以鎖定&#x200B;**透過對象構成所建立的目標對象**，並在歷程中運用擴充屬性。 [了解更多](../building-journeys/read-audience.md)

* 您現在可以鎖定&#x200B;**從 CSV 檔案上傳**&#x200B;至歷程和行銷活動中的目標對象。[了解更多](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* 目前無法將對象構成和自訂上傳 (CSV 檔案) 中的對象和屬性與 Healthcare Shield 或 Privacy and Security Shield 結合使用。
  >* **從 CSV 檔案上傳對象**&#x200B;的改進將在首次發布後的幾天內逐步推出。雖然某些使用者可以立即存取，但其他使用者在其環境可用之前可能會遇到延遲。

**歷程**

* **篩選您的歷程** - 除了現有的預定義日期篩選器之外，您現在可以使用&#x200B;**自訂日期篩選歷程**&#x200B;詳細目錄。這使您可以透過顯示在特定日期、特定月份、全年或指定時間範圍內發布的歷程來細化清單。[閱讀全文](../building-journeys/journey-gs.md#filter)
* **自訂動作** - 您現在可以更新 **content-type** 標題。 這個新的 **content-type** 應參考 JSON 內容。 [閱讀全文](../action/about-custom-action-configuration.md#url-configuration)
* **設定** - stepEvents 中的 IdentityMap 屬性現在已預先填入。主要身分定義為「primary = true」。[閱讀全文](../reports/sharing-field-list.md)
* **使用者介面** - 歷程畫面中的頂部欄已重新組織，以改善體驗。 在不同的更新中，請注意，允許您存取歷程屬性的「鉛筆」圖示現在顯示在頂部欄的左側，歷程名稱旁邊。[閱讀全文](../building-journeys/journey-gs.md#change-properties)

**簡訊頻道**

* **選擇加入/選擇退出關鍵字** - 當設定簡訊管道時，您現在可根據您的偏好自訂&#x200B;**選擇加入及選擇退出關鍵字**。 Journey Optimizer 會根據這些指定關鍵字來觸發回應。[了解更多](../sms/sms-configuration.md)

**行銷活動**

* **API 觸發的活動** - 在啟動 API 觸發的活動後產生的 cURL 程式碼已增強。 現在其可包含訊息中使用的所有個人化 (個人資料與內容) 變數。[閱讀全文](../campaigns/api-triggered-campaigns.md#execute)

**頻率規則**

* 除了電子郵件及推播之外，您現在還可以為簡訊和直接郵件管道建立頻率規則。 當達到頻率上限時，頻率規則會自動從訊息和動作中排除過度請求的設定檔。[閱讀全文](../configuration/frequency-rules.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->


## 2024 年 1 月發行說明 {#jan-2024}

**發行日期**：2024 年 1 月 30 日至 31 日

### 新功能{#jan24-features}

此發行版本提供下列新功能。

<table>
<thead>
<tr>
<th><strong>傳遞能力更新</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 現在支援 DMARC 驗證技術。</p>
<p>2024 年 2 月 1 日起，Google 和 Yahoo! 都要求您對傳送電子郵件所使用的任何網域留有 DMARC 記錄。請確定您已在 Journey Optimizer 中，為要委派給或即將委派給 Adobe 的所有子網域設定 DMARC 記錄。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/dmarc-record-update.md">詳細文件</a>。</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用案例教戰手冊</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在 Real-Time CDP 和 Journey Optimizer 中，利用特定產業使用案例教戰手冊的目錄，解決您可以使用 Adobe Experience Platform 和 Adobe Journey Optimizer 來執行的常見使用案例。</p><p>在您選擇最符合需求的教戰手冊後，您可加以啟用來產生歷程、訊息、結構描述或區段等支援使用案例所需的資產，並根據結構描述來予以自訂，以加速創造價值。</p>
<p>如需詳細資訊，請參閱<a href="../start/playbooks.md">詳細文件</a>。</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### 改進項目 {#jan24-improvements}

此發行版本隨附下列改進項目。

**報告**

* **新的網域型劃分 Widget** - 已新增新的 Widget 來增強 Campaign 和 Journey 報告。**退回原因 (依網域)**、**傳送次數與送達次數 (依網域)**、**開啟次數與點按次數 (依網域)** 和&#x200B;**退回數與錯誤數 (依網域)** Widget 會針對關鍵電子郵件傳送和追蹤量度，提供網域層級的詳細劃分。[了解更多](../reports/channel-report.md)

**簡訊頻道**

* **雙重確認選擇加入** - 簡訊的雙重確認選擇加入工作流程可確保使用者從其裝置發出請求時，明確選擇加入要接收訊息。 使用者開始進行同意流程的方式為，傳送傳入簡訊。確認同意後，隨即會傳送後續追蹤訊息，要求進行最終驗證。如果使用者設定檔不存在，則會在成功確認時加以建立。[了解更多](../sms/sms-configuration.md)

  請注意，此功能適用於 Sinch 和 Infobip 簡訊提供者。

**歷程**

* **反應事件期間** - 您可在&#x200B;**反應事件**&#x200B;中定義的最長期間現在為 29 天，而非 30 天。 [了解更多](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **讀取對象** - **讀取對象**&#x200B;活動現在仰賴批次區段的設定檔快照資料集，其會在排程的每日批次工作執行後產生，一天只會產生一次，因此將會是截至最後的每日批次工作的最新資料。[了解更多](../building-journeys/read-audience.md)

* **欄位群組** - 此發行版本修正在特定情況下無法儲存欄位群組的問題。

* 已在多個函數中修改 `<listObject>` 的支援。

**頻率規則**

* **每週頻率上限** - 除了以月為單位之外，您現在可以指定一週內所能傳送給客戶設定檔的訊息數量上限。頻率上限是以所選的行事曆期間為基礎，並會在對應的時間段開始時重設。 [了解更多](../configuration/frequency-rules.md#create-new-rule)

  >[!NOTE]
  >
  >每日頻率上限也可隨選提供。 請聯絡您的 Adobe 代表。

**決策管理**

* **Edge 的頻率限定** - 頻率限定計數器現已更新，並可在不到 3 秒內做出 Edge Decisioning API 決定。[了解更多](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
