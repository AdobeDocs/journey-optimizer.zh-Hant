---
solution: Journey Optimizer
product: journey optimizer
title: 檢查並測試您的文字訊息
description: 瞭解如何在Journey Optimizer中檢查並傳送簡訊
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 7b1be144776fd11cd4aa90aa315eee60b1acc40f
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 3%

---

# 檢查並傳送您的簡訊（簡訊/多媒體簡訊）{#send-sms}

## 預覽您的文字訊息 {#preview-sms}

定義訊息內容後，您可以使用測試設定檔或範例輸入資料（從CSV/JSON檔案上傳或手動新增）來預覽其內容。 如果您已插入個人化內容，您可以檢查此內容在訊息中的顯示方式。

若要這麼做，請按一下&#x200B;**[!UICONTROL 模擬內容]**，然後使用測試設定檔資料檢查您的訊息。

![](assets/sms_preview_2.png)

有關如何預覽及測試內容的詳細資訊，請參閱[內容管理](../content-management/preview-test.md)區段。

## 驗證您的內容 {#sms-validate}

您必須檢查編輯器上半區段的警示。 其中一些是簡單的警告，但其他警告可能會阻止您傳送訊息。 可能會發生兩種型別的警報：警告和錯誤。

![](assets/sms-alert-button.png)

* **警告**&#x200B;參考建議和最佳實務。 例如，如果您的文字訊息為空白，則會顯示警告訊息。

* **錯誤**&#x200B;會阻止您測試或啟動歷程，或發佈行銷活動，只要這些錯誤未解決。 例如，當主旨行遺失時，錯誤訊息會警告您。


>[!NOTE]
>
> 若要改善您的傳遞能力，請以提供者支援的格式使用電話號碼。 例如，Twilio和Sinch只支援E.164格式的電話號碼。

## 傳送您的簡訊 {#sms-send}

>[!IMPORTANT]
>
> 如果您的行銷活動受核准政策的約束，您將需要請求核准才能傳送您的文字訊息。 [了解更多](../test-approve/gs-approval.md)

當您的文字訊息準備就緒時，請完成[歷程](../building-journeys/journey-gs.md)或[行銷活動](../campaigns/create-campaign.md)的設定以傳送。

**相關主題**

* [設定簡訊頻道](sms-configuration.md)
* [簡訊/多媒體簡訊報告](../reports/journey-global-report-cja-sms.md)
* [建立文字訊息。](create-sms.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
