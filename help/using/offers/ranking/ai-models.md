---
product: experience platform
solution: Experience Platform
title: 開始使用AI模型
description: 瞭解允許對優惠排序的AI模型
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 3%

---

# 開始使用AI模型 {#ai-models}

[!DNL Journey Optimizer] 允許您使用經過培訓的模型系統來對給定配置檔案顯示報價。

此功能使您能夠建立不同的 **AI模型** 根據你的業務目標。 在決策中使用這些不同的基於目標的策略，經過訓練的模型系統將幫助您瞭解不同的人工智慧模型如何影響您的目標。

例如，您可以為電子郵件通道選擇AI模型，為推送通道選擇另一個模型。 對於每個渠道，經過培訓的模型系統將利用多個資料點來確定在給定位置應首先提供哪個優惠，而不是考慮優惠的優先順序分數或 [排序公式](create-ranking-formulas.md)。

## AI模型類型 {#ai-model-types}

目前， [!DNL Journey Optimizer]**提供一種AI模型， **自動優化**&#x200B;根據過去的產品效能優化產品。 有關此類AI模型的詳細資訊，請參閱 [此部分](auto-optimization-model.md)。

## 建立AI模型 {#create-ai-model}

建立和使用AI模型的主要步驟如下：

1. 建立將收集轉換和印象事件的資料集。 [了解更多](create-dataset.md)
1. 建立一個AI模型，該模型將利用資料集中的事件對優惠進行排序。 [了解更多](create-ranking-strategies.md)
1. 配置服務架構以自動捕獲事件。 [了解更多](schema-requirement.md)
1. 將AI模型分配給對合格報價進行評級的決定中的放置。 [了解更多](../offer-activities/configure-offer-selection.md)
