---
product: experience platform
solution: Experience Platform
title: 建立 AI 模型
description: 瞭解如何建立AI模型來對優惠方案進行排名
badge: label="舊版" type="Informative"
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 23%

---

# 建立 AI 模型 {#ai-rankings}

[!DNL Journey Optimizer]可讓您建立&#x200B;**AI模型**，以根據您的業務目標來排名優惠。

>[!CAUTION]
>
>若要建立、編輯或刪除AI模型，您必須擁有&#x200B;**管理排名策略**&#x200B;許可權。 [了解更多](../../administration/high-low-permissions.md#manage-ranking-strategies)

## 建立 AI 模型 {#create-ranking-strategy}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_metric"
>title="最佳化量度"
>abstract="[!DNL Journey Optimizer] 根據&#x200B;**轉換率**&#x200B;對產品建議進行排名 (轉換率 = 轉換事件總數/曝光事件總數)。轉換率使用兩種類型的量度來計算：**曝光事件** (所顯示的產品建議) 和&#x200B;**轉換事件** (讓使用者透過電子郵件或網頁進行點選的產品建議)。我們會透過所提供的 Web SDK 或 Mobile SDK 來自動擷取這些事件。"

若要建立AI模型，請遵循下列步驟：

1. 建立將會收集轉換事件的資料集。 [了解作法](../data-collection/create-dataset.md)

1. 在&#x200B;**[!UICONTROL 元件]**&#x200B;功能表中，存取&#x200B;**[!UICONTROL 排名]**&#x200B;標籤，然後選取&#x200B;**[!UICONTROL AI模型]**。

   ![](../assets/ai-ranking-list.png)

   列出目前為止建立的所有AI模型。

1. 按一下&#x200B;**[!UICONTROL 建立AI模型]**&#x200B;按鈕。

1. 指定AI模型的唯一名稱和說明，然後選取您要建立的AI模型型別：

   * **[!UICONTROL 自動最佳化]**&#x200B;會根據過去的優惠效能來最佳化優惠。 [了解更多](auto-optimization-model.md)
   * **[!UICONTROL 個人化最佳化]**&#x200B;會根據對象和優惠效能來最佳化和個人化優惠。 [了解更多](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >**[!UICONTROL 最佳化量度]**&#x200B;區段提供有關AI模型用來計算優惠排名之轉換事件的資訊。
   >
   >[!DNL Journey Optimizer] 根據&#x200B;**轉換率**&#x200B;對產品建議進行排名 (轉換率 = 轉換事件總數/曝光事件總數)。轉換率是使用兩種量度型別來計算：
   >* **曝光事件** （顯示的選件）
   >* **轉換事件** （透過電子郵件或網頁產生點按的優惠方案）。
   >
   >系統會使用所提供的網頁SDK或行動SDK自動擷取這些事件。 請在[Adobe Experience Platform Web SDK總覽](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant)中進一步瞭解此專案。

1. 選取轉換和曝光事件收集所在的資料集。 瞭解如何在[此區段](../data-collection/create-dataset.md)中建立這類資料集。<!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >下拉式清單中只會顯示從與&#x200B;**[!UICONTROL 體驗事件 — 主張互動]**&#x200B;欄位群組（先前稱為mixin）相關聯的結構描述建立的資料集。

1. 如果您正在建立&#x200B;**[!UICONTROL 個人化最佳化]** AI模型，請選取要用來訓練AI模型的區段。

   ➡️ [在影片中探索此功能](#video)

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >您最多可以選取5個對象。

1. 儲存並啟動AI模型。

   ![](../assets/ai-ranking-save-activate.png)

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

現在，每次顯示和/或按一下優惠時，您都希望&#x200B;**[!UICONTROL 體驗事件 — 主張互動]**&#x200B;欄位群組使用[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=zh-Hant#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"}或Mobile SDK自動擷取對應的事件。

若要能夠在事件型別（顯示優惠或按一下優惠）中傳送，您必須在傳送至Adobe Experience Platform的體驗事件中，為每個事件型別設定正確的值。 [了解作法](../data-collection/schema-requirement.md)

## 作法影片 {#video}

瞭解如何建立個人化最佳化模型，以及如何將其套用至決定。

>[!VIDEO](https://video.tv.adobe.com/v/3445962?captions=chi_hant&quality=12)
