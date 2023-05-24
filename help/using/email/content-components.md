---
solution: Journey Optimizer
product: journey optimizer
title: 使用電子郵件設計人員內容元件
description: 了解如何在電子郵件中使用內容元件
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 元件，電子郵件設計器，編輯器，電子郵件
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 54%

---

# 使用電子郵件設計器內容元件 {#content-components}

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

建立電子郵件內容時， **[!UICONTROL 內容元件]** 允許您使用原始元件進一步個性化您的電子郵件，這些原始元件一旦放入電子郵件中就可以編輯。

您可以根據需要在一個或多個結構元件內添加盡可能多的內容元件，這些元件定義了電子郵件的佈局。

## 新增內容元件 {#add-content-components}

若要將內容元件新增到電子郵件並根據您的需要進行調整，請依照以下步驟操作。

1. 在電子郵件設計工具中，使用現有內容或將&#x200B;**[!UICONTROL 結構元件]**&#x200B;拖放到您的空白內容以定義電子郵件的版面。[了解作法](content-from-scratch.md)

1. 若要存取「**[!UICONTROL 內容元件]**」區段，從電子郵件設計工具左窗格選取對應的按鈕。

   ![](assets/email_designer_content_components.png)

1. 將您選擇的內容元件拖放到相關結構元件內部。

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >您可以將多個元件新增到單一結構元件和結構元件的每個欄中。

1. 使用 **[!UICONTROL 設定]** 和 **[!UICONTROL 樣式]** 頁籤。 例如，您可以變更每個元件的文字樣式、邊框間距或邊界。[進一步了解對齊方式和邊框間距](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

1. 從 **[!UICONTROL 內容元件]**，您可以根據需要輕鬆刪除或複製任何內容元件。

   ![](assets/email_designer_content_components_settings_2.png)

## 容器 {#container}

要將特定樣式應用於一組內容元件，可以添加 **[!UICONTROL 容器]** 然後在其中添加所需的內容元件。 這樣，您就可以將不同的樣式應用於容器，這與應用於內部內容元件的樣式有所不同。

例如，新增&#x200B;**[!UICONTROL 容器]**&#x200B;元件，然後在該容器內部新增[按鈕](#button)元件。您可以為容器使用特定背景，為按鈕使用另一個背景。

![](assets/email_designer_container_component.png)

## 按鈕 {#button}

使用&#x200B;**[!UICONTROL 按鈕]**&#x200B;元件將一個或多個按鈕插入您的電子郵件，並將您的電子郵件對象重新導向到另一個頁面。

1. 從&#x200B;**[!UICONTROL 內容元件]**，將&#x200B;**[!UICONTROL 按鈕]**&#x200B;元件拖放到&#x200B;**[!UICONTROL 結構元件]**&#x200B;中。

1. 按一下新添加的按鈕以個性化文本並訪問 **[!UICONTROL 設定]** 和 **[!UICONTROL 樣式]** 頁籤。

   ![](assets/email_designer_button_component.png)

1. 從 **[!UICONTROL 連結]** 的子菜單。

1. 選擇您的受眾將如何與 **[!UICONTROL 目標]** 下拉清單：

   * **[!UICONTROL 無]**：當框架被點按時在相同框架中開啟連結 (預設)。
   * **[!UICONTROL 空白]**：在新的視窗或索引標籤中開啟連結。
   * **[!UICONTROL 自我]**：當框架被點按時在相同框架中開啟連結。
   * **[!UICONTROL 父系]**：在父框架中開啟連結。
   * **[!UICONTROL 頂端]**：在視窗的完整內文中開啟連結。

   ![](assets/email_designer_button_link.png)

1. 您可以變更樣式屬性 (例如&#x200B;**[!UICONTROL 邊框]**、**[!UICONTROL 大小]**、**[!UICONTROL 邊界]**&#x200B;等) 來進一步個人化您的按鈕。從「**[!UICONTROL 元件設定]**」窗格。

## 文字 {#text}

使用&#x200B;**[!UICONTROL 文字]**&#x200B;元件將文字插入電子郵件，並調整樣式 (邊框、大小、邊框間距等。)使用 **[!UICONTROL 樣式]** 頁籤。

![](assets/email_designer_text_component.png)

1. 從 **[!UICONTROL 內容元件]**，拖放 **[!UICONTROL 文本]** 元件 **[!UICONTROL 結構部件]**。

1. 按一下新添加的元件以個性化文本並訪問 **[!UICONTROL 設定]** 和 **[!UICONTROL 樣式]** 頁籤。

1. 使用以下工具列的選項變更文字：

   ![](assets/email_designer_27.png)

   * **[!UICONTROL 變更文字樣式]**：將粗體、斜體、底線或刪除線套用到文字。
   * **變更對齊方式**：選擇文字靠左對齊、靠右對齊、置中或左右對齊。
   * **[!UICONTROL 建立清單]**：新增項目符號清單或編號清單新增到文字。
   * **[!UICONTROL 設定標題]**：為文字新增標題，最多六層。
   * **字型大小**：選取文字的字型大小 (以像素為單位)。
   * **[!UICONTROL 更改字型顏色]**:選擇字型的顏色。
   * **[!UICONTROL 插入連結]**:將任何類型的連結添加到內容。
   * **[!UICONTROL 編輯影像]**：將影像或資產新增到文字元件。[瞭解有關資產管理的更多資訊](assets-essentials.md)
   * **[!UICONTROL 更改字型顏色]**:選擇字型的顏色。
   * **[!UICONTROL 新增個人化]**：新增個人化欄位以從設定檔資料自訂內容。[進一步了解內容個人化](../personalization/personalize.md)
   * **[!UICONTROL 顯示原始碼]**：顯示文字的原始碼。原始碼無法變更。
   * **[!UICONTROL 啟用條件式內容]**：新增條件式內容以使元件內容適應目標設定檔。[瞭解有關動態內容的詳細資訊](../personalization/get-started-dynamic-content.md)
   * **[!UICONTROL 複製]**：新增文字元件的副本。
   * **[!UICONTROL 刪除]**：從電子郵件刪除選取的文字元件。

1. 調整其他樣式屬性，例如文字顏色、字型系列、邊框、邊框間距、邊界等。從 **[!UICONTROL 樣式]** 頁籤。

   ![](assets/email_designer_text_component_2.png)

## 分隔線 {#divider}

使用&#x200B;**[!UICONTROL 分隔線]**&#x200B;元件以插入分隔線來組織電子郵件的版面和內容。

可以調整造型屬性，如從 **[!UICONTROL 設定]** 和 **[!UICONTROL 樣式]** 頁籤。

![](assets/email_designer_divider.png)

## HTML {#HTML}

使用 **[!UICONTROL HTML]**&#x200B;元件將現有 HTML 的不同部分進行複製貼上。這可讓您建立免費的模組化 HTML 元件以重複使用一些外部內容。

1. 從&#x200B;**[!UICONTROL 內容元件]**，將 **[!UICONTROL HTML]** 元件拖放到&#x200B;**[!UICONTROL 結構元件]**。

1. 按一下您新增的元件，然後選取「**[!UICONTROL 顯示原始碼]**」從內容關聯式工具列新增至 HTML。

   ![](assets/email_designer_html_component.png)

1. 複製並貼上要添加到電子郵件中的HTML代碼，然後按一下 **[!UICONTROL 保存]**。

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>為了簡單地使外部內容與電子郵件設計工具相容，Adobe 建議從頭開始建立訊息，然後將現有電子郵件的內容複製到元件中。

## 影像 {#image}

使用 **[!UICONTROL 影像]** 元件，將電腦中的影像檔案插入電子郵件內容。

1. 從 **[!UICONTROL 內容元件]**，拖放 **[!UICONTROL 影像]** 元件 **[!UICONTROL 結構部件]**。

   ![](assets/email_designer_image_content.png)

1. 按一下「**[!UICONTROL 瀏覽]**」從您的資產中選擇影像檔案。

   瞭解更多 [!DNL Assets Essentials]，請參閱 [Adobe Experience Manager Assets Essentials文檔](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}。

1. 按一下新添加的元件，然後從 **[!UICONTROL 設定]** 頁籤：

   * **[!UICONTROL 影像標題]**&#x200B;可讓您定義影像的標題。
   * **[!UICONTROL 替代文字]**&#x200B;可讓您定義連結到影像的註解。這對應於替代 HTML 屬性。

   ![](assets/email_designer_10.png)

1. 您也可以選擇 **[!UICONTROL 查找類似的股票照片]**。 [了解更多](stock.md)

1. 從 **[!UICONTROL 樣式]** 頁籤，調整其他樣式屬性，如邊距、邊框等。 或新增連結以將對象重新導向到「**[!UICONTROL 元件設定]**」窗格中的另一個內容。

## 社交 {#social}

使用&#x200B;**[!UICONTROL 社交]**&#x200B;元件將社交媒體頁面連結插入到電子郵件內容中。

1. 從&#x200B;**[!UICONTROL 內容元件]**，將&#x200B;**[!UICONTROL 社交]**&#x200B;元件拖放到&#x200B;**[!UICONTROL 結構元件]**&#x200B;中。

1. 選擇新添加的元件。

1. 在 **[!UICONTROL 社會]** 的 **[!UICONTROL 設定]** 頁籤，選擇要添加或刪除的社交媒體。

   ![](assets/email_designer_20.png)

1. 通過專用欄位選擇表徵圖的大小。

1. 按一下每個社交媒體表徵圖以配置 **[!UICONTROL URL]** 您的受眾將被重定向到。

   ![](assets/email_designer_21.png)

1. 如果需要，您還可以從資產中更改每個社交媒體的表徵圖。

1. 調整其他樣式屬性，例如樣式、邊界、邊框等。從 **[!UICONTROL 樣式]** 頁籤。

## 提供決定 {#offer-decision}

使用 **[!UICONTROL 提供決定]** 元件，以在消息中插入優惠。 的 [決策管理](../offers/get-started/starting-offer-decisioning.md) 引擎將選擇最佳優惠，交付給您的客戶。

1. 從 **[!UICONTROL 內容元件]**，拖放 **[!UICONTROL 提供決定]** 元件 **[!UICONTROL 結構部件]**。

1. 按一下 **[!UICONTROL 添加]** 選擇 **[!UICONTROL 提供決定]**。

   ![](assets/component_offers.png)

1. 從下拉清單中，選擇 **[!UICONTROL 放置]**。  然後，選擇 **[!UICONTROL 提供決定]** 要添加到內容中，然後按一下 **[!UICONTROL 添加]**。

   ![](assets/component_offers_2.png)

1. 從 **[!UICONTROL 提供決定]** 頁籤，可以預覽或更改插入的優惠。

瞭解如何將個性化服務添加到中的電子郵件中 [此部分](add-offers-email.md)。

>[!IMPORTANT]
>
>如果更改了在行程消息中使用的優惠決定，則需要取消發佈行程並重新發佈。  這將確保將更改納入旅程的消息，並確保消息與最新更新一致。
