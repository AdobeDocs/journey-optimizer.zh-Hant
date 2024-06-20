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
source-git-commit: ca743774017e8f6cf5f385119d9c71de6020bb19
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 2%

---

# 在你的電子郵件中新增視覺內容片段 {#use-visual-fragments}

片段是可重複使用的元件，可在跨Journey Optimizer行銷活動、歷程或內容範本的一封或多封電子郵件中參考。 此功能允許預先建置多個自訂內容區塊，可供行銷使用者在改良的設計流程中快速組合電子郵件內容。 [瞭解如何建立和管理片段](../content-management/fragments.md).

➡️ [在本影片中瞭解如何管理、編寫和使用片段](../content-management/fragments.md#video-fragments)

## 使用片段 {#use-fragment}

若要在電子郵件中使用片段，請遵循下列步驟。

>[!NOTE]
>
>您最多可以在給定傳送中新增30個片段。 片段最多只能巢狀1個層級。


1. 使用開啟任何電子郵件或範本內容 [電子郵件設計工具](get-started-email-design.md).

1. 選取 **[!UICONTROL 片段]** 圖示加以檢視。

   ![](assets/fragments-in-designer.png)

1. 將會顯示在目前沙箱上建立的所有視覺化片段清單。 它們會依建立日期排序：最近新增的視覺片段會先顯示在清單中。 您可以：

   * 透過開始輸入其標籤來搜尋特定片段。
   * 以遞增或遞減順序排序片段。
   * 變更片段的顯示方式（卡片或清單檢視）。
   * 重新整理清單。

   >[!NOTE]
   >
   >如果您在編輯內容時修改或新增了某些片段，清單會以最新變更更新。

1. 從清單拖放任何片段到您要插入它的區域。

   ![](assets/fragment-insert.png)

   >[!CAUTION]
   >
   >您可以新增任何 **草稿** 或 **即時** 片段至您的內容。 但是，如果正在使用狀態為草稿的片段，您將無法啟用您的歷程或行銷活動。 在歷程或行銷活動發佈中，草稿片段將顯示錯誤，您需要核准它們才能發佈。
   >
   > 請注意，在Journey Optimizer 6月發行後的數天內，片段狀態會逐步推出。 雖然有些使用者可以立即存取，但有些使用者在其環境中使用前可能會遇到延遲問題。 如果您的環境中尚未提供此增強功能，請注意，片段不需要 **即時** 用於您的歷程與行銷活動。

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

## 自訂可編輯欄位 {#customize-fields}

如果所選片段的某些部分已變為可編輯，您可以將片段新增到內容中後覆寫其預設值。 [瞭解如何使您的片段可自訂](../content-management/customizable-fragments.md)

若要自訂片段中可編輯的欄位，請遵循下列步驟：

1. 將片段新增至您的內容並選取它，以開啟右側的屬性窗格。

1. 片段中的所有可編輯欄位都會顯示在 **設定** 標籤，在 **片段** 區段。

   在右窗格中選取可編輯欄位時，預覽窗格中會以綠色反白顯示可編輯欄位，以便輕鬆識別它們在內容中的位置。

   在以下範例中，影像 **來源** 和 **替代文字** 可編輯以及「按一下此處」按鈕 **URL**.

   ![](assets/fragment-editable.png)

## 中斷繼承 {#break-inheritance}

當您編輯視覺片段時，變更會同步。 它們會自動傳播到包含該片段的所有草稿或即時歷程/行銷活動和內容範本。

新增至電子郵件或內容範本時，預設會同步片段。 不過，您可以中斷原始片段的繼承。 在這種情況下，片段的內容會複製到目前的設計中，且變更不再同步。

若要中斷繼承，請遵循下列步驟：

1. 選取片段。

1. 按一下內容工具列中的解鎖圖示。

   ![](assets/fragment-break-inheritance.png)

1. 該片段會成為不再連結至原始片段的獨立元素。 編輯它，就像內容中的任何其他內容元件一樣。 [了解更多](content-components.md)
