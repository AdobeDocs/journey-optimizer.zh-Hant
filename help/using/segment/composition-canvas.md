---
solution: Journey Optimizer
product: journey optimizer
title: 使用組合畫布
description: 瞭解如何使用合成畫布
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 3eb9466e-9d88-4470-a22f-5e24a29923ae
badge: label="Beta" type="Informative"
source-git-commit: 66cf0332c62a9c3b034398c3a6046cbcec622d40
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 28%

---

# 使用組合畫布 {#composition-canvas}

>[!BEGINSHADEBOX]

本文件提供下列內容：

* [開始使用對象組合](get-started-audience-orchestration.md)
* [建立您的第一個組合工作流程](create-compositions.md)
* **[使用組合畫布](composition-canvas.md)**
* [存取及管理對象](access-audiences.md)

>[!ENDSHADEBOX]

觀眾合成提供了一個可視畫布，允許您建立觀眾並使用各種活動（拆分、豐富等）。

在畫布中合成受眾的步驟如下：

1. [定義起始受眾](#starting-audience)
1. [添加一個或多個活動](#action-activities)
1. [將結果保存到新受眾](#save)

## 選擇起始受眾 {#starting-audience}

建立作品的第一步是選擇一個或多個現有受眾作為作品的基礎。

1. 選擇 **[!UICONTROL 觀眾]** 活動，然後為活動提供標籤。

1. 選擇目標受眾：

   * 按一下 **[!UICONTROL 添加受眾]** 按鈕選擇一個或多個現有受眾，
   * 按一下 **[!UICONTROL 生成規則]** 按鈕，使用 [分段服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html)。

   ![](assets/audiences-choose-audience.png)

1. 如果選擇了多個受眾，請指定如何合併這些受眾的配置檔案：

* **[!UICONTROL 聯合]**:包括來自選定受眾的所有配置檔案，
* **[!UICONTROL 交集]**:包括所有選定受眾共同的配置檔案，
* **[!UICONTROL 排除重疊]**:包括僅屬於某個受眾的個人資料。 不包括屬於多個受眾的配置檔案。

在本示例中，我們希望針對屬於金銀觀眾的所有個人資料。

![](assets/audiences-starting-audience.png)

一旦選擇了受眾，估計的配置檔案數就會顯示在活動的底部。

## 添加活動 {#action-activities}

在選擇開始受眾後添加活動以優化您的選擇。

要執行此操作，請按一下合成路徑上的+按鈕，然後選擇所需的活動。 右窗格開啟，允許您配置新添加的活動。

![](assets/audiences-select-activity.png)

可用活動包括：

* [觀眾](#audience):包括屬於一個或多個現有受眾的其他配置檔案，
* [排除](#exclude):排除屬於現有受眾的配置檔案或根據特定屬性排除配置檔案，
* [豐](#enrich):通過Adobe Experience Platform資料集中的附加屬性豐富觀眾的生活，
* [排名](#rank):根據特定屬性對配置檔案進行分級，指定要保留的配置檔案數，並將其包括到您的構成中，
* [拆分](#split):根據隨機百分比或屬性將合成分為多個路徑。

可以添加盡可能多的 **[!UICONTROL 觀眾]** 和 **[!UICONTROL 排除]** 活動。 但是，不能在之後添加其他活動 **[!UICONTROL 排名]** 和 **[!UICONTROL 拆分]** 活動。

通過按一下右窗格中的刪除按鈕，可以隨時從畫布中刪除活動。  如果要刪除的活動是合成中其他活動的父項，則會顯示一條消息，允許您指定是否僅刪除選定的活動或其所有子活動。

### 對象活動 {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="對象活動"
>abstract="對象活動可讓您在組合中包含屬於現有對象的其他設定檔。"

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="合併類型"
>abstract="指定應如何合併選取對象的設定檔。"

的 **[!UICONTROL 觀眾]** 活動允許您將屬於現有受眾的其他配置檔案包括在合成中。

此活動的配置與啟動 [受眾活動](#starting-audience)。

### 排除活動 {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="排除類型"
>abstract="使用排除對象類型以排除屬於現有對象的設定檔。使用屬性類型的排除可讓您根據特定屬性排除設定檔。"

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="排除活動"
>abstract="排除活動可讓您透過選取現有對象或使用規則從您的組合中排除設定檔。"

的 **[!UICONTROL 排除]** 活動允許您從組合中排除配置檔案。 有兩種排除類型：

* **[!UICONTROL 排除受眾]**:排除屬於現有受眾的配置檔案。

   按一下 **[!UICONTROL 添加受眾]** 按鈕，選擇要排除的受眾。

   ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL 使用屬性排除]**:基於特定屬性排除配置檔案。

   選擇要查找的屬性，然後指定要排除的值。 在本示例中，我們從其家庭地址位於日本的合成配置檔案中排除。

   ![](assets/audiences-exclude-attribute.png)

### 豐 {#enrich}

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

的 **[!UICONTROL 豐]** 活動允許您通過來自Adobe Experience Platform資料集的其他屬性來豐富受眾。 例如，您可以添加與購買的產品相關的資訊，如產品名稱、價格或製造商ID，並利用這些資訊對發送給受眾的交貨進行個性化設定。

>[!IMPORTANT]
>
>目前，資料集上的標籤（無論是在資料集級別還是在欄位級別）不會傳播到新建立的受眾。 這可能會影響結果受眾的訪問控制和/或資料治理。 因此，在合成受眾時請只使用test資料。

要配置活動，請執行以下步驟：

1. 選擇 **[!UICONTROL 濃縮資料集]** 包含要與受眾關聯的資料。

1. 在 **[!UICONTROL 濃縮標準]** 部分，選擇要用作源資料集（即受眾）和富集資料集之間的協調鍵的欄位。 在本示例中，我們使用已購買產品的ID作為協調密鑰。

1. 按一下 **[!UICONTROL 添加屬性]** 按鈕，然後從富集資料集中選擇一個或多個屬性以與受眾關聯。

   ![](assets/audiences-enrich-activity.png)

一旦發佈了該構圖，所選屬性就與受眾相關聯，並且可以在市場活動中加以利用以個性化遞送。

### 排名活動 {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="排名活動"
>abstract="排名可讓您根據特定屬性對設定檔進行排名，並將它們包含在您的組合中。例如，包含忠誠度點數最多的 50 個設定檔。"

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="新增設定檔限制"
>abstract="開啟此選項以指定要包含在組合中的設定檔的最大數量。"

的 **[!UICONTROL 排名]** 活動允許您根據特定屬性對配置檔案進行排序，並將它們包括到組合中。 例如，您可以包括50個具有最大忠誠積分的配置檔案。

1. 選擇要查找的屬性並指定排序順序（升序或降序）。

   >[!NOTE]
   >
   >您可以選擇具有以下資料類型的屬性：整數，數字，短 <!--(other?)-->

1. 切換 **[!UICONTROL 添加配置檔案限制]** 選項，並指定要包含在合成中的最大配置檔案數。

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

的 **[!UICONTROL 拆分]** 活動允許您將合成分為多個路徑。

此操作會自動添加 **[!UICONTROL 保存]** 活動。 發佈組合時，會針對每個路徑儲存一個對象到 Adobe Experience Platform 中。

有兩種拆分操作：

* **[!UICONTROL 分解百分比]**:將配置檔案隨機拆分為兩條或多條路徑。 例如，可以將配置檔案拆分為2條不同的路徑，每條路徑50%。 <!--and add an additional path for control group.-->

   ![](assets/audiences-split-percentage.png)

* **[!UICONTROL 屬性拆分]**:基於特定屬性拆分配置檔案。 在本示例中，我們將根據檔案室類型首選項拆分配置檔案。

   ![](assets/audiences-split.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL 其他配置檔案]** 選項允許您使用與其它路徑中指定的任何條件不匹配的其餘配置檔案建立附加路徑。

## 保存您的受眾 {#save}

配置將保存到Adobe Experience Platform的結果受眾。

要執行此操作，請選擇 **[!UICONTROL 保存受眾]** 活動，然後指定要建立的新訪問群體的名稱。

![](assets/audiences-publish.png)

一旦你的作品準備好，你就可以發佈它。 [瞭解如何建立作文](create-compositions.md)
