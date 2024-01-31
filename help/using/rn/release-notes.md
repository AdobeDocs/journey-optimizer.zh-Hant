---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 146a142afeb47debac0d56963e48225a85b0f2c4
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 28%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

![電子報](../assets/do-not-localize/nl-icon.png)立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，把每季最新產品更新、精彩故事、使用案例、提示等內容直接傳送到您的收件匣。

## 2024年1月早期發行說明 {#jan-2024}

**發行日期**： 2024年1月30日至31日

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
<p>Journey Optimizer現在支援DMARC驗證技術。</p>
<p>2024年2月1日起，Google和Yahoo！ 將要求您擁有DMARC記錄，才能使用任何網域來傳送電子郵件給他們。 請確定您已為已委派或正在委派給Journey Optimizer中Adobe的所有子網域設定DMARC記錄。</p>
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
<p>在Real-Time CDP和Journey Optimizer中運用產業特定使用案例教戰手冊的目錄，以解決您可以使用Adobe Experience Platform和Adobe Journey Optimizer執行的常見使用案例。</p><p>一旦您選擇了最符合您需求的教戰手冊，您可以啟用它來產生支援使用案例所需的資產，例如歷程、訊息、結構描述或區段，並根據您的結構描述自訂它們，以更快實現價值。</p>
<p>如需詳細資訊，請參閱<a href="../start/playbooks.md">詳細文件</a>。</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### 改進項目 {#jan24-improvements}

此發行版本隨附下列改進項目。

**報告**

* **新的網域型劃分Widget**  — 已新增新的Widget，以增強您的行銷活動和歷程報告。 此 **依網域區分的退信原因**， **依網域傳送和傳遞**， **依網域區分的開啟與點按** 和 **依網域區分的退回和錯誤** Widget會針對關鍵電子郵件傳送和追蹤量度，提供網域層級的詳細劃分。 [了解更多](../reports/channel-report.md)

**簡訊頻道**

* **雙重選擇加入**  — 簡訊的雙重選擇加入工作流程可確保使用者在從裝置起始請求時，明確選擇加入接收訊息。 使用者透過傳送傳入SMS訊息來起始同意程式。 確認同意後，會傳送後續訊息，要求最終驗證。 如果使用者設定檔不存在，則會在成功確認時建立。 [了解更多](../sms/sms-configuration.md#create-api)

  請注意，此功能適用於Sinch和Infobip簡訊提供者。

**歷程**

* **反應事件持續時間**  — 您可以在「 」中定義的最長持續時間 **反應事件** 現在是二十九天，而非30天。 [了解更多](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **讀取對象**  - **讀取對象** 活動現在仰賴批次區段的設定檔快照資料集，這僅在排程的每日批次工作執行後一天產生一次，因此資料將會刷新到最後的每日批次工作。 [了解更多](../building-journeys/read-audience.md)

* **欄位群組**  — 此版本修正特定情況下無法儲存欄位群組的問題。

**頻率規則**

* **每週和每日頻率上限**  — 您現在可指定在一週或一天內（不含月份），傳送至客戶設定檔的最大訊息數量。 頻率上限是以所選的日曆期間為基礎，並在對應的時間範圍開始時重設。 [進一步了解](../configuration/frequency-rules.md#create-new-rule)

**決定管理**

* **邊緣的頻率限定**  — 頻率上限計數器現已更新，並可在不到3秒內的邊緣決策API決策中使用。 [了解更多](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)