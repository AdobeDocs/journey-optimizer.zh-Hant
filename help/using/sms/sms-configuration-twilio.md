---
solution: Journey Optimizer
product: journey optimizer
title: 設定 Twilio 提供者
description: 瞭解如何使用Twilio設定您的環境以使用Journey Optimizer傳送文字訊息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 2%

---

# 設定 Twilio 提供者 {#sms-configuration-twilio}

## 設定SMS/MMS的API認證

若要使用Journey Optimizer設定Twilio，您需要建立用於Twilio的新API認證：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** `>` **[!UICONTROL SMS設定]**&#x200B;並選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表。 按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

1. 設定您的SMS API認證，如下所述：

   * **[!UICONTROL SMS供應商]**： Twilio。

   * **[!UICONTROL 名稱]**：為您的API認證選擇一個名稱。

   * **[!UICONTROL 帳戶SID]**&#x200B;和&#x200B;**[!UICONTROL 驗證權杖]**：存取您Twilio主控台儀表板頁面的&#x200B;**帳戶資訊**&#x200B;窗格，以尋找您的認證。

   * **[!UICONTROL 訊息SID]**：輸入指派給Twilio API所建立之每封訊息的唯一識別碼。 深入瞭解[Twilio檔案](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}。

   * **[!UICONTROL 傳入號碼]**：新增您的不重複傳入號碼。 這可讓您在不同的沙箱中使用相同的API認證，每個沙箱都有自己的傳入號碼。

1. 完成API認證的設定時，請按一下&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API認證]**&#x200B;功能表中，按一下bin圖示以刪除您的API認證。

1. 若要修改現有認證，請找到所需的API認證，然後按一下&#x200B;**[!UICONTROL 編輯]**&#x200B;選項以進行必要的變更。

1. 從您現有的API認證按一下&#x200B;**[!UICONTROL 驗證SMS連線]**，透過傳送範例訊息至指定裝置來測試及驗證SMS API認證。

1. 填寫&#x200B;**數字**&#x200B;和&#x200B;**訊息**&#x200B;欄位，然後按一下&#x200B;**[!UICONTROL 驗證連線]**。

   >[!IMPORTANT]
   >
   >訊息的結構必須符合提供者的裝載格式。

   ![](assets/verify-connection.png)

建立和設定API認證後，您現在需要建立SMS和MMS訊息的通道設定。 [了解更多](sms-configuration-surface.md)

## 設定RCS的API認證

Adobe Journey Optimizer使用[自訂SMS提供者](sms-configuration-custom.md)功能，透過Twilio支援RCS傳訊。 這可透過已驗證的企業設定檔傳送豐富的互動式訊息，並納入輪播、按鈕和多媒體內容等元素。

➡️ [在Twilio檔案中探索Twilio如何支援RCS](https://www.twilio.com/docs/rcs)

若要使用Twilio啟用RCS傳訊，必須透過自訂SMS提供者設定新的API認證。 現有的Twilio SMS認證不相容，因為RCS需要不同的裝載格式。

使用Twilio設定RCS：

1. **在Twilio註冊RCS傳訊**

   首先在Twilio平台中完成RCS註冊程式。 這包括設定您的企業設定檔，並為您的帳戶啟用RCS功能。

1. **建立SMS Webhook**

   [設定SMS Webhook](sms-configuration-custom.md#webhook)，以接收傳入的RCS訊息回應或傳遞更新。 此webhook必須正確連結至您的Twilio設定，才能進行雙向通訊。

1. **使用自訂作為SMS供應商建立API認證**

   在Journey Optimizer中，[使用「自訂」作為SMS供應商，專門為RCS定義新的API認證](sms-configuration-custom.md#api-credential)。 使用適當的RCS端點驗證方法、基本URL和標頭。

建立和設定API認證後，您現在需要為RCS訊息建立通道設定。 [了解更多](sms-configuration-surface.md)







