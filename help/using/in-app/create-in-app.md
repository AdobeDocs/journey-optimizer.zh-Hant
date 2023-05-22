---
title: 建立應用內通知
description: 瞭解如何在Journey Optimizer建立應用內消息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 應用程式內、訊息、建立、開始
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 9bebcde9edde40a0fadba34d8b40757036a6436d
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 6%

---

# 建立應用程式內訊息 {#create-in-app}

<!--
>[!BEGINTABS]

>[!TAB Add an In-app message to a journey]

>[!AVAILABILITY]
>
>The In-app activity is currently available as a beta to select users only. To join the beta program, contact Adobe Customer Care.

1. Open your journey, then drag and drop an **[!UICONTROL In-app]** activity from the **[!UICONTROL Actions]** section of the palette.

    When a profile reaches the end of their journey, any in-app messages displayed to them will automatically expire. For that reason, a Wait activity is automatically added after your In-app activity to ensure proper timing.

    ![](assets/in_app_journey_1.png)

1. Enter a **[!UICONTROL Label]** and **[!UICONTROL Description]** for your message.

1. Choose the [In-app surface](inapp-configuration.md) to use.

    ![](assets/in_app_journey_2.png)

1. You can now start designing your content with the **[!UICONTROL Edit content]** button. [Learn more](design-in-app.md)

1. Click **[!UICONTROL Edit trigger]** to configure your Trigger. 

    ![](assets/in_app_journey_4.png)

1. Choose the frequency of your trigger when your In-app message is active:

    * **[!UICONTROL Show every time]**: Always show the message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show once]**: Only show this message the first time the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show until click through]**: Show this message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur until an interact event is sent by the SDK with an action of "clicked".

1. From the **[!UICONTROL Mobile app trigger]** dropdown(s), choose the event(s) and criteria that will trigger your message:

    1. From the left drop-down, select the event required to trigger the message.
    1. From the right drop-down, select the validation required on the selected event.
    1. Click the **[!UICONTROL Add]** button if you want the trigger to consider multiple events or criteria. Then, repeat the steps above.
    1. Select how your events are linked, e.g. choose **[!UICONTROL And]** if you want **both** triggers to be true in order for a message to be shown or choose **[!UICONTROL Or]** if you want the message to be shown if **either** of the triggers are true.
    1. Click **[!UICONTROL Save]** when your Triggers have been configured.

    ![](assets/in_app_journey_3.png)
    
1. If necessary, complete your journey flow by dragging and dropping additional actions or events. [Learn more](../building-journeys/about-journey-activities.md)

1. Once your In-app message is ready, finalize the configuration and publish your journey to activate it.

For more information on how to configure a journey, refer to [this page](../building-journeys/journey-gs.md).

>[!TAB Add an In-app message to a campaign]
-->

1. 訪問 **[!UICONTROL 市場活動]** 菜單，然後按一下 **[!UICONTROL 建立市場活動]**。

1. 在 **[!UICONTROL 屬性]** 選擇市場活動執行類型：計畫或API觸發。 瞭解有關中市場活動類型的詳細資訊 [此頁](../campaigns/create-campaign.md#campaigntype)。

1. 在 **[!UICONTROL 操作]** 的 **[!UICONTROL 應用內消息]** 和 **[!UICONTROL 應用表面]** 先前為您的In-app消息配置的。 然後，按一下 **[!UICONTROL 建立]**。

   瞭解有關中的應用程式內配置的詳細資訊 [此頁](inapp-configuration.md)。

   ![](assets/in_app_create_1.png)

1. 從 **[!UICONTROL 屬性]** ，輸入 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]** 說明。

1. 要將自定義或核心資料使用標籤分配給In-app消息，請選擇 **[!UICONTROL 管理訪問]**。 [了解更多](../administration/object-based-access.md)。

1. 按一下 **[!UICONTROL 選擇受眾]** 按鈕，來定義可用Adobe Experience Platform段清單中的目標受眾。 [了解更多](../segment/about-segments.md)。

   ![](assets/in_app_create_2.png)

1. 在 **[!UICONTROL 標識命名空間]** 欄位中，選擇要用於標識選定段中的個體的命名空間。 [了解更多](../event/about-creating.md#select-the-namespace)。

1. 按一下 **[!UICONTROL 編輯觸發器]** 選擇要觸發消息的事件和條件：

   1. 按一下 **添加條件** 的子菜單。
   1. 選擇事件的連結方式，例如選擇 **[!UICONTROL 和]** 如果你願意 **兩者** 觸發器為true，以便顯示或選擇消息 **[!UICONTROL 或]** 的子菜單。 **或** 觸發器是真的。
   1. 按一下 **[!UICONTROL 生成組]** 將觸發器分組。

   ![](assets/in_app_create_3.png)

1. 選擇當In-app消息處於活動狀態時觸發器的頻率。 提供下列選項：

   * **[!UICONTROL 每次]**:在中選擇的事件時始終顯示消息 **[!UICONTROL 移動應用觸發器]** 下拉。
   * **[!UICONTROL 一次]**:僅在第一次選擇的事件時顯示此消息 **[!UICONTROL 移動應用觸發器]** 下拉。
   * **[!UICONTROL 直到按一下]**:在中選擇的事件時顯示此消息 **[!UICONTROL 移動應用觸發器]** 下拉，直到SDK使用「clicked」操作發送交互事件。
   * **[!UICONTROL X次數]**:顯示此消息X時間。

1. 如果需要，選擇 **[!UICONTROL 星期幾]** 或 **[!UICONTROL 一天中的時間]** 將顯示應用內消息。

1. 市場活動旨在在特定日期或循環頻率上執行。 瞭解如何配置 **[!UICONTROL 計畫]** 你的競選團隊 [此部分](../campaigns/create-campaign.md#schedule)。

   ![](assets/in-app-schedule.png)

1. 您現在可以開始使用 **[!UICONTROL 編輯內容]** 按鈕 [了解更多](design-in-app.md)

   ![](assets/in_app_create_4.png)

<!--
>[!ENDTABS]
-->

## 操作說明影片{#video}

下面的視頻顯示如何在市場活動中建立、配置和發佈應用內消息。

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**相關主題：**

* [設計應用內消息](design-in-app.md)
* [Test併發送您的應用內消息](send-in-app.md)
* [應用程式內報告](../reports/campaign-global-report.md#inapp-report)
* [應用內配置](inapp-configuration.md)