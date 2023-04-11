---
solution: Journey Optimizer
product: journey optimizer
title: 預覽並測試推播通知
description: 了解如何在Journey Optimizer中預覽和測試您的推播通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 9%

---

# 預覽並測試推播通知 {#send-push}

## 預覽推播通知 {#preview-push}

定義訊息內容後，您就可以使用測試設定檔進行預覽及測試。 如果您插入個人化內容，則可使用測試設定檔資料，檢查此內容在訊息中的顯示方式。

1. 按一下 **[!UICONTROL 模擬內容]**.

1. 按一下 **[!UICONTROL 管理測試設定檔]** 新增測試設定檔。

1. 使用 **[!UICONTROL 身分命名空間]** 和 **[!UICONTROL 身分值]** 欄位。 然後，按一下 **[!UICONTROL 新增設定檔]**.

   ![](assets/push_preview_1.png)

1. 選取測試設定檔後，您可以關閉 **[!UICONTROL 新增測試設定檔]** 窗口。

1. 從 **預覽和測試** 視窗中，測試設定檔資料會新增至訊息內容。

   選取要預覽內容的裝置類型： **[!UICONTROL iOS]** 或 **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## 驗證推播通知 {#push-validate}


您必須檢查編輯器上方區段的警報。 其中有些只是簡單的警告，但有些警告可能會阻止您傳送訊息。 可能會發生兩種警報：警告和錯誤。

* **警告** 請參閱建議和最佳實務。

* **錯誤** 只要未解決歷程，就會阻止您測試或啟動歷程，例如：

   * **[!UICONTROL 訊息的推送版本為空]**:遺失推播通知內文或標題時，會顯示此錯誤。 了解如何在中定義推播通知內容 [本節](create-push.md).

   * **[!UICONTROL 曲面不存在]**:如果在建立消息後刪除了所選曲面，則無法使用消息。 如果發生此錯誤，請在消息中選取另一個曲面 **[!UICONTROL 屬性]**. 進一步了解 [本節](../configuration/channel-surfaces.md).

   * **[!UICONTROL 推播iOS/Android裝載已超過4KB的限制]**:推播通知大小不能超過4KB。 若要遵守此限制，請嘗試減少使用影像或表情符號。 了解如何在 [本節](../push/create-push.md).

   ![](assets/push_alert.png)


>[!NOTE]
>
> 為了獲得更好的傳遞能力，您應始終使用提供商支援的格式的電話號碼。 例如， Twilio和Sinch僅支援E.164格式的電話號碼。

## 傳送推播通知{#push-send}

推送訊息準備就緒時，請完成 [歷程](../building-journeys/journey-gs.md) 或 [行銷活動](../campaigns/create-campaign.md) 來發送。

**相關主題**

* [設定推播通道](push-configuration.md)
* [推播通知報告](../reports/journey-global-report.md#push-global)
* [建立推播通知](create-push.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
* [在促銷活動中新增訊息](../campaigns/create-campaign.md)

