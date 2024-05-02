---
solution: Journey Optimizer
product: journey optimizer
title: 設定Infobip提供者
description: 瞭解如何使用Journey Optimizer和Infobip設定您的環境以傳送簡訊和多媒體簡訊
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 4%

---

# 設定Infobip提供者 {#sms-configuration-infobip}

若要使用Journey Optimizer設定Infobip，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至 **[!UICONTROL 管理]** `>` **[!UICONTROL 頻道]** 並選取 **[!UICONTROL API認證]** 功能表。 按一下 **[!UICONTROL 建立新的API認證]** 按鈕。

   ![](assets/sms_6.png)

1. 設定您的API認證，如下所述。

   * **[!UICONTROL 名稱]**：為您的API認證選擇名稱。

   * **[!UICONTROL API基底URL]** 和 **[!UICONTROL API金鑰]**：存取您的網頁介面首頁或API金鑰管理頁面以尋找您的認證。 進一步瞭解 [Infobip檔案](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL 選擇加入關鍵字]**：輸入將會自動觸發的預設或自訂關鍵字 **[!UICONTROL 選擇加入訊息]**. 對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 選擇加入訊息]**：輸入自訂回應，此回應會作為 **[!UICONTROL 選擇加入訊息]**.

   * **[!UICONTROL 選擇退出關鍵字]**：輸入將會自動觸發的預設或關鍵字 **[!UICONTROL 選擇退出訊息]**. 對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 選擇退出訊息]**：輸入自訂回應，此回應會作為 **[!UICONTROL 選擇退出訊息]**.

   * **[!UICONTROL 說明關鍵字]**：輸入將會自動觸發的預設或自訂關鍵字 **說明訊息**. 對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 說明訊息]**：輸入自訂回應，此回應會作為 **說明訊息**.

   * **[!UICONTROL 雙重選擇加入關鍵字]**：輸入觸發雙重加入流程的關鍵字。 如果使用者設定檔不存在，則會在成功確認時加以建立。對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 雙重選擇加入訊息]**：輸入自動傳送以回應雙重選擇加入確認的自訂回應。

   * **[!UICONTROL 主體實體ID]**：輸入您指派的DLT主要實體識別碼。

   * **[!UICONTROL 內容範本ID]**：輸入您註冊的DLT內容範本ID。

   * **[!UICONTROL 有效期]**：輸入訊息有效期（小時）。 如果在此時間範圍內無法傳遞訊息，系統會再次嘗試重新傳送訊息。 預設有效期設定為48小時。

   * **[!UICONTROL 回呼資料]**：輸入要在通知URL上傳送的其他使用者端資料。

1. 按一下 **[!UICONTROL 提交]** 完成API認證的設定時。

建立和設定API認證後，您現在需要建立SMS和MMS訊息的頻道介面。 [了解更多](sms-configuration-surface.md)
