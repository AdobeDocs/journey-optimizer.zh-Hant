---
title: 決定項目
description: 瞭解如何使用決定專案
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 26%

---

# 決定項目 {#items}

>[!CONTEXTUALHELP]
>id="ajo_exd_items"
>title="管理決定項目"
>abstract="Journey Optimizer 可讓您建立行銷優惠 (稱為決定項目)，您可以將其建立並組織到集中式目錄和集合中。目前，所有建立的決定項目都合併在一個「優惠」目錄中。在此畫面中，您還可以使用&#x200B;**編輯架構**&#x200B;按鈕來存取目錄的方案，並為您的決定項目建立自訂屬性。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html" text="設定項目目錄"

>[!BEGINSHADEBOX 「本檔案指南提供哪些內容」]

* [開始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的決定專案： [設定專案目錄](catalogs.md) - **[建立決定專案](items.md)** - [管理專案集合](collections.md)
* 設定專案的選取範圍： [建立決定規則](rules.md) - [建立排名方法](ranking.md)
* [建立選擇策略](selection-strategies.md)
* [建立決定原則](create-decision.md)

>[!ENDSHADEBOX]

Journey Optimizer 可讓您建立行銷優惠 (稱為決定項目)，您可以將其建立並組織到集中式目錄和集合中。這些範本由標準和自訂屬性組成，旨在精確符合您的需求。 此外，它們納入設定檔限制，可讓您定義決策專案可顯示給誰。

在建立決定專案之前，請確定您已建立 **決定規則** 如果要設定條件以決定要向誰顯示決策專案。 [瞭解如何建立決定規則](rules.md).

## 建立您的第一個決定項目

>[!CONTEXTUALHELP]
>id="ajo_exd_item_priority"
>title="定義決策項目的優先順序"
>abstract="如果一個設定檔符合多個項目的條件，則可以透過優先順序將此決定項目與其他決定項目進行比較。 較高的優先順序使該項目優先於其他項目。"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="定義自訂屬性"
>abstract="自訂屬性是根據您的需求訂製並且可以指派給決定項目的特定屬性。 它們是在決定項目的目錄方案中建立的。 只有當您已在目錄方案中新增至少一個自訂屬性時，才會顯示此區段。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html" text="設定項目目錄"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_constraints"
>title="新增對象或決定規則"
>abstract="預設情況下，所有設定檔都有資格接收決定項目，但您可以使用對象或規則將該項目限制為僅限特定設定檔。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html" text="使用對象"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/selection/rules.html" text="使用決定規則"

若要建立決定專案，請遵循下列步驟：

1. 瀏覽至 **[!UICONTROL 體驗決策]** > **[!UICONTROL 專案]**.

1. 定義決定專案的標準屬性：

   1. 提供名稱和說明。
   1. 指定開始和結束日期。 在此日期內，決策引擎僅會考慮該專案。
   1. 設定 **[!UICONTROL 優先順序]** 與其他專案比較，如果設定檔符合多個專案的資格。 較高的優先順序使該項目優先於其他項目。

   ![](assets/item-attributes.png)

   >[!NOTE]
   >
   >優先順序是整數資料型別。 整數資料型別的所有屬性都應包含整數值（無小數）。

1. 自訂屬性是根據您的需求訂製並且可以指派給決定項目的特定屬性。 它們會在決定專案的目錄結構描述中定義。 [瞭解如何使用目錄](catalogs.md)

1. 定義決定專案的屬性後，按一下 **[!UICONTROL 下一個]** 以設定料號的設定檔限制。

   依預設，所有設定檔都符合接收決定專案的資格，但您可以使用對象或規則將專案限製為僅特定設定檔，這兩個解決方案都對應不同的使用方式。 展開下列區段以取得詳細資訊：

   +++使用對象與決定規則

   基本上，對象的輸出是設定檔清單，而決定規則是在決策流程期間根據單一設定檔執行的函式。

   * **受眾**：一方面，受眾是一組Adobe Experience Platform設定檔，根據設定檔屬性和體驗事件符合特定邏輯。 不過，Offer Management不會重新計算對象，在展示優惠方案時，該對象可能不是最新狀態。

   * **決定規則**：另一方面，決定規則會根據Adobe Experience Platform中的可用資料，並決定可向誰顯示優惠方案。 在優惠或指定位置的決定中選取後，每次做出決定時都會執行規則，以確保每個設定檔取得最新和最佳優惠。

+++

   ![](assets/item-constraints.png)

   * 若要將決策專案的呈現限制在一或多個Adobe Experience Platform對象的成員中，請選取 **[!UICONTROL 屬於一或多個對象的訪客]** 選項，然後從左窗格新增一或多個對象，並使用 **[!UICONTROL 與]** / **[!UICONTROL 或]** 邏輯運運算元。 [深入瞭解對象](../audience/about-audiences.md).

   * 若要將特定決定規則關聯至決定專案，請選取 **[!UICONTROL 依規則]**，然後將需要的規則從左窗格拖曳到中央區域。 [進一步了解決定規則](rules.md).

   當您選取對象或決定規則時，您可以檢視有關預估合格設定檔的資訊。 按一下 **[!UICONTROL 重新整理]** 以更新資料。

   >[!NOTE]
   >
   >當規則引數包含不在設定檔中的資料（例如內容資料）時，設定檔預估無法使用。 例如，適用性規則要求目前天氣為≥80度。

1. 定義決定專案的限制後，按一下 **[!UICONTROL 下一個]** 以檢閱並儲存專案。

1. 決定專案現在會出現在清單中，並顯示 **[!UICONTROL 草稿]** 狀態。 當它準備好要呈現給設定檔時，按一下省略符號按鈕並選擇 **[!UICONTROL 核准]**.

   ![](assets/item-approve.png)

## 管理決定項目

從決定專案清單中，您可以編輯決定專案、變更其狀態(**草稿**， **已核准**， **已封存**)、複製或刪除它。

若要修改決定專案，請開啟它、進行修改並儲存。

選取決定專案或按一下省略符號按鈕會啟用以下所述的動作。

* **[!UICONTROL 核准]**：將決定專案的狀態設定為「已核准」。
* **[!UICONTROL 還原核准]**：將決定專案的狀態設回 **[!UICONTROL 草稿]**.
* **[!UICONTROL 複製]**：建立具有相同屬性和限制的決定專案。 依預設，新專案具有 **[!UICONTROL 草稿]** 狀態。
* **[!UICONTROL 刪除]**：從清單中移除決定專案。

  >[!IMPORTANT]
  >
  >刪除後，就無法再存取決定專案及其內容。 此動作無法復原。 如果決定專案用於集合或決定中，則無法刪除該專案。 您必須先從任何物件中移除決定專案。

* **[!UICONTROL 封存]**：將決定專案狀態設為 **[!UICONTROL 已封存]**. 該決定專案仍然可以從清單中使用，但您不能將其狀態設定回 **[!UICONTROL 草稿]** 或 **[!UICONTROL 已核准]**. 您只能複製或刪除它。
