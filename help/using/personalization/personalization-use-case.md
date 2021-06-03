---
title: 個人化使用案例
description: 個人化使用案例
source-git-commit: cd1b07bbb4b247d1d8c0cc87be9e4bdad22377ed
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---


# 個人化使用案例{#personalization-use-case}

![](../assets/do-not-localize/badge.png)

在此使用案例中，您將了解如何在單一推播通知訊息中使用多種類型的個人化。 將使用三種類型的個人化：

* **設定檔**:根據設定檔欄位的訊息個人化
* **選件決策**:根據優惠方案決策變數進行個人化
* **內容**:根據歷程中的內容資料進行個人化

此範例的目標是每次更新客戶訂單時推送事件至Journey Optimizer。 接著會傳送推播通知給客戶，其中包含訂單和個人化優惠方案的資訊。

針對此使用案例，需要下列必要條件：

* 建立並設計推播通知訊息，而不需發佈。 請參閱此[節](../create-message.md)。
* 設定訂單事件，包括訂單編號、狀態和項目名稱。 請參閱此[節](../event/about-events.md)。
* 建立決策（先前稱為「優惠方案活動」），請參閱此[區段](../offers/offer-activities/create-offer-activities.md)。

## 步驟1 — 在設定檔上新增個人化

1. 按一下&#x200B;**[!UICONTROL Message]**&#x200B;功能表，然後選取您的訊息。

   ![](assets/perso-uc.png)

1. 按一下&#x200B;**Title**&#x200B;欄位。

   ![](assets/perso-uc2.png)

1. 輸入主旨並新增設定檔個人化。 使用搜尋列來尋找設定檔的名字欄位。 在主題文本中，將游標置於要插入個性化欄位的位置，然後按一下&#x200B;**+**&#x200B;表徵圖。 按一下&#x200B;**「儲存」**。

   ![](assets/perso-uc3.png)

   >[!NOTE]
   >
   >保留草稿格式的訊息。 尚未發佈。

## 步驟2 — 建立歷程

1. 按一下&#x200B;**[!UICONTROL Journeys]**&#x200B;功能表並建立新歷程。

   ![](assets/perso-uc4.png)

1. 新增您的登入事件、**Message**&#x200B;和&#x200B;**End**&#x200B;活動。

   ![](assets/perso-uc5.png)

1. 在&#x200B;**Message**&#x200B;活動中，選取先前建立的訊息。 按一下&#x200B;**確定**。

   ![](assets/perso-uc6.png)

   系統會顯示訊息，通知您已將登入事件資料和歷程屬性傳遞至訊息。

   ![](assets/perso-uc7.png)

   >[!NOTE]
   >
   >訊息隨即出現，並顯示警告圖示。 這是因為訊息尚未發佈。

## 步驟3 — 在內容資料上新增個人化

1. 在&#x200B;**Message**&#x200B;活動中，按一下&#x200B;**開啟訊息**&#x200B;圖示。 訊息會在新索引標籤中開啟。

   ![](assets/perso-uc8.png)

1. 按一下&#x200B;**Title**&#x200B;欄位。

   ![](assets/perso-uc9.png)

1. 選擇&#x200B;**Context**&#x200B;類別。 只有在歷程將內容資料傳遞至訊息時，才能使用此項目。 按一下&#x200B;**Journey Orchestration**。 會出現下列內容資訊：

   * **事件**:此類別會重新分組歷程中訊息活動之前所 **** 放置事件的所有欄位。
   * **歷程屬性**:指定設定檔之歷程的相關技術欄位，例如歷程ID或遇到的特定錯誤。請參閱[Journey Orchestration檔案](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/syntax/journey-properties.html#building-advanced-conditions-journeys)。

   ![](assets/perso-uc10.png)

1. 展開&#x200B;**Events**&#x200B;項目，並尋找與事件相關的訂單編號欄位。 您也可以使用搜尋方塊。 按一下&#x200B;**+**&#x200B;圖示，在主旨文字中插入個人化欄位。 按一下&#x200B;**「儲存」**。

   ![](assets/perso-uc11.png)

1. 現在按一下&#x200B;**Body**&#x200B;欄位。

   ![](assets/perso-uc12.png)

1. 鍵入消息，然後從&#x200B;**Context**&#x200B;類別插入訂單項名稱和訂單進度。

   ![](assets/perso-uc13.png)

1. 從下拉式清單中，選取&#x200B;**選件決策**&#x200B;以插入offer decisioning變數。 選取位置，然後按一下決策旁的&#x200B;**+**&#x200B;圖示（先前稱為「優惠方案活動」），將其新增至內文。

   ![](assets/perso-uc14.png)

1. 按一下「驗證」以確定沒有錯誤，然後按一下「**儲存**」。

   ![](assets/perso-uc15.png)

1. 現在，發佈訊息。

   ![](assets/perso-uc16.png)

## 步驟4 — 測試並發佈歷程

1. 再次開啟歷程。 如果歷程已開啟，請務必重新整理頁面。 訊息發佈後，您就會看到歷程中沒有錯誤。 按一下&#x200B;**Test**&#x200B;按鈕，然後按一下&#x200B;**觸發事件**。

   ![](assets/perso-uc17.png)

1. 輸入要在測試中傳遞的不同值。 測試模式只適用於測試設定檔。 設定檔識別碼必須與測試設定檔相對應。 按一下&#x200B;**Send**。

   ![](assets/perso-uc18.png)

   推播通知會傳送並顯示在測試設定檔的行動電話上。

   ![](assets/perso-uc19.png)

1. 確認沒有錯誤並發佈歷程。

