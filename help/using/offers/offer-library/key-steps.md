---
title: 建立優惠的重要步驟
description: 探索建立優惠方案所需的關鍵步驟
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 13%

---

# 建立和管理優惠的重要步驟 {#key-steps-to-manage-offers}

建立、設定和管理優惠，以及在決定中使用優惠的主要步驟如下所示。

![](../assets/offer-create-manage-process.png)

如需完整端對端範例，說明如何設定優惠方案、在決定中使用優惠方案，並在電子郵件中運用此決定，請檢視 [此頁面](../offers-e2e.md).

## 建立元件 {#create-components}

在開始建立優惠方案之前，您必須定義要在優惠方案中使用的數個元件。

1. **建立版位**，此容器會用來展示您的選件。 例如，您可以建立專用於影像格式之優惠方案的版位，並位於訊息頂端。

1. **建立決定規則** 會指定顯示優惠的條件。

1. **建立集合限定詞** （先前稱為「標籤」）可讓您關聯至選件，輕鬆整理並搜尋至資料庫。

1. 如果您想要定義規則，以決定應先針對指定位置顯示哪個優惠方案（而不是考慮優惠方案的優先順序分數），您可以 **建立排名公式**.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">建立位置</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">建立決定規則</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">建立標籤</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">建立排名公式</a>
</div>
<p>
</td>
</tr>
</table>

## 建立和管理優惠方案 {#create-and-manage-offers}

1. **建立優惠方案**，並設定其內容和屬性。

1. **建立遞補優惠**，這是客戶不符合任何選定優惠方案資格時顯示的最後選用優惠方案。

1. **建立集合** 加入您建立的個人化優惠方案，並在決定中使用。

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">建立優惠方案</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">建立後備優惠方案</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">建立集合</a>
</div>
<p>
</td>
</tr>
</table>

## 建立及設定決定 {#create-and-configure-decisions}

1. **建立決定** 此維度會將刊登版位與個人化優惠和遞補優惠結合在一起。 決策引擎將使用此組合來尋找特定設定檔的最佳選件。

1. **設定決定**. 若要這麼做，請選取位置，並針對每個位置，選取集合和遞補。

1. 如有需要，您可以 **指派排名公式** 至某個位置。

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">建立決定</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">設定決定</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">指派排名</a>
</div>
<p>
</td>
</tr>
</table>
