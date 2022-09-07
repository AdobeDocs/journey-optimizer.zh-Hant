---
title: 建立優惠的重要步驟
description: 探索建立優惠方案所需的關鍵步驟
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 13%

---

# 建立和管理優惠的重要步驟 {#key-steps-to-manage-offers}

建立、設定和管理優惠方案以及在決策中使用優惠方案的主要步驟如下。

![](../assets/offer-create-manage-process.png)

如需完整的端對端範例，說明如何設定優惠方案、在決策中使用優惠方案，以及在電子郵件中運用此決策、結帳 [本頁](../offers-e2e.md).

## 建立元件 {#create-components}

開始建立選件之前，您必須定義要在選件中使用的數個元件。

1. **建立版位**，這些容器將用來展示您的選件。 例如，您可以建立僅以影像格式專用於優惠方案的版位，並位於訊息頂端。

1. **建立決策規則** 以指定要呈現選件的條件。

1. **建立標籤** 建立選件的關聯，讓您可輕鬆組織選件，並將其搜尋至資料庫。

1. 如果您想要定義規則，以決定應先針對指定版位呈現哪個優惠方案（而非考慮優惠方案的優先順序分數），您可以 **建立排名公式**.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">建立位置</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">建立決定規則</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">建立標籤</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../ranking/create-ranking-formulas.md">建立排名公式</a></p></td>
</table>

## 建立和管理優惠方案 {#create-and-manage-offers}

1. **建立優惠方案**，並設定其內容和屬性。

1. **建立回退優惠方案**，這是客戶不符合任何所選選件資格時，最後要顯示的優惠方案。

1. **建立集合** 納入您建立的個人化優惠方案，並用於決策中。

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">建立優惠方案</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">建立遞補優惠</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">建立集合</a></p></td></tr>
</table>

## 建立和設定決策 {#create-and-configure-decisions}

1. **建立決策** 可結合版位與個人化優惠方案和備援優惠方案。 決策引擎會使用此組合來尋找特定設定檔的最佳選件。

1. **設定決策**. 若要這麼做，請選取版位，然後針對每個版位選取集合和後援。

1. 如有需要，您可以 **指派排名公式** 設定決策時的位置。

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">建立決定</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">設定決策</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">指派排名</a></p></td>
</tr>
</table>
