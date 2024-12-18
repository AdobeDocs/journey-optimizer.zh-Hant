---
solution: Journey Optimizer
product: journey optimizer
title: 使用組合畫布
description: 瞭解如何使用構成畫布
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 3eb9466e-9d88-4470-a22f-5e24a29923ae
source-git-commit: 01c14590fe55d8f11c1ff2b18141933b0b3dd5ca
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 28%

---

# 使用組合畫布 {#composition-canvas}

>[!BEGINSHADEBOX]

此文件提供如何在 Adobe Journey Optimizer 中使用客群構成的詳細資訊。 如果您沒有使用Adobe Journey Optimizer，[請按一下這裡](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=zh-Hant){target="_blank"}。

>[!ENDSHADEBOX]

對象構成提供視覺畫布，可讓您建立對象並使用各種活動（分割、擴充等）。

在畫布中組成對象的步驟如下：

1. [定義您的開始對象](#starting-audience)
1. [新增一或多個活動](#action-activities)
1. [將結果儲存至新的對象](#save)

## 選取起始對象 {#starting-audience}

建立構成的第一步是選取一或多個現有對象作為構成的基礎。

1. 選取&#x200B;**[!UICONTROL 對象]**&#x200B;活動，然後提供活動的標籤。

1. 選擇要鎖定的對象：

   * 按一下「**[!UICONTROL 新增對象]**」按鈕以選取一或多個現有對象，
   * 按一下&#x200B;**[!UICONTROL 建置規則]**&#x200B;按鈕，使用[細分服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hant)建立新的對象定義。

   ![](assets/audiences-choose-audience.png)

1. 如果選取多個對象，請指定合併這些對象之設定檔的方式：

* **[!UICONTROL 聯合]**：包含所選對象的所有設定檔，
* **[!UICONTROL 交集]**：包含所有選定對象通用的設定檔，
* **[!UICONTROL 排除重疊]**：僅包含屬於其中一個對象的設定檔。 屬於多個對象的設定檔將不會包括在內。

在此範例中，我們要將目標鎖定於屬於金級和銀級受眾的所有設定檔。

![](assets/audiences-starting-audience.png)

選取對象後，預估的個人資料數量會顯示在活動底部。

## 新增活動 {#action-activities}

在選取您的開始對象後新增活動，以精簡您的選取範圍。

若要這麼做，請按一下構成路徑上的+按鈕，然後選取所需活動。 右側窗格隨即開啟，可讓您設定新新增的活動。

![](assets/audiences-select-activity.png)

可用的活動包括：

* [對象](#audience)：包含屬於一或多個現有對象的其他設定檔，
* [排除](#exclude)：排除屬於現有對象的設定檔，或根據特定屬性排除設定檔，
* [擴充](#enrich)：使用來自Adobe Experience Platform資料集的其他屬性擴充您的對象，
* [排名](#rank)：根據特定屬性排名設定檔，指定要保留的設定檔數目，並將其納入您的構成中，
* [分割](#split)：根據隨機百分比或屬性，將構成分割為多個路徑。

您可以在構成中視需要新增最多&#x200B;**[!UICONTROL 個對象]**&#x200B;和&#x200B;**[!UICONTROL 排除]**&#x200B;個活動。 不過，在&#x200B;**[!UICONTROL Rank]**&#x200B;與&#x200B;**[!UICONTROL 分割]**&#x200B;活動之後，無法新增其他活動。

您可以隨時按一下右窗格中的刪除按鈕，從畫布中移除活動。  如果要刪除的活動是構成中其他活動的父項，則會顯示一則訊息，允許您指定是隻刪除所選活動，還是刪除其所有子活動。

### 客群活動 {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="客群活動"
>abstract="客群活動可讓您在組合中包含屬於現有客群的其他輪廓。"

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="合併類型"
>abstract="指定應如何合併選取客群的輪廓。"

**[!UICONTROL 對象]**&#x200B;活動可讓您在構成中包含屬於現有對象的其他設定檔。

此活動的設定與起始[對象活動](#starting-audience)相同。

### 排除活動 {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="排除類型"
>abstract="使用排除客群類型以排除屬於現有客群的輪廓。使用屬性類型的排除可讓您根據特定屬性排除輪廓。"

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="排除活動"
>abstract="排除活動可讓您透過選取現有客群或使用規則從您的組合中排除輪廓。"

**[!UICONTROL 排除]**&#x200B;活動可讓您從構成中排除設定檔。 有兩種排除型別可用：

* **[!UICONTROL 排除對象]**：排除屬於現有對象的設定檔。

  按一下&#x200B;**[!UICONTROL 新增對象]**&#x200B;按鈕，然後選取要排除的對象。

  ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL 使用屬性排除]**：根據特定屬性排除設定檔。

  選取要查詢的屬性，然後指定要排除的值。 在此範例中，我們將從首頁地址位於日本的構成設定檔中排除。

  >[!NOTE]
  >
  >只能指定一個排除值。

  ![](assets/audiences-exclude-attribute.png)

### 擴充活動 {#enrich}

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich"
>title="擴充活動"
>abstract="使用擴充活動透過來自 Adobe Experience Platform 資料集的其他屬性來擴充您的客群。例如，您可以新增與所購買產品相關的資訊 (例如名稱、價格或製造商 ID)，並利用這些資訊來個人化傳遞給客群的內容。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_dataset"
>title="擴充資料集"
>abstract="選取擴充資料集，其中會包含要和客群建立關聯的資料。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_criteria"
>title="擴充條件"
>abstract="選取欄位以用作來源資料集 (即客群) 和擴充資料集之間的調和金鑰。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_attributes"
>title="擴充屬性"
>abstract="從擴充資料集中選取要和客群相關聯的一或多個屬性。一旦發佈組合，這些屬性就會和客群相關聯，並且可以在 Journey Optimizer 行銷活動中加以利用以將傳遞個人化。"

**[!UICONTROL 擴充]**&#x200B;活動可讓您利用來自Adobe Experience Platform資料集的其他屬性來擴充您的對象。 例如，您可以新增與所購買產品相關的資訊 (例如名稱、價格或製造商 ID)，並利用這些資訊來個人化傳遞給客群的內容。

使用&#x200B;**[!UICONTROL 擴充]**&#x200B;活動時，請注意下列限制：

* 用於擴充的&#x200B;**資料集**&#x200B;必須是記錄型別（相對於事件型別），而且它們不能是系統資料集，也不能標籤為設定檔。 它們必須小於1GB。
* **擴充支援1:1聯結**。 也就是說，如果結合索引鍵在擴充資料集上具有多個相符專案，系統會挑選其中一個相符專案，並將其用於1:1結合。
* **可以在RTCDP目的地**&#x200B;中啟用對象，但無法啟用其擴充屬性（如果有的話）。
* 擴充屬性尚未與原則執行服務整合。 因此，您套用至擴充屬性的任何資料使用標籤，都不會在Journey Optimizer行銷活動或歷程中強制執行。

若要設定活動，請遵循下列步驟：

1. 選取&#x200B;**[!UICONTROL 擴充資料集]**，其中包含您要與對象建立關聯的資料。

1. 在&#x200B;**[!UICONTROL 擴充條件]**&#x200B;區段中，選取要做為來源資料集（即對象）與擴充資料集之間調解金鑰的欄位。 在此範例中，我們使用購買產品的ID作為調解金鑰。

1. 按一下&#x200B;**[!UICONTROL 新增屬性]**&#x200B;按鈕，然後從擴充資料集中選取一或多個屬性以關聯至對象。

   ![](assets/audiences-enrich-activity.png)

構成發佈後，選取的屬性會與對象建立關聯，並可在行銷活動中運用以個人化傳送。

### 排名活動 {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="排名活動"
>abstract="排名可讓您根據特定屬性對輪廓進行排名，並將它們包含在您的組合中。例如，包含忠誠度點數最多的 50 個輪廓。"

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="新增輪廓限制"
>abstract="開啟此選項以指定要包含在組合中的輪廓的最大數量。"

**[!UICONTROL 排名]**&#x200B;活動可讓您根據特定屬性來排名設定檔，並將它們納入您的組合中。 例如，您可以包含忠誠度點數最高的50個設定檔。

1. 選取您要查閱的屬性，並指定排名順序（升序或降序）。

   >[!NOTE]
   >
   >您可以選取具有以下資料型別的屬性：整數、數字、短<!--(other?)-->

1. 將&#x200B;**[!UICONTROL 新增設定檔限制]**&#x200B;選項切換為開啟，並指定要包含在構成中的設定檔數目上限。

   ![](assets/audiences-rank.png)

### 分割活動 {#split}

<!-- [!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Control Group"
>abstract="Use control groups to isolate a portion of the profiles. This allows you to measure the impact of a marketing activity and make a comparison with the behavior of the rest of the population."-->

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="分割活動"
>abstract="分割活動可讓您將組合分成多個路徑。發佈組合時，會針對每個路徑儲存一個客群到 Adobe Experience Platform 中。"

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="分割類型"
>abstract="使用百分比分割類型將輪廓隨機分割為多個路徑。屬性分割類型可讓您根據特定屬性分割輪廓。"

>[!CONTEXTUALHELP]
>id="ajo_ao_split_otherprofiles_text"
>title="其他輪廓"
>abstract="若剩餘的輪廓和其他路徑中指定的任何條件都不相符，開啟此選項為剩餘輪廓建立額外路徑。"

**[!UICONTROL 分割]**&#x200B;活動可讓您將撰寫分割成多個路徑。

此操作會在每個路徑的結尾自動新增&#x200B;**[!UICONTROL 儲存]**&#x200B;活動。 發佈組合時，會針對每個路徑儲存一個客群到 Adobe Experience Platform 中。

有兩種分割操作可供使用：

* **[!UICONTROL 百分比分割]**：將設定檔隨機分割成兩個或多個路徑。 例如，您可以將設定檔分割為2個各自為50%的相異路徑。<!--and add an additional path for control group.-->

  ![](assets/audiences-split-percentage.png)

* **[!UICONTROL 屬性分割]**：根據特定屬性分割設定檔。 在此範例中，我們根據它們的空間型別偏好來分割輪廓。

  ![](assets/audiences-split.png)

  若要設定以屬性為基礎的分割活動，請遵循下列步驟：

   1. 按一下&#x200B;**[!UICONTROL 屬性]**&#x200B;欄位旁的按鈕，選取要做為分割條件的屬性。
   1. 視需要新增多個路徑。 針對每個路徑，提供標籤並指定用來決定應包含在該特定路徑中的設定檔的值。

      >[!NOTE]
      >
      >每個路徑只能指定一個值。

   1. 開啟&#x200B;**[!UICONTROL 其他設定檔]**&#x200B;選項，使用不符合其他路徑中指定的任何條件的剩餘設定檔建立其他路徑。

## 儲存您的對象 {#save}

設定將儲存至Adobe Experience Platform中的結果對象。

若要這麼做，請選取每個路徑結尾的&#x200B;**[!UICONTROL 儲存對象]**&#x200B;活動，然後指定要建立的新對象名稱。

![](assets/audiences-publish.png)

當構成準備就緒後，即可發佈。 [瞭解如何建立組合](create-compositions.md)
