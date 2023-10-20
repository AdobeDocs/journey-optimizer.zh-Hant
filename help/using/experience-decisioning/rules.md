---
title: 決定規則
description: 瞭解如何使用決定規則
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: f92e3882d3b5e515e672a4af8e787813d4d939ce
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 15%

---

# 決定規則 {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="建立決定規則"
>abstract="決定規則可讓您透過直接在決定專案層級或特定選取策略中套用限制，來定義決定專案的對象。 這可讓您精確控制應該向誰展示哪些專案。"

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* [開始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理決定項目
   * [設定項目目錄](catalogs.md)
   * [建立決定項目](items.md)
   * [管理項目集合](collections.md)
* 設定項目的選取範圍
   * **[建立決定規則](rules.md)**
   * [建立排名方法](ranking.md)
* [建立選擇策略](selection-strategies.md)
* [建立決定原則](create-decision.md)

>[!ENDSHADEBOX]

決定規則可讓您透過直接在決定專案層級或特定選取策略中套用限制，來定義決定專案的對象。 這可讓您精確控制應該向誰展示哪些專案。

例如，假設您的決策專案為女性設計，其中含有瑜伽相關產品。 使用決定規則，您可以指定只向性別為「女性」且已在「瑜伽」中指明「地標」的個人檔案顯示這些專案。

>[!NOTE]
>
>除了專案與選擇策略層級的決定規則之外，您也可以在行銷活動層級定義您打算的對象。 [了解更多](../campaigns/create-campaign.md#audience)


決定規則清單可在 **[!UICONTROL 設定]** / **[!UICONTROL 決定規則]** 功能表。

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>目前，決定規則是使用Journey Optimizer的 **決定管理** 功能表。 因此， **[!UICONTROL 決定規則]** Experience Decisioning中的清單包含從兩個Journey Optimizer建立的規則 **[!UICONTROL 決定管理]** 或 **[!UICONTROL 體驗決策]** 功能表。

若要建立規則，請遵循下列步驟：

1. 瀏覽至 **[!UICONTROL 設定]** / **[!UICONTROL 決定規則]**.
1. Journey Optimizer的決策管理使用者介面會顯示在中央區域中。 請依照以下詳細步驟操作： [決策管理檔案](../offers/offer-library/creating-decision-rules.md) 以根據您的需求建置規則。

1. 建立規則後，該規則會出現在清單中，並可用於決策專案和選擇策略，以控管將決策專案呈現給設定檔。
