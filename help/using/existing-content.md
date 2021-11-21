---
title: 匯入或編寫您的電子郵件代碼
description: 了解如何匯入電子郵件內容或為電子郵件編碼
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 52011299-0c65-49c3-9edd-ba7bed5d7205
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 9%

---

# 匯入或編碼您的電子郵件內容 {#existing-content}

Journey Optimizer可讓您匯入現有的HTML內容，以設計電子郵件。 此內容可以是原始HTML碼，或來自現有HTML檔案或郵遞區號資料夾的內容。

若要編寫HTML內容或匯入現有內容，請遵循下列步驟：

1. [建立訊息](create-message.md)

1. 開啟 **[!UICONTROL Email Designer]** 從 **[!UICONTROL Edit Content]** 區段。

   ![](assets/import-html_1.png)

1. 選取「**[!UICONTROL Code your own]**」或「**[!UICONTROL Import HTML]**」。請參閱以下章節以了解後續步驟。

## 自行編碼 {#import-raw-html-code}

使用 **[!UICONTROL Code your own]** 模式可匯入原始HTML和/或為電子郵件內容編碼。 此方法需要HTML技能。

>[!CAUTION]
>
> 影像來源 [Adobe Experience Manager Assets Essentials](assets-essentials.md) 無法參考。 您的HTML程式碼中參考的影像必須儲存至公用位置。

1. 在電子郵件設計工具首頁中，選擇 **[!UICONTROL Code your own]**.

   ![](assets/code-your-own.png)

1. 輸入或貼上原始HTML程式碼。

1. 使用左窗格來利用 [!DNL Journey Optimizer] 個人化功能。 如需詳細資訊，請參閱[本章節](personalization/personalize.md)。

   ![](assets/code-editor.png)

1. 如果您想要開啟電子郵件設計工具以從新設計啟動電子郵件，請選取 **[!UICONTROL Change your design]** ，從「選項」菜單。

   ![](assets/code-editor-change-design.png)

1. 按一下 **[!UICONTROL Preview]** 按鈕，使用測試設定檔來檢查訊息設計和個人化。 如需詳細資訊，請參閱[本章節](preview.md)。

   ![](assets/code-editor-preview.png)

1. 程式碼準備就緒後，按一下 **[!UICONTROL Save]** 然後返回訊息建立畫面，以完成訊息。

   ![](assets/code-editor-save.png)

## 匯入HTML {#import-html-content-from-file}

您可以在電子郵件設計工具中匯入HTML內容。 此內容可以是：

* 安 **HTML檔案** 帶有整合樣式表，
* A **.zip資料夾** 使用HTML檔案、樣式表(.css)和影像。

   >[!NOTE]
   >
   >.zip檔案結構沒有限制。 但是，參照必須是相對的，並且與.zip資料夾的樹結構相符。

若要匯入包含HTML內容的檔案，請遵循下列步驟：

1. 在電子郵件設計工具首頁中，選擇 **[!UICONTROL Import HTML]**.

   ![](assets/import-html_2.png)

1. 拖放包含您HTML內容的HTML或.zip檔案。

1. 上傳HTML內容後，您就可以運用電子郵件設計工具功能來編輯和預覽您的電子郵件。 [在本節中瞭解更多](create-email-content.md)。

   ![](assets/html-imported.png)
