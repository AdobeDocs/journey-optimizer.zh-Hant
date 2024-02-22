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
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 16%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於[發行說明](release-notes.md)。

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024年2月早期發行說明 {#e-2024}

**發行日期**： 2024年2月21日至22日

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
<p>您現在可以使用新的網頁應用程式內傳訊功能，透過強制回應覆蓋訊息，直接在網站上顯示個人化內容。 此功能可讓您有效地與網路訪客互動，提高使用者互動、保留率和轉換率。<br/><br/></p>
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
<p>您現在可以建立SMS和直接郵件頻道的頻率規則。 達到頻率上限時，頻率規則會自動將過度請求的設定檔從訊息和動作中排除。 <br/><br/></p>
<img src="assets/do-not-localize/sms-dm-rules.gif">
</tr>
</tbody>
</table>

### 改進項目 {#e-improvements}

此發行版本隨附下列改進項目。

**對象**

* **種子清單**  — 使用時，現在支援變體 **種子清單**. 如同來自目標對象的每個設定檔，種子地址會收到相同訊息的所有變體的副本（例如內容實驗的不同處理）。

先前作為測試版提供，以下改進功能現已可供所有使用者使用：

* 您現在可以鎖定目標 **透過對象構成建立的對象** 並在Journeys中運用擴充屬性。 [了解更多](../building-journeys/read-audience.md)

* 您現在可以鎖定目標 **從CSV檔案上傳的對象** 至歷程與行銷活動。 [了解更多](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* 來自對象構成和自訂上傳（CSV檔案）的對象和屬性目前無法用於Healthcare Shield或Privacy and Security Shield。
  >* 請注意，從CSV檔案上傳的受眾改良功能，將在初次發行後的數天內逐步推出。 雖然部分使用者可立即存取，但其他使用者在其帳戶中可以使用之前可能會遇到延遲問題。

**歷程**

* **篩選您的歷程**  — 您現在可以使用 **用於篩選歷程的自訂日期** 清查，以及現有的預先定義日期篩選器。 這可讓您調整清單，顯示在特定日期、特定月內、整年或指定時間範圍內建立或發佈的歷程。
* **自訂動作**  — 您現在可以更新 **content-type** 標頭。 這個新的 **content-type** 應該參考JSON內容。
* **設定** - stepEvents中的identityMap屬性現在已預先填入。 主要身分定義為「primary = true」。
* **使用者介面**  — 歷程畫面中的頂端列已重新整理，以改善體驗。 在不同的更新中，請注意允許您存取歷程屬性的「鉛筆」圖示現在會顯示在頂端列的左側、歷程名稱旁邊。

**簡訊頻道**

* **選擇加入/選擇退出關鍵字**  — 設定簡訊通道時，您現在可以自訂 **選擇加入和選擇退出關鍵字** 根據您的偏好設定。 Journey Optimizer會根據這些指定的關鍵字觸發回應。

**行銷活動**

* **API觸發的行銷活動**  — 增強啟用API觸發的行銷活動後產生的cURL程式碼。 它現在包含訊息中使用的所有個人化（設定檔和內容）變數。

**決策管理**

* **上限規則**  — 您現在可以新增 **多個上限規則** 一個選件。 這可讓您提高控制優惠傳送方式的等級。

**內容範本**

* **縮圖** - A **縮圖檢視** 現在可用於內容範本和片段，以改進視覺存取。

  >[!AVAILABILITY]
  >
  >此功能以Limited Availability (LA)形式發行，適合少數客戶使用。

* **多頻道範本**  — 內容範本現在可用於 **所有管道**，但Web除外。 針對電子郵件，您現在可以選取型別(HTML或內容)。
