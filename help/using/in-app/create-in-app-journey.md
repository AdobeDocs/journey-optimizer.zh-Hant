---
title: 在行程中建立應用內通知
description: 瞭解如何在Journey Optimizer建立應用內消息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 應用程式內、訊息、建立、開始
hide: true
hidefromtoc: true
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
source-git-commit: 252011710574122c1f321a388b65bdafb7c666df
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 5%

---

# 在歷程建立應用程式內訊息 {#create-in-app-journey}

>[!AVAILABILITY]
>
>應用內活動當前可作為測試版僅供選擇用戶使用。 若要加入測試版計畫，請連絡 Adobe 客戶服務。

1. 開啟行程，然後拖放 **[!UICONTROL 應用程式內]** 活動 **[!UICONTROL 操作]** 的子菜單。

   當配置檔案到達其行程結束時，顯示給他們的任何應用內消息將自動過期。 因此，在應用程式內活動之後會自動添加一個等待活動，以確保正確的計時。

   ![](assets/in_app_journey_1.png)

1. 輸入 **[!UICONTROL 標籤]** 和 **[!UICONTROL 說明]** 的子郵件。

1. 選擇 [應用內曲面](inapp-configuration.md) 的下界。

   ![](assets/in_app_journey_2.png)

1. 您現在可以開始使用 **[!UICONTROL 編輯內容]** 按鈕 [了解更多](design-in-app.md)

1. 按一下 **[!UICONTROL 編輯觸發器]** 來配置觸發器。

   ![](assets/in_app_journey_4.png)

1. 選擇In-app消息處於活動狀態時觸發器的頻率：

   * **[!UICONTROL 每次顯示]**:在中選擇的事件時始終顯示消息 **[!UICONTROL 移動應用觸發器]** 下拉。
   * **[!UICONTROL 顯示一次]**:僅在第一次選擇的事件時顯示此消息 **[!UICONTROL 移動應用觸發器]** 下拉。
   * **[!UICONTROL 直到按一下為止顯示]**:在中選擇的事件時顯示此消息 **[!UICONTROL 移動應用觸發器]** 下拉，直到SDK使用「clicked」操作發送交互事件。

1. 從 **[!UICONTROL 移動應用觸發器]** 下拉清單，選擇將觸發消息的事件和條件：

   1. 從左下拉框中，選擇觸發消息所需的事件。
   1. 從右下拉框中，選擇選定事件所需的驗證。
   1. 按一下 **[!UICONTROL 添加]** 按鈕。 然後，重複上述步驟。
   1. 選擇事件的連結方式，例如選擇 **[!UICONTROL 和]** 如果你願意 **兩者** 觸發器為true，以便顯示或選擇消息 **[!UICONTROL 或]** 的子菜單。 **或** 觸發器是真的。
   1. 按一下 **[!UICONTROL 保存]** 已配置觸發器。

   ![](assets/in_app_journey_3.png)

1. 如有必要，請通過拖放其他操作或事件來完成行程流。 [了解更多](../building-journeys/about-journey-activities.md)

1. 在您的應用內消息準備好後，完成配置並發佈您的行程以激活它。

有關如何配置行程的詳細資訊，請參閱 [此頁](../building-journeys/journey-gs.md)。

## 應用內活動限制 {#in-app-activity-limitations}

* 此功能目前不適用於醫療保健客戶。

* 個性化只能包含配置檔案屬性。

* 應用內顯示與行程生命週期相關聯，這意味著當某個配置檔案的行程結束時，該行程內的所有應用內消息將不再顯示該配置檔案。  因此，無法直接從行程活動中停止應用內消息。 相反，您需要結束整個過程，以阻止應用程式內消息顯示到配置檔案。

* 在test模式下，In-app顯示取決於行程的壽命。 要防止測試期間過早結束行程，請調整 **[!UICONTROL 等待時間]** 價值 **[!UICONTROL 等待]** 活動。

* **[!UICONTROL 反應]** 活動無法用於對應用程式內開啟或按一下做出響應。

* 在用戶配置檔案到達畫布中的應用內活動的那一刻和他們開始看到應用內消息的時間之間，會發生激活延遲。 這種延遲可以從15分鐘到1小時不等。

**相關主題：**

* [設計應用內消息](design-in-app.md)
* [Test併發送您的應用內消息](send-in-app.md)
* [應用程式內報告](../reports/campaign-global-report.md#inapp-report)
* [應用內配置](inapp-configuration.md)
