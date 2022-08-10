---
product: experience platform
solution: Experience Platform
title: 開始使用AI模型
description: 瞭解允許對優惠排序的AI模型
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 3188bc97b8103d2a01101a23d8c242a3e2924f76
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 4%

---

# 開始使用AI模型 {#ai-models}

[!DNL Journey Optimizer] 允許您使用經過培訓的模型系統來對給定配置檔案顯示報價。

此功能使您能夠建立不同的 **AI模型** 根據你的業務目標。 在決策中使用這些不同的基於目標的策略，經過訓練的模型系統將幫助您瞭解不同的人工智慧模型如何影響您的目標。

例如，您可以為電子郵件通道選擇AI模型，為推送通道選擇另一個模型。 對於每個渠道，經過培訓的模型系統將利用多個資料點來確定在給定位置應首先提供哪個優惠，而不是考慮優惠的優先順序分數或 [排序公式](create-ranking-formulas.md)。

## AI 模型類型 {#ai-model-types}

有兩種類型的AI模型可在 [!DNL Journey Optimizer]:

* **自動優化模型** 旨在為業務客戶設定之回報最大化(KPI)之服務。 該等主要表現指標可以以兌換率、收入等形式呈列。 此時，自動優化將重點放在優化服務點擊量，同時將服務轉換作為我們的目標。 自動優化是非個性化的，並且基於產品的「全局」效能進行優化。 [了解更多](auto-optimization-model.md)

* **個性化模型** 允許您定義業務目標並利用客戶資料來培訓面向業務的模型，以便提供個性化的服務並最大化KPI。 [了解更多](personalized-optimization-model.md)

>[!CAUTION]
>
>目前，只有選擇用戶才可以提前訪問個性化優化模型。

## 建立AI模型 {#create-ai-model}

建立和使用AI模型的主要步驟如下：

1. 建立將收集轉換和印象事件的資料集。 [了解更多](create-dataset.md)
1. 建立一個AI模型，該模型將利用資料集中的事件對優惠進行排序。 [了解更多](create-ranking-strategies.md)
1. 配置服務架構以自動捕獲事件。 [了解更多](schema-requirement.md)
1. 將AI模型分配給對合格報價進行評級的決定中的放置。 [了解更多](../offer-activities/configure-offer-selection.md)
