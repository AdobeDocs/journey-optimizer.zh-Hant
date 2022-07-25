---
title: 個性化用例冒號(&C);訂單狀態通知
description: 瞭解如何使用配置檔案、提供決策和上下文資訊對郵件進行個性化設定。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# 個性化用例：訂單狀態通知 {#personalization-use-case}

在此使用情形中，您將看到如何在單個推送通知消息中使用多種類型的個性化設定。 將使用三種個性化類型：

* **配置檔案**:基於配置檔案欄位的消息個性化
* **提供決定**:基於offer decisioning變數的個性化
* **上下文**:基於旅程上下文資料的個性化

此示例的目標是將事件推送到 [!DNL Journey Optimizer] 每次更新客戶訂單。 隨後向客戶發送推送通知，其中包含有關訂單的資訊和個性化的優惠。

對於此用例，需要以下先決條件：

* 配置訂單事件，包括訂單編號、狀態和物料名稱。 請參閱此 [節](../event/about-events.md)。
* 建立決定，請參閱 [節](../offers/offer-activities/create-offer-activities.md)。

## 步驟1 — 建立行程 {#create-journey}

1. 按一下 **[!UICONTROL Journeys]** 菜單並建立新的行程。

   ![](assets/perso-uc4.png)

1. 添加您的條目事件和 **推** 操作活動。

   ![](assets/perso-uc5.png)

1. 配置和設計推送通知消息。 請參閱此 [節](../messages/get-started-content.md)。

## 步驟2 — 在配置檔案上添加個性化 {#add-perso}

1. 在 **推** 活動，按一下 **編輯內容**。

1. 按一下 **標題** 的子菜單。

   ![](assets/perso-uc2.png)

1. 鍵入主題並添加配置檔案個性化。 使用搜索欄查找配置檔案的名字欄位。 在主題文本中，將游標置於要插入個性化欄位的位置，然後按一下 **+** 表徵圖 按一下「**儲存**」。

   ![](assets/perso-uc3.png)

## 步驟3 — 在上下文資料上添加個性化 {#add-perso-contextual-data}

1. 在 **推** 活動，按一下 **編輯內容** 並按一下 **標題** 的子菜單。

   ![](assets/perso-uc9.png)

1. 選擇 **上下文屬性** 的子菜單。 上下文屬性僅在行程將上下文資料傳遞到消息時才可用。 按一下 **Journey Orchestration**。 將顯示以下上下文資訊：

   * **事件**:此類別重新分組行程中通道操作活動之前發生的事件中的所有欄位。
   * **旅程屬性**:與給定配置檔案的行程相關的技術欄位，例如行程ID或遇到的特定錯誤。 瞭解詳情 [Journey Orchestration文檔](../building-journeys/expression/journey-properties.md)。

   ![](assets/perso-uc10.png)

1. 展開 **事件** 項，並查找與事件相關的訂單編號欄位。 您也可以使用搜索框。 按一下 **+** 表徵圖，在主題文本中插入個性化欄位。 按一下「**儲存**」。

   ![](assets/perso-uc11.png)

1. 現在，按一下 **身體** 的子菜單。

   ![](assets/perso-uc12.png)

1. 鍵入消息並插入， **[!UICONTROL Contextual attributes]** 菜單中的命令。

   ![](assets/perso-uc13.png)

1. 從左菜單中，選擇 **提供決策** 的子菜單。 選取放置，然後按一下 **+** 表徵圖。

   ![](assets/perso-uc14.png)

1. 按一下「validate（驗證）」以確保沒有錯誤，然後按一下 **保存**。

   ![](assets/perso-uc15.png)

## 步驟4 -Test並發佈行程 {#test-publish}

1. 按一下 **Test** 按鈕，然後按一下 **觸發事件**。

   ![](assets/perso-uc17.png)

1. 輸入要傳遞到test中的不同值。 Test模式僅用於test配置檔案。 配置檔案標識符需要與test配置檔案對應。 按一下 **發送**。

   ![](assets/perso-uc18.png)

   推送通知被發送並顯示在test配置檔案的行動電話上。

   ![](assets/perso-uc19.png)

1. 驗證沒有錯誤並發佈行程。
