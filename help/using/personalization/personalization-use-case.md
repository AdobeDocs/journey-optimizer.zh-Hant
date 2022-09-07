---
title: 個人化使用案例&冒號；訂單狀態通知
description: 了解如何使用設定檔、選件決策和內容資訊來個人化訊息。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# 個人化使用案例：訂單狀態通知 {#personalization-use-case}

在此使用案例中，您將了解如何在單一推播通知訊息中使用多種類型的個人化。 將使用三種類型的個人化：

* **設定檔**:根據設定檔欄位的訊息個人化
* **優惠方案決策**:根據決策管理變數進行個人化
* **內容**:根據歷程中的內容資料進行個人化

此範例的目標是將事件推送至 [!DNL Journey Optimizer] 每次更新客戶訂單時。 接著會傳送推播通知給客戶，其中包含訂單和個人化優惠方案的資訊。

針對此使用案例，需要下列必要條件：

* 設定訂單事件，包括訂單編號、狀態和項目名稱。 請參閱 [節](../event/about-events.md).
* 建立決策，請參閱 [節](../offers/offer-activities/create-offer-activities.md).

## 步驟1 — 建立歷程 {#create-journey}

1. 按一下 **[!UICONTROL Journeys]** 功能表和建立新歷程。

   ![](assets/perso-uc4.png)

1. 新增您的參加項目事件，以及 **推播** 動作活動。

   ![](assets/perso-uc5.png)

1. 設定及設計您的推播通知訊息。 請參閱 [節](../messages/get-started-content.md).

## 步驟2 — 在設定檔上新增個人化 {#add-perso}

1. 在 **推播** 活動，按一下 **編輯內容**.

1. 按一下 **標題** 欄位。

   ![](assets/perso-uc2.png)

1. 輸入主旨並新增設定檔個人化。 使用搜尋列來尋找設定檔的名字欄位。 在主題文字中，將游標置於您要插入個人化欄位的位置，然後按一下 **+** 表徵圖。 按一下「**儲存**」。

   ![](assets/perso-uc3.png)

## 步驟3 — 在內容資料上新增個人化 {#add-perso-contextual-data}

1. 在 **推播** 活動，按一下 **編輯內容** 並按一下 **標題** 欄位。

   ![](assets/perso-uc9.png)

1. 選取 **內容屬性** 功能表。 只有在歷程將內容資料傳遞至訊息時，才能使用內容屬性。 按一下 **Journey Orchestration**. 會出現下列內容資訊：

   * **事件**:此類別會重新分組歷程中頻道動作活動之前所放置之事件的所有欄位。
   * **歷程屬性**:指定設定檔之歷程的相關技術欄位，例如歷程ID或遇到的特定錯誤。 深入了解 [Journey Orchestration檔案](../building-journeys/expression/journey-properties.md).

   ![](assets/perso-uc10.png)

1. 展開 **事件** 項目，並尋找與事件相關的訂單編號欄位。 您也可以使用搜尋方塊。 按一下 **+** 圖示，在主旨文字中插入個人化欄位。 按一下「**儲存**」。

   ![](assets/perso-uc11.png)

1. 現在按一下 **主體** 欄位。

   ![](assets/perso-uc12.png)

1. 輸入訊息並插入，從 **[!UICONTROL Contextual attributes]** 菜單、訂單項目名稱和訂單進度。

   ![](assets/perso-uc13.png)

1. 從左側功能表中，選取 **優惠方案決策** 來插入決策變數。 選取放置位置，然後按一下 **+** 圖示加入內文。

   ![](assets/perso-uc14.png)

1. 按一下「驗證」以確定沒有錯誤，然後按一下 **儲存**.

   ![](assets/perso-uc15.png)

## 步驟4 — 測試並發佈歷程 {#test-publish}

1. 按一下 **測試** 按鈕，然後按一下 **觸發事件**.

   ![](assets/perso-uc17.png)

1. 輸入要在測試中傳遞的不同值。 測試模式只適用於測試設定檔。 設定檔識別碼必須對應至測試設定檔。 按一下 **傳送**.

   ![](assets/perso-uc18.png)

   推播通知會傳送並顯示在測試設定檔的行動電話上。

   ![](assets/perso-uc19.png)

1. 確認沒有錯誤並發佈歷程。
