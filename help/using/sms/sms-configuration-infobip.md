---
solution: Journey Optimizer
product: journey optimizer
title: 設定 Infobip 提供者
description: 瞭解如何使用Journey Optimizer和Infobip設定您的環境以傳送簡訊和多媒體簡訊
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 2%

---

# 設定 Infobip 提供者 {#sms-configuration-infobip}

>[!BEGINSHADEBOX]

如果未提供選擇加入或選擇退出關鍵字，系統會使用標準同意訊息來尊重使用者隱私權。 新增自訂關鍵字會自動覆寫預設值。

**預設關鍵字：**

* **選擇加入**：訂閱，是，取消停止，開始，繼續，繼續，開始
* **選擇退出**：停止、結束、取消、結束、取消訂閱、否
* **說明**：說明

>[!ENDSHADEBOX]

## 設定簡訊的API認證

若要使用Journey Optimizer設定Infobip，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 管道]**&#x200B;並選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表。 按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

1. 設定您的SMS API認證，如下所述：

   +++ 設定的SMS認證清單

   | 設定欄位 | 說明 |
   |---|---|    
   | 簡訊供應商 | Infobip |
   | 名稱 | 選擇您的API認證名稱。 |
   | API基本URL和API金鑰 | 存取您的網頁介面首頁或API金鑰管理頁面以尋找您的認證。 深入瞭解[Infobip檔案](https://www.infobip.com/docs/api){target="_blank"} |
   | 選擇加入關鍵字 | 輸入將會自動觸發選擇加入訊息的預設或自訂關鍵字。 對於多個關鍵字，請使用逗號分隔值。 |
   | 選擇加入訊息 | 輸入自訂回應，此回應會自動作為您的選擇加入訊息傳送。 |
   | 選擇退出關鍵字 | 輸入將會自動觸發選擇退出訊息的預設或自訂關鍵字。 對於多個關鍵字，請使用逗號分隔值。 |
   | 選擇退出訊息 | 輸入自訂回應，此回應會自動作為您的選擇退出訊息傳送。 |
   | 說明關鍵字 | 輸入將會自動觸發您的&#x200B;**說明訊息**&#x200B;的預設或自訂關鍵字。 對於多個關鍵字，請使用逗號分隔值。 |
   | 說明訊息 | 輸入自動傳送為&#x200B;**說明訊息**&#x200B;的自訂回應。 |
   | 雙重選擇加入關鍵字 | 輸入觸發雙重加入流程的關鍵字。 如果使用者輪廓不存在，則會在成功確認時加以建立。對於多個關鍵字，請使用逗號分隔值。 [進一步瞭解SMS雙重選擇加入](https://video.tv.adobe.com/v/3440291/?learn=on&captions=chi_hant)。 |
   | 雙重選擇加入訊息 | 輸入自動傳送以回應雙重選擇加入確認的自訂回應。 |
   | 主體實體ID | 輸入指派的DLT主要實體識別碼。 |
   | 內容範本ID | 輸入註冊的DLT內容範本ID。 |
   | 有效期 | 輸入以小時為單位的訊息有效期。 如果在此時間範圍內無法傳遞訊息，系統會再次嘗試重新傳送訊息。 預設有效期設定為48小時。 |
   | 回呼資料 | 輸入要在通知URL上傳送的其他使用者端資料。 |
   | 傳入號碼 | 新增您的不重複傳入號碼。 這可讓您在不同的沙箱中使用相同的API認證，每個沙箱都有自己的傳入號碼。 |
   | 自訂傳入關鍵字 | 為特定動作定義唯一的關鍵字，例如DISCOUNT、OFFERS、ENROLL。 這些關鍵字會擷取並儲存為設定檔中的屬性，可讓您在歷程中觸發串流區段資格，並提供自訂回應或動作。 |
   | 預設傳入回複訊息 | 輸入當一般使用者傳送的傳入SMS不符合任何已定義的關鍵字時傳送的預設回覆。 |

   +++

1. 啟用&#x200B;**[!UICONTROL 模糊選擇退出]**&#x200B;選項，以偵測類似選擇退出關鍵字（例如，&#39;CANCIL&#39;）的訊息，並在&#x200B;**[!UICONTROL 模糊自動回覆]**&#x200B;欄位中自訂確認回覆。

   **[!UICONTROL 模糊選擇退出]**&#x200B;會識別指出使用者想要取消訂閱的SMS訊息，即使該訊息與定義的選擇退出關鍵字不完全相符。 它可以偵測常見的選擇退出片語和某些冒犯性詞語，協助確保您的行銷活動遵守使用者偏好設定並保持合規性。

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

Adobe Journey Optimizer使用[自訂SMS提供者](sms-configuration-custom.md)功能，透過Infobip支援RCS傳訊。 這可透過已驗證的企業設定檔傳送豐富的互動式訊息，並納入輪播、按鈕和多媒體內容等元素。

➡️ [在Infobip檔案中探索Infobip如何支援RCS](https://www.infobip.com/docs/api/channels/rcs)

若要使用Infobip啟用RCS傳訊，必須透過自訂SMS提供者設定新的API認證。 現有的Infobip SMS憑證不相容，因為RCS需要不同的裝載格式。

使用Infobip設定RCS：

1. **透過Infobip註冊您的企業以使用RCS**

   首先在Infobip平台內完成RCS上線和註冊程式。 這涉及設定您的RCS寄件者設定檔，以及確保您的帳戶已啟用RCS。 深入瞭解[Infobip檔案](https://www.infobip.com/docs/rcs/get-started)

1. **建立SMS Webhook**

   [在Journey Optimizer中設定自訂SMS webhook](sms-configuration-custom.md#webhook)。 此webhook將負責處理來自Infobip平台的傳遞回條、入站RCS訊息和狀態更新。

1. **使用自訂作為SMS供應商建立API認證**

   [在Journey Optimizer中建立新的API認證](sms-configuration-custom.md#api-credential)，選取[自訂]作為SMS提供者。 使用適當的RCS端點驗證方法、基本URL和標頭。

建立和設定API認證後，您現在需要為RCS訊息建立通道設定。 [了解更多](sms-configuration-surface.md)
