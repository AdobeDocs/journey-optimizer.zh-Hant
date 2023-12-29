---
solution: Journey Optimizer
product: journey optimizer
title: 使用視覺化片段
description: 瞭解如何在Journey Optimizer行銷活動和歷程中建立電子郵件時使用視覺片段
feature: Email Design, Fragments
topic: Content Management
role: User
level: Beginner
exl-id: 25a00f74-ed08-479c-9a5d-4185b5f3c684
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 3%

---

# 在你的電子郵件中新增視覺內容片段 {#use-visual-fragments}

您可以在以下專案中使用視覺效果片段： [電子郵件](get-started-email-design.md) 在歷程或行銷活動中，或在 [內容範本](../content-management/content-templates.md).

>[!NOTE]
>
>瞭解如何在中建立和管理片段 [本節](../content-management/fragments.md).

➡️ [在本影片中瞭解如何管理、編寫和使用片段](../content-management/fragments.md#video-fragments)

## 使用片段 {#use-fragment}

1. 使用開啟任何電子郵件或範本內容 [電子郵件設計工具](get-started-email-design.md).

1. 選取 **[!UICONTROL 片段]** 圖示加以檢視。

   ![](assets/fragments-in-designer.png)

1. 將會顯示在目前沙箱上建立的所有視覺化片段清單。 您可以：

   * 透過開始輸入其標籤來搜尋特定片段。
   * 以遞增或遞減順序排序片段。
   * 變更片段的顯示方式（卡片或清單檢視）。

   >[!NOTE]
   >
   >片段會依建立日期排序：最近新增的視覺化片段會先顯示在清單中。

1. 您可以搜尋並重新整理清單。

   >[!NOTE]
   >
   >如果您在編輯內容時修改或新增了某些片段，清單會以最新變更更新。

1. 從清單拖放任何片段到您要插入它的區域。

   ![](assets/fragment-insert.png)

1. 如同任何其他元件，您可以在內容中移動片段。

1. 選取片段以在右側顯示對應的窗格。 從那裡，您可以從您的內容中刪除片段或複製它。 您也可以從片段上方顯示的內容功能表直接執行這些動作。

   ![](assets/fragment-right-pane.png)

1. 從 **[!UICONTROL 設定]** 標籤，您可以：

   * 選擇您要顯示片段的裝置。
   * 視需要在新索引標籤中開啟片段以編輯。 [了解更多](../content-management/fragments.md#edit-fragments)
   * 探索引用。 [了解更多](../content-management/fragments.md#explore-references)

1. 您可以使用進一步自訂您的片段 **[!UICONTROL 樣式]** 標籤。

1. 如有需要，您可以中斷具有原始片段的繼承。 [了解更多](#break-inheritance)

1. 新增任意數量的片段，並且 **[!UICONTROL 儲存]** 您的變更。

## 中斷繼承 {#break-inheritance}

當您編輯視覺片段時，變更會同步。 它們會自動傳播至所有 **[!UICONTROL 草稿]** 歷程/行銷活動以及包含該片段的內容範本。

>[!NOTE]
>
>變更不會傳播至中使用的電子郵件 **[!UICONTROL 即時]** 歷程或行銷活動。

新增至電子郵件或內容範本時，預設會同步片段。

不過，您可以中斷原始片段的繼承。 在這種情況下，片段的內容會複製到目前的設計中，且變更不再同步。

若要中斷繼承，請遵循下列步驟：

1. 選取片段。

1. 按一下內容工具列中的解鎖圖示。

   ![](assets/fragment-break-inheritance.png)

1. 該片段會成為不再連結至原始片段的獨立元素。 編輯它，就像內容中的任何其他內容元件一樣。 [了解更多](content-components.md)
