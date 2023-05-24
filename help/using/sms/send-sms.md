---
solution: Journey Optimizer
product: journey optimizer
title: 預覽和testSMS消息
description: 瞭解如何在Journey Optimizer預覽和testSMS消息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 12%

---

# 預覽和testSMS消息 {#send-sms}

## 預覽您的SMS {#preview-sms}

定義訊息內容後，您就可以使用測試設定檔進行預覽及測試。 如果插入了個性化內容，則可以使用test配置檔案資料檢查此內容在消息中的顯示方式。

1. 按一下 **[!UICONTROL 模擬內容]**。

1. 按一下 **[!UICONTROL 管理test配置檔案]** 添加test配置檔案。

1. 查找您的test配置檔案 **[!UICONTROL 標識命名空間]** 和 **[!UICONTROL 標識值]** 的子菜單。 然後，按一下 **[!UICONTROL 添加配置檔案]**。

   ![](assets/sms_preview_3.png)

1. 選擇test配置檔案後，可以關閉 **[!UICONTROL 添加test配置檔案]** 的子菜單。

1. 從 **預覽和test** 窗口，test配置檔案資料將添加到消息內容。

   ![](assets/sms_preview_2.png)


## 驗證您的SMS{#sms-validate}

必須在編輯器的上部檢查警報。 其中有些是簡單的警告，但有些則會阻止您發送消息。 可以發生兩種類型的警報：警告和錯誤。

* **警告** 請參閱建議和最佳做法。 例如，如果SMS消息為空，則會顯示警告消息。

* **錯誤** 只要未解決，就不能測試或激活行程，或發佈活動。 例如，當主題行丟失時，會出現一條錯誤消息警告您。

![](assets/sms-alert-button.png)

>[!NOTE]
>
> 要提高傳送能力，請使用提供商支援的格式的電話號碼。 例如， Twilio和Sinch僅支援E.164格式的電話號碼。

## 發送您的SMS{#sms-send}

當您的SMS消息準備就緒時，請完成您的 [旅程](../building-journeys/journey-gs.md) 或 [活動](../campaigns/create-campaign.md) 寄出去。

**相關主題**

* [設定簡訊頻道](sms-configuration.md)
* [簡訊報告](../reports/journey-global-report.md#sms-global)
* [建立簡訊訊息](create-sms.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
