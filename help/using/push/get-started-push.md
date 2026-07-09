---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用推播通知
description: 了解如何在 Journey Optimizer 建立推播通知
feature: Overview, Push
topic: Content Management
role: User
level: Beginner
exl-id: c1f16edd-efdf-41c2-a0ad-5f55009008f5
TQID: https://experienceleague.adobe.com/S-3ZtTNfgZGEFChfjaXPihxGWpdkWacrWF9AWc-AyZY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 651
ht-degree: 57%

---

# 開始使用推播通知 {#gs-push-notification}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;開始使用 Adobe Journey Optimizer 中的推播通知，透過歷程和行銷活動觸及您的行動應用程式使用者和網頁訪客。

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>如果這是您第一次建立推播通知，請確定已設定推播通道。 [了解更多](push-gs.md)。

推播通知可協助您隨時聯絡行動應用程式使用者，尤其是當使用者目前未使用您的應用程式或瀏覽您的網站時。 推播通知可協助您達成各種使用案例，例如提供服務的更新、要求使用者採取動作、提醒使用者留意新交易等。裝置平台要求選擇加入，一般使用者才能接收或檢視您的通知。 使用者選擇加入的時間，最早可在應用程式於安裝後首次啟動後收到，或在後續的工作階段或工作流程收到。

[!DNL Journey Optimizer] 支援推播通知，並協助您以領先業界的輸送率傳送高度相關的通知。 推播通知可能包括個人化和歷程型內容，以利用您的品牌對[!DNL Adobe CX Enterprise]的資料深入分析。

可建立的推播通知：

* 在&#x200B;**歷程**&#x200B;中：一旦在歷程新增推播活動並定義基本設定後，使用&#x200B;**[!UICONTROL 動作：推播]**&#x200B;右側窗格，建立推播通知的內容。 [了解如何建立歷程](../building-journeys/journey-gs.md)

* 在&#x200B;**行銷活動**&#x200B;中：一旦建立行銷活動，請選取「推播通知」作為動作並定義基本設定。 了解如何建立[動作行銷活動](../campaigns/campaign-action.md#action-campaign-action) | [API 觸發的行銷活動](../campaigns/api-triggered-campaigns.md) | [協調的行銷活動](../orchestrated/create-orchestrated-campaign.md#create)

使用專用索引標籤定義 **iOS**、**Android** 及&#x200B;**網頁**&#x200B;平台的推播通知設定。

>[!NOTE]
>
>**[!DNL Journey Optimizer]** 提供管理電子郵件和簡訊訊息中選擇退出的方式，而推播通知不需要由您執行任何動作，因為收件者可以透過其裝置自行取消訂閱。 例如，在下載或使用您的應用程式時，他們可以選擇停止通知。 同樣地，他們也可以透過行動裝置作業系統或網頁瀏覽器設定變更通知設定。 若要在 AEP 輪廓檢視器中驗證輪廓的推播同意狀態，請參閱[檢查推播選擇退出狀態](../privacy/opt-out.md#push-opt-out-status)。

</br>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-push.md">
<img alt="銷售機會" src="../assets/do-not-localize/push-create.jpg">
</a>
<div><a href="create-push.md"><strong>建立推播通知</strong>
</div>
<p>
</td>
<td>
<a href="design-push.md">
<img alt="不頻繁" src="../assets/do-not-localize/push-design.jpg">
</a>
<div>
<a href="design-push.md"><strong>設計推播通知</strong></a>
</div>
<p></td>
<td>
<a href="send-push.md">
<img alt="驗證" src="../assets/do-not-localize/push-sending.jpg">
</a>
<div>
<a href="send-push.md"><strong>傳送推播通知</strong></a>
</div>
<p>
</td>
<td>
<a href="push-gs.md">
<img alt="驗證" src="../assets/do-not-localize/push-config.jpg">
</a>
<div>
<a href="push-gs.md"><strong>設定推播通知</strong></a>
</div>
<p>
</td>
</tr></table>

## 使用案例

當您需要快速並直接在他們的裝置上聯絡使用者時，推送通知的運作會最佳化，無需讓他們進入您的應用程式或檢查其收件匣。

| 優點 | 原因 | 範例使用案例 |
| --- | --- | --- |
| 時效性更新 | 即刻傳遞，即使使用者未主動使用您的應用程式 | 航班延遲警報、訂單狀態變更、突發新聞 |
| 重新參與 | 在一段閒置時間後提示使用者返回您的應用程式 | 購物車放棄提醒、回饋行銷活動 |
| 相較於簡訊的成本降低 | 不像SMS收取每則訊息的電信業者費用 | 大量促銷或交易式通知 |
| 豐富互動式內容 | 支援影像、動作按鈕和深層連結 | 具有點選以購買按鈕的產品促銷活動，多媒體預覽 |
| 裝置原生功能 | 運用其他管道無法使用的作業系統層級功能 | 震動警報、應用程式圖示徽章、地理圍欄位置觸發器 |
| 高選擇加入可能性 | 系統會在應用程式安裝或首次啟動時，提示使用者選擇加入 | 入門流程、第一天參與行銷活動 |

## 何時不使用

推播通知不適合每則訊息。 在下列情況下考慮另一個管道：

* 您的對象推送選擇加入率低或顯示拒絕通知，因為訊息可能永遠無法送達
* 訊息需要長格式內容，電子郵件可處理得更好，並允許更詳細的格式設定
* 內容為敏感或私密內容，且不應在鎖定熒幕上顯示，讓裝置附近的任何人都能看見
* 您的大部分使用者會從案頭存取您的服務，而非在推播通知觸及受限或無觸及範圍的行動應用程式中

