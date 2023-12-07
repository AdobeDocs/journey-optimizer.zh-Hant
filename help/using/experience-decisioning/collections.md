---
title: 集合
description: 瞭解如何使用集合
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 50%

---

# 集合 {#collections}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collections"
>title="建立集合"
>abstract="集合可讓您根據自己的喜好對決定項目進行分類和分組。 這些類別是透過制定利用決定項目屬性的規則所建立的。"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collection_rules"
>title="為您的集合定義規則"
>abstract="新增一項或多項規則以決定要包含在集合中的項目。 選擇一個項目屬性作為標準。 選取所需的運算子並輸入要篩選的值。 視需要新增盡可能多的規則。"

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_collection"
>title="選擇一個集合"
>abstract="選取包含要考慮的優惠的集合。 建立選擇策略時必須執行此步驟。 集合可讓您根據自己的喜好對決定項目進行分類和分組。 例如，您可以建立一個集合，其中包含在「類別」自訂屬性中具有「瑜珈」值的所有決定項目。"

>[!BEGINSHADEBOX 「本檔案指南提供哪些內容」]

* [開始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的決定專案： [設定專案目錄](catalogs.md) - [建立決定專案](items.md) - **[管理專案集合](collections.md)**
* 設定專案的選取範圍： [建立決定規則](rules.md) - [建立排名方法](ranking.md)
* [建立選擇策略](selection-strategies.md)
* [建立決定原則](create-decision.md)

>[!ENDSHADEBOX]

集合可讓您根據自己的喜好對決定項目進行分類和分組。 這些類別是透過制定利用決定項目屬性的規則所建立的。

例如，假設您已將「類別」自訂屬性新增至決定專案的目錄結構描述。 這可讓您建立包含「類別」屬性中具有「瑜伽」值的所有決定專案的集合。

集合清單可從 **[!UICONTROL 專案]** 功能表。

若要建立集合，請依照下列步驟進行：

1. 瀏覽至 **[!UICONTROL 專案]** > **[!UICONTROL 集合]** 並按一下 **[!UICONTROL 建立集合]**.
1. 提供集合的名稱和說明。
1. 新增一項或多項規則以決定要包含在集合中的項目。 執行方法：

   1. 選擇一個項目屬性作為標準。 屬性清單包含在目錄結構描述中定義的所有標準和自訂屬性。 [進一步瞭解專案的目錄](catalogs.md)
   1. 選取所需的運運算元，並輸入篩選依據的值。
   1. 重複這些步驟，視需要新增任意數量的規則。 新增多個規則時，您可以選擇 **與** 和 **或** 運運算元加以組合。 若要這麼做，請按一下運運算元徽章，在兩個選項之間切換。

   ![](assets/collection-create.png)

1. 定義收集規則後，按一下 **[!UICONTROL 建立]**. 集合現在會顯示在清單中。
