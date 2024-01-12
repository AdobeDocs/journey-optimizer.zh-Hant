---
solution: Journey Optimizer
product: journey optimizer
title: 關於 Adobe Experience Platform 對象
description: 了解如何使用 Adobe Experience Platform 對象
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: d18b24f6afcd64745fe7bd3b3bc9832342b91c7b
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 47%

---

# 開始使用 Adobe Experience Platform 對象 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="對象"
>abstract="透過使用即時客戶設定檔資料，Adobe Experience Platform 能讓您輕鬆建置區段定義，以建立能夠擷取客戶獨特行為與偏好的目標的對象。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="選取行銷活動的對象"
>abstract="此清單顯示所有可用的 Adobe Experience Platform 對象。為你的行銷活動選取目標對象。在行銷活動中設定的訊息將傳送給屬於所選對象的所有個人。[進一步了解對象](../audience/about-audiences.md)"

受眾是指一組具有類似行為和/或特徵的人。 它們可由Adobe Experience Platform使用區段定義或受眾組合來產生，或從CSV檔案匯入。 進一步瞭解 [Adobe Experience Platform Segmentation Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hant){target="_blank"}.

[!DNL Journey Optimizer] 可讓您直接從建置Adobe Experience Platform對象 **[!UICONTROL 受眾]** 選單，並將其運用在您的歷程或行銷活動中。

## 在 [!DNL Journey Optimizer] 中使用對象 {#segments-in-journey-optimizer}

您可以在行銷活動中選取使用產生的任何Adobe Experience Platform對象 [區段定義](../audience/creating-a-segment-definition.md).

>[!NOTE]
>
>此外，您也可以鎖定使用建立的Adobe Experience Platform對象 [對象組合](../audience/get-started-audience-orchestration.md) 或 [已從CSV檔案上傳](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}. 這些功能目前以 Private Beta 的形式提供。


您可以在 **[!DNL Journey Optimizer]** 中以不同方式善用對象：

* 選擇&#x200B;**行銷活動**&#x200B;的對象，將訊息傳送給屬於所選對象的所有個人。 [了解如何定義行銷活動的對象](../campaigns/create-campaign.md#define-the-audience-audience)。

* 在歷程中使用&#x200B;**讀取對象**&#x200B;協調流程活動，讓對象中的所有個人進入歷程並接收歷程中包含的訊息。

  假設您有「銀級客戶」對象。 透過此活動，您可以讓所有銀級客戶進入歷程，並向其傳送一系列個人化訊息。 [了解如何設定讀取對象活動](../building-journeys/read-audience.md#configuring-segment-trigger-activity)。

* 在歷程中使用&#x200B;**對象資格**&#x200B;事件活動，以根據 Adobe Experience Platform 對象進入和退出，讓個人進入歷程或在歷程中前進。

  例如，您可以讓所有新的銀級客戶進入歷程，並向其傳送訊息。 如需有關如何使用此活動的詳細資訊，請參閱[了解如何設定對象資格活動](../building-journeys/audience-qualification-events.md)。

* 在歷程中使用&#x200B;**條件**&#x200B;活動，以根據對象成員資格建置條件。 [了解如何在條件中使用對象](../building-journeys/condition-activity.md#using-a-segment)。

## 對象評估方法 {#evaluation-method-in-journey-optimizer}

在Adobe Journey Optimizer中，使用下列三種評估方法之一，從區段定義產生對象。

+++ 串流區段

當新資料流入系統時，對象的設定檔清單會即時保持最新。

串流細分是持續進行的資料選擇流程，其會根據使用者活動來更新對象。 在建置區段定義並儲存產生的對象後，區段定義會套用至傳入 Journey Optimizer 的資料。 這表示當個人設定檔資料變更時，將會在對象中新增或移除該個人，以確保您的目標對象永遠相關。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"}

>[!NOTE]
>
>請務必使用正確事件作為串流細分條件。 [了解更多](#streaming-segmentation-events-guardrails)

+++

+++ 批次分段

每24小時評估對象的設定檔清單。

批次細分是串流細分的替代方法，其可透過區段定義一次處理所有設定檔資料。 這會建立對象的快照，可儲存和匯出以供使用。 不過，和串流區段不同，批次區段不會持續即時更新對象清單，而且批次程式之後傳入的新資料不會反映在對象中，直到下一個批次程式為止。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#batch){target="_blank"}

+++

+++ 邊緣分段

邊緣區段是即時評估Adobe Experience Platform中區段的能力 [在邊緣](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant){target="_blank"}, enabling same-page and next-page personalization use cases. Currently only select query types can be evaluated with edge segmentation. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/edge-segmentation.html#query-types){target="_blank"}

+++

如果您知道要使用的評估方法，請使用下拉式清單選取它。 您也可以按一下帶有放大鏡的瀏覽圖示資料夾圖示，以檢視可用區段定義評估方法的清單。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#segment-properties){target="_blank"}

![](assets/evaluation-methods.png)

<!--The determination between batch segmentation and streaming segmentation is made by the system for each audience, based on the complexity and the cost of evaluating the segment definition rule. You can view the evaluation method for each audience in the **[!UICONTROL Evaluation method]** column of the audience list.
    
![](assets/evaluation-method.png)

>[!NOTE]
>
>If the **[!UICONTROL Evaluation method]** column does not display, you  need to add it using configuration button on the top right of the list.-->

在您首次定義對象後，設定檔會在符合資格時新增至對象中。

最多可能需要 24 小時才能從先前的資料回填對象。 回填對象之後，該對象會持續保持在最新狀態，並隨時準備好進行目標定位。

### 串流區段的事件使用情形 {#streaming-segmentation-events-guardrails}

串流區段對於具有高價值使用案例的即時個人化相當實用。 不過，請務必選擇正確的 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events){target="_blank"} 以用作分段條件。

因此，為了串流區段最佳效能，請避免使用以下事件：

* **訊息已開啟** 互動型別事件

  在建立受眾時，請使用 **訊息已開啟** 互動事件變得不可靠，因為它們不是使用者活動的實際指標，可能會對細分效能產生負面影響。 瞭解本課程內容 [Adobe部落格](https://blog.adobe.com/en/publish/2021/06/24/what-apples-mail-privacy-protection-means-for-email-marketers){target="_blank"}.

  因此，Adobe建議不要使用 **訊息已開啟** 串流區段的互動事件。 請改用真正的使用者活動訊號，例如點選、購買或信標資料。

* **已傳送訊息** 意見反應狀態事件

  此 **已傳送訊息** 回饋事件通常用於在傳送電子郵件之前進行頻率或隱藏檢查。 Adobe建議避免使用這項功能，因為它會對效能造成壓力，並可能導致系統效能降低。

  因此，對於頻率或隱藏邏輯，請使用商業規則，而不是 **已傳送訊息** 意見反應事件。 請注意，個別設定檔的每日頻率上限即將推出，以補充商業規則的現有每月頻率。

>[!NOTE]
>
>您可以使用 **訊息已開啟** 和 **已傳送訊息** 批次分段中的事件沒有任何效能問題。
