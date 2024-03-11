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
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: ht
source-wordcount: '609'
ht-degree: 100%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於[發行說明](release-notes.md)。

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024 年 2 月搶先發行說明 {#e-2024}

**發行日期**：2024 年 2 月 21 日至 22 日

### 新功能{#e-features}

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
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>簡訊和直接郵件的頻率規則</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在您可以為簡訊和直接郵件管道建立頻率規則。當達到頻率上限時，頻率規則會自動從訊息和動作中排除過度請求的設定檔。 <br/><br/></p>
<img src="assets/do-not-localize/sms-dm-rules.gif">
</tr>
</tbody>
</table>

### 改進項目 {#e-improvements}

此發行版本隨附下列改進項目。

**對象**

* **種子清單** - 使用&#x200B;**種子清單**&#x200B;時現在支援變體。與目標對象的每個個人資料一樣，種子地址會收到相同訊息的所有變體的副本 (例如內容實驗的不同處理方式)。

以下改進之前以測試版形式提供，現在可供所有使用者使用：

* 您現在可以鎖定&#x200B;**透過對象構成所建立的目標對象**，並在歷程中運用擴充屬性。 [了解更多](../building-journeys/read-audience.md)

* 您現在可以鎖定&#x200B;**從 CSV 檔案上傳**&#x200B;至歷程和行銷活動中的目標對象。[了解更多](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* 目前無法將對象構成和自訂上傳 (CSV 檔案) 中的對象和屬性與 Healthcare Shield 或 Privacy and Security Shield 結合使用。
  >* 請注意，從 CSV 檔案上傳對象的改進將在首次發佈後的幾天內逐步推出。雖然某些使用者可以立即存取，但其他使用者在其帳戶中可用之前可能會遇到延遲。

**歷程**

* **篩選您的歷程** - 除了現有的預定義日期篩選器之外，您現在可以使用&#x200B;**自訂日期篩選歷程**&#x200B;詳細目錄。這使您可以透過顯示在特定日期、特定月份、全年或指定時間範圍內建立或發布的歷程來細化清單。
* **自訂動作** - 您現在可以更新 **content-type** 標題。 這個新的 **content-type** 應參考 JSON 內容。
* **設定** - stepEvents 中的 IdentityMap 屬性現在已預先填入。主要身分定義為「primary = true」。
* **使用者介面** - 歷程畫面中的頂部欄已重新組織，以改善體驗。 在不同的更新中，請注意，允許您存取歷程屬性的「鉛筆」圖示現在顯示在頂部欄的左側，歷程名稱旁邊。

**簡訊頻道**

* **選擇加入/選擇退出關鍵字** - 當設定簡訊管道時，您現在可根據您的偏好自訂&#x200B;**選擇加入及選擇退出關鍵字**。 Journey Optimizer 會根據這些指定關鍵字來觸發回應。

**行銷活動**

* **API 觸發的活動** - 在啟動 API 觸發的活動後產生的 cURL 程式碼已增強。 現在其可包含訊息中使用的所有個人化 (個人資料與內容) 變數。

**決策管理**

* **上限規則** - 您現在可針對單一活動內容新增&#x200B;**多重上限規則**。這可讓您針對活動內容傳送方式提高控制等級。

**內容範本**

* **縮圖** - **縮圖檢視**&#x200B;現可用於內容範本與片段，改善視覺存取。

  >[!AVAILABILITY]
  >
  >此功能以有限可用性 (LA) 形式向一小部分客戶發布。

* **多管道範本** - 內容範本現可用於&#x200B;**所有管道**，網路除外。對於電子郵件，您現可選取類型 (HTML 或內容)。
