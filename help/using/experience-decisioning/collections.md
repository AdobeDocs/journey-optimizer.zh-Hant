---
title: 集合
description: 瞭解如何使用集合
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 17%

---

# 集合 {#collections}

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* [開始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理決定項目
   * [設定項目目錄](catalogs.md)
   * [建立決定項目](items.md)
   * **[管理項目集合](collections.md)**
* 設定項目的選取範圍
   * [建立決定規則](rules.md)
   * [建立排名方法](ranking.md)
* [建立選擇策略](selection-strategies.md)
* [建立決定原則](create-decision.md)

>[!ENDSHADEBOX]

集合可讓您根據偏好設定將決策專案分類及分組。 這些類別是透過精心設計利用決策專案屬性的規則所建立。

例如，假設您已將「類別」自訂屬性新增至決定專案的目錄結構描述。 這可讓您建立包含「類別」屬性中具有「瑜伽」值的所有決定專案的集合。

集合清單可從 **[!UICONTROL 專案]** 功能表。

若要建立集合，請依照下列步驟進行：

1. 瀏覽至 **[!UICONTROL 專案]** > **[!UICONTROL 集合]** 並按一下 **[!UICONTROL 建立集合]**.
1. 提供集合的名稱和說明。
1. 新增一或多個規則以決定要包含在集合中的專案。 執行方法：

   1. 選擇要作為條件的料號屬性。 屬性清單包含在目錄結構描述中定義的所有標準和自訂屬性。 [進一步瞭解專案的目錄](catalogs.md)
   1. 選取所需的運運算元，並輸入篩選依據的值。
   1. 重複這些步驟，視需要新增任意數量的規則。 新增多個規則時，您可以選擇 **與** 和 **或** 運運算元加以組合。 若要這麼做，請按一下運運算元徽章，在兩個選項之間切換。

   ![](assets/collection-create.png)

1. 定義收集規則後，按一下 **[!UICONTROL 建立]**. 集合現在會顯示在清單中。
