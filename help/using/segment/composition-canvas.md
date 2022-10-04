---
title: 使用合成畫布
description: 了解如何使用構圖畫布
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: a51b41ddbb562137dc1f6cf15160ce326cc0564a
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# 使用合成畫布 {#composition-canvas}

合成畫布是視覺畫布，可讓您運用對象和活動（分割、排除……）來建立合成。

在合成畫布中配置合成的步驟如下：

1. [定義起始對象](#starting-audience)
1. [新增一或多個活動](#action-activities)
1. [將結果儲存到新受眾](#save)

## 選取開始對象 {#starting-audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="合併類型"
>abstract="指定應如何合併所選對象的設定檔。"

建立構圖的第一個步驟是選取一或多個現有對象，作為構圖的基礎。

選取 **[!UICONTROL 對象]** 活動，然後按一下 **[!UICONTROL 新增對象]** 按鈕，然後選取一或多個對象。

在此範例中，我們想要鎖定屬於金級和銀級受眾的所有設定檔。

![](assets/audiences-starting-audience.png)

如果您選取多個對象，請指定如何合併這些對象的設定檔：

* **[!UICONTROL 聯合]**:包含來自所選對象的所有設定檔，
* **[!UICONTROL 交集]**:包含所有所選對象共同的設定檔，
* **[!UICONTROL 排除重疊]**:包含僅屬於其中一個對象的設定檔。 不會包含屬於多個對象的設定檔。

## 新增活動 {#action-activities}

在選取您的起始對象後新增活動，以調整您的選取範圍。

若要這麼做，請按一下構成路徑上的+按鈕，然後選取所需的活動。 右窗格隨即開啟，可讓您設定活動。

![](assets/audiences-select-activity.png)

>[!NOTE]
>
>您可以新增 **[!UICONTROL 對象]** 和 **[!UICONTROL 排除]** 活動。 不過，在 **[!UICONTROL 排名]** 和 **[!UICONTROL 分割]** 活動。

您可以隨時按一下右窗格中的刪除按鈕，從畫布中移除活動。 在此活動之後新增的所有活動也將從畫布中移除。

可用活動包括：

* [對象](#audience):包含屬於一或多個現有對象的其他設定檔，
* [排除](#exclude):排除屬於現有對象的設定檔，或根據特定屬性排除設定檔，
* [排名](#rank):根據特定屬性來排名設定檔，指定要保留的設定檔數目，並將其納入您的構成中，
* [分割](#split):根據隨機百分比或屬性，將您的構圖分割成多個路徑。

### 對象活動 {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="對象活動"
>abstract="「對象」活動可讓您在合成中包含屬於現有對象的其他設定檔。"

此 **[!UICONTROL 對象]** 活動可讓您在構成中包含屬於現有對象的其他設定檔。

此活動的設定與開始 [對象活動](#starting-audience).

### 排除活動 {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="排除類型"
>abstract="使用排除對象類型來排除屬於現有對象的設定檔。 使用屬性類型排除可讓您根據特定屬性排除設定檔。"

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="排除活動"
>abstract="「排除」活動可讓您選取現有對象或使用規則，從您的構成中排除設定檔。"

此 **[!UICONTROL 排除]** 活動可讓您從構成中排除設定檔。 有兩種排除類型可供使用：

* **[!UICONTROL 排除對象]**:排除屬於現有對象的設定檔。

   按一下 **[!UICONTROL 新增對象]** 按鈕，然後選取要排除的對象。

   ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL 使用屬性排除]**:根據特定屬性排除設定檔。

   選取要查詢的屬性，然後指定要排除的值。 在此範例中，我們會從其首頁位址位於日本的構成設定檔中排除。

   ![](assets/audiences-exclude-attribute.png)

### 排名活動a {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="排名活動"
>abstract="「排名」活動可讓您根據特定屬性來排名設定檔，並將其納入您的構成中。 例如，包含50個設定檔，其忠誠度點數最多。"

此 **[!UICONTROL 排名]** 活動可讓您根據特定屬性來排名設定檔，並將其納入您的構成中。 例如，您可以包含50個設定檔，其忠誠度點數最多。

1. 選取您要查詢的屬性，並指定排名順序（遞增或遞減）。

   >[注意]
   >
   >您可以選取具有下列資料類型的屬性：整數，數字，短 <!--(other?)-->

1. 切換 **[!UICONTROL 新增設定檔限制]** 選項，並指定要包含在合成中的設定檔數目上限。

   ![](assets/audiences-rank.png)

### 分割活動 {#split}

>[!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="控制組為"
>abstract="使用控制組來隔離部分設定檔。 這可讓您測量行銷活動的影響，並與其他人口的行為進行比較。"

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="分割活動"
>abstract="「分割」活動可讓您將構圖分割為多個路徑。 發佈構圖時，每個路徑會將一個對象儲存至Adobe Experience Platform。"

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="分割類型"
>abstract="使用「百分比分割」類型將設定檔隨機分割為多個路徑。 屬性分割類型可讓您根據特定屬性來分割設定檔。"

此 **[!UICONTROL 分割]** 活動可讓您將構圖分割為多個路徑。

此操作會自動新增 **[!UICONTROL 儲存]** 活動。 發佈構圖時，每個路徑會將一個對象儲存至Adobe Experience Platform。

可使用兩種類型的拆分操作：

* **[!UICONTROL 百分比分割]**:將設定檔隨機分割為兩個或多個路徑。 例如，您可以將設定檔分割為2個不同的路徑，每個路徑45%，然後為控制組新增其他路徑。

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

更多詳情:

* [開始使用受眾構成](get-started-audience-orchestration.md)
* [建立合成工作流程](create-compositions.md)
* [存取及管理對象](access-audiences.md)
