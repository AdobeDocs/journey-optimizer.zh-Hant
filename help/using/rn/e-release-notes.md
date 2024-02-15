---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 9eb0e37b0547a3eb00802711825ecff63ab5f4a6
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 20%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於[發行說明](release-notes.md)。

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024年2月早期發行說明 {#e-2024}

**發行日期**： 2024年2月20日至21日

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
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Business Rules (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以建立套用至SMS和直接郵件頻道的頻率限定規則。 此外，您可以依通訊型別設定頻率限定規則。<br/><br/></p>
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>



### 改進項目 {#e-improvements}

此發行版本隨附下列改進項目。

**對象**

* 使用時，現在支援變體 **種子清單**. 如同來自目標對象的每個設定檔，種子地址會收到相同訊息的所有變體的副本（例如內容實驗的不同處理）。

先前作為測試版提供，以下改進功能現已可供所有使用者使用：

* 您現在可以鎖定目標 **從CSV檔案上傳的對象** 至歷程與行銷活動。 [了解更多](../audience/about-audiences.md#segments-in-journey-optimizer)
* 您現在可以鎖定目標 **透過對象構成建立的對象** 並在Journeys中運用擴充屬性。 [了解更多](../building-journeys/read-audience.md)

**歷程**

* 您現在可以使用 **用於篩選歷程的自訂日期** 清查，以及現有的預先定義日期篩選器。 這可讓您調整清單，方法是顯示特定日期、特定月內、整年或指定時間範圍內發佈的歷程。
* 您現在可以在中的「content-type」標頭上更新 **自訂動作**.
* stepEvents中的identityMap屬性現在已預先填入。 主要身分定義為「primary = true」。
* 歷程畫面中的頂端列已重新整理，以改善體驗。 在不同的更新中，請注意允許您存取歷程屬性的「鉛筆」圖示現在會顯示在頂端列的左側、歷程名稱旁邊。


**簡訊頻道**

* 設定簡訊通道時，您現在可以自訂 **選擇加入和選擇退出關鍵字** 根據您的偏好設定。 Journey Optimizer會根據這些指定的關鍵字觸發回應。

**行銷活動**

* 已在的「cURL請求」區段中新增資訊 **API觸發的行銷活動** 處「草稿」狀態的範例cURL要求，指定只有在行銷活動已發佈並執行後才會顯示範例cURL要求。

**決策管理**

* 您現在可以新增 **多個上限規則** 一個選件。 這可讓您提高控制優惠傳送方式的等級。

**內容範本**

* A **縮圖檢視** 現在可用於內容範本和片段，以改進視覺存取。
* 內容範本現在可用於 **所有管道**，但Web除外。