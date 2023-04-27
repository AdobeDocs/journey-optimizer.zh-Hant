---
solution: Journey Optimizer
product: journey optimizer
title: 傳送訊息給訂閱者
description: 了解如何建立歷程，以傳送訊息給清單的訂閱者
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，使用案例，訊息，訂閱者，清單，讀取
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 17%

---

# 使用案例：傳送訊息給清單的訂閱者{#send-a-message-to-the-subscribers-of-a-list}

此使用案例的用途是建立歷程，以傳送訊息給清單的訂閱者。

在此範例中， **[!UICONTROL 同意和偏好設定詳細資訊]** 欄位組 [!DNL Adobe Experience Platform] 中所有規則的URL區段。 要查找此欄位組，請從 **[!UICONTROL 資料管理]** 菜單，選擇 **[!UICONTROL 結構]**. 在 **[!UICONTROL 欄位群組]** 頁簽，在搜索欄位中輸入欄位組的名稱。

![此欄位群組包含訂閱元素](assets/consent-and-preference-details-field-group.png)

若要設定此歷程，請依照下列步驟操作：

1. 建立以 **[!UICONTROL 閱讀]** 活動。 [閱讀全文](journey-gs.md)。
1. 新增 **[!UICONTROL 電子郵件]** 動作活動至歷程。 [閱讀全文](journeys-message.md)。
1. 在 **[!UICONTROL 電子郵件參數]** 區段 **[!UICONTROL 電子郵件]** 活動設定，取代預設電子郵件地址(`PersonalEmail.adress`)及清單訂閱者的電子郵件地址：

   1. 按一下 **[!UICONTROL 啟用參數覆蓋]** 表徵圖 **[!UICONTROL 地址]** 欄位，然後按一下 **[!UICONTROL 編輯]** 表徵圖。

      ![](assets/message-to-subscribers-uc-1.png)

   1. 在運算式編輯器中，輸入運算式以擷取訂閱者的電子郵件地址。 [閱讀全文](expression/expressionadvanced.md)。

      此範例顯示包含映射欄位參考的運算式：

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      在此範例中，會使用下列函式：

      | 函數 | 說明 | 範例 |
      | --- | --- | --- |
      | `entry` | 根據選取的命名空間參考對應元素 | 請參閱特定訂閱清單 |
      | `firstEntryKey` | 檢索映射的第一個條目鍵 | 擷取訂閱者的第一個電子郵件地址 |

      在此範例中，訂閱清單的名稱為 `daily-email`. 電子郵件地址定義為 `subscribers` 地圖，連結至訂閱清單地圖。

      深入了解 [欄位參考](expression/field-references.md) 在運算式中。

      ![](assets/message-to-subscribers-uc-2.png)

   1. 在 **[!UICONTROL 新增運算式]** 對話框，按一下 **[!UICONTROL 確定]**.

>[!CAUTION]
>
>電子郵件地址覆寫僅用於特定使用案例。 在大多數情況下，您不需要變更電子郵件地址，因為&#x200B;**[!UICONTROL 執行欄位]**&#x200B;中定義為主要電子郵件的值才是應該使用的值。 [了解更多](../configuration/primary-email-addresses.md)
