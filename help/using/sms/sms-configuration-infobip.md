---
solution: Journey Optimizer
product: journey optimizer
title: 設定 Infobip 提供者
description: 瞭解如何使用Journey Optimizer和Infobip設定您的環境以傳送簡訊和多媒體簡訊
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 794ac45177e467be4bd5b8f7288e07c85e4d806a
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 5%

---

# 設定 Infobip 提供者 {#sms-configuration-infobip}

若要使用Journey Optimizer設定Infobip，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 管道]**&#x200B;並選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表。 按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

1. 設定您的API認證，如下所述。

   * **[!UICONTROL SMS供應商]**： Infobip。

   * **[!UICONTROL 名稱]**：為您的API認證選擇一個名稱。

   * **[!UICONTROL API基底URL]**&#x200B;和&#x200B;**[!UICONTROL API金鑰]**：存取您的網頁介面首頁或API金鑰管理頁面以尋找您的認證。 深入瞭解[Infobip檔案](https://www.infobip.com/docs/api){target="_blank"}。

   * **[!UICONTROL 選擇加入關鍵字]**：輸入將會自動觸發您&#x200B;**[!UICONTROL 選擇加入訊息]**&#x200B;的預設或自訂關鍵字。 對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 選擇加入訊息]**：輸入自訂回應，此回應會自動傳送為您的&#x200B;**[!UICONTROL 選擇加入訊息]**。

   * **[!UICONTROL 選擇退出關鍵字]**：輸入將會自動觸發您&#x200B;**[!UICONTROL 選擇退出訊息]**&#x200B;的預設或關鍵字。 對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 選擇退出訊息]**：輸入自訂回應，此回應會自動傳送為您的&#x200B;**[!UICONTROL 選擇退出訊息]**。

   * **[!UICONTROL 說明關鍵字]**：輸入將會自動觸發您&#x200B;**說明訊息**&#x200B;的預設或自訂關鍵字。 對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 說明訊息]**：輸入自動傳送為您&#x200B;**說明訊息**&#x200B;的自訂回應。

   * **[!UICONTROL 雙重加入關鍵字]**：輸入觸發雙重加入程式的關鍵字。 如果使用者設定檔不存在，則會在成功確認時加以建立。對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 雙重選擇加入訊息]**：輸入自動傳送以回應雙重選擇加入確認的自訂回應。

   * **[!UICONTROL 主要實體識別碼]**：輸入您指派的DLT主要實體識別碼。

   * **[!UICONTROL 內容範本識別碼]**：輸入您註冊的DLT內容範本識別碼。

   * **[!UICONTROL 有效期間]**：輸入訊息有效期間（小時）。 如果在此時間範圍內無法傳遞訊息，系統會再次嘗試重新傳送訊息。 預設有效期設定為48小時。

   * **[!UICONTROL 回撥資料]**：輸入將在通知URL上傳送的其他使用者端資料。

   * **[!UICONTROL 傳入號碼]**：新增您的不重複傳入號碼。 這可讓您在不同的沙箱中使用相同的API認證，每個沙箱都有自己的傳入號碼。

1. 完成API認證的設定時，請按一下&#x200B;**[!UICONTROL 提交]**。

建立和設定API認證後，您現在需要建立SMS和MMS訊息的頻道介面。 [了解更多](sms-configuration-surface.md)
