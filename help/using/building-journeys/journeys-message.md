---
title: 在歷程中新增訊息
description: 在歷程中新增訊息
feature: Journeys
topic: 內容管理
role: User
level: Intermediate
source-git-commit: d76eee0efa6735d6d81d7d7c752ed253b4cbebb5
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 3%

---

# 在歷程中新增訊息

[!DNL Journey Optimizer] 訊息功能是內建的，您只需要設計內容並發佈訊息即可。請參閱[本節](../get-started-content.md)。然後，您只需在歷程中新增使用Journey Optimizer設計的推送或電子郵件訊息。

如果您使用協力廠商系統來傳送訊息，則可建立自訂動作。 了解更多[小節](../action/action.md)。

## 新增訊息活動

1. 如同往常一樣，從事件或&#x200B;**讀取區段**&#x200B;活動開始您的歷程。

   ![](../assets/jo-message0.png)

1. 從浮動視窗的&#x200B;**Actions**&#x200B;區段，將&#x200B;**Message**&#x200B;活動拖放至畫布中。

   ![](../assets/jo-message1.png)

1. 新增標籤和說明。

   ![](../assets/jo-message2.png)

1. 在&#x200B;**Message**&#x200B;欄位內按一下。 隨即顯示Journey Optimizer中設計的可用訊息清單。 您可以依狀態篩選清單。

   ![](../assets/jo-message3.png)

1. 選擇消息，然後按一下&#x200B;**選擇**。 您也可以按一下&#x200B;**Create message**&#x200B;直接從此螢幕建立新郵件。

   ![](../assets/jo-message4-ter.png)

   如果要檢查郵件，可以按一下&#x200B;**Message**&#x200B;欄位中的&#x200B;**開啟郵件**&#x200B;表徵圖。 訊息會在新索引標籤中開啟。

   ![](../assets/jo-message4-bis.png)

1. 將後續步驟新增至您的歷程。

## 電子郵件參數和推播參數

**[!UICONTROL Email parameters]**&#x200B;和&#x200B;**[!UICONTROL Push parameters]**&#x200B;區段顯示唯讀欄位。 您通常會在建立訊息時執行此設定。 請參閱[本節](../get-started-content.md)。

![](../assets/jo-message4.png)

若要強制指定值，您可以使用欄位右側的&#x200B;**啟用參數override**&#x200B;圖示。 此選項可能適用於測試用途。 例如，對於電子郵件，您可以新增您的電子郵件地址。 發佈歷程後，會傳送電子郵件給您。
