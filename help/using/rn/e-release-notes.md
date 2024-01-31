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
source-git-commit: 97967e8043df9b75d3120e4a7bfccff700f5d57f
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 16%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於[發行說明](release-notes.md)。

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面和更新後的檔案會發佈在 [發行說明](release-notes.md)，於發行日期。

## 2024年1月早期發行說明 {#e-2024}

**發行日期**： 2024年1月20日至31日

### 新功能{#e-features}

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
<p>如需詳細資訊，請參閱<a href="../configuration/dmarc-record.md">詳細文件</a>。</p>
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
<p>在Real-Time CDP和Journey Optimizer中運用產業特定使用案例教戰手冊的目錄，以解決您可以使用Adobe Experience Platform和Adobe Journey Optimizer執行的常見使用案例。</p><p>一旦您選擇了最符合您需求的教戰手冊，您可以啟用它來產生支援使用案例所需的資產，例如歷程、訊息、結構描述或區段，並根據您的結構描述自訂它們，以更快實現價值。</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
<!--<p>For more information, refer to the <a href="../start/playbooks.md">detailed documentation</a>.</p>-->
</tr>
</tbody>
</table>

### 改進項目 {#e-improvements}

此發行版本隨附下列改進項目。

**報告**

* **新的網域型劃分Widget**  — 已新增新的Widget，以增強您的行銷活動和歷程報告。 此 **依網域區分的退信原因**， **依網域傳送和傳遞**， **依網域區分的開啟與點按** 和 **依網域區分的退回和錯誤** Widget會針對關鍵電子郵件傳送和追蹤量度，提供網域層級的詳細劃分。 [了解更多](../reports/channel-report.md)

**簡訊頻道**

* **雙重選擇加入**  — 簡訊的雙重選擇加入工作流程可確保使用者在從裝置起始請求時，明確選擇加入接收訊息。 使用者透過傳送傳入SMS訊息來起始同意程式。 確認同意後，會傳送後續訊息，要求最終驗證。 如果使用者設定檔不存在，則會在成功確認時建立。 [了解更多](../sms/sms-configuration.md#create-api)

  請注意，這僅適用於Sinch和Infobip簡訊提供者。

**歷程**

* **反應事件持續時間**  — 您可以在「 」中定義的最長持續時間 **反應事件** 現在是二十九天，而非30天。 [了解更多](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **讀取對象**  - 「讀取對象」活動現在仰賴批次區段的設定檔快照集資料集，這僅在排程的每日批次工作執行後一天產生一次，因此資料將會刷新到最後的每日批次工作。

* **欄位群組**  — 修正阻止欄位群組在某些情況下儲存的問題。

* **運算式編輯器**  — 我們目前在所有運算式和其他函式中支援listObject資料型別。 [更多資訊](../building-journeys/expression/functions.md)

**頻率規則**

* **每週和每日頻率上限**  — 您現在可指定在一週或一天內（不含月份），傳送至客戶設定檔的最大訊息數量。 頻率上限是以所選的日曆期間為基礎，並在對應的時間範圍開始時重設。 [進一步了解](../configuration/frequency-rules.md#create-new-rule)

**決定管理**

* **邊緣的頻率限定**  — 頻率上限計數器現已更新，並可在不到3秒內的邊緣決策API決策中使用。