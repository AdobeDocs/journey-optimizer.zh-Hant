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
source-git-commit: afc09bbcb76d53404574bb53c0a896109cd7f1da
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 3%

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

   ![AI模型詳細資料窗格，包含名稱和說明欄位](assets/journey-model-details.png){width="80%"}

   >[!NOTE]
   >
   >排名物件是將套用排名公式的實體。 依預設，排名物件設定為&#x200B;**[!UICONTROL 歷程]**。

<!--
1. Select the type of AI model you want to create:

    * **[!UICONTROL Auto-optimization]** optimizes based on past performance. [Learn more](../experience-decisioning/ranking/auto-optimization-model.md)
    * **[!UICONTROL Personalized optimization]** optimizes and personalizes based on audiences and performance. [Learn more](../experience-decisioning/ranking/personalized-optimization-model.md)-->

1. 在&#x200B;**[!UICONTROL 最佳化量度]**&#x200B;中，來自您的預設[!DNL Customer Journey Analytics] [資料檢視](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"}的所有量度都會顯示在清單中。 選取您想要最佳化模型的量度。

   ![AI模型詳細資料窗格，包含名稱和說明欄位](assets/journey-model-metrics.png){width="80%"}

   根據[!DNL Journey Optimizer]轉換率&#x200B;**排名** （轉換率=轉換事件總數/曝光事件總數）。 轉換率的計算方式為：

   * **曝光事件** （顯示的專案）
   * **轉換事件** （導致點按或轉換的專案）

   系統會使用Web SDK或Mobile SDK自動擷取這些事件。 進一步瞭解[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant)概觀。

1. 選取轉換和曝光事件收集所在的資料集。 在[本節](../experience-decisioning/data-collection/create-dataset.md)中瞭解如何建立這類資料集。

   ![轉換和曝光事件的資料集選取範圍](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >下拉式清單中只會顯示從與&#x200B;**[!UICONTROL 體驗事件 — 主張互動]**&#x200B;欄位群組（先前稱為mixin）相關聯的結構描述建立的資料集。

1. &#x200B;<!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->選取要用來訓練AI模型的區段。

   >[!NOTE]
   >
   >您最多可以選取50個對象。

1. 儲存並啟動AI模型。

現在當您建立排名公式時，可以選擇AI模型。

## 選取排名公式的AI模型 {#select-ai-model-for-ranking-formula}

您現在可以將AI模型設定為參考，以建立排名公式。 請遵循下列步驟。

1. 建立排名公式。 [了解作法](journey-ranking-formulas.md#create-journey-ranking-formula)

1. 使用&#x200B;**[!UICONTROL 選取AI模型]**&#x200B;按鈕來選取您要使用的AI模型。

   ![包含AI模型選擇的歷程排名公式詳細資料窗格](assets/journey-formula-ai-model.png){width="80%"}

1. 在&#x200B;**[!UICONTROL 條件]**&#x200B;區段中的至少一個區段中，定義條件並選取&#x200B;**[!UICONTROL AI模型分數]**&#x200B;作為排名方法。 例如，如果歷程有「促銷」標籤，則排名分數是AI模型分數。

   ![排名公式：促銷標籤使用AI模型分數](assets/journey-formula-ex-2.png){width="60%"}

1. 按一下&#x200B;**[!UICONTROL 建立]**&#x200B;以完成您的排名公式。

## 將AI模型指派給規則集 {#assign-ai-model-to-ruleset}

若要使用AI模型來排名您的歷程，您必須將參考此AI模型的公式指派給規則集。

1. 從&#x200B;**[!UICONTROL 商業規則]**&#x200B;功能表，建立您要用於歷程仲裁的規則集。 [了解作法](rule-sets.md#Create)

1. 請務必選取&#x200B;**[!UICONTROL 歷程]**&#x200B;網域。

1. 在規則集屬性中，將&#x200B;**[!UICONTROL 排名方法]**&#x200B;設定為&#x200B;**[!UICONTROL 公式]** （而非&#x200B;**[!UICONTROL 優先順序]**）。

1. 選取使用您從下拉式清單建立的AI模型的公式。

1. 建立您要新增至規則集的歷程上限規則。 [了解作法](journey-capping.md#create-rule)

1. 儲存規則集。

現在，使用AI模型的公式已指派給規則集。 然後，您可以將該規則集套用至您的歷程。

## 將規則集套用至歷程 {#assign-rule-set-to-journey}

若要將規則集指派給歷程，請遵循下列步驟。

1. 建立或開啟您要指派規則集的歷程。 [了解如何建立歷程](../building-journeys/journey-gs.md)

1. 在歷程屬性中，從下拉式清單中選取規則集。 [瞭解如何進行](journey-capping.md#apply-capping)。

   >[!NOTE]
   >
   >一次只能將一個規則集套用至歷程。

1. 儲存歷程。

套用上限時，使用此規則集的所有歷程都會使用AI模型，以選取的公式進行排名。
