---
title: 決定規則
description: 瞭解如何使用決定規則
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="限量版"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 24%

---

# 決定規則 {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="建立決定規則"
>abstract="決定規則可讓您透過直接在決定項目層級或在特定選擇策略內套用限制來定義決定項目的對象。 這能讓您精確控制應向誰呈現哪些項目。"

## 關於決定規則 {#about}

決定規則可讓您透過直接在決定項目層級或在特定選擇策略內套用限制來定義決定項目的對象。 這能讓您精確控制應向誰呈現哪些項目。

例如，假設您的決策專案為女性設計，其中含有瑜伽相關產品。 透過決定規則，您可以指定只向性別為「女性」且已在「瑜伽」中指明「地標」的個人檔案顯示這些專案。

>[!NOTE]
>
>除了專案與選擇策略層級的決定規則之外，您也可以在行銷活動層級定義您打算的對象。 [了解更多](../campaigns/create-campaign.md#audience)

決定規則清單可在 **[!UICONTROL 策略設定]** 功能表。

![](assets/decision-rules-list.png)

## 建立決定規則 {#create}

若要建立決定規則，請遵循下列步驟：

1. 瀏覽至 **[!UICONTROL 策略設定]** / **[!UICONTROL 決定規則]** 然後按一下 **[!UICONTROL 建立規則]** 按鈕。

1. 決定規則建立畫面隨即開啟。 為規則命名並提供說明。

1. 使用Adobe Experience Platform區段產生器建立符合您需求的決定規則。 若要這麼做，Tou可運用各種資料來源，例如來自Adobe Experience Platform的設定檔屬性、對象或內容資料。 [瞭解如何善用內容資料](#context-data)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >相較於Adobe Experience Platform區段服務使用的區段產生器，用來建立決定規則的區段產生器呈現出一些特性。  不過，檔案中描述的全域程式對於建置決定規則仍然有效。 [瞭解如何建立區段定義](../audience/creating-a-segment-definition.md)

1. 當您在工作區中新增及設定新欄位時， **[!UICONTROL 對象屬性]** 窗格會顯示受眾之預估設定檔的相關資訊。 按一下 **[!UICONTROL 重新整理預估值]** 以更新資料。

   >[!NOTE]
   >
   >當規則引數包含不在設定檔中的資料（例如內容資料）時，設定檔預估無法使用。

1. 決策規則準備就緒後，按一下 **[!UICONTROL 儲存]**. 建立的規則會顯示在清單中，並可用於決定專案和選取策略，以控管將決定專案呈現給設定檔。

