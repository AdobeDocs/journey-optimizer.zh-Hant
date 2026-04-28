---
title: 實驗報告中使用的統計計算
description: 深入瞭解A/B測試和多臂吃角子老虎機
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 1f7b74d2-77c3-4113-8e6a-1e2a95117748
source-git-commit: a659f596c0d37f4b91ec41e52c02c8385f6ae16b
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 19%

---

# A/B 和多臂吃角子老虎機實驗 {#mab-vs-ab}

>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="實驗類型"
>abstract="實驗類型會決定在測試期間，流量於處理之間分配的方式。 選擇最符合您目標的方法：</br><b>A/B 實驗</b>：依照您定義的處理方式與測量績效，分割流量，直到結果具有統計顯著性為止。 最適合在控制式比較中了解哪個處理效果更好。</br><b>多臂吃角子老虎機</b>：隨著資料收集，將流量轉移到績效更好的處理，在速度和最佳化間取得平衡。 想要在實驗期間將轉換次數最大化時非常有用。</br><b>自備多臂吃角子老虎機</b>：使用您自己的演算法決定流量分配，在使用自訂模型或策略時即可保有彈性。"

此頁面提供&#x200B;**A/B**&#x200B;與&#x200B;**多臂吃角子老虎機**&#x200B;實驗的詳細比較，說明其各自的優點、限制，以及每種方法最有效的案例。


## A/B {#ab-test}

傳統A/B實驗涉及在處理間平均分割流量，並維持此配置，直到實驗結束為止。 一旦達到統計顯著性，就會識別成功處理並隨後進行縮放。

### 優點

傳統A/B實驗的關鍵優勢包括：

* **統計嚴格**

  固定設計提供定義清晰的錯誤率和信賴區間。

  假設測試架構（例如95%信賴度）更易於套用和理解。

  適當支援的實驗可降低誤報的可能性。

* **簡單性**

  方法簡單明瞭，設計與執行都相當容易。

  結果可明確傳達給非技術利害關係人。

* **完整的資料彙集**

  每個處理方法都能獲得足夠的曝光度，不僅可分析成功變體，還可分析表現缺佳的替代方案。

  這些額外的資訊可為長期策略性決定提供資訊。

* **偏誤控制項**

  固定配置會降低偏誤的易感性，例如「獲勝者的詛咒」或回歸至平均值。

### 限制

傳統A/B實驗的主要限制如下：

* **機會成本**

  相當一部分的流量會導向不良的處理，可能會減少測試期間的轉換或收入。

  在實驗結束前，無法實施成功處理。

* **固定期間需求**

  測試通常必須在預先指定的範圍內執行，即使外部條件，例如季節性、市場變化、中途改變。

  Adaptation during the experiment is limited.

## 多臂吃角子老虎機 {#mab-experiment}

Multi-armed bandit algorithms use adaptive allocation: as evidence accumulates, more traffic is directed toward better-performing treatments. The objective is to maximize cumulative reward during the experiment rather than focus solely on the final result.

### 優點

The key strengths of Multi-armed bandit methods are:

* **Faster Optimization**

  Promising treatments are prioritized earlier, improving overall performance during the test.

* **Adaptivity**

  Allocations update continuously as data is collected, making Multi-armed bandit suitable for dynamic environments.

* **Reduced Opportunity Cost**

  Poor treatments are phased out quickly, minimizing wasted traffic.

* **Suitability for Continuous Testing**

  Effective for ongoing experimentation or contexts where traffic is costly.

### 限制

The main limitations of Multi-armed bandit methods are:

* **Weaker Statistical Guarantees**

  Traditional hypothesis testing is harder to apply, and stopping rules are less clear.

* **Reduced Transparency**

  Adaptive allocation can be difficult to explain to stakeholders.

* **Limited Information on Underperforming Treatments**

  Weak treatments receive little exposure, limiting diagnostic insight.

* **Implementation Complexity**

  Requires advanced algorithms and infrastructure, with greater potential for misconfiguration.

## When to use A/B vs Multi-armed bandit

| 藍本 | Recommended Method |
|-|-|
| You are running exploratory or research-driven tests | A/B |
| 您正在執行永遠啟動的行銷活動，例如廣告、建議 | 多臂吃角子老虎 |
| 您想要在測試期間最大化轉換 | 多臂吃角子老虎 |
| 您需要清晰、自信的深入分析 | A/B |
| 您需要快速適應，例如季節性輪班 | 多臂吃角子老虎 |
| 您的流量有限，希望快速最佳化投資報酬率 | 多臂吃角子老虎 |
| 您的流量高，可以承受較慢的學習速度 | A/B |
| 利害關係人需要明確的決策點 | A/B |
