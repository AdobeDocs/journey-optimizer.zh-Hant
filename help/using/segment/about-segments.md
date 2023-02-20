---
solution: Journey Optimizer
product: journey optimizer
title: 關於 Adobe Experience Platform 區段
description: 了解如何設定Adobe Experience Platform區段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 6c255d66fb89ba756add062d8a4315dd622fd8e7
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 1%

---

# 開始使用Adobe Experience Platform區段 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="區段"
>abstract="透過運用即時客戶設定檔資料，Adobe Experience Platform可讓您輕鬆建立目標區段，以擷取客戶的獨特行為和偏好。"

[!DNL Journey Optimizer]  可讓您直接使用Adobe Experience Platform的即時客戶設定檔資料，建立 **[!UICONTROL 區段]** 功能表，並將其用於您的歷程或行銷活動中。

此外，您也可以從分段服務本身建立區段。 了解更多 [Adobe Experience Platform區段服務檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## 在中使用區段 [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

您可以在 **[!DNL Journey Optimizer]** 以不同方式：

* 選擇區段作為 **行銷活動的對象**，訊息會傳送至屬於所選區段的所有個人。 [了解如何定義行銷活動的對象](../campaigns/create-campaign.md#define-the-audience-audience).

* 使用 **讀取區段** 歷程中的協調活動，讓區段中的所有個人都進入歷程並接收歷程中包含的訊息。

   假設您有「銀色客戶」區段。 透過此活動，您可以讓所有銀級客戶進入歷程，並傳送一系列個人化訊息。 [了解如何設定讀取區段活動](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* 使用 **區段資格** 歷程中的事件活動，根據Adobe Experience Platform區段入口和出口，讓個人進入或前進歷程。

   例如，您可以讓所有新銀級客戶進入歷程並傳送訊息。 有關如何使用此活動的詳細資訊，請參閱 [了解如何設定區段資格活動](../building-journeys/segment-qualification-events.md).

* 使用 **條件** 歷程中的活動，以根據區段成員資格來建立條件。 [了解如何在條件中使用區段](../building-journeys/condition-activity.md#using-a-segment).

## 受眾評估方法{#evaluation-method-in-journey-optimizer}

在Adobe Journey Optimizer中，受眾是使用下列兩種評估方法之一從區段定義產生：

* **串流細分**:當新資料流入系統時，區段的對象清單會即時保持最新。

   串流區段是持續進行的資料選取程式，會根據使用者活動更新您的區段。 建立並儲存區段後，會對傳入的資料套用區段定義至Journey Optimizer。 這表示個人的設定檔資料會隨著變更而新增或從區段中移除，確保您的目標對象始終具有相關性。

* **批次分段**:每24小時評估一次區段的對象清單。

   批次分段是串流分段的替代方法，可透過區段定義一次處理所有設定檔資料。 這會建立對象的快照，可儲存並匯出以供使用。 不過，與串流細分不同，批次細分不會持續即時更新對象清單，而批次處理後傳入的新資料要等到下一個批次處理後，才會反映在區段中。」

系統會根據評估區段規則的複雜度和成本，對每個區段定義進行批次分段和串流分段之間的決定。 您可以在 **[!UICONTROL 評價方法]** 欄。

![](assets/evaluation-method.png)

>[!NOTE]
>
>若 **[!UICONTROL 評價方法]** 欄未顯示，您需要使用清單右上方的設定按鈕來新增欄。

在您首次定義區段後，設定檔會在符合資格時新增至對象。

從先前的資料回填受眾最多需要24小時。 回填對象後，對象會持續保持最新狀態，且隨時準備進行目標定位。
