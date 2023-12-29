---
title: 管理網頁修改
description: 瞭解如何管理Journey Optimizer網頁內容中的修改
feature: Web Channel
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 213511b4-7556-4a25-aa23-b50acd11cd34
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 11%

---

# 管理網頁修改 {#manage-web-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="輕鬆管理所有變更"
>abstract="使用此窗格，您可以瀏覽和管理您新增到網頁的所有調整和樣式。"

您可以輕鬆管理新增至網頁的所有元件、調整和樣式。 您也可以直接從專用窗格新增修改。

## 使用修改窗格 {#use-modifications-pane}

1. 選取 **[!UICONTROL 修改]** 圖示來在左側顯示對應的窗格。

   ![](assets/web-designer-modifications-pane.png)

1. 您可以檢閱對頁面所做的每項變更。

1. 選取不想要的修改，然後按一下 **[!UICONTROL 刪除修改]** 選項來自 **[!UICONTROL 更多動作]** 按鈕以移除它。

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >刪除動作時請務必謹慎，因為動作可能會影響後續動作。

1. 若要同時刪除多項修改，請按一下 **[!UICONTROL 選取]** 按鈕在頂端 **[!UICONTROL 修改]** 窗格，檢查您選擇的修改內容，然後按一下 **[!UICONTROL 刪除]** 圖示。

   ![](assets/web-designer-modifications-select-delete.png)

1. 使用 **[!UICONTROL 更多動作]** 按鈕在頂端 **[!UICONTROL 修改]** 窗格，一次刪除所有修改。

   ![](assets/web-designer-delete-modifications.png)

1. 您也可以僅刪除無效的修改，亦即其他變更已覆寫這些變更。 例如，如果您修改文字的顏色，然後刪除該文字，則顏色修改會變成無效，因為該文字已不存在。

1. 您可以使用取消和重做動作 **[!UICONTROL 還原/重做]** 按鈕。

   ![](assets/web-designer-undo-redo.png)

   按住按鈕以在 **[!UICONTROL 還原]** 和 **[!UICONTROL 取消復原]** 選項。 然後按一下按鈕本身，套用所需的動作。

## 從專用窗格新增修改 {#add-modifications}

使用網頁設計工具編輯頁面時，您可以直接從 **[!UICONTROL 修改]** 窗格 — 不需從Web設計工具介面選取元件並加以編輯。 請遵循下列步驟。

1. 從 **[!UICONTROL 修改]** 窗格，按一下 **[!UICONTROL 更多動作]** 按鈕。

1. 選取 **[!UICONTROL 新增修改]**.

   ![](assets/web-designer-add-modification.png)

1. 選取修改型別：

   * **[!UICONTROL CSS選取器]** - [瞭解更多](#css-selector)
   * **[!UICONTROL 頁面`<Head>`]** - [瞭解更多](#page-head)

1. 輸入您的內容和 **[!UICONTROL 儲存]** 您的變更。

1. 按一下 **[!UICONTROL 更多動作]** 按鈕進行修改並選取 **[!UICONTROL 資訊]** 以顯示其詳細資料。

   ![](assets/web-designer-add-modification-info.png)

### CSS選取器 {#css-selector}

若要新增 **CSS選取器** 輸入修改，請遵循下列步驟。

1. 選取 **[!UICONTROL CSS選取器]** 作為修改型別。

1. 此 **[!UICONTROL CSS元素選取器]** 欄位可協助您尋找並選取要套用變更的HTML元素（或DOM樹狀結構中的節點）。 <!--specify the desired CSS element that you want to modify.-->

   ![](assets/web-designer-add-modification-css.png)

1. 選取動作型別(**[!UICONTROL 設定內容]** 或 **[!UICONTROL 設定屬性]**)並填入必要資訊/內容。

   * **[!UICONTROL 設定內容]**：指定進入元素的內容，該元素由 **[!UICONTROL CSS元素選取器]** 欄位。

   * **[!UICONTROL 設定屬性]**：指定要與目前CSS選取器關聯的屬性，以便此選取器可接著由此屬性識別。 若要這麼做，請在 **[!UICONTROL 屬性名稱]** 中的欄位和值 **[!UICONTROL 內容]** 欄位。 如果屬性已經存在，則會更新值；否則，會以指定的名稱和值新增屬性。

     ![](assets/web-designer-add-modification-css-attribute.png)

### 頁面 `<head>` {#page-head}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_head"
>title="新增自訂程式碼"
>abstract="HEAD 元素是中繼資料的容器，位於 HTML 標記和 BODY 標記之間。僅新增 SCRIPT 和 STYLE 元素。新增 DIV 標記和其他元素可能會造成其餘的 HEAD 元素出現在 BODY 中。"

您可以使用新增自訂程式碼 **[!UICONTROL 頁面`<head>`]** 修改型別。

此 `<head>` 元素是中繼資料（資料的相關資料）的容器，並放置在 `<html>` 標籤與 `<body>` 標籤之間。 在此情況下，程式碼不會等待內文或頁面載入事件，而是在頁面載入開始時執行。

此 `<head>` 元素常用來新增JavaScript或CSS程式碼至頁面頂端。 後續視覺化動作的選取器，會根據此標籤中新增的 HTML 元素而定。

若要新增 **頁面`<head>`** 輸入修改，請遵循下列步驟。

1. 選取 **[!UICONTROL 頁面`<head>`]** 作為修改型別。

   ![](assets/web-designer-add-modification-head-type.png)

1. 在中新增您的自訂程式碼 **[!UICONTROL 內容]** 方塊。

   >[!CAUTION]
   >
   >您只能新增 `<script>` 和 `<style>` 元素至 `<head>` 區段。 新增 `<div>` 標籤和其他元素可能會導致剩餘 `<head>` 元素以跳入 `<body>`.

1. 按一下 **[!UICONTROL 進階編輯選項]** 按鈕。 「運算式」編輯器開啟。

   ![](assets/web-designer-add-modification-head-advanced.png)

   您可以善用 [!DNL Journey Optimizer] 運算式編輯器及其所有個人化和編寫功能。 [了解更多](../personalization/personalization-build-expressions.md)

#### 自訂程式碼範例 {#custom-code-examples}

您可以使用 **[!UICONTROL 頁面`<head>`]** 修改型別：

* 使用JavaScript內嵌或連結至外部JavaScript檔案。

  例如，若要變更元素的顏色：

  ```
  <script type="text/javascript">
  document.getElementById("element_id").style.color = "blue";
  </script>
  ```

* 設定樣式內嵌或連結至外部樣式表。

  例如，若要定義覆蓋元素的類別：

  ```
  <style>
  .overlay
  { position: absolute; top:0; left: 0; right: 0; bottom: 0; background: red; }
  </style>
  ```

#### 自訂程式碼最佳作法 {#custom-code-best-practices}

+++ **請一律將自訂程式碼包裝在一個元素中。**

例如：

```
<script>
// Code goes here
</script>
```

如需進行任何修改，請在此容器內進行變更。

如果您不再需要自訂程式碼，只需將此容器留空，但不要將其移除。 這可確保其他體驗修改不受影響。

+++

+++ **請勿在自訂程式碼指令碼中執行document.write動作。**

指令碼會非同步執行。這通常會導致document.write動作出現在頁面上的錯誤位置。 不建議在自訂程式碼建立的指令碼中使用document.write。

+++

+++ **如果您建立元素然後加以修改，請勿刪除原始元素。**

每次變更都會在 **[!UICONTROL 修改]** 面板。 因為第二個動作會修改元素1，如果您刪除元素1，該動作便沒有任何專案需要修改，因此變更不再有作用。

+++

+++ **使用時要小心**[!UICONTROL &#x200B;頁面 `<head>`]**影響相同URL之兩個行銷活動的修改型別。**

如果您使用 **[!UICONTROL 頁面`<head>`]** 針對影響相同URL的兩個行銷活動的修改型別，JavaScript會從兩個行銷活動插入頁面。 [!DNL Journey Optimizer] 自動決定傳遞內容的順序。 確定程式碼不取決於放置位置。 您可以自行確定程式碼中是否有衝突。

+++
