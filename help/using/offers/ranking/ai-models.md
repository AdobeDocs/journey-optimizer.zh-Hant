---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 開始使用AI模型
description: 瞭解允許排名優惠方案的AI模型
badge: label="舊版" type="Informative"
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 15%

---

# 開始使用AI模型 {#ai-models}

[!DNL Journey Optimizer]可讓您使用經過訓練的模型系統，為特定設定檔顯示的優惠方案排名。

此功能可讓您根據您的業務目標建立不同的&#x200B;**AI模型**。 在決定中使用這些不同的目標型策略，經過訓練的模型系統將幫助您瞭解不同的AI模型如何影響您的目標。

例如，您可以為電子郵件頻道選取一個AI模型，並為推播頻道選取另一個模型。 對於每個管道，經過訓練的模型系統將運用多個資料點來決定應先針對指定位置顯示哪個優惠，而不是考慮優惠的優先順序分數或[排名公式](create-ranking-formulas.md)。

>[!IMPORTANT]
>
>目前，Journey Optimizer編寫管道不支援AI模型。

➡️ [在影片中探索此功能](#video)

## AI 模型類型 {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_type"
>title="選擇模式類型"
>abstract="選取您要建立的 AI 模式類型：「**自動最佳化**」可以根據過去的產品建議績效來最佳化產品建議，而「**個人化最佳化**」可根據對象和產品建議績效來最佳化和個人化產品建議。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="建立 AI 模型"

[!DNL Journey Optimizer]中有兩種可用的AI模型型別：

* **自動最佳化模型**&#x200B;旨在提供可最大化業務使用者端所設定回報(KPI)的優惠方案。 這些KPI可以是轉換率、收入等形式。 此時，自動最佳化的重點是最佳化優惠點按，並將優惠轉換作為我們的目標。 自動最佳化是非個人化的，並根據選件的「全域」效能進行最佳化。 [了解更多](auto-optimization-model.md)

* **個人化最佳化模型**&#x200B;可讓您定義業務目標，並利用客戶資料來訓練業務導向模型，以提供個人化優惠並最大化KPI。 [了解更多](personalized-optimization-model.md)

## 建立AI模型 {#create-ai-model}

建立及使用AI模型的主要步驟如下：

1. 建立將收集轉換和曝光事件的資料集。 [了解更多](../data-collection/create-dataset.md)

1. 建立AI模型，運用資料集中的事件來排名選件。 [了解更多](create-ranking-strategies.md)

1. 設定您的優惠方案綱要以自動擷取事件。 [了解更多](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >AI模型需要意見事件以體驗事件的形式傳送才能收集。 [進一步了解決定管理資料集合](../data-collection/data-collection.md)

1. 將AI模型指派給決定中的位置，以排名合格的優惠。 [了解更多](../offer-activities/configure-offer-selection.md)

## 操作說明影片 {#video}

瞭解如何為Offer Decisioning建立AI模型，以及如何將其套用至決策。

>[!VIDEO](https://video.tv.adobe.com/v/3445655?captions=chi_hant&quality=12)
