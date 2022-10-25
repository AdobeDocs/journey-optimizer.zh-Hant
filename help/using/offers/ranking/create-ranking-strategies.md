---
product: experience platform
solution: Experience Platform
title: 建立 AI 模型
description: 了解如何建立AI模型以排名選件
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 3188bc97b8103d2a01101a23d8c242a3e2924f76
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 7%

---

# 建立 AI 模型 {#ai-rankings}

[!DNL Journey Optimizer] 可讓您建立 **AI模型** 以根據您的業務目標來排名優惠方案。

>[!CAUTION]
>
>若要建立、編輯或刪除AI模型，您必須具備 **管理排名策略** 權限。 [了解更多](../../administration/high-low-permissions.md#manage-ranking-strategies)

## 建立 AI 模型 {#create-ranking-strategy}

要建立AI模型，請執行以下步驟：

1. 在 **[!UICONTROL 元件]** 菜單，訪問 **[!UICONTROL 排名]** ，然後選取 **[!UICONTROL AI模型]**.

   ![](../assets/ai-ranking-list.png)

   列出了迄今建立的所有AI模型。

1. 按一下 **[!UICONTROL 建立AI模型]** 按鈕。

1. 為AI模型指定唯一名稱和說明，然後選擇要建立的AI模型類型：

   * **[!UICONTROL 自動最佳化]** 根據過去的優惠方案效能來最佳化優惠方案。 [了解更多](auto-optimization-model.md)
   * **[!UICONTROL 個人化]** 根據區段和選件效能來最佳化和個人化選件。 [了解更多](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL 最佳化量度]** 區段提供AI模型用來計算選件排名的轉換事件相關資訊。
   >
   >[!DNL Journey Optimizer] 根據 **轉換率** （轉換率=轉換事件總數/曝光事件總數）。 轉換率是使用兩種量度來計算：
   >* **曝光事件** （顯示的選件）
   >* **轉換事件** （透過電子郵件或網頁點按的選件）。

   >
   >這些事件會使用已提供的Web SDK或行動SDK自動擷取。 如需深入了解，請參閱 [Adobe Experience Platform Web SDK概述](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant).

1. 選取要收集轉換和曝光事件的資料集。 了解如何在 [本節](#create-dataset). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >僅從與 **[!UICONTROL 體驗事件 — 主張互動]** 欄位群組（先前稱為mixin）會顯示在下拉式清單中。

1. 如果您要建立 **[!UICONTROL 個人化]** AI模型，選取用於訓練AI模型的區段。

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >最多可選取5個區段。

1. 儲存並啟動AI模型。

   ![](../assets/ai-ranking-save-activate.png)
