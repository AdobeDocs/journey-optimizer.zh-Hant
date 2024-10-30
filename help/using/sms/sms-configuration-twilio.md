---
solution: Journey Optimizer
product: journey optimizer
title: 設定 Twilio 提供者
description: 瞭解如何使用Twilio設定您的環境以使用Journey Optimizer傳送文字訊息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: c9a35c2950c061318f673cdd53d0a5fd08063c27
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%

---

# 設定 Twilio 提供者 {#sms-configuration-twilio}

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

建立和設定API認證後，您現在需要建立SMS和MMS訊息的通道設定。 [了解更多](sms-configuration-surface.md)
