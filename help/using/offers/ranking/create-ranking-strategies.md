---
product: experience platform
solution: Experience Platform
title: 建立 AI 模型
description: 瞭解如何建立AI模型以對產品排序
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 3188bc97b8103d2a01101a23d8c242a3e2924f76
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 9%

---

# 建立 AI 模型 {#ai-rankings}

[!DNL Journey Optimizer] 允許您建立 **AI模型** 根據您的業務目標對優惠進行排名。

>[!CAUTION]
>
>要建立、編輯或刪除AI模型，必須 **管理排名策略** 權限。 [了解更多](../../administration/high-low-permissions.md#manage-ranking-strategies)

## 建立 AI 模型 {#create-ranking-strategy}

要建立AI模型，請執行以下步驟：

1. 在 **[!UICONTROL Components]** 菜單，訪問 **[!UICONTROL Ranking]** ，然後選擇 **[!UICONTROL AI models]**。

   ![](../assets/ai-ranking-list.png)

   列出迄今建立的所有人工智慧模型。

1. 按一下「**[!UICONTROL Create AI model]**」按鈕。

1. 為AI模型指定唯一名稱和說明，然後選擇要建立的AI模型類型：

   * **[!UICONTROL Auto-optimization]** 根據過去的服務效能優化服務。 [了解更多](auto-optimization-model.md)
   * **[!UICONTROL Personalized]** 根據細分市場優化和個性化服務，並提供效能。 [了解更多](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL Optimization metric]** 部分提供有關AI模型用於計算優惠排名的轉換事件的資訊。
   >
   >[!DNL Journey Optimizer] 基於 **轉換率** （轉換率=轉換事件總數/印象事件總數）。 轉換率使用兩種度量計算：
   >* **印象事件** （顯示的優惠）
   >* **轉換事件** （通過電子郵件或web提供點擊）。

   >
   >這些事件是使用已提供的Web SDK或移動SDK自動捕獲的。 在中瞭解有關此的詳細資訊 [Adobe Experience PlatformWeb SDK概述](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant)。

1. 選擇收集轉換和印象事件的資料集。 瞭解如何在 [此部分](#create-dataset)。 <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >僅從與 **[!UICONTROL Experience Event - Proposition Interactions]** 欄位組（以前稱為mixin）顯示在下拉清單中。

1. 如果要建立 **[!UICONTROL Personalization]** AI模型，選擇用於訓練AI模型的段。

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >最多可選取5個段。

1. 保存並激活AI模型。

   ![](../assets/ai-ranking-save-activate.png)
