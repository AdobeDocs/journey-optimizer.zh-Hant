---
title: 建立優惠的重要步驟
description: 探索建立優惠方案所需的關鍵步驟。
feature: 優惠
topic: 整合
role: User
level: Intermediate
source-git-commit: 5631a1937b854c3e14d1816df9e8d30690588303
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 11%

---

# 建立和管理選件{#key-steps}的關鍵步驟

建立、設定和管理優惠方案以及在決策中使用優惠方案的主要步驟如下。

![](../../assets/offer-create-manage-process.png)

如需完整的端對端範例，說明如何設定選件，請在決策中使用選件，並在電子郵件中運用此決策，請查看[此頁面](../offers-e2e.md)。

## 建立元件

開始建立選件之前，您必須定義要在選件中使用的數個元件。

1. **建立版位**，這是用來展示優惠方案的容器。例如，您可以建立僅以影像格式專用於優惠方案的版位，並位於訊息頂端。

1. **建立決** 策規則，以指定要在哪個條件下顯示選件。

1. **建** 立您要與選件建立關聯的標籤，讓您輕鬆組織選件，並在資料庫中搜尋選件。

1. 如果您想要定義規則，以決定應先針對指定版位呈現哪個優惠方案（而非考慮優惠方案的優先順序分數），您可以&#x200B;**建立排名公式**。

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">建立位置</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">建立決定規則</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">建立標籤</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../offer-library/create-ranking-formulas.md">建立排名公式</a></p></td>
</table>

## 建立和管理優惠

1. **建立選件**，並設定其內容和屬性。

1. **建立備援優惠方案**，如果客戶不符合任何所選優惠方案的資格，這是最後顯示的優惠方案。

1. **建立集** 合，納入您建立的個人化優惠方案，並用於決策中。

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">建立優惠方案</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">建立遞補優惠</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">建立集合</a></p></td></tr>
</table>

## 建立和設定決策

1. **建立將** 刊登版位與個人化優惠方案及後援優惠方案結合的決策。此組合將供Offer decisioning引擎用來尋找特定設定檔的最佳選件。

1. **設定決策**。若要這麼做，請選取版位，然後針對每個版位選取集合和後援。

1. 如有需要，您可以在設定決策時，將排名公式&#x200B;**指派給位置。**

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">建立決定</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">設定決策</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">指派排名</a></p></td>
</tr>
</table>
