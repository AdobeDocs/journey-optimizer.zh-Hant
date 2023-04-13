---
solution: Journey Optimizer
product: journey optimizer
title: 使用電子郵件設計人員內容元件
description: 了解如何在電子郵件中使用內容元件
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 元件，電子郵件設計工具，編輯器，電子郵件
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: 93e3ed9e1a9a437353b800aee58952b86eab9370
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 7%

---

# 使用電子郵件設計工具內容元件 {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components_email"
>title="關於內容元件"
>abstract="內容元件指可用於建立電子郵件版面的空白內容預留位置。"

>[!CONTEXTUALHELP]
>id="ac_content_components_landing_page"
>title="關於內容元件"
>abstract="內容元件指可用於建立登陸頁面版面的空白內容預留位置。"

>[!CONTEXTUALHELP]
>id="ac_content_components_fragment"
>title="關於內容元件"
>abstract="內容元件指可用於建立片段版面的空白內容預留位置。"

>[!CONTEXTUALHELP]
>id="ac_content_components_template"
>title="關於內容元件"
>abstract="內容元件指可用於建立範本版面的空白內容預留位置。"

建立電子郵件內容時， **[!UICONTROL 內容元件]** 可讓您使用原始元件進一步個人化電子郵件，放入電子郵件後，即可編輯這些原始元件。

您可以在一或多個結構元件內新增所需的內容元件，以定義電子郵件的版面。

## 新增內容元件 {#add-content-components}

若要新增內容元件至您的電子郵件並根據您的需求進行調整，請遵循下列步驟。

1. 在電子郵件設計工具中，使用現有內容或拖放 **[!UICONTROL 結構元件]** 填入空白內容，以定義電子郵件的版面。 [了解作法](content-from-scratch.md)

1. 若要存取 **[!UICONTROL 內容元件]** 節，從「電子郵件設計工具」左窗格中選擇相應的按鈕。

   ![](assets/email_designer_content_components.png)

1. 將您選取的內容元件拖放至相關結構元件內。

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >可以將多個元件添加到單個結構元件中，並添加到結構元件的每列中。

1. 使用 **[!UICONTROL 元件設定]** 窗格。 例如，您可以變更每個元件的文字樣式、邊框間距或邊界。 [進一步了解對齊方式和邊框間距](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

## 容器 {#container}

您可以新增一個簡單容器，在其中新增另一個內容元件。 這可讓您將特定樣式套用至容器，而容器與內使用的元件不同。

例如，新增 **[!UICONTROL 容器]** 元件，然後新增 [按鈕](#button) 元件。 您可以為容器使用特定背景，為按鈕使用另一個背景。

![](assets/email_designer_container_component.png)

## 按鈕 {#button}

使用 **[!UICONTROL 按鈕]** 元件，將一或多個按鈕插入電子郵件中，並將您的電子郵件對象重新導向至其他頁面。

1. 從 **[!UICONTROL 內容元件]**，拖放 **[!UICONTROL 按鈕]** 元件 **[!UICONTROL 結構元件]**.

1. 按一下您新增的按鈕，以個人化文字並存取 **[!UICONTROL 元件設定]** 在「電子郵件設計工具」右窗格中。

   ![](assets/email_designer_button_component.png)

1. 在 **[!UICONTROL 連結]** 欄位中，新增按一下按鈕時要重新導向的URL。

1. 選擇將對象重新導向至 **[!UICONTROL 目標]** 下拉式清單：

   * **[!UICONTROL 無]**:在與點按連結相同的時間格中開啟連結（預設）。
   * **[!UICONTROL 空白]**:在新視窗或索引標籤中開啟連結。
   * **[!UICONTROL Self]**:在按一下連結時的同一幀中開啟連結。
   * **[!UICONTROL 父級]**:開啟父框架中的連結。
   * **[!UICONTROL 頂端]**:在窗口的正文中開啟連結。

   ![](assets/email_designer_button_link.png)

1. 您可以透過變更樣式屬性(例如 **[!UICONTROL 邊框]**, **[!UICONTROL 大小]**, **[!UICONTROL 利潤]**、等 從 **[!UICONTROL 元件設定]** 框。

## 文字 {#text}

使用 **[!UICONTROL 文字]** 元件，將文字插入電子郵件中，並調整樣式（邊框、大小、邊框間距等） 使用 **[!UICONTROL 元件設定]** 框。

![](assets/email_designer_text_component.png)

1. 從 **[!UICONTROL 內容元件]**，拖放 **[!UICONTROL 文字]** 元件 **[!UICONTROL 結構元件]**.

1. 按一下您新新增的元件，以個人化文字並存取 **[!UICONTROL 元件設定]** 在「電子郵件設計工具」的右窗格中。

1. 使用工具列中的下列選項變更文字：

   ![](assets/email_designer_27.png)

   * **[!UICONTROL 更改文本樣式]**:將粗體、斜體、底線或直線套用至您的文字。
   * **更改對齊方式**:在文本的左對齊、右對齊、居中對齊或對齊對齊對齊之間進行選擇。
   * **[!UICONTROL 建立清單]**:將項目符號或數字清單新增至您的文字。
   * **[!UICONTROL 設定標題]**:在文字中加上最多六個標題層。
   * **字型大小**:選取文字的字型大小（像素）。
   * **[!UICONTROL 編輯影像]**:新增影像或資產至文字元件。 [深入了解資產管理](assets-essentials.md)
   * **[!UICONTROL 顯示原始碼]**:顯示文本的原始碼。 無法修改。
   * **[!UICONTROL 複製]**:新增文字元件的復本。
   * **[!UICONTROL 刪除]**:從電子郵件中刪除選取的文字元件。
   * **[!UICONTROL 新增個人化]**:新增個人化欄位以自訂來自您設定檔資料的內容。 [深入了解內容個人化](../personalization/personalize.md)
   * **[!UICONTROL 啟用條件式內容]**:新增條件式內容，以調整元件的內容與目標設定檔。 [深入了解動態內容](../personalization/get-started-dynamic-content.md)

1. 調整其他樣式屬性，如文本顏色、字型系列、邊框、邊框間距、邊距等。 從 **[!UICONTROL 元件設定]** 框。

## 除法器 {#divider}

使用 **[!UICONTROL 除法器]** 元件，插入分隔線以組織電子郵件的版面和內容。

您可以調整樣式屬性，例如線條顏色、樣式和高度， **[!UICONTROL 元件設定]** 框。

![](assets/email_designer_divider.png)

## HTML {#HTML}

使用 **[!UICONTROL HTML]** 元件來複製並貼上現有HTML的不同部分。 這可讓您建立免費的模組化HTML元件，以重複使用某些外部內容。

1. 從 **[!UICONTROL 內容元件]**，拖放 **[!UICONTROL HTML]** 元件 **[!UICONTROL 結構元件]**.

1. 按一下新增的元件，然後選取 **[!UICONTROL 顯示原始碼]** 來新增HTML。

   ![](assets/email_designer_html_component.png)

1. 複製並貼上您要新增至電子郵件的HTML程式碼，然後按一下 **[!UICONTROL 儲存]**.

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>為了讓外部內容與電子郵件設計工具相容，Adobe建議從草稿開始建立訊息，並將內容從您現有的電子郵件複製到元件中。

## 影像 {#image}

使用 **[!UICONTROL 影像]** 元件，將電腦中的影像檔案插入電子郵件內容中。

1. 從 **[!UICONTROL 內容元件]**，拖放 **[!UICONTROL 影像]** 元件 **[!UICONTROL 結構元件]**.

1. 按一下 **[!UICONTROL 瀏覽]** 從資產中選擇影像檔案。

   若要進一步了解 [!DNL Assets Essentials]，請參閱 [Adobe Experience Manager Assets Essentials檔案](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}.

1. 按一下新增的元件，並使用 **[!UICONTROL 元件設定]** 窗格：

   * **[!UICONTROL 影像標題]** 可讓您定義影像的標題。
   * **[!UICONTROL 替代文字]** 可讓您定義連結至影像的註解。 這對應於altHTML屬性。

   ![](assets/email_designer_10.png)

1. 調整其他樣式屬性，例如邊界、邊框等。 或新增連結，將您的對象重新導向至 **[!UICONTROL 元件設定]** 框。

## 社交 {#social}

使用 **[!UICONTROL 社交]** 元件，將社交媒體頁面的連結插入您的電子郵件內容中。

1. 從 **[!UICONTROL 內容元件]**，拖放 **[!UICONTROL 社交]** 元件 **[!UICONTROL 結構元件]**.

1. 按一下您新新增的元件。

1. 在 **[!UICONTROL 社交]** 欄位 **[!UICONTROL 元件設定]** ，選擇您要新增或移除的社交媒體。

   ![](assets/email_designer_20.png)

1. 通過專用欄位選擇表徵圖的大小。

1. 按一下您的每個社交媒體圖示，以設定 **[!UICONTROL URL]** 系統會將您的對象重新導向至其中。

   ![](assets/email_designer_21.png)

1. 如有需要，您也可以在 **[!UICONTROL 影像]** 欄位。

1. 調整其他樣式屬性，如樣式、邊界、邊框等。 從 **[!UICONTROL 元件設定]** 框。

## 優惠方案決策 {#offer-decision}

使用 **[!UICONTROL 優惠方案決策]** 元件，將選件插入訊息中。 此 [決策管理](../offers/get-started/starting-offer-decisioning.md) 引擎會挑選最合適的優惠方案，傳送給您的客戶。

了解如何在 [本節](add-offers-email.md).

>[!IMPORTANT]
>
>如果對歷程訊息中使用的優惠方案決策進行變更，您需要取消發佈歷程並重新發佈。  這可確保將變更納入歷程的訊息中，且訊息與最新更新一致。
