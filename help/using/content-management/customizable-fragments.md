---
solution: Journey Optimizer
product: journey optimizer
title: 可自訂的片段
description: 瞭解如何透過將其部分欄位設為可編輯來自訂片段。
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: cd47ca1d-f707-4425-b865-14f3fbbe5fd1
source-git-commit: 71d4fae1eecb2acfcf3ba889c58bf71fb74d48fa
workflow-type: tm+mt
source-wordcount: '1472'
ht-degree: 1%

---

# 可自訂的片段 {#customizable-fragments}

在行銷活動或歷程動作中使用片段時，由於繼承，預設情況下這些片段會鎖定。 這表示對片段所做的任何變更都會自動傳播至使用片段的所有行銷活動和歷程。

透過&#x200B;**可自訂的片段**，當片段新增至行銷活動或歷程動作時，片段內的特定欄位可以定義為可編輯。 例如，假設您有一個片段包含橫幅、一些文字和按鈕。 您可以將某些欄位（例如影像或按鈕目標URL）指定為可編輯。 這可讓使用者在將片段納入其行銷活動或歷程時修改這些元素，提供量身打造的體驗，而不會影響原始片段。

可自訂的片段不需要中斷片段繼承，這之前已停止將片段層級的集中式變更傳播至行銷活動和歷程。 此方法可在使用時調整內容部分，靈活地以內容特定的詳細資料覆寫預設值。

運用可自訂的片段，您可以有效地管理和個人化您的內容，而不需要建立全新的內容區塊或中斷原始片段的繼承。 這可確保在片段層級進行的變更仍會傳播，同時允許在行銷活動或歷程層級進行必要的自訂。

視覺效果和運算式片段都可以標示為可自訂。 有關如何繼續處理每種型別片段的詳細說明，請參閱以下章節。

![](../content-management/assets/do-not-localize/gif-fragments.gif)

## 將可編輯欄位新增至視覺片段 {#visual}

若要讓視覺化片段的某些部分可編輯，請遵循下列步驟：

>[!NOTE]
>
>可編輯的欄位可新增至&#x200B;**影像**、**文字**&#x200B;和&#x200B;**按鈕**&#x200B;元件。 針對&#x200B;**HTML**&#x200B;元件，使用個人化編輯器新增可編輯的欄位，類似於運算式片段。 [瞭解如何在HTML元件和運算式片段中新增可編輯的欄位](#expression)

1. 開啟片段內容版本畫面。

1. 選取片段中要設定可編輯欄位的元件。

1. 元件屬性窗格會在右側開啟。 選取&#x200B;**可編輯欄位**&#x200B;標籤，然後切換&#x200B;**啟用版本**&#x200B;選項。

1. 窗格中會列出所有可編輯所選元件的欄位。 可編輯的欄位取決於所選的元件型別。

   在以下範例中，我們允許編輯「按一下這裡」按鈕URL。

   ![](assets/fragment-param-enable.png)

1. 按一下&#x200B;**總覽**&#x200B;以檢查所有可編輯的欄位及其預設值。

   在此範例中，按鈕URL欄位會以元件中定義的預設值顯示。 使用者將片段新增至內容後，即可自訂此值。

   ![](assets/fragment-param-preview.png)

1. 準備就緒後，儲存您的變更以更新片段。

1. 將片段新增到電子郵件後，使用者將能夠自訂片段中設定的所有可編輯欄位。 [瞭解如何自訂視覺片段中的可編輯欄位](../email/use-visual-fragments.md#customize-fields)

## 將可編輯的欄位新增至HTML元件和運算式片段 {#expression}

若要讓HTML元件或運算式片段的某些部分可編輯，您必須在運算式編輯器中使用特定語法。 這涉及宣告具有預設值的&#x200B;**變數**，使用者在將片段新增至其內容後可以覆寫該變數。

例如，假設您要建立片段以新增至您的電子郵件，並允許使用者自訂用於不同位置的特定顏色，例如框架或按鈕的背景顏色。 建立片段時，您必須使用&#x200B;**唯一識別碼**&#x200B;宣告變數（例如&quot;color&quot;），並在片段內容中要套用此顏色的所需位置呼叫它。 將片段新增至其內容時，使用者將能夠自訂在任何參考變數的地方使用的顏色。

針對HTML元件，只有特定元素才能變成可編輯的欄位。 展開以下區段以取得詳細資訊。

+++HTML元件中的可編輯元素：

下列元素可成為HTML元件中的可編輯欄位：

* 部分文字
* 連結或影像的完整URL （不適用於URL的一部分）
* 整個CSS屬性（無法搭配部分屬性使用）

例如，在下列程式碼中，每個以紅色反白顯示的元素都可以成為屬性：

![](assets/fragment-html.png){width="70%"}

+++

若要宣告變數並將其用於片段中，請遵循下列步驟：

1. 開啟您的運算式片段，然後在個人化編輯器中編輯其內容。

   ![](assets/fragment-html-edit.png)

   針對HTML元件，選取片段中的元件，然後按一下&#x200B;**顯示原始程式碼**&#x200B;按鈕。

1. 宣告您要讓使用者編輯的變數。 導覽至左側導覽窗格中的&#x200B;**協助程式功能**&#x200B;功能表，然後新增&#x200B;**內嵌**&#x200B;協助程式功能。 宣告及呼叫變數的語法會自動新增至內容中。

   ![](assets/fragment-add-helper.png)

1. 以唯一ID取代`"name"`以識別可編輯的欄位。

   >[!NOTE]
   >
   >欄位ID必須是唯一的，而且不能有空格。 此ID應在您的內容中要顯示變數值的任何位置使用。

1. 新增下表詳述的引數，調整語法以符合您的需求：

   | 動作 | 參數 | 範例 |
   | ------- | ------- | ------- |
   | 宣告具有&#x200B;**預設值**&#x200B;的可編輯欄位。 將片段新增至內容時，如果您未自訂該片段，將會使用此預設值。 | 在內嵌標籤之間新增預設值。 | `{{#inline "editableFieldID"}}default_value{{/inline}}` |
   | 為可編輯欄位定義&#x200B;**標籤**。 編輯片段的欄位時，此標籤將顯示在電子郵件Designer中。 | `name="title"` | `{{#inline "editableFieldID" name="title"}}default_value{{/inline}}` |
   | 宣告包含需要發佈的&#x200B;**影像來源**&#x200B;的可編輯欄位。 | `assetType="image"` | `{{#inline "editableFieldID" assetType="image"}}default_value{{/inline}}` |
   | 宣告包含需要追蹤之&#x200B;**URL**&#x200B;的可編輯欄位。<br/>請注意，現成的「映象頁面URL」和「取消訂閱連結」預先定義區塊無法成為可編輯的欄位。 | `assetType="url"` | `{{#inline "editableFieldID" assetType="url"}}default_value{{/inline}}` |

1. 在您要顯示可編輯欄位值的每個位置，使用程式碼中的`{{{name}}}`語法。 將`name`取代為先前定義之欄位的唯一識別碼。

   ![](assets/fragment-call-variable.png)

1. 儲存並發佈您的片段。

將片段新增至其電子郵件內容時，使用者現在可以使用其選擇的值覆寫變數的預設值：

* 對於運算式片段，會使用特定語法來覆寫變數值。 [瞭解如何自訂運算式片段中的可編輯欄位](../personalization/use-expression-fragments.md#customize-fields)

* 對於HTML元件，變數會顯示在電子郵件Designer的可編輯欄位清單中。 [瞭解如何自訂視覺片段中的可編輯欄位](../email/use-visual-fragments.md#customize-fields)

### 可編輯的運算式片段範例 {#example}

在以下範例中，我們正在建立呈現新運動集合的運算式片段。 依預設，片段會顯示此內容： *要尋找更多嗎？ 不要錯過我們最新的運動系列！*

我們希望讓使用者能夠使用自己選擇的運動來取代本內容中的「運動」。 例如：*正在尋找更多嗎？ 不要錯過我們最新的瑜伽系列！*

若要這麼做：

1. 以ID &quot;sport&quot;宣告&quot;sport&quot;變數。

   根據預設，如果使用者在其內容中新增片段後未變更變數的值，它將顯示`{{#inline}}`和`{{/inline}}`標籤之間定義的值，即「sports」。

1. 在您想要顯示變數值（即預設為「sports」）或使用者選擇的值的片段內容中新增``{{{sport}}}``語法。

   ![](assets/fragment-expression-custom.png)

1. 將運算式片段新增至其內容時，使用者可以直接從運算式編輯器中選擇變更變數值。 [瞭解如何自訂運算式片段中的可編輯欄位](../personalization/use-expression-fragments.md#customize-fields)

   ![](assets/fragment-expression-use.png)

## 將RTF文字新增至可自訂的片段 {#rich-text}

RTF文字（例如分行符號、粗體、斜體等）可以使用HTML元件新增到可編輯的片段中。 若要執行此操作，請遵循下列步驟。
<!--
➡️ [Learn how to add and use rich text to an editable fragment in this video](#video)-->

### 建立包含RTF文字的片段 {#add-rich-text}

1. 建立視覺化[片段](create-fragments.md)並開始新增元件。

1. 新增[HTML元件](../email/content-components.md#HTML)並開啟HTML編輯器。

1. 導覽至左側導覽窗格中的&#x200B;**[!UICONTROL 協助程式功能]**&#x200B;功能表，然後新增&#x200B;**內嵌**&#x200B;協助程式功能。

1. 將`"name"`取代為您要用於可編輯內容的ID，例如&quot;EditableContent&quot;。

1. 將`render_content`取代為您想要的預設豐富內容所對應的HTML程式碼。 您可以新增粗體、斜體、分行符號、專案符號清單等。

   ![](assets/fragment-rich-editable-content.png)

1. 在同一HTML元件中，為您的樣式元素新增另一個&#x200B;**內嵌**&#x200B;協助程式函式。

1. 以與您想要的預設樣式相對應的ID和HTML程式碼取代`"name"`和`render_content`。

   ![](assets/fragment-rich-editable-styling.png)

1. 儲存您的內容。 選取的可編輯欄位會顯示在右側。

   ![](assets/fragment-rich-editable-fields.png)

1. 儲存並[發佈](create-fragments.md#publish)片段。

### 使用RTF可編輯片段 {#use-rich-text}

將片段新增至其電子郵件內容時，使用者現在可以編輯您建立的RTF文字內容和樣式。 若要以行銷人員身分使用RTF可編輯片段，請遵循下列步驟。

1. [在行銷活動或歷程中建立電子郵件](../email/create-email.md)，然後新增包含[已建立](#add-rich-text)之RTF文字的片段。

   您可以在右側看到已建立的兩個可編輯欄位。

   ![](assets/fragment-use-rich-editable-fields.png)

1. 您可以按一下&#x200B;**[!UICONTROL 模擬內容]**，檢視可編輯的內容和樣式如何呈現。 [進一步瞭解預覽內容](preview-test.md)

1. 選取其中一個可編輯欄位旁的&#x200B;**[!UICONTROL 新增個人化]**&#x200B;圖示。

1. 在開啟的個人化編輯器中，新增或移除可編輯欄位的元素，視需要更新<!--CSS-->樣式和/或內容。

   ![](assets/fragment-rich-editable-fields-update-styling.png)

<!--
## How-to video {#video}

This video shows how to make HTML components within a fragment editable, allowing for dynamic updates to both content and styling.

>[!VIDEO](https://video.tv.adobe.com/v/3464363/?learn=on&#x26;enablevpops)
-->