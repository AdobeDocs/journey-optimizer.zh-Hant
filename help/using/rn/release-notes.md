---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 13ee474819aa0b63561946d94111cd76f3d5689d
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 95%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

![電子報](../assets/do-not-localize/nl-icon.png)立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，把每季最新產品更新、精彩故事、使用案例、提示等內容直接傳送到您的收件匣。

## 2024 年 1 月搶先發行說明 {#jan-2024}

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
<p>2024年2月1日起，Google和Yahoo！ 要求您擁有用於向其傳送電子郵件的任何網域的DMARC記錄。 請確定您已在 Journey Optimizer 中，為要委派給或即將委派給 Adobe 的所有子網域設定 DMARC 記錄。</p>
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

* **每週和每日頻率上限** - 除了以月為單位之外，您現在可以指定一週或一天內所能傳送給客戶設定檔的訊息數量上限。頻率上限是以所選的行事曆期間為基礎，並會在對應的時間段開始時重設。 [進一步了解](../configuration/frequency-rules.md#create-new-rule)

**決定管理**

* **Edge 的頻率限定** - 頻率限定計數器現已更新，並可在不到 3 秒內做出 Edge Decisioning API 決定。[了解更多](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)