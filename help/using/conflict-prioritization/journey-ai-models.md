---
title: 歷程仲裁AI模型
description: 瞭解如何建立並使用AI模型來排名歷程以進行仲裁，以便根據AI驅動的分數為每個設定檔選取最佳歷程。
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="有限可用性" type="Informative"
hide: true
hidefromtoc: true
exl-id: 3e7c3069-b022-4709-936d-acaad56b5882
source-git-commit: a1b9d589773c168cc8ad0cfac0cd1ba178ae4bb6
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 4%

---

# 使用AI模型來排名歷程 {#journey-ai-models}

>[!AVAILABILITY]
>
>此功能目前處於「有限可用性」。 請聯絡您的 Adobe 代表以取得存取權。

[!DNL Adobe Journey Optimizer]可協助您控制當設定檔符合超出系統允許範圍的資格時，可輸入哪些歷程。 若要這麼做，您可以使用[規則集](rule-sets.md)來定義歷程專案或並行的最大值。 當設定檔符合的歷程數量超過上限允許時，指派給每個歷程的優先順序將決定選取的歷程。

除了使用優先順序之外，您也可以在排名公式中使用&#x200B;**AI模型**，以根據經過訓練的模型分數來動態排名歷程。

## 建立 AI 模型 {#create-ai-model}

<!--Do you need specific permissions to create AI models?
>[!CAUTION]
>
>To create, edit, or delete AI models, you must have the **Manage Ranking Strategies** permission. [Learn more](../administration/high-low-permissions.md#manage-ranking-strategies)-->

若要建立歷程排名的AI模型，請遵循下列步驟。

1. 建立將會收集轉換事件的資料集。 [了解作法](../experience-decisioning/data-collection/create-dataset.md)

1. 存取&#x200B;**[!UICONTROL 協調流程排名]**&#x200B;區段，然後選取&#x200B;**[!UICONTROL AI模型]**&#x200B;標籤。 隨即顯示先前建立的AI模型清單。

1. 按一下&#x200B;**[!UICONTROL 建立AI模型]**。

1. 為AI模型指定唯一名稱，並在必要時指定說明。

   ![顯示名稱和描述欄位的AI模型詳細資料](assets/journey-model-details.png){width="85%"}

   >[!NOTE]
   >
   >排名物件是將套用排名公式的實體。 依預設，排名物件設定為&#x200B;**[!UICONTROL 歷程]**。

<!--
1. Select the type of AI model you want to create:

    * **[!UICONTROL Auto-optimization]** optimizes based on past performance. [Learn more](../experience-decisioning/ranking/auto-optimization-model.md)
    * **[!UICONTROL Personalized optimization]** optimizes and personalizes based on audiences and performance. [Learn more](../experience-decisioning/ranking/personalized-optimization-model.md)-->

1. 在&#x200B;**[!UICONTROL 最佳化量度]**&#x200B;區段中，來自您的預設[!DNL Customer Journey Analytics] [資料檢視](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"}的所有量度都會顯示在清單中。 選取您想要最佳化模型的量度。

   ![最佳化量度下拉式清單，列出AI模型的Customer Journey Analytics量度](assets/journey-model-metrics.png){width="70%"}

   根據[!DNL Journey Optimizer]轉換率&#x200B;**排名** （轉換率=轉換事件總數/曝光事件總數）。 轉換率的計算方式為：

   * **曝光事件** （顯示的專案）
   * **轉換事件** （導致點按或轉換的專案）

   系統會使用Web SDK或Mobile SDK自動擷取這些事件。 進一步瞭解[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)概觀。

1. 選取轉換和曝光事件收集所在的資料集。 在[本節](../experience-decisioning/data-collection/create-dataset.md)中瞭解如何建立這類資料集。

   ![轉換和曝光事件的資料集選取範圍](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >下拉式清單中只會顯示從與&#x200B;**[!UICONTROL 體驗事件 — 主張互動]**&#x200B;欄位群組相關聯的結構描述建立的資料集。 您最多可以選取5個資料集。

1. <!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->選取要用來訓練AI模型的區段。

   >[!NOTE]
   >
   >您最多可以選取50個對象。

1. 儲存並啟動AI模型。

現在當您建立排名公式時，可以選擇AI模型。

## 在公式中參考AI模型來對歷程排名 {#reference-ai-model}

您現在可以設定AI模型作為參考，以建立排名公式，然後將公式指派給規則集並將規則集套用至歷程。 若要執行此操作，請遵循下列步驟。

1. 建立排名公式。 [了解作法](journey-ranking-formulas.md#create-journey-ranking-formula)

1. 使用&#x200B;**[!UICONTROL 選取AI模型]**&#x200B;按鈕來選取您要在公式中使用的AI模型。

   ![使用Select AI模型按鈕的歷程排名公式詳細資料](assets/journey-formula-ai-model.png){width="80%"}

1. 在&#x200B;**[!UICONTROL 條件]**&#x200B;區段中的至少一個區段中，定義條件並選取&#x200B;**[!UICONTROL AI模型分數]**&#x200B;作為排名方法。 例如，如果歷程有「促銷」標籤，則排名分數是AI模型分數。

   ![排名公式範例，其中Promo標籤准則使用AI模型分數作為排名方法](assets/journey-formula-ex-2.png){width="60%"}

1. 按一下&#x200B;**[!UICONTROL 建立]**&#x200B;以完成您的排名公式。

1. 現在建立規則集，並選取您建立為排名方法的公式。 [了解作法](journey-ranking-formulas.md#assign-formula-to-ruleset)

1. 建立歷程上限規則並儲存規則集。

1. 將規則集套用至所需的歷程並儲存。 [了解作法](journey-ranking-formulas.md#assign-rule-set-to-journey)

   >[!NOTE]
   >
   >一次只能將一個規則集套用至歷程。

套用上限時，使用此規則集的所有歷程都將使用參照所選AI模型的公式進行排名。
