---
title: 在Experience Decisioning中善用內容資料
description: 瞭解如何在Experience Decisioning中善用內容資料
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="限量版"
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# 在Experience Decisioning中善用內容資料 {#context}

有了Experience Decisioning，您可以利用Adobe Experience Platform中提供的任何資訊來執行各種動作，例如建立 [決定規則](rules.md) 或 [排名公式](ranking.md). 例如，您可以設計決定規則，要求進行決定請求時目前的天氣為≥80度。

>[!NOTE]
>
>內容資料是在Adobe Experience Platform中定義，並在進行決定請求時傳送到。 其中不包含歷史資料。

若要使用內容資料，您必須先定義要在Experience Decisioning中提供的資料。 完成後，此資料會順暢地整合至的Experience Decisioning **[!UICONTROL 內容資料]** 建立決定規則時可用的標籤。 您也可以在編輯排名公式時運用資料。

![](assets/decision-rules-context.png)

使用Adobe Experience Platform資料摘要Experience Decisioning的步驟如下：

1. 建立 **體驗事件結構描述**  在Adobe Experience Platform及其相關頁面中 **資料集**. [瞭解如何建立方案](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. 建立新的Adobe Experience Platform資料流：

   1. 導覽至 **[!UICONTROL 資料串流]** 功能表並選取 **[!UICONTROL 新增資料串流]**.

   1. 在 **[!UICONTROL 事件結構描述]** 從下拉式清單中，選取先前建立的Experience Event綱要，然後按一下 **[!UICONTROL 儲存]**.

      ![](assets/decision-rule-context-datastream.png)

   1. 按一下 **[!UICONTROL 新增服務]** 並選取「Adobe Experience Platform」作為服務。 在 **[!UICONTROL 事件資料集]** 從下拉式清單中，選取先前建立的事件資料集，並啟用 **[!UICONTROL Adobe Journey Optimizer]** 選項。

      ![](assets/decision-rules-context-datastream-service.png)

資料串流儲存後，系統會自動擷取所選資料集的資訊並整合至Experience Decisioning，且通常會在24小時內提供使用。

如需如何使用Adobe Experience Platform的詳細指引，請探索下列資源：

* [體驗資料模型(XDM)結構描述](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [資料集](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [資料串流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
