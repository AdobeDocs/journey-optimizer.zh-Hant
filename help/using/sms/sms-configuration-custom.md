---
solution: Journey Optimizer
product: journey optimizer
title: 設定您的自訂提供者
description: 瞭解如何設定環境，以透過自訂提供者使用Journey Optimizer傳送文字訊息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: af03ad62c2c7b29d695670f083e0dfb6d0c71b93
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 1%

---

# 設定自訂提供者(Beta) {#sms-configuration-custom}

>[!AVAILABILITY]
>
>自訂提供者目前僅供選定使用者使用，做為Beta版。 請洽詢您的Adobe代表，以便納入Beta。
>
>請注意，此Beta不支援選擇加入/選擇退出同意管理和傳遞報告的傳入訊息。

若要在Journey Optimizer中使用無法透過Adobe立即使用的自訂提供者（例如Sinch、Infobip、Twilio）傳送訊息，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]**&#x200B;並選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表。

1. 按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

   ![](assets/sms_byo_1.png)

1. 設定您的SMS API認證，如下所述：

   * **[!UICONTROL SMS供應商]**：自訂。

   * **[!UICONTROL 名稱]**：輸入您的API認證名稱。

   * **[!UICONTROL 提供者AppId]**：輸入您的SMS提供者提供的應用程式ID。

   * **[!UICONTROL 提供者名稱]**：輸入您的SMS提供者的名稱。

   * **[!UICONTROL 提供者URL]**：輸入簡訊提供者的URL。

   * **[!UICONTROL 驗證型別{&#x200B;1}：選取您的授權型別。]**&#x200B;支援的授權型別為&#x200B;**持有者應用程式**&#x200B;或&#x200B;**基本**。

   * **[!UICONTROL API Token]**：輸入您的SMS提供者提供的API Token。

   * **[!UICONTROL 提供者承載]**：新增您的提供者承載，例如`{"from": "+1234XXXXXX", "to": "+1374XXXXXX", "content": "This is a test message", "contentType": "TEXT"}`。

     確定承載包含`{{toNumber}}`、`{{fromNumber}}`、`{{message}}`。

1. 完成API認證的設定時，請按一下&#x200B;**[!UICONTROL 提交]**。

建立和設定API認證後，您現在需要建立SMS訊息的頻道介面。 [了解更多](sms-configuration-surface.md)

設定後，您就可以運用所有立即可用的頻道功能，例如訊息製作、個人化、連結追蹤和報告。

## 操作說明影片 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
