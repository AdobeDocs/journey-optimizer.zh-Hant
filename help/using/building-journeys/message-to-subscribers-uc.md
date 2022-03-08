---
title: 傳送訊息給訂閱者
description: 瞭解如何構建向清單的訂閱者發送消息的旅程
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 5%

---

# 用例：向清單的訂閱者發送消息{#send-a-message-to-the-subscribers-of-a-list}

此使用案例的目的是建立向清單的訂戶發送消息的行程。

在此示例中， **[!UICONTROL Consent and Preference Details]** 欄位組 [!DNL Adobe Experience Platform] 的子菜單。 要查找此欄位組，請從 **[!UICONTROL Data Management]** 菜單，選擇 **[!UICONTROL Schemas]**。 在 **[!UICONTROL Field groups]** 頁籤，在搜索欄位中輸入欄位組的名稱。

![此欄位組包括預訂元素](assets/consent-and-preference-details-field-group.png)

要配置此行程，請執行以下步驟：

1. 建立以 **[!UICONTROL Read]** 的子菜單。 [閱讀全文](journey-gs.md)。
1. 添加 **[!UICONTROL Message]** 活動，通過電子郵件，到旅程。 [閱讀全文](journeys-message.md)。
1. 在 **[!UICONTROL Email parameters]** 的下界 **[!UICONTROL Message]** 活動設定，替換預設電子郵件地址(`PersonalEmail.adress`)，其電子郵件地址為：

   1. 按一下 **[!UICONTROL Enable parameter override]** 表徵圖 **[!UICONTROL Address]** ，然後按一下 **[!UICONTROL Edit]** 表徵圖

      ![](assets/message-to-subscribers-uc-1.png)

      若要修改電子郵件地址，您必須先已發佈該郵件。

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

   1. 在 **[!UICONTROL Add an expression]** 對話框，按一下 **[!UICONTROL Ok]**。

   ![](assets/message-to-subscribers-uc-3.png)

1. 以 **[!UICONTROL End]** 的子菜單。
