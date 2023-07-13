---
solution: Journey Optimizer
product: journey optimizer
title: 關於Adobe Experience Platform對象
description: 瞭解如何使用Adobe Experience Platform受眾
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# 開始使用Adobe Experience Platform對象 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="對象"
>abstract="善用即時客戶個人檔案資料，Adobe Experience Platform可讓您輕鬆建立區段定義，以建立目標受眾，擷取客戶的獨特行為和偏好。"

[!DNL Journey Optimizer] 可讓您直接從使用即時客戶個人檔案資料來建置和運用Adobe Experience Platform對象 **[!UICONTROL 受眾]** 選單，並用於您的歷程或行銷活動。

進一步瞭解 [Adobe Experience Platform Segmentation Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## 在中使用對象 [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

您可以善用下列專案的對象： **[!DNL Journey Optimizer]** 以不同方式：

* 選擇受眾 **行銷活動**，會將訊息傳送給屬於所選對象的所有個人。 [瞭解如何定義行銷活動的對象](../campaigns/create-campaign.md#define-the-audience-audience).

* 使用 **讀取對象** 歷程中的協調活動，讓對象中的所有個人進入歷程並接收歷程中包含的訊息。

  假設您有「銀級客戶」受眾。 透過此活動，您可以讓所有銀級客戶進入歷程，並向他們傳送一系列個人化訊息。 [瞭解如何設定讀取對象活動](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* 使用 **對象資格** 歷程中的事件活動，用於根據Adobe Experience Platform受眾進入和退出，讓個人進入歷程或是在歷程中前進。

  例如，您可以讓所有新的銀級客戶進入歷程，並向他們傳送訊息。 有關如何使用此活動的詳細資訊，請參閱 [瞭解如何設定對象資格活動](../building-journeys/audience-qualification-events.md).

* 使用 **條件** 歷程中的活動，以根據對象成員資格建立條件。 [瞭解如何在條件中使用對象](../building-journeys/condition-activity.md#using-a-segment).

## 對象評估方法{#evaluation-method-in-journey-optimizer}

在Adobe Journey Optimizer中，對象是使用下列兩種評估方法之一從區段定義產生的：

* **串流區段**：當新資料流入系統時，對象的設定檔清單會即時保持最新。

  串流細分是持續的資料選擇過程，會更新您的對象以回應使用者活動。 在建立區段定義並儲存產生的對象後，區段定義會套用至傳入Journey Optimizer的資料。 這表示個人會隨著其設定檔資料變更而從對象中新增或移除，以確保您的目標對象永遠相關。

* **批次細分**：每24小時評估對象的設定檔清單。

  批次細分是可透過區段定義一次處理所有設定檔資料的串流細分的替代方法。 這會建立對象的快照，可儲存並匯出以供使用。 不過，和串流細分不同，批次細分不會持續即時更新對象清單，而且批次程式之後傳入的新資料要等到下一個批次程式才會反映在對象中。」

系統會根據評估區段定義規則的複雜性和成本，針對每個對象，決定批次區段和串流區段之間的劃分。 您可以檢視中每個對象的評估方法 **[!UICONTROL 評估方法]** 對象清單的欄。

![](assets/evaluation-method.png)

>[!NOTE]
>
>如果 **[!UICONTROL 評估方法]** 欄不顯示，您需要使用清單右上角的設定按鈕新增它。

在您首次定義對象後，設定檔符合資格時就會新增到對象中。

從先前資料回填對象最長可能需要24小時。 回填對象後，對象會持續保持最新狀態，並隨時準備好進行目標定位。
