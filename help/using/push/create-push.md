---
solution: Journey Optimizer
product: journey optimizer
title: 設定推播通知
description: 了解如何在Journey Optimizer中建立推播通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 15%

---

# 建立推播通知 {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="推播訊息建立"
>abstract="新增您的推播訊息並開始使用運算式編輯器對其進行個人化。"

## 在歷程或行銷活動中建立推播通知 {#create}

若要建立推播通知，請遵循下列步驟：

>[!BEGINTABS]

>[!TAB 新增推送至歷程]

1. 開啟您的歷程，然後從浮動視窗的「動作」區段拖放推播活動。

   ![](assets/push_create_1.png)

1. 提供訊息的基本資訊（標籤、說明、類別），然後選擇要使用的訊息表面。

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >如果您要從歷程傳送推播通知，您可以運用Adobe Journey Optimizer的「傳送時間最佳化」功能，根據歷史開啟率和點按率預測傳送訊息的最佳時機，以最大化參與。 [了解如何使用傳送時間最佳化](../building-journeys/journeys-message.md#send-time-optimization)

   如需如何設定歷程的詳細資訊，請參閱 [本頁](../building-journeys/journey-gs.md)

1. 在歷程設定畫面中，按一下 **[!UICONTROL 編輯內容]** 按鈕來設定推播內容。 [設計推播通知](design-push.md)

1. 定義訊息內容後，您就可以使用測試設定檔進行預覽及測試。 

1. 推送就緒時，請完成 [歷程](../building-journeys/journey-gs.md) 來發送。

   若要透過推播開啟和/或互動來追蹤收件者的行為，請確定已在 [電子郵件活動](../building-journeys/journeys-message.md).

>[!TAB 新增推送至促銷活動]

1. 建立新的排程或API觸發促銷活動，請選取 **[!UICONTROL 推播通知]** 作為您的動作，並選取 **[!UICONTROL 應用程式表面]** 來使用。 [進一步了解推播設定](push-configuration.md).

   ![](assets/push_create_3.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 從 **[!UICONTROL 屬性]** 區段，編輯您的促銷活動 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]**.

   ![](assets/push_create_4.png)

1. 按一下 **[!UICONTROL 選取對象]** 按鈕，從可用的Adobe Experience Platform區段清單中定義要鎖定的對象。 [了解更多](../segment/about-segments.md)。

1. 在 **[!UICONTROL 身分命名空間]** 欄位中，選擇要使用的命名空間，以識別所選區段中的個人。 [了解更多](../event/about-creating.md#select-the-namespace)。

   ![](assets/push_create_5.png)

1. 促銷活動設計為在特定日期或循環頻率上執行。 了解如何設定 **[!UICONTROL 排程]** 在 [本節](../campaigns/create-campaign.md#schedule).

1. 從 **[!UICONTROL 動作觸發器]** 菜單，選擇 **[!UICONTROL 頻率]** 推播通知的：

   * 一次
   * 每日
   * 每週
   * 每月

1. 在促銷活動設定畫面中，按一下 **[!UICONTROL 編輯內容]** 按鈕來設定推播內容。 [設計推播通知](design-push.md)

1. 定義訊息內容後，您就可以使用測試設定檔進行預覽及測試。 

1. 推送就緒時，請完成 [行銷活動](../campaigns/create-campaign.md) 來發送。

   若要透過推播開啟和/或互動來追蹤收件者的行為，請確定已在 [行銷活動](../campaigns/create-campaign.md).

>[!ENDTABS]

**相關主題**

* [設定推播通道](push-gs.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)

## 快速傳送模式 {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="快速傳送模式"
>abstract="快速傳送模式讓您可以在推播管道上向 30M 以下的對象規模執行高速訊息傳送。"

快速傳送模式（歷程中先前稱為突發模式）是 [!DNL Journey Optimizer] 可透過促銷活動以大量傳送非常快速的推送訊息的附加元件。

當訊息傳送延遲是業務關鍵型時，或您想在行動電話上傳送緊急推播警報（例如，向已安裝您的新聞頻道應用程式的使用者傳送重大新聞），則會使用快速傳送。

如需使用快速傳送模式時效能的詳細資訊，請參閱 [Adobe Journey Optimizer產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html).

### 先決條件 {#prerequisites}

快速傳遞報文傳送附帶下列要求：

* 可快速傳送 **[!UICONTROL 已排程]** 僅限促銷活動，且不適用於API觸發的促銷活動、
* 推送訊息中不允許任何個人化，
* 目標受眾必須包含少於3000萬個設定檔，
* 您可以使用快速傳送模式，同時執行最多5個促銷活動。

### 啟動快速傳遞模式

1. 建立推播通知促銷活動並切換 **[!UICONTROL 快速傳遞]** 選項。

![](assets/create-campaign-burst.png)

1. 設定訊息內容並選取要鎖定的對象。 [了解如何建立行銷活動](#create)

   >[!IMPORTANT]
   >
   >確保訊息內容不包含任何個人化，且對象包含少於3000個設定檔。

1. 照常檢閱並啟動您的行銷活動。 請注意，在測試模式中，訊息不會透過快速傳送模式傳送。