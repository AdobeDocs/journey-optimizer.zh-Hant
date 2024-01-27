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
source-git-commit: fae367cbbacffbbecde4cdbf7b39b1baeec452d1
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 20%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於[發行說明](release-notes.md)。

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024年1月早期發行說明 {#oct-jan-2024}

**發行日期**： 2024年1月30日至31日

### 新功能{#jan-2024-features}

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
<p>Journey Optimizer現在支援DMARC驗證技術。</p>
<p>2024年2月1日起，Google和Yahoo！ 將要求您擁有DMARC記錄，才能使用任何網域來傳送電子郵件給他們。 請確定您已為已委派或正在委派給Journey Optimizer中Adobe的所有子網域設定DMARC記錄。</p>
<!--img src="assets/channel-reports.png"/-->
<p>如需詳細資訊，請參閱<a href="../configuration/dmarc-record-update.md">詳細文件</a>。</p>
</tr>
</tbody>
</table>



### 改進項目 {#jan-2024-improvements}

此發行版本隨附下列改進項目。

**報告**

* **管道報表（依網域）**  — 已新增新的Widget，以增強您的行銷活動和歷程報告。 此 **依網域區分的退信原因**， **依網域傳送和傳遞**， **依網域區分的開啟與點按** 和 **依網域區分的退回和錯誤** Widget會針對關鍵電子郵件傳送和追蹤量度，提供網域層級的詳細劃分。

**簡訊頻道**

* **雙重選擇加入**  — 簡訊的雙重選擇加入工作流程可確保使用者在從裝置起始請求時，明確選擇加入接收訊息。 使用者透過傳送傳入SMS訊息來起始同意程式。 確認同意後，會傳送後續訊息，要求最終驗證。 如果使用者設定檔不存在，則會在成功確認時建立。

  請注意，這僅適用於Sinch和Infobip簡訊提供者。

**歷程**

* **反應事件持續時間**  — 您可以在「 」中定義的最長持續時間 **反應事件** 現在是二十九天，而非30天。

* **日期篩選器**  — 除了現有的預先定義日期篩選器外，您現在可以使用自訂日期來篩選歷程詳細目錄。 這可讓您調整清單，方法是顯示特定日期、特定月內、整年或指定時間範圍內發佈的歷程。

* **讀取對象**   — 讀取對象活動現在仰賴批次區段的設定檔快照資料集，這僅在排程的每日批次工作執行後每天產生一次。

**頻率規則**

* **每週和每日頻率上限**  — 您現在可指定在一週或一天內（不含月份），傳送至客戶設定檔的最大訊息數量。 頻率上限是以所選的日曆期間為基礎，並在對應的時間範圍開始時重設。


**決策管理**

* **邊緣的頻率標示**  — 頻率上限計數器現已更新，並可在不到3秒內的邊緣決策API決策中使用。