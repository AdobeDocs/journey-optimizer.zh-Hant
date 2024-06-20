---
solution: Journey Optimizer
product: journey optimizer
title: 可自訂的片段
description: 瞭解如何透過將其部分欄位設為可編輯來自訂片段。
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: ca743774017e8f6cf5f385119d9c71de6020bb19
workflow-type: tm+mt
source-wordcount: '1185'
ht-degree: 0%

---


# 可自訂的片段 {#customizable-fragments}

在行銷活動或歷程動作中使用片段時，由於繼承，預設情況下這些片段會鎖定。 這表示對片段所做的任何變更都會自動傳播至使用片段的所有行銷活動和歷程。 有了可自訂的片段，當片段新增到行銷活動或歷程動作時，片段中的特定欄位可以定義為可編輯。 例如，假設您有一個片段包含橫幅、一些文字和按鈕。 您可以將某些欄位（例如影像或按鈕目標URL）指定為可編輯。 這可讓使用者在將片段納入其行銷活動或歷程時修改這些元素，提供量身打造的體驗，而不會影響原始片段。

可自訂的片段不需要中斷片段繼承，這之前已停止將片段層級的集中式變更傳播至行銷活動和歷程。 此方法可在使用時調整內容部分，靈活地以內容特定的詳細資料覆寫預設值。

運用可自訂的片段，您可以有效地管理和個人化您的內容，而不需要建立全新的內容區塊或中斷原始片段的繼承。 這可確保在片段層級進行的變更仍會傳播，同時允許在行銷活動或歷程層級進行必要的自訂。

視覺效果和運算式片段都可以標示為可自訂。 有關如何繼續處理每種型別片段的詳細說明，請參閱以下章節。

![](../content-management/assets/do-not-localize/gif-fragments.gif)

## 在視覺片段中新增可編輯欄位 {#visual}

若要讓視覺化片段的某些部分可編輯，請遵循下列步驟：

>[!NOTE]
>
>可編輯欄位可新增至 **影像**， **文字** 和 **按鈕** 元件。 的 **HTML** 元件、可編輯的欄位是使用個人化編輯器新增的，類似於運算式片段。 [瞭解如何在HTML元件和運算式片段中新增可編輯欄位](#expression)

1. 開啟片段內容版本畫面。

1. 選取片段中要設定可編輯欄位的元件。

1. 元件屬性窗格會在右側開啟。 選取 **可編輯欄位** 標籤然後切換 **啟用版本** 選項。

1. 窗格中會列出所有可編輯所選元件的欄位。 可編輯的欄位取決於所選的元件型別。

   在以下範例中，我們允許編輯「按一下這裡」按鈕URL。

   ![](assets/fragment-param-enable.png)

1. 按一下 **概觀** 以檢查所有可編輯的欄位及其預設值。

   在此範例中，按鈕URL欄位會以元件中定義的預設值顯示。 使用者將片段新增至內容後，即可自訂此值。

   ![](assets/fragment-param-preview.png)

1. 準備就緒後，儲存您的變更以更新片段。

1. 將片段新增到電子郵件後，使用者將能夠自訂片段中設定的所有可編輯欄位。 [瞭解如何自訂視覺片段中的可編輯欄位](../email/use-visual-fragments.md#customize-fields)

## 在HTML元件和運算式片段中新增可編輯欄位 {#expression}

若要讓HTML元件或運算式片段的某些部分可編輯，您必須在運算式編輯器中使用特定語法。 這涉及宣告 **變數** 具有預設值，使用者可在將片段新增至其內容後覆寫。

例如，假設您要建立片段以新增至您的電子郵件，並允許使用者自訂用於不同位置的特定顏色，例如框架或按鈕的背景顏色。 建立片段時，您需要使用 **唯一識別碼**，例如「color」，並在片段內容中要套用此顏色的所需位置呼叫它。 將片段新增至其內容時，使用者將能夠自訂在任何參考變數的地方使用的顏色。

對於HTML元件，只有特定元素才能變成可編輯的欄位。 展開以下區段以取得詳細資訊。

+++HTML元件中的可編輯元素：

下列元素可以成為HTML元件中的可編輯欄位：

* 部分文字
* 連結或影像的完整URL （不適用於URL的一部分）
* 整個CSS屬性（無法搭配部分屬性使用）

例如，在下列程式碼中，每個以紅色反白顯示的元素都可以成為屬性：

![](assets/fragment-html.png){width=&quot;70%}

+++

若要宣告變數並將其用於片段中，請遵循下列步驟：

1. 開啟您的運算式片段，然後在個人化編輯器中編輯其內容。 對於HTML元件，選取片段中的元件，然後按一下 **顯示原始程式碼** 按鈕。

   ![](assets/fragment-html-edit.png)

1. 宣告您要讓使用者編輯的變數。 導覽至 **輔助函式** 功能表並新增 **內嵌** 輔助函式。 宣告及呼叫變數的語法會自動新增至內容中。

   ![](assets/fragment-add-helper.png)

1. 取代 `"name"` 具有唯一ID以識別可編輯欄位。

   >[!NOTE]
   >
   >欄位ID必須是唯一的，而且不能有空格。 此ID應在您的內容中要顯示變數值的任何位置使用。

1. 新增下表詳述的引數，調整語法以符合您的需求：

   | 動作 | 參數 | 範例 |
   | ------- | ------- | ------- |
   | 使用宣告可編輯欄位 **預設值**. 將片段新增至內容時，如果您未自訂該片段，將會使用此預設值。 | 在內嵌標籤之間新增預設值。 | `{{#inline "editableFieldID"}}default_value{{/inline}}` |
   | 定義 **標籤** 至可編輯欄位。 編輯片段的欄位時，此標籤將顯示在電子郵件Designer中。 | `name="title"` | `{{#inline "editableFieldID" name="title"}}default_value{{/inline}}` |
   | 宣告包含 **影像來源** 需要發佈的資訊。 | `assetType="image"` | `{{#inline "editableFieldID" assetType="image"}}default_value{{/inline}}` |
   | 宣告包含 **URL** 需要追蹤的專案。<br/>請注意，現成的「映象頁面URL」和「取消訂閱連結」預先定義區塊無法成為可編輯的欄位。 | `assetType="url"` | `{{#inline "editableFieldID" assetType="url"}}default_value{{/inline}}` |

1. 使用 `{{{name}}}` 程式碼中每個要顯示可編輯欄位值的位置的語法。 取代 `name` 具有先前定義之欄位的唯一ID。

   ![](assets/fragment-call-variable.png)

1. 儲存您的片段。

將片段新增至其電子郵件內容時，使用者現在可以使用其選擇的值覆寫變數的預設值：

* 對於運算式片段，會使用特定語法來覆寫變數值。 [瞭解如何自訂運算式片段中的可編輯欄位](../personalization/use-expression-fragments.md#customize-fields)

* 對於HTML元件，變數會顯示在電子郵件Designer的可編輯欄位清單中。 [瞭解如何自訂視覺片段中的可編輯欄位](../email/use-visual-fragments.md#customize-fields)

## 可編輯的運算式片段範例 {#example}

在以下範例中，我們正在建立呈現新運動集合的運算式片段。 依預設，片段會顯示此內容： *正在尋找更多嗎？ 不要錯過我們最新的運動系列！*

我們希望讓使用者能夠使用自己選擇的運動來取代本內容中的「運動」。 例如： *正在尋找更多嗎？ 不要錯過我們最新的瑜伽系列！*

若要這麼做：

1. 以ID &quot;sport&quot;宣告&quot;sport&quot;變數。

   根據預設，如果使用者在內容中新增片段後沒有變更變數值，則會顯示 `{{#inline}}` 和 `{{/inline}}` 標籤，即「運動」。

1. 新增 ``{{{sport}}}`` 您要顯示變數值（即預設為「sports」）或使用者所選值的片段內容語法。

   ![](assets/fragment-expression-custom.png)

1. 將運算式片段新增至其內容時，使用者可以直接從運算式編輯器中選擇變更變數值。 [瞭解如何自訂運算式片段中的可編輯欄位](../personalization/use-expression-fragments.md#customize-fields)

   ![](assets/fragment-expression-use.png)
