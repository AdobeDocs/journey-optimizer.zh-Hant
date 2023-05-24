---
solution: Journey Optimizer
product: journey optimizer
title: 預覽和test推送通知
description: 瞭解如何在Journey Optimizer預覽和test推送通知
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

# 預覽和test推送通知 {#send-push}

## 預覽推送通知 {#preview-push}

定義訊息內容後，您就可以使用測試設定檔進行預覽及測試。 如果插入了個性化內容，則可以使用test配置檔案資料檢查此內容在消息中的顯示方式。

1. 按一下 **[!UICONTROL 模擬內容]**。

1. 按一下 **[!UICONTROL 管理test配置檔案]** 添加test配置檔案。

1. 查找您的test配置檔案 **[!UICONTROL 標識命名空間]** 和 **[!UICONTROL 標識值]** 的子菜單。 然後，按一下 **[!UICONTROL 添加配置檔案]**。

   ![](assets/push_preview_1.png)

1. 選擇test配置檔案後，可以關閉 **[!UICONTROL 添加test配置檔案]** 的子菜單。

1. 從 **預覽和test** 窗口，test配置檔案資料將添加到消息內容。

   選擇要預覽內容的設備類型： **[!UICONTROL iOS]** 或 **[!UICONTROL 安卓]**。

   ![](assets/push_preview_3.png)

## 驗證推送通知 {#push-validate}


必須在編輯器的上部檢查警報。 其中有些是簡單的警告，但有些則會阻止您發送消息。 可以發生兩種類型的警報：警告和錯誤。

* **警告** 請參閱建議和最佳做法。

* **錯誤** 只要未解決，就阻止您測試或激活行程，例如：

   * **[!UICONTROL 消息的推送版本為空]**:當缺少推送通知正文或標題時，將顯示此錯誤。 瞭解如何在中定義推送通知內容 [此部分](create-push.md)。

   * **[!UICONTROL 曲面不存在]**:如果在建立消息後刪除了所選曲面，則不能使用消息。 如果出現此錯誤，請在消息中選擇另一個曲面 **[!UICONTROL 屬性]**。 瞭解有關中的通道曲面的詳細資訊 [此部分](../configuration/channel-surfaces.md)。

   * **[!UICONTROL 推送iOS/Android負載超過4KB的限制]**:推送通知大小不能超過4KB。 要尊重此限制，請嘗試減少使用影像或表情符號。 瞭解如何在中管理推送通知內容 [此部分](../push/create-push.md)。

   ![](assets/push_alert.png)


>[!NOTE]
>
> 為了獲得更好的交付能力，您應始終使用提供商支援的格式中的電話號碼。 例如， Twilio和Sinch僅支援E.164格式的電話號碼。

## 傳送推播通知{#push-send}

當您的推送消息就緒時，請完成您的 [旅程](../building-journeys/journey-gs.md) 或 [活動](../campaigns/create-campaign.md) 寄出去。

**相關主題**

* [配置推送通道](push-configuration.md)
* [推播通知報告](../reports/journey-global-report.md#push-global)
* [建立推播通知](create-push.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
* [在市場活動中添加消息](../campaigns/create-campaign.md)

