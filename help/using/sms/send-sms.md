---
solution: Journey Optimizer
product: journey optimizer
title: 檢查並測試您的SMS訊息
description: 瞭解如何在Journey Optimizer中檢查並傳送簡訊
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 6%

---

# 檢查並傳送簡訊 {#send-sms}

## 預覽簡訊 {#preview-sms}

定義訊息內容後，您就可以使用測試設定檔來預覽其內容。 如果您已插入個人化內容，您可以使用測試設定檔資料檢查此內容在訊息中的顯示方式。

若要這麼做，請按一下 **[!UICONTROL 模擬內容]** 然後新增測試設定檔，以使用測試設定檔資料檢查您的訊息。

![](assets/sms_preview_2.png)

有關如何選取測試設定檔及預覽內容的詳細資訊，請參閱 [內容管理](../content-management/preview-test.md) 區段。

## 驗證簡訊{#sms-validate}

您必須檢查編輯器上半區段的警示。 其中一些是簡單的警告，但其他警告可能會阻止您傳送訊息。 可能會發生兩種型別的警報：警告和錯誤。

* **警告** 請參閱建議和最佳實務。 例如，如果SMS訊息為空，則會顯示警告訊息。

* **錯誤** 阻止您測試或啟動歷程，或發佈行銷活動（只要它們未解決）。 例如，當主旨行遺失時，錯誤訊息會警告您。

![](assets/sms-alert-button.png)

>[!NOTE]
>
> 若要改善您的傳遞能力，請以提供者支援的格式使用電話號碼。 例如，Twilio和Sinch只支援E.164格式的電話號碼。

## 傳送簡訊{#sms-send}

當您的SMS訊息準備就緒時，請完成您的 [歷程](../building-journeys/journey-gs.md) 或 [行銷活動](../campaigns/create-campaign.md) 以傳送。

**相關主題**

* [設定簡訊頻道](sms-configuration.md)
* [簡訊報告](../reports/journey-global-report.md#sms-global)
* [建立簡訊訊息](create-sms.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
