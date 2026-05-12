---
solution: Journey Optimizer
product: journey optimizer
title: 設定 Infobip 提供者
description: 瞭解如何使用Journey Optimizer和Infobip設定您的環境以傳送簡訊和多媒體簡訊
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
TQID: https://experienceleague.adobe.com/hkloRlDuOO-lNSezWvOcD3dtsHrhDqCJGo3cHq5pWog
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 9e5edbefb19b7cf30da3a7164300e966a42e8711
workflow-type: tm+mt
source-wordcount: 769
ht-degree: 1%

---

# 設定 Infobip 提供者 {#sms-configuration-infobip}

透過將Infobip與Adobe Journey Optimizer整合，您可以將文字訊息傳送至您的設定檔，作為歷程和行銷活動的一部分。

若要將Infobip設定為簡訊提供者，請遵循下列步驟：

1. [建立API認證](#api-credential)
1. [建立 Webhook](sms-webhook.md)
1. [建立頻道設定](sms-configuration-surface.md)
1. [透過簡訊頻道動作建立歷程或行銷活動](create-sms.md)

## 設定簡訊的API認證 {#api-credential}

若要使用Journey Optimizer設定Infobip，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 管道]**&#x200B;並選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表。 按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

1. 設定您的SMS API認證，如下所述：

   +++ 設定的SMS認證清單

   | 設定欄位 | 說明 |
   |---|---|
   | 簡訊供應商 | Infobip |
   | 名稱 | 選擇您的API認證名稱。 |
   | API基本URL和API金鑰 | 存取您的網頁介面首頁或API金鑰管理頁面以尋找您的認證。 對於區域或替代網域端點（例如`api-ny2.infobip.com`），請指定完整的基底URL，並使用Infobip支援來驗證您的授權權杖。 </br>在[Infobip檔案](https://www.infobip.com/docs/api){target="_blank"}中進一步瞭解 |
   | 主體實體ID | 輸入指派的DLT主要實體識別碼。 |
   | 內容範本ID | 輸入註冊的DLT內容範本ID。 |
   | 有效期 | 輸入以小時為單位的訊息有效期。 如果在此時間範圍內無法傳遞訊息，系統會再次嘗試重新傳送訊息。 預設有效期設定為48小時。 |
   | 回呼資料 | 輸入要在通知URL上傳送的其他使用者端資料。 |
   | 傳入號碼 | 新增您的不重複傳入號碼。 這可讓您在不同的沙箱中使用相同的API認證，每個沙箱都有自己的傳入號碼。 |

   +++

1. 啟用&#x200B;**[!UICONTROL 模糊選擇退出]**&#x200B;選項，以偵測類似選擇退出關鍵字（例如，&#39;CANCIL&#39;）的訊息，並在&#x200B;**[!UICONTROL 模糊自動回覆]**&#x200B;欄位中自訂確認回覆。

   **[!UICONTROL 模糊選擇退出]**&#x200B;會識別指出使用者想要取消訂閱的SMS訊息，即使該訊息與定義的選擇退出關鍵字不完全相符。 它可以偵測常見的選擇退出片語和某些冒犯性詞語，協助確保您的行銷活動遵守使用者偏好設定並保持合規性。

1. 選取&#x200B;**[!UICONTROL 使用傳入的自訂資料集]**，將此認證的傳入SMS路由至您從下拉式清單中選擇的預先建立資料集。 [進一步瞭解如何使用傳入關鍵字的自訂資料集](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >資料集結構描述必須是&#x200B;**[!UICONTROL XDM ExperienceEvent]**，而且至少包含下列欄位群組：
   >* Adobe CJM ExperienceEvent — 訊息互動細節
   >* Adobe CJM ExperienceEvent — 訊息執行詳細資料
   >* Adobe CJM ExperienceEvent — 訊息設定檔詳細資料
   >
   >必須為設定檔啟用結構描述和資料集。

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

在建立及設定您的API認證後，您現在需要建立[您的Webhook](sms-webhook.md)以及RCS訊息的通道設定。 [了解更多](sms-configuration-surface.md)
