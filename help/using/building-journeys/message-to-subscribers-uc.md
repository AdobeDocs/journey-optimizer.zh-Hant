---
solution: Journey Optimizer
product: journey optimizer
title: 傳送訊息給訂閱者
description: 瞭解如何構建向清單的訂閱者發送消息的旅程
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 旅程，用例，消息，訂閱者，清單，讀取
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 17%

---

# 用例：向清單的訂閱者發送消息{#send-a-message-to-the-subscribers-of-a-list}

此使用案例的目的是建立向清單的訂戶發送消息的行程。

在此示例中， **[!UICONTROL 同意和首選項詳細資訊]** 欄位組 [!DNL Adobe Experience Platform] 的子菜單。 要查找此欄位組，請從 **[!UICONTROL 資料管理]** 菜單，選擇 **[!UICONTROL 架構]**。 在 **[!UICONTROL 欄位組]** 頁籤，在搜索欄位中輸入欄位組的名稱。

![此欄位組包括預訂元素](assets/consent-and-preference-details-field-group.png)

要配置此行程，請執行以下步驟：

1. 建立以 **[!UICONTROL 閱讀]** 的子菜單。 [閱讀全文](journey-gs.md)。
1. 添加 **[!UICONTROL 電子郵件]** 到旅程的活動。 [閱讀全文](journeys-message.md)。
1. 在 **[!UICONTROL 電子郵件參數]** 的下界 **[!UICONTROL 電子郵件]** 活動設定，替換預設電子郵件地址(`PersonalEmail.adress`)，其電子郵件地址為：

   1. 按一下 **[!UICONTROL 啟用參數覆蓋]** 表徵圖 **[!UICONTROL 地址]** ，然後按一下 **[!UICONTROL 編輯]** 表徵圖

      ![](assets/message-to-subscribers-uc-1.png)

   1. 在表達式編輯器中，輸入用於檢索訂閱者電子郵件地址的表達式。 [閱讀全文](expression/expressionadvanced.md)。

      此示例顯示包含對映射欄位的引用的表達式：

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      在本示例中，使用了以下函式：

      | 函數 | 說明 | 範例 |
      | --- | --- | --- |
      | `entry` | 根據所選命名空間引用映射元素 | 請參閱特定訂閱清單 |
      | `firstEntryKey` | 檢索映射的第一個條目鍵 | 檢索訂閱者的第一個電子郵件地址 |

      在本示例中，訂閱清單被命名 `daily-email`。 電子郵件地址被定義為 `subscribers` 映射，它連結到訂閱清單映射。

      閱讀有關 [引用欄位](expression/field-references.md) 中。

      ![](assets/message-to-subscribers-uc-2.png)

   1. 在 **[!UICONTROL 添加表達式]** 對話框，按一下 **[!UICONTROL 確定]**。

>[!CAUTION]
>
>電子郵件地址覆寫僅用於特定使用案例。 在大多數情況下，您不需要變更電子郵件地址，因為&#x200B;**[!UICONTROL 執行欄位]**&#x200B;中定義為主要電子郵件的值才是應該使用的值。 [了解更多](../configuration/primary-email-addresses.md)
