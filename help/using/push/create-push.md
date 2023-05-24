---
solution: Journey Optimizer
product: journey optimizer
title: 設定推播通知
description: 了解如何在 Journey Optimizer 建立推播通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 16%

---

# 建立推播通知 {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="推播訊息建立"
>abstract="新增您的推播訊息並開始使用運算式編輯器對其進行個人化。"

## 在行程或市場活動中建立推送通知 {#create}

要建立推送通知，請執行以下步驟：

>[!BEGINTABS]

>[!TAB 將推送至行程]

1. 開啟行程，然後從調色板的「操作」部分拖放「推送」活動。

   ![](assets/push_create_1.png)

1. 提供有關消息的基本資訊（標籤、說明、類別），然後選擇要使用的消息面。 的 **[!UICONTROL 曲面]** 預設情況下，欄位是預填充的，用戶使用該通道的最後一個曲面。

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >如果您從行程發送推送通知，則可以利用Adobe Journey Optimizer的「發送時間優化」功能來預測發送消息的最佳時間，以便根據歷史開啟和按一下速率來最大化預訂。 [瞭解如何使用發送時間優化](../building-journeys/journeys-message.md#send-time-optimization)

   有關如何配置行程的詳細資訊，請參閱 [此頁](../building-journeys/journey-gs.md)

1. 在旅程配置螢幕中，按一下 **[!UICONTROL 編輯內容]** 按鈕來配置推送內容。 [設計推送通知](design-push.md)

1. 定義訊息內容後，您就可以使用測試設定檔進行預覽及測試。 

1. 當您的推送就緒時，請完成您的 [旅程](../building-journeys/journey-gs.md) 寄出去。

   要通過推式開啟和/或交互來跟蹤收件人的行為，請確保在中啟用了跟蹤部分中的專用選項 [電子郵件活動](../building-journeys/journeys-message.md)。

>[!TAB 向市場活動添加推送]

1. 建立新的計畫市場活動或API觸發的市場活動，選擇 **[!UICONTROL 推送通知]** 選擇 **[!UICONTROL 應用表面]** 的下界。 [瞭解有關推送配置的詳細資訊](push-configuration.md)。

   ![](assets/push_create_3.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 從 **[!UICONTROL 屬性]** 編輯活動 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]**。

   ![](assets/push_create_4.png)

1. 按一下 **[!UICONTROL 選擇受眾]** 按鈕，來定義可用Adobe Experience Platform段清單中的目標受眾。 [了解更多](../segment/about-segments.md)。

1. 在 **[!UICONTROL 標識命名空間]** 欄位中，選擇要用於標識選定段中的個體的命名空間。 [了解更多](../event/about-creating.md#select-the-namespace)。

   ![](assets/push_create_5.png)

1. 市場活動旨在在特定日期或循環頻率上執行。 瞭解如何配置 **[!UICONTROL 計畫]** 你的競選團隊 [此部分](../campaigns/create-campaign.md#schedule)。

1. 從 **[!UICONTROL 操作觸發器]** 的子菜單。 **[!UICONTROL 頻率]** 您的推送通知：

   * 一次
   * 每日
   * 每週
   * 每月

1. 在市場活動配置螢幕中，按一下 **[!UICONTROL 編輯內容]** 按鈕來配置推送內容。 [設計推送通知](design-push.md)

1. 定義訊息內容後，您就可以使用測試設定檔進行預覽及測試。 

1. 當您的推送就緒時，請完成您的 [活動](../campaigns/create-campaign.md) 寄出去。

   要通過推式開啟和/或交互來跟蹤收件人的行為，請確保在中啟用了跟蹤部分中的專用選項 [活動](../campaigns/create-campaign.md)。

>[!ENDTABS]

**相關主題**

* [配置推送通道](push-gs.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)

## 快速傳送模式 {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="快速傳送模式"
>abstract="快速傳送模式讓您可以在推播管道上向 30M 以下的對象規模執行高速訊息傳送。"

快速交付模式（以前稱為「Burst」模式）是 [!DNL Journey Optimizer] 附加功能，允許通過市場活動快速發送大量推送消息。

當消息傳遞的延遲對業務至關重要時，當您想在手機上發送緊急推送警報時，會使用快速傳遞，例如向已安裝新聞頻道應用的用戶發送突發新聞。

有關使用快速交付模式時的效能的詳細資訊，請參閱 [Adobe Journey Optimizer產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html)。

### 先決條件 {#prerequisites}

快速傳遞消息傳遞附帶以下要求：

* 可快速交付 **[!UICONTROL 計畫]** 僅市場活動，且不適用於API觸發的市場活動，
* 推送消息中不允許個性化，
* 目標受眾必須包含少於3000萬個配置檔案，
* 您可以使用快速交付模式同時執行最多5個市場活動。

### 激活快速交付模式

1. 建立推送通知市場活動並在 **[!UICONTROL 快速交付]** 的雙曲餘切值。

![](assets/create-campaign-burst.png)

1. 配置消息內容並選擇目標受眾。 [瞭解如何建立市場活動](#create)

   >[!IMPORTANT]
   >
   >確保消息內容不包括任何個性化設定，並且受眾包含的配置檔案少於3000萬。

1. 像往常一樣查看並激活您的市場活動。 請注意，在test模式下，消息不會通過快速傳遞模式發送。