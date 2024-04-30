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
source-git-commit: 29228a17176421ccf29598d6ebba815b800db7a2
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 16%

---

# 決定規則 {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="建立決定規則"
>abstract="決定規則可讓您透過直接在決定項目層級或在特定選擇策略內套用限制來定義決定項目的對象。 這能讓您精確控制應向誰呈現哪些項目。"

>[!BEGINSHADEBOX 「本檔案指南提供哪些內容」]

* [開始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的決定專案： [設定專案目錄](catalogs.md) - [建立決定專案](items.md) - [管理專案集合](collections.md)
* 設定專案的選取範圍： **[建立決定規則](rules.md)** - [建立排名方法](ranking.md)
* [建立選擇策略](selection-strategies.md)
* [建立決定原則](create-decision.md)

>[!ENDSHADEBOX]

決定規則可讓您透過直接在決定項目層級或在特定選擇策略內套用限制來定義決定項目的對象。 這能讓您精確控制應向誰呈現哪些項目。

例如，假設您的決策專案為女性設計，其中含有瑜伽相關產品。 透過決定規則，您可以指定只向性別為「女性」且已在「瑜伽」中指明「地標」的個人檔案顯示這些專案。

>[!NOTE]
>
>除了專案與選擇策略層級的決定規則之外，您也可以在行銷活動層級定義您打算的對象。 [了解更多](../campaigns/create-campaign.md#audience)

決定規則清單可在 **[!UICONTROL 設定]** / **[!UICONTROL 決定規則]** 功能表。

![](assets/decision-rules-list.png)

## 建立決定規則 {#create}

若要建立決定規則，請遵循下列步驟：

1. 瀏覽至 **[!UICONTROL 設定]** / **[!UICONTROL 決定規則]** 然後按一下 **[!UICONTROL 建立規則]** 按鈕。

1. 決定規則建立畫面隨即開啟。 為規則命名並提供說明。

1. 使用Adobe Experience Platform區段產生器建立符合您需求的決定規則。 若要這麼做，Tou可運用各種資料來源，例如來自Adobe Experience Platform的設定檔屬性、對象或內容資料。 [瞭解如何在決定規則中運用內容資料](#context-data)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >相較於Adobe Experience Platform區段服務使用的區段產生器，用來建立決定規則的區段產生器呈現出一些特性。  不過，檔案中描述的全域程式對於建置決定規則仍然有效。 [瞭解如何建立區段定義](../audience/creating-a-segment-definition.md)

1. 當您在工作區中新增及設定新欄位時， **[!UICONTROL 對象屬性]** 窗格會顯示受眾之預估設定檔的相關資訊。 按一下 **[!UICONTROL 重新整理預估值]** 以更新資料。

   >[!NOTE]
   >
   >當規則引數包含不在設定檔中的資料（例如內容資料）時，設定檔預估無法使用。

1. 決策規則準備就緒後，按一下 **[!UICONTROL 儲存]**. 建立的規則會顯示在清單中，並可用於決定專案和選取策略，以控管將決定專案呈現給設定檔。

## 在決定規則中善用內容資料 {#context-data}

Experience Decisioning規則建立畫面可讓您運用Adobe Experience Platform中的任何可用資訊來建立決定規則。 例如，您可以設計決定規則，要求目前天氣為≥80度。

若要這麼做，您首先需要定義要在Experience Decisioning中提供的資料。 完成後，此資料會順暢地整合至的Experience Decisioning **[!UICONTROL 內容資料]** 建立決定規則時可用的標籤。

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
