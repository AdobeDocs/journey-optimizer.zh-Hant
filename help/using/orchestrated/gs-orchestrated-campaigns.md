---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用協調行銷活動
description: 了解如何開始使用協調行銷活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 15f5fdfde0e9f7c93739a624918838dbd6787833
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 19%

---

# 開始使用協調行銷活動 {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="協調的行銷活動"
>abstract="**行銷活動策劃**<br/>&#x200B;分割、合併、擴充及操控關聯式資料集以定義您的對象<br/><br/>

**運用多實體資料**<br/>&#x200B;瞭解協調的行銷活動如何運用關聯式資料集豐富資料以進行細分和個人化&#x200B;<br/><br/>**臨機細分和精確計數**<br/>&#x200B;使用精確計數逐步建立您的區段&#x200B;<br/><br/>**可用管道**<br/>&#x200B;電子郵件、簡訊、推播通知、直接郵件」

+++ 目錄

| 歡迎使用協調行銷活動 | 首次投放的協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| <b>[開始使用協調的行銷活動](gs-orchestrated-campaigns.md)</b><br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](gs-schemas.md)</li><li>[手動結構描述](manual-schema.md)</li><li>[檔案上傳結構描述](file-upload-schema.md)</li><li>[擷取資料](ingest-data.md)</li></ul>[存取及管理協調的行銷活動](access-manage-orchestrated-campaigns.md)<br/><br/>[建立協調行銷活動的重要步驟](gs-campaign-creation.md) | [建立並排程行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[同時加入](activities/and-join.md) - [建立客群](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [頻道活動](activities/channels.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調和](activities/reconciliation.md) - [儲存客群](activities/save-audience.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer]中的行銷活動協調流程可跨管道支援複雜且品牌啟動的行銷活動，協助您大規模提高參與度、收入和客戶忠誠度。

雖然跨頻道行銷至關重要，但精心安排的行銷活動可讓其順暢無礙。 透過視覺化的拖放介面，您可以跨多個管道設計和自動化複雜的行銷工作流程，從細分到訊息傳遞。 所有事情都在一個直覺式環境中進行，專為速度、控制能力和效率而打造。

![](assets/canvas-example-diagram.png){zoomable="yes"}

## 核心功能

Campaign協調流程圍繞四大支柱建立：

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="隨選受眾" src="assets/do-not-localize/icon-audience.svg" width="50px"></a></td><td><b>隨選受眾</b><br/>立即跨資料集查詢，以使用任何資料型別和維度的組合來建立受眾區段。</td></tr>
<tr style="border: 0;">
<td><img alt="多實體細分和傳送" src="assets/do-not-localize/icon-entity.svg" width="50px"></a></td><td><b>多實體區段和傳送</b><br/>超越以人員為基礎的行銷活動 — 精準使用產品目錄、商店位置或服務資料等實體來鎖定目標。</td></tr>
<tr style="border: 0;">
<td><img alt="預先傳送的可見度和精確度" src="assets/do-not-localize/icon-visibility.svg" width="50px"></a></td><td><b>預先傳送可見度和精確度</b><br/>在啟動前取得精確的分段計數和完整的行銷活動範圍，以確保精確度和可信度。</td></tr>
<tr style="border: 0;">
<td><img alt="多步驟行銷活動工作流程" src="assets/do-not-localize/icon-multistep.svg" width="50px"></a></td><td><b>多步驟行銷活動工作流程</b><br/>設計多步驟行銷活動，從每日訊息到複雜的行銷活動，例如季節性促銷活動或主要產品上市。</td></tr>
</table>

## 協調的行銷活動和歷程

即使協調的行銷活動視覺效果與歷程類似，但可解決不同用途和使用案例：

* **歷程** - 1到1個畫布，每個設定檔以自己的步調在不同步驟中行進。 每個客戶的狀態會保留在其內容中，以觸發即時動作。

* **協調的行銷活動** — 不同於歷程，協調的行銷活動使用計算區段的批次畫布來運作。 所有設定檔都會同時處理。

## 先決條件

使用協調的行銷活動前，請務必確保您擁有適當的許可權。 協調行銷活動的存取權僅限指派給相關&#x200B;**[!UICONTROL 產品設定檔]**&#x200B;的使用者，例如協調行銷活動管理員、協調行銷活動核准者、協調行銷活動管理員或協調行銷活動檢視者。

如果您無法存取協調的行銷活動功能，請聯絡您的管理員以請求必要的許可權。

➡️ [進一步瞭解與協調行銷活動相關的產品設定檔](../administration/ootb-product-profiles.md)

## 讓我們深入探討

現在您已瞭解哪些是精心安排的行銷活動，是時候更深入地研究這些檔案區段以開始使用此功能了。

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="存取並管理工作流程" src="assets/do-not-localize/workflow-access.jpeg">
</a>
<div>
<a href="gs-campaign-creation.md"><strong>設定步驟</strong></a>
</div>
<p>
</td>
<td>
<a href="create-orchestrated-campaign.md">
<img alt="銷售機會" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-orchestrated-campaign.md"><strong>建立協調行銷活動</strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="不頻繁" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>使用活動</strong></a>
</div>
<p></td>
</tr></table>
