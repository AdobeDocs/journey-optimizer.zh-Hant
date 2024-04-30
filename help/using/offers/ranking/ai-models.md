---
product: experience platform
solution: Experience Platform
title: 開始使用AI模型
description: 瞭解允許排名優惠方案的AI模型
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12f6c41252809bcc85bc076902f9a831a6c6e7d9
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 14%

---

# 開始使用AI模型 {#ai-models}

[!DNL Journey Optimizer] 可讓您使用經過訓練的模型系統，為要針對指定設定檔顯示的優惠方案排名。

此功能可讓您建立不同的 **AI模型** 根據您的業務目標而定。 在決定中使用這些不同的目標型策略，經過訓練的模型系統將幫助您瞭解不同的AI模型如何影響您的目標。

例如，您可以為電子郵件頻道選取一個AI模型，並為推播頻道選取另一個模型。 對於每個管道，經過訓練的模型系統將運用多個資料點來決定應先針對指定位置顯示哪個優惠方案，而不是考慮優惠方案的優先順序分數或 [排名公式](create-ranking-formulas.md).

>[!IMPORTANT]
>
>目前，Journey Optimizer編寫管道不支援排名模型。

## AI 模式類型 {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_type"
>title="選擇模式類型"
>abstract="選取您要建立的 AI 模式類型：「**自動最佳化**」可以根據過去的功能表現來最佳化功能選擇，而「**個人化最佳化**」可根據對象和功能表現來最佳化和個人化功能選擇。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="建立 AI 模型"

有兩種型別的AI模型可用於 [!DNL Journey Optimizer]：

* **自動最佳化模型** 旨在提供可大幅提升業務客戶所設定回報(KPI)的優惠方案。 這些KPI可以是轉換率、收入等形式。 此時，自動最佳化的重點是最佳化優惠點按，並將優惠轉換作為我們的目標。 自動最佳化是非個人化的，並根據選件的「全域」效能進行最佳化。 [了解更多](auto-optimization-model.md)

* **個人化最佳化模型** 可讓您定義業務目標，並利用客戶資料來訓練業務導向的模型，以提供個人化優惠並最大化KPI。 [了解更多](personalized-optimization-model.md)

## 建立AI模型 {#create-ai-model}

建立及使用AI模型的主要步驟如下：

1. 建立將收集轉換和曝光事件的資料集。 [了解更多](../data-collection/create-dataset.md)

1. 建立AI模型，運用資料集中的事件來排名選件。 [了解更多](create-ranking-strategies.md)

1. 設定您的優惠方案綱要以自動擷取事件。 [了解更多](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >排名模型需要意見事件以體驗事件的形式傳送才能收集。 [進一步了解決定管理資料收集](../data-collection/data-collection.md)

1. 將AI模型指派給決定中的位置，以排名合格的優惠。 [了解更多](../offer-activities/configure-offer-selection.md)
