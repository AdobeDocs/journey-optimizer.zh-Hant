---
title: 在歷程中建立應用程式內通知
description: 了解如何在Journey Optimizer中建立應用程式內訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 應用程式內，消息，建立，開始
hide: true
hidefromtoc: true
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 2%

---

# 在歷程中建立應用程式內訊息 {#create-in-app-journey}

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

## 應用程式內活動限制 {#in-app-activity-limitations}

* 此功能目前不適用於醫療保健客戶。

* 個人化只能包含設定檔屬性。

* 應用程式內顯示會系結至歷程有效期限，這表示當描述檔的歷程結束時，該歷程中的所有應用程式內訊息都會停止為該描述檔顯示。 這表示您無法直接從歷程活動中停止應用程式內。 你必須結束這個旅程。
* 應用程式內顯示會連結至歷程的有效期限，這表示一旦完成特定使用者設定檔的歷程，該歷程中的所有應用程式內訊息就不會為該設定檔顯示。 因此，無法直接從歷程活動停止應用程式內訊息。 相反地，您需要結束整個歷程，以阻止應用程式內訊息顯示至設定檔。

* 使用此功能，您將無法使用 **[!UICONTROL 反應]** 回應應用程式內開啟或按一下的活動。

* 使用者設定檔到達畫布中的應用程式內活動與開始看到該應用程式內訊息之間，會發生啟用延遲。 此延遲的範圍可從15分鐘到1小時。

**相關主題：**

* [設計應用程式內訊息](design-in-app.md)
* [測試並傳送您的應用程式內訊息](send-in-app.md)
* [應用程式內報告](../reports/campaign-global-report.md#inapp-report)
* [應用程式內設定](inapp-configuration.md)