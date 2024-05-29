---
solution: Journey Optimizer
product: journey optimizer
title: 設定 Twilio 提供者
description: 瞭解如何使用Twilio設定您的環境以使用Journey Optimizer傳送文字訊息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 8f045e1b709c0059ce21cda68c21e8732f58e51e
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---

# 設定 Twilio 提供者 {#sms-configuration-twilio}

若要使用Journey Optimizer設定Twilio，您需要建立用於Twilio的新API認證：

1. 在左側邊欄中，瀏覽至 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 並選取 **[!UICONTROL API認證]** 功能表。 按一下 **[!UICONTROL 建立新的API認證]** 按鈕。

1. 設定您的SMS API認證，如下所述：

   * **[!UICONTROL 簡訊供應商]**： Twilio。

   * **[!UICONTROL 名稱]**：為您的API認證選擇名稱。

   * **[!UICONTROL 帳戶SID]** 和 **[!UICONTROL 驗證權杖]**：存取 **帳戶資訊** [Twilio主控台儀表板]頁面的窗格，以尋找您的認證。

   * **[!UICONTROL 訊息SID]**：輸入指派給Twilio API所建立每則訊息的唯一識別碼。 進一步瞭解 [Twilio檔案](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

1. 按一下 **[!UICONTROL 提交]** 完成API認證的設定時。

建立和設定API認證後，您現在需要建立SMS和MMS訊息的頻道介面。 [了解更多](sms-configuration-surface.md)
