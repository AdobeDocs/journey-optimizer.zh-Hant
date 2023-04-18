---
title: 建立應用程式內通知
description: 了解如何在Journey Optimizer中建立應用程式內訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 應用程式內，消息，建立，開始
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 4%

---

# 建立應用程式內訊息 {#create-in-app}

應用程式內訊息是在行銷活動的內容中建立。

>[!BEGINTABS]

>[!TAB 將應用程式內訊息新增至歷程]

>[!AVAILABILITY]
>
>應用程式內活動目前僅供選取使用者的測試版使用。 若要加入測試版計畫，請連絡 Adobe 客戶服務。

1. 開啟您的歷程，然後拖放 **[!UICONTROL 應用程式內]** 活動 **[!UICONTROL 動作]** 區段。

   當設定檔達到其歷程結尾時，顯示給他們的任何應用程式內訊息都會自動過期。 因此，應用程式內活動之後會自動新增「等待」活動，以確保計時正確。

   ![](assets/in_app_journey_1.png)

1. 輸入 **[!UICONTROL 標籤]** 和 **[!UICONTROL 說明]** 為您的訊息。

1. 選擇 [應用程式內曲面](inapp-configuration.md) 來使用。

   ![](assets/in_app_journey_2.png)

1. 您現在可以開始使用 **[!UICONTROL 編輯內容]** 按鈕。 [了解更多](design-in-app.md)

1. 按一下 **[!UICONTROL 編輯觸發器]** 來設定您的觸發器。

   ![](assets/in_app_journey_4.png)

1. 選擇應用程式內訊息作用中時觸發的頻率：

   * **[!UICONTROL 每次顯示]**:在 **[!UICONTROL 行動應用程式觸發器]** 下拉式清單中。
   * **[!UICONTROL 顯示一次]**:只會在第一次選取事件時顯示此訊息， **[!UICONTROL 行動應用程式觸發器]** 下拉式清單中。
   * **[!UICONTROL 顯示直到點進]**:當 **[!UICONTROL 行動應用程式觸發器]** 下拉式清單，直到SDK以「已點按」動作傳送interact事件為止。

1. 從 **[!UICONTROL 行動應用程式觸發器]** 下拉式清單，選擇將觸發訊息的事件和條件：

   1. 從左側下拉式清單中，選取觸發訊息所需的事件。
   1. 從右下拉式清單中，選取所選事件所需的驗證。
   1. 按一下 **[!UICONTROL 新增]** 按鈕。 然後，重複上述步驟。
   1. 選取事件的連結方式，例如選擇 **[!UICONTROL 和]** 如果您想要 **both** 觸發為true，以便顯示或選擇訊息 **[!UICONTROL 或]** 如果您想要顯示訊息，如果 **heer** 觸發器是真的。
   1. 按一下 **[!UICONTROL 儲存]** 觸發器時。

   ![](assets/in_app_journey_3.png)

1. 如有必要，請拖放其他動作或事件，以完成您的歷程流程。 [了解更多](../building-journeys/about-journey-activities.md)

1. 應用程式內訊息準備就緒後，請完成設定並發佈您的歷程以啟用它。

如需如何設定歷程的詳細資訊，請參閱 [本頁](../building-journeys/journey-gs.md).

>[!TAB 新增應用程式內訊息至促銷活動]

1. 存取 **[!UICONTROL 行銷活動]** ，然後按一下 **[!UICONTROL 建立行銷活動]**.

1. 在 **[!UICONTROL 屬性]** 區段，選取促銷活動執行類型的時間：排程或API觸發。 進一步了解行銷活動類型，請參閱 [本頁](../campaigns/create-campaign.md#campaigntype).

1. 在 **[!UICONTROL 動作]** 區段，選擇 **[!UICONTROL 應用程式內訊息]** 和 **[!UICONTROL 應用程式表面]** 先前已針對您的應用程式內訊息設定。 然後，按一下 **[!UICONTROL 建立]**.

   深入了解應用程式內設定，位於 [本頁](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. 從 **[!UICONTROL 屬性]** 部分，輸入 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]** 說明。

1. 若要將自訂或核心資料使用量標籤指派至應用程式內訊息，請選取 **[!UICONTROL 管理存取]**. [了解更多](../administration/object-based-access.md)。

1. 按一下 **[!UICONTROL 選取對象]** 按鈕，從可用的Adobe Experience Platform區段清單中定義要鎖定的對象。 [了解更多](../segment/about-segments.md)。

   ![](assets/in_app_create_2.png)

1. 在 **[!UICONTROL 身分命名空間]** 欄位中，選擇要使用的命名空間，以識別所選區段中的個人。 [了解更多](../event/about-creating.md#select-the-namespace)。

1. 按一下 **[!UICONTROL 編輯觸發器]** 若要選擇將觸發訊息的事件和條件：

   1. 按一下 **新增條件** 如果您希望觸發器考慮多個事件或條件。
   1. 選取事件的連結方式，例如選擇 **[!UICONTROL 和]** 如果您想要 **both** 觸發為true，以便顯示或選擇訊息 **[!UICONTROL 或]** 如果您想要顯示訊息，如果 **heer** 觸發器是真的。
   1. 按一下 **[!UICONTROL 建立群組]** 將觸發器分組。

   ![](assets/in_app_create_3.png)

1. 選擇應用程式內訊息作用中時觸發的頻率。 提供下列選項：

   * **[!UICONTROL 每次]**:在 **[!UICONTROL 行動應用程式觸發器]** 下拉式清單中。
   * **[!UICONTROL 一次]**:只會在第一次選取事件時顯示此訊息， **[!UICONTROL 行動應用程式觸發器]** 下拉式清單中。
   * **[!UICONTROL 直到點進]**:當 **[!UICONTROL 行動應用程式觸發器]** 下拉式清單，直到SDK以「已點按」動作傳送interact事件為止。
   * **[!UICONTROL X次]**:顯示此消息X時間。

1. 如果需要，請選擇 **[!UICONTROL 星期]** 或 **[!UICONTROL 每日時間]** 應用程式內訊息隨即顯示。

1. 促銷活動設計為在特定日期或循環頻率上執行。 了解如何設定 **[!UICONTROL 排程]** 在 [本節](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. 您現在可以開始使用 **[!UICONTROL 編輯內容]** 按鈕。 [了解更多](design-in-app.md)

   ![](assets/in_app_create_4.png)

>[!ENDTABS]

## 作法影片{#video}

以下影片說明如何在行銷活動中建立、設定和發佈應用程式內訊息。

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**相關主題：**

* [設計應用程式內訊息](design-in-app.md)
* [測試並傳送您的應用程式內訊息](send-in-app.md)
* [應用程式內報告](../reports/campaign-global-report.md#inapp-report)
* [應用程式內設定](inapp-configuration.md)