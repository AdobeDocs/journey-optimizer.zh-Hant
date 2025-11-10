---
title: 建立產品建議的重要步驟
description: 探索建立產品建議所需的關鍵步驟
badge: label="舊版" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 7%

---

# 建立和管理優惠的重要步驟 {#key-steps-to-manage-offers}

建立、設定和管理優惠，以及在決定中使用優惠的主要步驟如下所示。

![](../assets/offer-create-manage-process.png)

如需說明如何設定優惠方案的完整端對端範例、在決定中使用優惠方案，並在電子郵件中運用此決定，請檢視[此頁面](../offers-e2e.md)。

## 建立元件 {#create-components}

在開始建立優惠方案之前，您必須定義要在優惠方案中使用的數個元件。

1. [建立版位](creating-placements.md)，這些是用來展示您的優惠方案的容器。 例如，您可以建立專用於影像格式之優惠方案的版位，並位於訊息頂端。

1. [建立決定規則](creating-decision-rules.md)，以指定提供優惠的條件。

1. [建立與優惠方案關聯的集合限定詞](creating-tags.md) （先前稱為「標籤」），讓您輕鬆整理優惠方案並在資料庫中搜尋。

1. 如果您想要定義規則，以決定應先針對指定位置顯示哪個優惠（而不是考慮優惠的優先順序分數），您可以[建立排名公式](../ranking/create-ranking-formulas.md)。

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Create placements</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Create decision rules</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Create collection qualifiers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Create ranking formulas</a>
</div>
<p>
</td>
</tr>
</table>
-->

## 建立和管理優惠方案 {#create-and-manage-offers}

1. [建立優惠方案](creating-personalized-offers.md)，並設定其內容和屬性。

1. [建立遞補優惠方案](creating-fallback-offers.md)，如果客戶不符合任何選取優惠方案的資格，則這些方案是最後要顯示的優惠方案。

1. [建立集合](creating-collections.md)以包含您建立的個人化優惠，並在決定中使用這些優惠。

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Create offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Create fallback offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Create collections</a>
</div>
<p>
</td>
</tr>
</table>
-->

## 建立及設定決定 {#create-and-configure-decisions}

1. [建立將刊登版位與個人化優惠和遞補優惠結合的決定](../offer-activities/create-offer-activities.md)。 決策引擎將使用此組合來尋找特定設定檔的最佳選件。

1. [設定決定](../offer-activities/create-offer-activities.md#add-decision-scopes)。 若要這麼做，請選取位置，並針對每個位置，選取集合和遞補。

1. 如有需要，您可以在設定決定時[將排名公式](../offer-activities/configure-offer-selection.md#assign-ranking-formula)或[AI排名](../offer-activities/configure-offer-selection.md#use-ranking-strategy)指派給位置。

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Create decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Configure decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Assign ranking</a>
</div>
<p>
</td>
</tr>
</table>
-->