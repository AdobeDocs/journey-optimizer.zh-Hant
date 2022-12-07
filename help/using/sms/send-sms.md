---
solution: Journey Optimizer
product: journey optimizer
title: 預覽您的SMS訊息
description: 了解如何在Journey Optimizer中預覽和測試您的SMS訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 6%

---

# 傳送您的SMS訊息 {#send-sms}

## 預覽您的SMS訊息 {#preview-sms}

定義訊息內容後，您就可以使用測試設定檔來預覽和測試。 如果您插入個人化內容，則可以利用測試設定檔資料，檢查訊息中此內容的顯示方式。

1. 按一下 **[!UICONTROL 模擬內容]**.

1. 按一下 **[!UICONTROL 管理測試設定檔]** 新增測試設定檔。

1. 使用 **[!UICONTROL 身分命名空間]** 和 **[!UICONTROL 身分值]** 欄位。 然後，按一下 **[!UICONTROL 新增設定檔]**.

   ![](assets/sms_preview_3.png)

1. 選取測試設定檔後，您可以關閉 **[!UICONTROL 新增測試設定檔]** 窗口。

   ![](assets/sms_preview_1.png)

1. 在「預覽與測試」視窗中，測試設定檔資料會運用在訊息內容中。

   例如，對於此SMS訊息，兩個訊息內容都會個人化：

   ![](assets/sms_preview_2.png)

## 驗證您的簡訊{#sms-preview}

>[!NOTE]
>
> 為了獲得更好的傳遞能力，您應始終使用提供商支援的格式的電話號碼。 例如， Twilio和Sinch僅支援E.164格式的電話號碼。

您也必須檢查編輯器上方區段的警報。  其中有些是簡單警告，但有些警告可能會阻止您使用訊息。 可能會發生兩種警報：

* **警告** 請參閱建議和最佳實務。 例如，如果您的SMS訊息空白，則會顯示訊息。

* **錯誤** 只要未解決歷程，就無法進行測試或啟動歷程。 例如，訊息會警告您主題行已遺失。

![](assets/sms-alert-button.png)

當您的SMS訊息準備就緒時，請完成 [歷程](../building-journeys/journey-gs.md) 或 [行銷活動](../campaigns/create-campaign.md) 來發送。

**相關主題**

* [設定簡訊頻道](sms-configuration.md)
* [簡訊報告](../reports/journey-global-report.md#sms-global)
* [建立 SMS 訊息](create-sms.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
