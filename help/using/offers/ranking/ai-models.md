---
product: experience platform
solution: Experience Platform
title: 開始使用AI模型
description: 了解可將選件排名的AI模型
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12bc2373ac5c391764df3880c5c87666a19e99b2
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# 開始使用AI模型 {#ai-models}

[!DNL Journey Optimizer] 可讓您使用經過訓練的模型系統來排名選件，以針對指定的設定檔顯示。

此功能可讓您建立不同的 **AI模型** 根據您的業務目標。 在決策中使用這些不同的目標型策略，經過訓練的模型系統將幫助您了解不同的AI模型如何影響您的目標。

例如，您可以為電子郵件通道選取一個AI模型，為推播通道選取另一個模型。 對於每個管道，經過訓練的模型系統將運用多個資料點來決定應先針對指定版位呈現哪個優惠方案，而非考慮優惠方案的優先順序分數或 [排名公式](create-ranking-formulas.md).

## AI模型類型 {#ai-model-types}

提供兩種AI模型，位於 [!DNL Journey Optimizer]:

* **自動最佳化模型** 旨在提供由企業客戶所設定的可發揮最大回報(KPI)的優惠方案。 這些KPI可以是轉換率、收入等形式。 此時，自動最佳化著重於以選件轉換作為目標來最佳化選件點擊。 自動最佳化是非個人化的，且會根據選件的「全域」效能來最佳化。 [深入了解](auto-optimization-model.md)

* **個人化模型** 可讓您定義業務目標，並運用客戶資料來訓練以業務為導向的模型，以提供個人化優惠方案並最大化KPI。 [深入了解](personalized-optimization-model.md)

   >[!CAUTION]
   >
   >個人化最佳化模型目前僅供選取使用者提早存取。

## 建立AI模型 {#create-ai-model}

建立和使用AI模型的主要步驟如下：

1. 建立將收集轉換和曝光事件的資料集。 [深入了解](create-dataset.md)
1. 建立AI模型，以運用資料集中的事件來排名選件。 [深入了解](create-ranking-strategies.md)
1. 設定優惠方案結構以自動擷取事件。 [深入了解](schema-requirement.md)
1. 將AI模型指派給排名合格優惠方案的決策中的版位。 [深入了解](../offer-activities/configure-offer-selection.md)
