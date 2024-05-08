---
title: 排名方法
description: 瞭解如何使用排名方法
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
badge: label="限量版"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 12%

---

# 排名方法 {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="建立排名公式"
>abstract="公式可讓您定義規則，以決定應先呈現哪個項目，而不是考慮項目的優先順序分數。 建立排名方法後，您可以將其指派給選取策略，以定義應先選取哪些專案。"

排名方法可讓您針對要針對指定設定檔顯示的專案進行排名。 建立排名方法後，您可以將其指派給選取策略，以定義應先選取哪些專案。

有兩種排名方法可供使用：

* **公式** 可讓您定義規則，以決定應先顯示哪個專案，而不是考慮專案的優先順序分數。

* **AI模型** 可讓您使用經過訓練的模型系統，這些系統將利用多個資料點來決定應該首先顯示哪個專案。

## 建立排名方法 {#create}

若要建立排名方法，請依照下列步驟進行：

1. 導覽至 **[!UICONTROL 策略設定]** 功能表，然後選取 **[!UICONTROL 公式]** 或 **[!UICONTROL AI模型]** 功能表，視您要使用的排名型別而定。

1. 按一下 **[!UICONTROL 建立公式]** 或 **[!UICONTROL 建立AI模型]** 按鈕。

   ![](assets/ranking-create.png)

1. 設定公式或AI模型以符合您的需求，然後儲存。

   有關如何建立排名公式和AI模型的詳細資訊，請參閱決策管理檔案：

   * [排名公式](../offers/ranking/create-ranking-formulas.md)
   * [AI模型](../offers/ranking/ai-models.md)


## 在公式中善用決定專案屬性 {#items}

排名公式的表示方式為 **PQL語法** 和可以運用各種屬性，例如設定檔屬性、 [內容資料](context-data.md) 以及與決策專案相關的屬性。

若要在公式中運用與決策專案相關的屬性，請務必遵循排名公式程式碼中的以下語法。 展開每個區段以取得詳細資訊：

+++運用決策專案標準屬性

![](assets/formula-attribute.png)

+++

+++善用決策專案自訂屬性

![](assets/formula-attribute-custom.png)

+++
