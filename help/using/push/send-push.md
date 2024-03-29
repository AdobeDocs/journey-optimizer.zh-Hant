---
solution: Journey Optimizer
product: journey optimizer
title: 檢查並傳送推播通知
description: 瞭解如何在Journey Optimizer中檢查並傳送推播通知
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 7%

---

# 檢查並傳送推播通知 {#send-push}

## 預覽推播通知 {#preview-push}

定義訊息內容後，您就可以使用測試設定檔來預覽其內容。 如果您已插入個人化內容，您可以使用測試設定檔資料檢查此內容在訊息中的顯示方式。

若要這麼做，請按一下 **[!UICONTROL 模擬內容]** 然後新增測試設定檔。 然後，您可以選取要預覽內容的裝置型別： **[!UICONTROL iOS]** 或 **[!UICONTROL Android]**.

![](assets/push_preview_3.png)

有關如何選取測試設定檔及預覽內容的詳細資訊，請參閱 [內容管理](../content-management/preview-test.md) 區段。

## 驗證推播通知 {#push-validate}

您必須檢查編輯器上半區段的警示。 其中一些是簡單的警告，但其他警告可能會阻止您傳送訊息。 可能會發生兩種型別的警報：警告和錯誤。

* **警告** 請參閱建議和最佳實務。

* **錯誤** 防止您測試或啟動歷程，只要它們未解決，例如：

   * **[!UICONTROL 訊息的推播版本為空白]**：當遺失推播通知本文或標題時，就會顯示此錯誤。 瞭解如何在中定義推播通知內容 [本節](create-push.md).

   * **[!UICONTROL 表面不存在]**：如果您選取的表面在訊息建立後即被刪除，則無法使用訊息。 如果發生此錯誤，請在訊息中選取另一個曲面 **[!UICONTROL 屬性]**. 瞭解更多有關管道表面的 [本節](../configuration/channel-surfaces.md).

   * **[!UICONTROL 推播iOS/Android承載已超過4KB的限制]**：推播通知大小不得超過4KB。 為遵守此限制，請嘗試減少使用影像或表情符號。 瞭解如何在中管理您的推播通知內容 [本節](../push/create-push.md).

  ![](assets/push_alert.png)


>[!NOTE]
>
> 為了提供更好的傳遞能力，您應該一律使用提供者支援格式的電話號碼。 例如，Twilio和Sinch只支援E.164格式的電話號碼。

## 傳送推播通知{#push-send}

當您的推送訊息就緒時，請完成設定 [歷程](../building-journeys/journey-gs.md) 或 [行銷活動](../campaigns/create-campaign.md) 以傳送。

**相關主題**

* [設定推播頻道](push-configuration.md)
* [推播通知報告](../reports/journey-global-report.md#push-global)
* [建立推播通知](create-push.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
* [在行銷活動中新增訊息](../campaigns/create-campaign.md)

