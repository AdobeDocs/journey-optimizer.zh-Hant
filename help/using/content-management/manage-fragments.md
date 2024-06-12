---
solution: Journey Optimizer
product: journey optimizer
title: 管理片段
description: 瞭解如何管理您的內容片段
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 1fc708e1-a993-4a2a-809c-c5dc08a4bae1
source-git-commit: e35f6b8ddc1e7bb8a737b33be200115a3022c99c
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 2%

---

# 管理片段 {#manage-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="新片段狀態"
>abstract="從 **草稿** 和 **即時** 狀態已在Journey Optimizer 6月版本中引入，在此版本之前建立的所有片段都會具有「草稿」狀態，即使它們用於歷程或行銷活動亦然。 如果您對這些片段進行變更，您需要發佈這些片段，以讓這些片段「即時」，並將變更傳播至關聯的行銷活動和歷程。"

若要管理您的片段，請從以下位置存取片段清單： **[!UICONTROL 內容管理]** > **[!UICONTROL 片段]** 左側功能表。

![](assets/fragment-list.png)

在目前沙箱建立的所有片段 —  [從 **[!UICONTROL 片段]** 功能表](#create-fragments)，使用 [另存為片段](#save-as-fragment) 選項 — 會顯示。

您可以在其上篩選片段：

* 型別： **[!UICONTROL 視覺]** 或 **[!UICONTROL 運算式]**
* 標記
* 建立或修改日期

您可以選擇顯示所有片段，或僅顯示目前使用者建立或修改的專案。

您也可以顯示 **[!UICONTROL 已封存]** 片段。 [了解更多](#archive-fragments)

![](assets/fragment-list-filters.png)

從 **[!UICONTROL 更多動作]** 按鈕時，您可以：

* 復製片段。

* 使用 **[!UICONTROL 探索引用]** 檢視歷程、行銷活動或使用範本的選項。 [了解更多](#explore-references)

* 封存片段。 [了解更多](#archive-fragments)

* 編輯片段的 [標籤](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## 編輯片段 {#edit-fragments}

若要編輯片段，請遵循以下步驟。

1. 從以下位置按一下所需的專案： **[!UICONTROL 片段]** 清單。
1. 從片段屬性中，您可以 [探索引用](#explore-references)， [管理其存取權](../administration/object-based-access.md)，並更新片段詳細資訊，包括 [標籤](../start/search-filter-categorize.md#tags).

   ![](../email/assets/fragment-edit-content.png)

1. 選取對應的按鈕來編輯內容，就像從頭開始建立片段時一樣。 [了解更多](#create-from-scratch)

>[!NOTE]
>
>當您編輯片段時，變更會自動傳播至使用該片段的所有內容，但中使用的內容除外 **[!UICONTROL 即時]** 歷程或行銷活動。 您也可以中斷原始片段的繼承。 進一步瞭解 [將視覺化片段新增至您的電子郵件](../email/use-visual-fragments.md#break-inheritance) 和 [利用運算式片段](../personalization/use-expression-fragments.md#break-inheritance) 區段。

## 探索參考 {#explore-references}

您可以顯示目前使用片段的歷程、行銷活動和內容範本清單。

若要這麼做，請選取 **[!UICONTROL 探索引用]** 來自 **[!UICONTROL 更多動作]** 「片段」清單或「片段屬性」畫面中的「 」功能表。

![](assets/fragment-explore-references.png)

選取索引標籤以在歷程、行銷活動、範本和片段之間切換。 您可以檢視其狀態，然後按一下名稱，重新導向至已引用片段的對應專案。

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>如果片段用於歷程、行銷活動或範本中，且標籤阻止您存取該片段，您會在選取的標籤上方看到警告訊息。 [深入瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md)

## 封存片段 {#archive-fragments}

您可以從不再與您的品牌相關的專案清除片段清單。

若要這麼做，請按一下 **[!UICONTROL 更多動作]** 按鈕並選取 **[!UICONTROL 封存]**. 它會從片段清單中消失，從而防止使用者在未來的電子郵件或範本中使用它。

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>如果您封存內容中使用的片段， <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->該內容將不會受到影響。

若要取消封存片段，請在 **[!UICONTROL 已封存]** 專案並選取 **[!UICONTROL 取消封存]** 從 **[!UICONTROL 更多動作]** 功能表。 現在仍可從片段清單存取，並可用於任何電子郵件或範本。

![](assets/fragment-list-unarchive.png)
