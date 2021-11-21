---
title: 使用電子郵件設計人員內容元件
description: 了解如何在電子郵件中使用內容元件
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 2%

---

# 使用電子郵件設計工具內容元件 {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components"
>title="關於內容元件"
>abstract="內容元件是空白的內容預留位置，可用來建立電子郵件版面。"


從頭建立電子郵件內容時， **[!UICONTROL Content components]** 可讓您使用原始的空白元件進一步個人化您的電子郵件，放入電子郵件後即可使用這些元件。
您可以新增 **[!UICONTROL Content components]** 你需要內 **[!UICONTROL Structure component]** 定義電子郵件的版面。

## 按鈕 {#buttons}

使用 **[!UICONTROL Button]** 元件，在電子郵件中插入多個按鈕，並將您的電子郵件對象重新導向至其他頁面。

1. 從 **[!UICONTROL Content components]**，拖放 **[!UICONTROL Button]** 在 **[!UICONTROL Structure component]**.

   ![](assets/email_designer_13.png)

1. 按一下您新增的按鈕，以個人化文字並存取 **[!UICONTROL Components Settings]** 在電子郵件設計工具的右窗格中。

   ![](assets/email_designer_14.png)

1. 在 **[!UICONTROL Link]** 欄位 **[!UICONTROL Components Settings]**，新增您希望對象在按一下按鈕時重新導向的URL。

1. 選擇將對象重新導向至 **[!UICONTROL Target]** 下拉式清單：

   * **[!UICONTROL None]**:在與點按連結相同的時間格中開啟連結（預設）。
   * **[!UICONTROL Blank]**:在新視窗或索引標籤中開啟連結。
   * **[!UICONTROL Self]**:在按一下連結時的同一幀中開啟連結。
   * **[!UICONTROL Parent]**:開啟父框架中的連結。
   * **[!UICONTROL Top]**:在窗口的正文中開啟連結。

   ![](assets/email_designer_15.png)

1. 您現在可以透過變更 **[!UICONTROL Style]**, **[!UICONTROL Margin]** 和 **[!UICONTROL Border]** 例如，

## 文字 {#text}

使用 **[!UICONTROL Text]** 元件，在電子郵件中插入文字。 您可以在 **[!UICONTROL Component Settings]**.

1. 在 **[!UICONTROL Content Components]**，拖放 **[!UICONTROL Text]** 在 **[!UICONTROL Structure component]**.

   ![](assets/email_designer_11.png)

1. 按一下您新新增的元件，以個人化文字並存取 **[!UICONTROL Components Settings]** 在電子郵件設計工具的右窗格中。

1. 使用工具列中的下列選項變更文字：

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Change text style]**:將粗體、斜體、底線或直線套用至您的文字。
   * **更改對齊方式**:在文本的左對齊、右對齊、居中對齊或對齊對齊對齊之間進行選擇。
   * **[!UICONTROL Create list]**:將項目符號或數字清單新增至您的文字。
   * **[!UICONTROL Set heading]**:在文字中加上最多六個標題層。
   * **字型大小**:選取文字的字型大小（像素）。
   * **[!UICONTROL Edit image]**:新增影像或資產至文字元件。 [深入了解資產管理](assets-essentials.md).
   * **[!UICONTROL Show the source code]**:顯示文本的原始碼。 無法修改。
   * **[!UICONTROL Duplicate]**:新增文字元件的復本。
   * **[!UICONTROL Delete]**:從電子郵件中刪除選取的文字元件。
   * **[!UICONTROL Add personalization]**:新增個人化欄位以自訂來自您設定檔資料的內容。 [深入了解內容個人化](personalization/personalize.md).

1. 為獲得更好的使用者體驗，您可以新增個人化欄位以鎖定您的對象。 如需詳細資訊，請參閱本[區段](personalization/personalize.md)。

1. 調整 **[!UICONTROL Text color]**, **[!UICONTROL Font family]** 和 **[!UICONTROL Size]** 在 **[!UICONTROL Components Settings]**.

   ![](assets/email_designer_12.png)

## 除法器 {#divider}

使用 **[!UICONTROL Divider]** 元件，插入分隔線以組織電子郵件的版面和內容。
您可以選取斷線的顏色、樣式和大小，位於 **[!UICONTROL Component Settings]**.

![](assets/email_designer_16.png)

## HTML {#HTML}

使用 **[!UICONTROL HTML]** 複製並貼上現有HTML的不同部分。 這可讓您建立免費的模組化HTML元件。

為了讓外部內容與電子郵件設計工具相容，Adobe建議從草稿開始建立訊息，並將內容從您現有的電子郵件複製到元件中。

1. 在 **[!UICONTROL Content Components]**，拖放 **[!UICONTROL HTML]** 在 **[!UICONTROL Structure component]**.

   ![](assets/email_designer_22.png)

1. 按一下您新新增的元件，然後 **[!UICONTROL Show the source code]** 來新增HTML。

   ![](assets/email_designer_23.png)

1. 複製並貼上您要新增至電子郵件的HTML程式碼，然後按一下 **[!UICONTROL Save]**.

1. 您現在可以透過變更 **[!UICONTROL Style]**, **[!UICONTROL Margin]** 和 **[!UICONTROL Border]** 例如新增連結，將您的對象重新導向至其他內容。

## 影像 {#image}

使用 **[!UICONTROL Image]** 元件，從您的電腦在電子郵件中插入影像檔案。

1. 在 **[!UICONTROL Content Components]**，拖放 **[!UICONTROL Image]** 在 **[!UICONTROL Structure component]**.

   ![](assets/email_designer_9.png)

1. 按一下 **[!UICONTROL Browse]** 從資產中選擇影像檔案。

   若要進一步了解 [!DNL Assets Essentials]，請參閱 [Adobe Experience Manager Assets Essentials檔案](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}。

1. 按一下新增的元件，開始設定 **[!UICONTROL Content Components]** 並能夠 **[!UICONTROL Components Settings]** 在電子郵件設計工具的右窗格中。

1. 設定影像屬性：

   * **[!UICONTROL Image Title]** 可讓您定義影像的標題。
   * **[!UICONTROL Alt text]** 可讓您定義連結至影像的註解。 這對應於altHTML屬性。

   ![](assets/email_designer_10.png)

1. 您現在可以透過變更 **[!UICONTROL Style]**, **[!UICONTROL Margin]** 和 **[!UICONTROL Border]** 例如新增連結，將您的對象重新導向至其他內容。

## 影片 {#Video}

>[!CONTEXTUALHELP]
>id="ac_edition_video"
>title="視訊設定"
>abstract="使用此元件在電子郵件中插入視訊。 請注意，視訊無法用於所有電子郵件用戶端。 建議設定後援影像。"
>additional-url="https://www.emailonacid.com/blog/article/email-development/a_how_to_guide_to_embedding_html5_video_in_email/" text="其他資訊"

使用 **[!UICONTROL Video]** 元件，透過URL連結在電子郵件中插入視訊。

1. 在 **[!UICONTROL Content Components]**，拖放 **[!UICONTROL Video]** 在 **[!UICONTROL Structure component]**.

   ![](assets/email_designer_17.png)

1. 按一下新增的元件，開始設定 **[!UICONTROL Content Components]** 並能夠 **[!UICONTROL Components Settings]** 在電子郵件設計工具的右窗格中。

1. 在 **[!UICONTROL Video link]** 欄位 **[!UICONTROL Components Settings]**，新增您的視訊URL。

   ![](assets/email_designer_18.png)

1. 您可以新增 **[!UICONTROL Poster image]** 指定要顯示的影像，直到對象按一下播放按鈕為止。

1. 您現在可以透過變更 **[!UICONTROL Style]**, **[!UICONTROL Margin]** 和 **[!UICONTROL Border]** 例如，

## 社交 {#social}

使用 **[!UICONTROL Social]** 元件，在電子郵件中插入社交媒體頁面的連結。

1. 在 **[!UICONTROL Content Components]**，拖放 **[!UICONTROL Social]** 在 **[!UICONTROL Structure component]**.

   ![](assets/email_designer_19.png)

1. 按一下新增的元件，開始設定 **[!UICONTROL Content Components]** 並能夠 **[!UICONTROL Components Settings]** 在電子郵件設計工具的右窗格中。

1. 在 **[!UICONTROL Social]** 欄位 **[!UICONTROL Components Settings]**，選擇您要新增或移除的社交媒體。

   ![](assets/email_designer_20.png)

1. 在 **[!UICONTROL Size of images]** 欄位。

1. 按一下您的每個社交媒體圖示，以設定 **[!UICONTROL URL]** 系統會將您的對象重新導向至其中。

   ![](assets/email_designer_21.png)

1. 如有需要，您也可以在 **[!UICONTROL Image]** 欄位。

1. 您現在可以透過變更 **[!UICONTROL Style]**, **[!UICONTROL Margin]** 和 **[!UICONTROL Border]**.

## 優惠方案決策 {#offer-decision}

使用 **[!UICONTROL Offer decision]** 元件，將決策（先前稱為優惠方案活動）插入訊息中。 決策會利用決策管理來挑選最適合提供給客戶的優惠方案。

相關主題：

* [開始使用決定管理](offers/get-started/starting-offer-decisioning.md).
* [將個人化優惠方案新增至訊息](deliver-personalized-offers.md).
