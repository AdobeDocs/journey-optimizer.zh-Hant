---
solution: Journey Optimizer
product: journey optimizer
title: 傳送訊息給訂閱者
description: 瞭解如何建立歷程，以傳送訊息給清單的訂閱者
feature: Journeys, Use Cases, Subscriptions
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: 歷程，使用案例，訊息，訂閱者，清單，讀取
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 17%

---

# 使用案例：傳送訊息給清單的訂閱者{#send-a-message-to-the-subscribers-of-a-list}

此使用案例的目的是建立歷程，以傳送訊息給清單的訂閱者。

在此範例中， **[!UICONTROL 同意和偏好設定詳細資料]** 欄位群組來源 [!DNL Adobe Experience Platform] 已使用。 若要尋找此欄位群組，請從 **[!UICONTROL 資料管理]** 功能表，選擇 **[!UICONTROL 方案]**. 在 **[!UICONTROL 欄位群組]** 標籤，在搜尋欄位中輸入欄位群組的名稱。

![此欄位群組包含訂閱元素](assets/consent-and-preference-details-field-group.png)

若要設定此歷程，請遵循下列步驟：

1. 建立以「 」開始的歷程 **[!UICONTROL 讀取]** 活動。 [閱讀全文](journey-gs.md)。
1. 新增 **[!UICONTROL 電子郵件]** 歷程的動作活動。 [閱讀全文](journeys-message.md)。
1. 在 **[!UICONTROL 電子郵件引數]** 的區段 **[!UICONTROL 電子郵件]** 活動設定，取代預設的電子郵件地址(`PersonalEmail.adress`)填入訂閱者清單的電子郵件地址：

   1. 按一下 **[!UICONTROL 啟用引數覆寫]** 圖示右側 **[!UICONTROL 地址]** 欄位，然後按一下 **[!UICONTROL 編輯]** 圖示。

      ![](assets/message-to-subscribers-uc-1.png)

   1. 在運算式編輯器中，輸入運算式以擷取訂閱者的電子郵件地址。 [閱讀全文](expression/expressionadvanced.md)。

      此範例顯示包含對應欄位參照的運算式：

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      在此範例中，會使用下列函式：

      | 函數 | 說明 | 範例 |
      | --- | --- | --- |
      | `entry` | 根據選取的名稱空間參考對應元素 | 請參閱特定訂閱清單 |
      | `firstEntryKey` | 擷取對應的第一個專案索引鍵 | 擷取訂閱者的第一個電子郵件地址 |

      在此範例中，訂閱清單名為 `daily-email`. 電子郵件地址在中定義為金鑰 `subscribers` 對應，此對應會連結至訂閱清單對應。

      深入瞭解 [欄位參考](expression/field-references.md) 在運算式中。

      ![](assets/message-to-subscribers-uc-2.png)

   1. 在 **[!UICONTROL 新增運算式]** 對話方塊，按一下 **[!UICONTROL 確定]**.

>[!CAUTION]
>
>電子郵件地址覆寫僅用於特定使用案例。 在大多數情況下，您不需要變更電子郵件地址，因為&#x200B;**[!UICONTROL 執行欄位]**&#x200B;中定義為主要電子郵件的值才是應該使用的值。 [了解更多](../configuration/primary-email-addresses.md)
