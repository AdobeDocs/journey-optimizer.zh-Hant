---
solution: Journey Optimizer
product: journey optimizer
title: 使用組合畫布
description: 了解如何使用構圖畫布
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 3eb9466e-9d88-4470-a22f-5e24a29923ae
badge: label="Beta" type="Informity"
source-git-commit: 242fd8dbb04d62b9ec838655985add4ea0d7b377
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 27%

---

# 使用組合畫布 {#composition-canvas}

>[!BEGINSHADEBOX]

本檔案提供下列內容：

* [開始使用對象組合](get-started-audience-orchestration.md)
* [建立您的第一個合成工作流程](create-compositions.md)
* **[使用組合畫布](composition-canvas.md)**
* [存取及管理對象](access-audiences.md)

>[!ENDSHADEBOX]

對象構成提供視覺畫布，可讓您建立對象並使用各種活動（分割、擴充等）。

在畫布中撰寫對象的步驟如下：

1. [定義起始對象](#starting-audience)
1. [新增一或多個活動](#action-activities)
1. [將結果儲存到新受眾](#save)

## 選取開始對象 {#starting-audience}

建立構圖的第一個步驟是選取一或多個現有對象，作為構圖的基礎。

1. 選取 **[!UICONTROL 對象]** 活動然後提供活動的標籤。

1. 選擇要定位的對象：

   * 按一下 **[!UICONTROL 新增對象]** 按鈕，以選取一或多個現有對象，
   * 按一下 **[!UICONTROL 建置規則]** 按鈕，使用 [區段服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](assets/audiences-choose-audience.png)

1. 如果選取了多個對象，請指定應如何合併這些對象的設定檔：

* **[!UICONTROL 聯合]**:包含來自所選對象的所有設定檔，
* **[!UICONTROL 交集]**:包含所有所選對象共同的設定檔，
* **[!UICONTROL 排除重疊]**:包含僅屬於其中一個對象的設定檔。 不會包含屬於多個對象的設定檔。

在此範例中，我們想要鎖定屬於金級和銀級受眾的所有設定檔。

![](assets/audiences-starting-audience.png)

選取對象後，預估的設定檔數量會顯示在活動底部。

## 新增活動 {#action-activities}

在選取您的起始對象後新增活動，以調整您的選取範圍。

若要這麼做，請按一下構成路徑上的+按鈕，然後選取所需的活動。 右窗格隨即開啟，可讓您設定新新增的活動。

![](assets/audiences-select-activity.png)

可用活動包括：

* [對象](#audience):包含屬於一或多個現有對象的其他設定檔，
* [排除](#exclude):排除屬於現有對象的設定檔，或根據特定屬性排除設定檔，
* [豐富](#enrich):來自Adobe Experience Platform資料集的其他屬性，讓您的受眾更為豐富，
* [排名](#rank):根據特定屬性來排名設定檔，指定要保留的設定檔數目，並將其納入您的構成中，
* [分割](#split):根據隨機百分比或屬性，將您的構圖分割成多個路徑。

您可以新增 **[!UICONTROL 對象]** 和 **[!UICONTROL 排除]** 活動。 不過，在 **[!UICONTROL 排名]** 和 **[!UICONTROL 分割]** 活動。

您可以隨時按一下右窗格中的刪除按鈕，從畫布中移除活動。  如果要刪除的活動是構成中其他活動的父項，則會顯示一條消息，允許您指定是否僅刪除所選活動或其所有子活動。

### 對象活動 {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="對象活動"
>abstract="對象活動可讓您在組合中包含屬於現有對象的其他設定檔。"

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="合併類型"
>abstract="指定應如何合併選取對象的設定檔。"

此 **[!UICONTROL 對象]** 活動可讓您在構成中包含屬於現有對象的其他設定檔。

此活動的設定與開始 [對象活動](#starting-audience).

### 排除活動 {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="排除類型"
>abstract="使用排除對象類型以排除屬於現有對象的設定檔。使用屬性類型的排除可讓您根據特定屬性排除設定檔。"

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="排除活動"
>abstract="排除活動可讓您透過選取現有對象或使用規則從您的組合中排除設定檔。"

此 **[!UICONTROL 排除]** 活動可讓您從構成中排除設定檔。 有兩種排除類型可供使用：

* **[!UICONTROL 排除對象]**:排除屬於現有對象的設定檔。

   按一下 **[!UICONTROL 新增對象]** 按鈕，然後選取要排除的對象。

   ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL 使用屬性排除]**:根據特定屬性排除設定檔。

   選取要查詢的屬性，然後指定要排除的值。 在此範例中，我們會從其首頁位址位於日本的構成設定檔中排除。

   ![](assets/audiences-exclude-attribute.png)

### 豐富 {#enrich}

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich"
>title="擴充活動"
>abstract="使用擴充活動以排除屬於現有對象的設定檔。使用屬性類型的排除可讓您根據特定屬性排除設定檔。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_dataset"
>title="擴充資料集"
>abstract="選取擴充資料集，其中會包含要和對象建立關聯的資料。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_criteria"
>title="擴充條件"
>abstract="選取欄位以用作來源資料集 (即對象) 和擴充資料集之間的調解金鑰。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_attributes"
>title="擴充屬性"
>abstract="從擴充資料集中選取要和對象相關聯的一或多個屬性。一旦發佈組合，這些屬性就會和對象相關聯，並且可以在行銷活動中加以利用以將傳遞個人化。"

此 **[!UICONTROL 豐富]** 活動可讓您透過來自Adobe Experience Platform資料集的其他屬性，讓對象更為豐富。 例如，您可以新增與購買產品相關的資訊，如其名稱、價格或製造商ID，並運用這些資訊來個人化傳送給對象的傳送。

>[!IMPORTANT]
>
>目前，資料集上的標籤（無論是在資料集層級或欄位層級）都不會傳播至新建立的對象。 這可能會影響所產生對象的存取控制和/或資料控管。 因此，合成對象時，請僅使用測試資料。

若要設定活動，請遵循下列步驟：

1. 選取 **[!UICONTROL 擴充資料集]** 包含您要與對象建立關聯的資料。

1. 在 **[!UICONTROL 擴充條件]** 區段，選取要作為來源資料集（即對象）與擴充資料集之間調解金鑰的欄位。 在此範例中，我們使用已購買產品的ID作為調解金鑰。

1. 按一下 **[!UICONTROL 新增屬性]** 按鈕，然後從擴充資料集中選取一或多個屬性，以關聯至對象。

   ![](assets/audiences-enrich-activity.png)

發佈構圖後，選取的屬性會與對象相關聯，並可在行銷活動中運用，以個人化傳送。

### 排名活動 {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="排名活動"
>abstract="排名可讓您根據特定屬性對設定檔進行排名，並將它們包含在您的組合中。例如，包含忠誠度點數最多的 50 個設定檔。"

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="新增設定檔限制"
>abstract="開啟此選項以指定要包含在組合中的設定檔的最大數量。"

此 **[!UICONTROL 排名]** 活動可讓您根據特定屬性來排名設定檔，並將其納入您的構成中。 例如，您可以包含50個設定檔，其忠誠度點數最多。

1. 選取您要查詢的屬性，並指定排名順序（遞增或遞減）。

   >[!NOTE]
   >
   >您可以選取具有下列資料類型的屬性：整數，數字，短 <!--(other?)-->

1. 切換 **[!UICONTROL 新增設定檔限制]** 選項，並指定要包含在合成中的設定檔數目上限。

   ![](assets/audiences-rank.png)

### 分割活動 {#split}

<!-- [!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Control Group"
>abstract="Use control groups to isolate a portion of the profiles. This allows you to measure the impact of a marketing activity and make a comparison with the behavior of the rest of the population."-->

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="分割活動"
>abstract="分割活動可讓您將組合分成多個路徑。發佈組合時，會針對每個路徑儲存一個對象到 Adobe Experience Platform 中。"

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="分割類型"
>abstract="使用百分比分割類型將設定檔隨機分割為多個路徑。屬性分割類型可讓您根據特定屬性分割設定檔。"

>[!CONTEXTUALHELP]
>id="ajo_ao_split_otherprofiles_text"
>title="其他設定檔"
>abstract="開啟此選項以建立額外路徑，其中剩餘的設定檔和其他路徑中指定的任何條件都不相符。"

此 **[!UICONTROL 分割]** 活動可讓您將構圖分割為多個路徑。

此操作會自動新增 **[!UICONTROL 儲存]** 活動。 發佈組合時，會針對每個路徑儲存一個對象到 Adobe Experience Platform 中。

可使用兩種類型的拆分操作：

* **[!UICONTROL 百分比分割]**:將設定檔隨機分割為兩個或多個路徑。 例如，您可以將設定檔分割為2個不同的路徑，每個路徑50%。 <!--and add an additional path for control group.-->

   ![](assets/audiences-split-percentage.png)

* **[!UICONTROL 屬性分割]**:根據特定屬性分割設定檔。 在此示例中，我們將根據檔案室類型首選項拆分配置檔案。

   ![](assets/audiences-split.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL 其他設定檔]** 選項可讓您使用其餘設定檔建立其他路徑，這些設定檔不符合其他路徑中指定的任何條件。

## 儲存您的對象 {#save}

設定將儲存至Adobe Experience Platform的產生對象。

若要這麼做，請選取 **[!UICONTROL 儲存對象]** 活動（在每個路徑結尾），然後指定要建立的新對象的名稱。

![](assets/audiences-publish.png)

您的構圖準備就緒後，即可發佈。 [了解如何建立作品](create-compositions.md)
