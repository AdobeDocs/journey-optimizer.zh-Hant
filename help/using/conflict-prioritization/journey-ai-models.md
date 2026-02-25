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
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 4%

---

# 使用AI模型來排名歷程 {#journey-ai-models}

>[!AVAILABILITY]
>
>此功能目前處於「有限可用性」。 請聯絡您的 Adobe 代表以取得存取權。

[!DNL Adobe Journey Optimizer]可協助您控制當設定檔符合超出系統允許範圍的資格時，可輸入哪些歷程。 若要這麼做，您可以使用[規則集](rule-sets.md)來定義歷程專案或並行的最大值。 當設定檔符合的歷程數量超過上限允許時，指派給每個歷程的優先順序將決定選取的歷程。

您可以使用&#x200B;**AI模型**，根據訓練好的模型分數來動態排名歷程，而不使用優先順序或排名公式。 您可以從UI中的&#x200B;**[!UICONTROL 協調流程排名]**&#x200B;區段建立AI模型，並在規則集中使用這些模型，以將模型套用至歷程。

如需[!DNL Journey Optimizer]中可用AI模型型別的概觀，請參閱「決策」一節中的[開始使用AI模型](../experience-decisioning/ranking/ai-models.md#ai-model-types)。

## 建立 AI 模型 {#create-ai-model}

>[!CAUTION]
>
>若要建立、編輯或刪除AI模型，您必須擁有&#x200B;**管理排名策略**&#x200B;許可權。 [了解更多](../administration/high-low-permissions.md#manage-ranking-strategies)

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

1. **[!UICONTROL 最佳化量度]**&#x200B;區段提供有關AI模型所使用的轉換事件的資訊。 根據[!DNL Journey Optimizer]轉換率&#x200B;**排名** （轉換率=轉換事件總數/曝光事件總數）。 轉換率的計算方式為：

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
   >您最多可以選取5個對象。

1. 儲存並啟動AI模型。

現在當您設定規則集時，可使用AI模型。

## 將AI模型指派給規則集 {#assign-ai-model-to-ruleset}

若要使用AI模型來排名您的歷程，您必須在公式中使用它，並將此公式指派給規則集。

1. 使用您建立的AI模型建立排名公式。 [了解作法](journey-ranking-formulas.md#create-journey-ranking-formula)

1. 從&#x200B;**[!UICONTROL 商業規則]**&#x200B;功能表，建立您要用於歷程仲裁的規則集。 [了解作法](rule-sets.md#Create)

1. 請務必選取&#x200B;**[!UICONTROL 歷程]**&#x200B;網域。

1. 在規則集屬性中，將&#x200B;**[!UICONTROL 排名方法]**&#x200B;設定為&#x200B;**[!UICONTROL 公式]** （而非&#x200B;**[!UICONTROL 優先順序]**）。

1. 從下拉式清單中選取使用您建立的AI模型的公式。

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
