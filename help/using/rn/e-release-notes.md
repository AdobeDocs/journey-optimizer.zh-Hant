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
workflow-type: ht
source-wordcount: '558'
ht-degree: 100%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於[發行說明](release-notes.md)。

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024 年 1 月搶先發行說明 {#e-2024}

**發行日期**：2024 年 1 月 20 日至 31 日

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
<p>Journey Optimizer 現在支援 DMARC 驗證技術。</p>
<p>2024 年 2 月 1 日起，Google 和 Yahoo! 將要求您需有 DMARC 記錄，才能使用任何網域向其傳送電子郵件。請確定您已在 Journey Optimizer 中，為要委派給或即將委派給 Adobe 的所有子網域設定 DMARC 記錄。</p>
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
<p>在 Real-Time CDP 和 Journey Optimizer 中，利用特定產業使用案例教戰手冊的目錄，解決您可以使用 Adobe Experience Platform 和 Adobe Journey Optimizer 來執行的常見使用案例。</p><p>在您選擇最符合需求的教戰手冊後，您可加以啟用來產生歷程、訊息、結構描述或區段等支援使用案例所需的資產，並根據結構描述來予以自訂，以加速創造價值。</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
<!--<p>For more information, refer to the <a href="../start/playbooks.md">detailed documentation</a>.</p>-->
</tr>
</tbody>
</table>

### 改進項目 {#e-improvements}

此發行版本隨附下列改進項目。

**報告**

* **新的網域型劃分 Widget** - 已新增新的 Widget 來增強 Campaign 和 Journey 報告。**退回原因 (依網域)**、**傳送次數與送達次數 (依網域)**、**開啟次數與點按次數 (依網域)** 和&#x200B;**退回數與錯誤數 (依網域)** Widget 會針對關鍵電子郵件傳送和追蹤量度，提供網域層級的詳細劃分。[了解更多](../reports/channel-report.md)

**簡訊頻道**

* **雙重確認選擇加入** - 簡訊的雙重確認選擇加入工作流程可確保使用者從其裝置發出請求時，明確選擇加入要接收訊息。 使用者開始進行同意流程的方式為，傳送傳入簡訊。確認同意後，隨即會傳送後續追蹤訊息，要求進行最終驗證。如果使用者設定檔不存在，則會在成功確認時加以建立。[了解更多](../sms/sms-configuration.md#create-api)

  請注意，這僅適用於 Sinch 和 Infobip 簡訊提供者。

**歷程**

* **反應事件期間** - 您可在&#x200B;**反應事件**&#x200B;中定義的最長期間現在為 29 天，而非 30 天。 [了解更多](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **讀取對象** - 讀取對象活動現在仰賴批次區段的設定檔快照資料集，其會在排程的每日批次工作執行後產生，一天只會產生一次，因此將會是截至最後的每日批次工作的最新資料。

* **欄位群組** - 已修正在特定情況下無法儲存欄位群組的問題。

* **運算式編輯器** - 我們目前在所有運算式和其他函數中支援 listObject 資料類型。[更多資訊](../building-journeys/expression/functions.md)

**頻率規則**

* **每週和每日頻率上限** - 除了以月為單位之外，您現在可以指定一週或一天內所能傳送給客戶設定檔的訊息數量上限。頻率上限是以所選的行事曆期間為基礎，並會在對應的時間段開始時重設。 [進一步了解](../configuration/frequency-rules.md#create-new-rule)

**決定管理**

* **Edge 的頻率限定** - 頻率限定計數器現已更新，並可在不到 3 秒內做出 Edge Decisioning API 決定。