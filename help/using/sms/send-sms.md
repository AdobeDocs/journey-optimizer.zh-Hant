---
solution: Journey Optimizer
product: journey optimizer
title: 預覽並測試您的SMS訊息
description: 了解如何在Journey Optimizer中預覽和測試您的SMS訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 6%

---

# 預覽並測試您的SMS訊息 {#send-sms}

## 預覽您的SMS {#preview-sms}

定義訊息內容後，您就可以使用測試設定檔來預覽和測試。 如果您插入個人化內容，則可使用測試設定檔資料，檢查此內容在訊息中的顯示方式。

1. 按一下 **[!UICONTROL 模擬內容]**.

1. 按一下 **[!UICONTROL 管理測試設定檔]** 新增測試設定檔。

1. 使用 **[!UICONTROL 身分命名空間]** 和 **[!UICONTROL 身分值]** 欄位。 然後，按一下 **[!UICONTROL 新增設定檔]**.

   ![](assets/sms_preview_3.png)

1. 選取測試設定檔後，您可以關閉 **[!UICONTROL 新增測試設定檔]** 窗口。

1. 從 **預覽和測試** 視窗中，測試設定檔資料會新增至訊息內容。

   ![](assets/sms_preview_2.png)


## 驗證您的簡訊{#sms-validate}

您必須檢查編輯器上方區段的警報。 其中有些只是簡單的警告，但有些警告可能會阻止您傳送訊息。 可能會發生兩種警報：警告和錯誤。

* **警告** 請參閱建議和最佳實務。 例如，如果您的SMS訊息空白，則會顯示警告訊息。

* **錯誤** 只要行銷活動未解決，就無法測試或啟動歷程，也無法發佈行銷活動。 例如，當主題行遺失時，錯誤訊息會警告您。

![](assets/sms-alert-button.png)

>[!NOTE]
>
> 若要改善傳遞能力，請使用提供者支援的格式電話號碼。 例如， Twilio和Sinch僅支援E.164格式的電話號碼。

## 傳送您的簡訊{#sms-send}

當您的SMS訊息準備就緒時，請完成 [歷程](../building-journeys/journey-gs.md) 或 [行銷活動](../campaigns/create-campaign.md) 來發送。

**相關主題**

* [設定簡訊頻道](sms-configuration.md)
* [簡訊報告](../reports/journey-global-report.md#sms-global)
* [建立簡訊訊息](create-sms.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
