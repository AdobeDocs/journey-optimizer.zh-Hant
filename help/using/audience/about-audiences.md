---
solution: Journey Optimizer
product: journey optimizer
title: 關於 Adobe Experience Platform 對象
description: 了解如何使用 Adobe Experience Platform 對象
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 298562247af79b9dd504a957c197856d702d0f6b
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 93%

---

# 開始使用 Adobe Experience Platform 對象 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="對象"
>abstract="透過使用即時客戶設定檔資料，Adobe Experience Platform 能讓您輕鬆建置區段定義，以建立能夠擷取客戶獨特行為與偏好的目標的對象。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="選取行銷活動對象"
>abstract="此清單會顯示所有可用的Adobe Experience Platform對象。 選取行銷活動要定位的對象。 行銷活動中設定的訊息將傳送給屬於所選對象的所有個人。 [深入瞭解對象](../audience/about-audiences.md)"

[!DNL Journey Optimizer] 可讓您直接從&#x200B;**[!UICONTROL 對象]**&#x200B;選單，使用即時客戶設定檔資料來建置和使用 Adobe Experience Platform 對象，然後用於歷程或行銷活動。

在 [Adobe Experience Platform 細分服務文件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hant)中了解更多。

## 在 [!DNL Journey Optimizer] 中使用對象 {#segments-in-journey-optimizer}

您可以在 **[!DNL Journey Optimizer]** 中以不同方式善用對象：

* 選擇&#x200B;**行銷活動**&#x200B;的對象，將訊息傳送給屬於所選對象的所有個人。 [了解如何定義行銷活動的對象](../campaigns/create-campaign.md#define-the-audience-audience)。

* 在歷程中使用&#x200B;**讀取對象**&#x200B;協調流程活動，讓對象中的所有個人進入歷程並接收歷程中包含的訊息。

  假設您有「銀級客戶」對象。 透過此活動，您可以讓所有銀級客戶進入歷程，並向其傳送一系列個人化訊息。 [了解如何設定讀取對象活動](../building-journeys/read-audience.md#configuring-segment-trigger-activity)。

* 在歷程中使用&#x200B;**對象資格**&#x200B;事件活動，以根據 Adobe Experience Platform 對象進入和退出，讓個人進入歷程或在歷程中前進。

  例如，您可以讓所有新的銀級客戶進入歷程，並向其傳送訊息。 如需有關如何使用此活動的詳細資訊，請參閱[了解如何設定對象資格活動](../building-journeys/audience-qualification-events.md)。

* 在歷程中使用&#x200B;**條件**&#x200B;活動，以根據對象成員資格建置條件。 [了解如何在條件中使用對象](../building-journeys/condition-activity.md#using-a-segment)。

## 對象評估方法{#evaluation-method-in-journey-optimizer}

在 Adobe Journey Optimizer 中，使用下列兩種評估方法的其中之一從區段定義產生對象：

* **串流細分**：當新資料流入系統時，對象的設定檔清單會即時保持在最新狀態。

  串流細分是持續進行的資料選擇流程，其會根據使用者活動來更新對象。 在建置區段定義並儲存產生的對象後，區段定義會套用至傳入 Journey Optimizer 的資料。 這表示個人會隨著其設定檔資料變更而從對象中新增或移除，以確保目標對象總是相關。

* **批次細分**：每 24 小時都會評估對象的設定檔清單。

  批次細分是串流細分的替代方法，其可透過區段定義一次處理所有設定檔資料。 這會建立對象的快照，可儲存和匯出以供使用。 不過，和串流細分不同，批次細分不會持續即時更新對象清單，而且在批次程序後傳入的新資料，要等到下一個批次程序才會反映在對象中。

系統會根據評估區段定義規則的複雜性和成本，針對每個對象決定採用批次細分或串流細分。 您可以在對象清單的&#x200B;**[!UICONTROL 評估方法]**&#x200B;欄中，檢視每個對象的評估方法。

![](assets/evaluation-method.png)

>[!NOTE]
>
>如果未顯示&#x200B;**[!UICONTROL 評估方法]**&#x200B;欄，您需要使用清單右上方的設定按鈕予以新增。

在您首次定義對象後，設定檔會在符合資格時新增至對象中。

最多可能需要 24 小時才能從先前的資料回填對象。 回填對象之後，該對象會持續保持在最新狀態，並隨時準備好進行目標定位。
