---
solution: Journey Optimizer
product: journey optimizer
title: 在歷程中新增訊息
description: 了解如何在歷程中新增訊息
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 18%

---

# 電子郵件、簡訊、推播{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] 隨附內建的訊息功能。 您只需在歷程中新增推送、簡訊或電子郵件訊息活動，以及 [定義設定和內容](../messages/messages-in-journeys.md). 接著會在歷程的內容中執行及傳送。

您也可以設定特定動作以傳送訊息：

* 如果您使用協力廠商系統來傳送訊息，則可建立自訂動作。 了解更多資訊 [節](../action/action.md).

* 如果您正在使用Campaign和Journey Optimizer，請參閱下列區段：

   * [[!DNL Journey Optimizer] 和Campaign Classicv7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] 和Campaign Standard](../action/acs-action.md)

若要在歷程中新增訊息，請遵循下列步驟：

1. 利用[事件](general-events.md)或[讀取區段](read-segment.md)活動來開始您的歷程。

1. 從調色盤的&#x200B;**動作**&#x200B;區段 ，拖放&#x200B;**電子郵件**、**簡訊**&#x200B;或&#x200B;**推播**&#x200B;活動至畫布。

   ![](../messages/assets/add-a-message.png)


   設定訊息及定義其內容的所有步驟在 [本節](../messages/get-started-content.md).

## 更新即時內容{#update-live-content}

您可以更新即時歷程中的訊息內容（電子郵件、簡訊、推播）。

若要這麼做，請開啟您的即時歷程，選取訊息活動，然後按一下 **編輯內容**.

![](assets/add-a-message2.png)

不過，您無法變更個人化中使用的屬性，不論是設定檔屬性或內容資料（來自事件或歷程屬性）。
