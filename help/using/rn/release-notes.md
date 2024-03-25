---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '1392'
ht-degree: 99%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

![電子報](../assets/do-not-localize/nl-icon.png)立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，把每季最新產品更新、精彩故事、使用案例、提示等內容直接傳送到您的收件匣。

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

當歷程處於中繼狀態時，它是唯讀的。 [了解更多](../building-journeys/journey-gs.md#filter)

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

* **選擇加入/選擇退出關鍵字** - 當設定簡訊管道時，您現在可根據您的偏好自訂&#x200B;**選擇加入及選擇退出關鍵字**。 Journey Optimizer 會根據這些指定關鍵字來觸發回應。[了解更多](../sms/sms-configuration.md#create-api)

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

* **雙重確認選擇加入** - 簡訊的雙重確認選擇加入工作流程可確保使用者從其裝置發出請求時，明確選擇加入要接收訊息。 使用者開始進行同意流程的方式為，傳送傳入簡訊。確認同意後，隨即會傳送後續追蹤訊息，要求進行最終驗證。如果使用者設定檔不存在，則會在成功確認時加以建立。[了解更多](../sms/sms-configuration.md#create-api)

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
