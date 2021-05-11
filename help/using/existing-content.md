---
title: 匯入或編寫您的電子郵件
description: 瞭解如何匯入電子郵件內容或為電子郵件編碼
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 5%

---

# 匯入或編碼您的電子郵件內容{#existing-content}

![](assets/do-not-localize/badge.png)

Journey Optimizer允許您匯入現有的HTML內容，以設計您的電子郵件。 此內容可以是原始HTML程式碼，或現有HTML檔案或郵遞區號檔案夾中的內容。

若要編碼HTML內容或匯入現有內容，請遵循下列步驟：

1. [建立訊息](create-message.md)

1. 從&#x200B;**[!UICONTROL Edit Content]**&#x200B;區段開啟&#x200B;**[!UICONTROL Email Designer]**。

   ![](assets/import-html_1.png)

1. 選取「**[!UICONTROL Code your own]**」或「**[!UICONTROL Import HTML]**」。請參閱以下章節以取得後續步驟。

## 編寫您自己的{#import-raw-html-code}程式碼

使用&#x200B;**[!UICONTROL Code your own]**&#x200B;模式可匯入原始HTML和／或編寫您的電子郵件內容。 此方法需要HTML技巧。

>[!CAUTION]
>
> 使用此方法時，無法參考來自[Adobe Experience Manager Assets Essentials](assets-essentials.md)的影像。 HTML程式碼中參考的影像必須儲存在公共位置。

1. 在「電子郵件設計器」首頁中，選擇&#x200B;**[!UICONTROL Code your own]**。

   ![](assets/code-your-own.png)

1. 輸入或貼上您的原始HTML程式碼。

1. 使用左窗格來運用[!DNL Journey Optimizer]個人化功能。 如需詳細資訊，請參閱[本章節](personalization/personalize.md)。

   ![](assets/code-editor.png)

1. 如果要開啟「電子郵件設計器」以從新設計啟動電子郵件，請從「選項」菜單中選擇&#x200B;**[!UICONTROL Change your design]**。

   ![](assets/code-editor-change-design.png)

1. 按一下&#x200B;**[!UICONTROL Preview]**&#x200B;按鈕，使用測試設定檔檢查訊息設計和個人化。 如需詳細資訊，請參閱[本章節](preview.md)。

   ![](assets/code-editor-preview.png)

1. 程式碼準備就緒後，按一下&#x200B;**[!UICONTROL Save]**，然後返回訊息建立畫面以完成訊息的定版。

   ![](assets/code-editor-save.png)


## 匯入HTML {#import-html-content-from-file}

您可以在電子郵件設計人員中匯入HTML內容。 此內容可以是：

* **HTML檔案**&#x200B;包含整合的樣式表，
* **.zip資料夾**&#x200B;包含HTML檔案、樣式表(.css)和影像。

   >[!NOTE]
   >
   >.zip檔案結構沒有限制。 但是，參照必須是相對的，並且與。zip檔案夾的樹狀結構相符。

若要匯入包含HTML內容的檔案，請遵循下列步驟：

1. 在「電子郵件設計器」首頁中，選擇&#x200B;**[!UICONTROL Import HTML]**。

   ![](assets/import-html_2.png)

1. 拖放包含HTML內容的HTML或。zip檔案。

1. 上傳HTML內容後，您就可以運用「電子郵件設計工具」功能來編輯和預覽您的電子郵件。 [在本節中進一步瞭解](create-email-content.md)。

   ![](assets/html-imported.png)
