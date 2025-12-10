---
solution: Journey Optimizer
product: Journey Optimizer
title: 開始使用AI模型
description: 瞭解允許排名優惠方案的AI模型
feature: Ranking, Decisioning
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 07679823-2288-4528-b09a-12fd76a69482
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 18%

---

# 開始使用AI模型 {#ai-models}

[!DNL Journey Optimizer]可讓您使用經過訓練的模型系統，為特定設定檔顯示的優惠方案排名。

此功能可讓您根據您的業務目標建立不同的&#x200B;**AI模型**。 在決定中使用這些不同的目標型策略，經過訓練的模型系統將幫助您瞭解不同的AI模型如何影響您的目標。

<!--For example, you can select an AI model for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given decision policy?, rather than taking into account the offers' priority scores or a [ranking formula](create-ranking-formulas.md).

>[!IMPORTANT]
>
>For now, ranking models are not supported in Journey Optimizer authored channels.-->

## AI 模型類型 {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_exd_ai_model_type"
>title="選擇模式類型"
>abstract="選取您要建立的 AI 模式類型：「**自動最佳化**」可以根據過去的產品建議績效來最佳化產品建議，而「**個人化最佳化**」可根據對象和產品建議績效來最佳化和個人化產品建議。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="建立 AI 模型"

[!DNL Journey Optimizer]中有兩種可用的AI模型型別：

* **自動最佳化模型**&#x200B;旨在提供可最大化業務使用者端所設定回報(KPI)的優惠方案。 這些KPI可以是轉換率、收入等形式。 此時，自動最佳化的重點是最佳化優惠點按，並將優惠轉換作為我們的目標。 自動最佳化是非個人化的，並根據選件的「全域」效能進行最佳化。 [了解更多](auto-optimization-model.md)

* **個人化最佳化模型**&#x200B;可讓您定義業務目標，並利用客戶資料來訓練業務導向模型，以提供個人化優惠並最大化KPI。 [了解更多](personalized-optimization-model.md)

## 建立AI模型 {#create-ai-model}

能夠建立和使用AI模型的主要步驟如下：

1. 建立將收集轉換和曝光事件的資料集。 [了解更多](../data-collection/create-dataset.md)

1. 建立AI模型，運用資料集中的事件來排名選件。 [了解更多](create-ai-models.md)

1. 設定您的優惠方案綱要以自動擷取事件。 [了解更多](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >排名模型需要意見事件以體驗事件的形式傳送才能收集。 [進一步瞭解Decisioning資料集合](../data-collection/data-collection.md)

1. 將AI模型指派給選取策略，以便為符合資格的優惠進行排名。 [了解更多](../selection-strategies.md#select-ranking-method)
