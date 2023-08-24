---
title: 在歷程中建立應用程式內通知
description: 瞭解如何在歷程中新增應用程式內訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 應用程式內、訊息、建立、開始
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
source-git-commit: 066491e19a0a3be84c3e6ca6fefe88a9beb26285
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 2%

---


# 在歷程建立應用程式內訊息 {#create-in-app-journey}

若要在歷程中新增應用程式內訊息，請遵循下列步驟：

1. 開啟您的歷程，然後拖放 **[!UICONTROL 應用程式內]** 活動來自 **[!UICONTROL 動作]** 區段。

   當設定檔到達其歷程結尾時，顯示給設定檔的任何應用程式內訊息都會自動過期。 因此，會在應用程式內活動後自動新增等待活動，以確保適當的時機。

   ![](assets/in_app_journey_1.png)

1. 輸入 **[!UICONTROL 標籤]** 和 **[!UICONTROL 說明]** 您的訊息。

1. 選擇 [應用程式內表面](inapp-configuration.md) 以使用。

   ![](assets/in_app_journey_2.png)

1. 您現在可以開始使用設計內容 **[!UICONTROL 編輯內容]** 按鈕。 [了解更多](design-in-app.md)

1. 按一下 **[!UICONTROL 編輯觸發器]** 以設定您的觸發器。

   ![](assets/in_app_journey_4.png)

1. 從 **[!UICONTROL 應用程式內訊息觸發器]** 視窗，選擇將觸發訊息的事件和條件：

   1. 按一下 **[!UICONTROL 新增條件]** 是否希望觸發器考量多個事件或條件。
   1. 從 **[!UICONTROL 選取事件]** 下拉式清單，選取觸發器的事件型別。
   1. 選取事件的連結方式，例如，選擇 **[!UICONTROL 與]** 如果您願意 **兩者** 觸發器設為true以顯示或選擇訊息 **[!UICONTROL 或]** 如果您希望訊息顯示時機 **兩者之一** 的觸發程式為true。
   1. 按一下 **[!UICONTROL 建立群組]** 將觸發程式群組在一起。

   ![](assets/in_app_journey_3.png)

1. 選擇應用程式內訊息生效時觸發的頻率：

   * **[!UICONTROL 每次]**：永遠顯示中選取的事件時的訊息 **[!UICONTROL 行動應用程式觸發器]** 會出現下拉式清單。
   * **[!UICONTROL 一次]**：僅在中選取的事件第一次顯示這則訊息 **[!UICONTROL 行動應用程式觸發器]** 會出現下拉式清單。
   * **[!UICONTROL 直到點進為止]**：當在選取的事件時顯示此訊息 **[!UICONTROL 行動應用程式觸發器]** 下拉式清單會一直出現，直到SDK以「已點按」的動作傳送互動事件為止。
   * **[!UICONTROL X次數]**：僅顯示訊息的特定次數，由中設定的值決定 **[!UICONTROL 顯示時間]** 欄位。

1. 選取一週中要觸發應用程式內訊息的日期和特定時間，然後按一下 **[!UICONTROL 儲存]**.

1. 如有必要，請拖放其他動作或事件以完成您的歷程流程。 [了解更多](../building-journeys/about-journey-activities.md)

1. 應用程式內訊息準備就緒後，請完成設定並發佈您的歷程以將其啟用。

有關如何設定歷程的詳細資訊，請參閱 [此頁面](../building-journeys/journey-gs.md).

## 應用程式內活動限制 {#in-app-activity-limitations}

* 此功能目前不適用於Healthcare客戶。

* 個人化只能包含設定檔屬性。

* 應用程式內顯示會繫結至歷程期限，這表示當設定檔的歷程結束時，該歷程中的所有應用程式內訊息將不再顯示該設定檔。  因此，無法直接從歷程活動停止應用程式內訊息。 而是必須結束整個歷程，才能停止將應用程式內訊息顯示給設定檔。

* 在測試模式中，應用程式內顯示取決於歷程的有效期限。 為避免歷程在測試期間過早結束，請調整 **[!UICONTROL 等待時間]** 您的價值 **[!UICONTROL 等待]** 活動。

* **[!UICONTROL 反應]** 活動無法用於對應用程式內開啟或點按做出反應。

* 從使用者設定檔到達畫布中的應用程式內活動到開始看到應用程式內訊息的時間，可能會發生啟用延遲。

## 應用程式內報告 {#inapp-report}

從您的歷程 **[!UICONTROL 全域報告]**，則 **[!UICONTROL 應用程式內]** 索引標籤會詳細說明歷程中傳送之應用程式內傳遞的相關主要資訊。

進一步瞭解 [歷程全域報告](../reports/journey-global-report.md).

![](assets/in-app-journey-report.png)

+++進一步瞭解應用程式內報表可用的不同量度和Widget。

此 **[!UICONTROL 應用程式內績效]** KPI會詳細說明與訪客與您應用程式內訊息的參與度相關的主要資訊，例如：

* **[!UICONTROL 不重複曝光次數]**：應用程式內訊息已傳送給的不重複使用者人數。

* **[!UICONTROL 曝光數]**：傳送給所有使用者的應用程式內訊息總數。

* **[!UICONTROL 點按率]**：與看到訊息的使用者相比，與應用程式內訊息中所包含按鈕互動的使用者百分比。

* **[!UICONTROL 解除率]**：收件者已解除的應用程式內訊息百分比。

此 **[!UICONTROL 應用程式內摘要]** 圖表會顯示相關期間您應用程式內曝光次數的演變。

此 **[!UICONTROL 依據按鈕的點按]** 圖表和表格包含每個按鈕的收件者行為可用資料：

* **[!UICONTROL 點按次數]**：與應用程式內訊息所含按鈕互動的收件者總數。

* **[!UICONTROL 點按率]**：與看到訊息的使用者相比，與應用程式內訊息中所包含按鈕互動的使用者百分比。
+++

**相關主題：**

* [設計應用程式內訊息](design-in-app.md)
* [測試並傳送您的應用程式內訊息](send-in-app.md)
* [應用程式內報告](../reports/campaign-global-report.md#inapp-report)
* [應用程式內設定](inapp-configuration.md)
