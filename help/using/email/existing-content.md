---
solution: Journey Optimizer
product: journey optimizer
title: 匯入電子郵件內容
description: 了解如何匯入電子郵件內容
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: 電子郵件，匯入，內容， html， zip， css
exl-id: 52011299-0c65-49c3-9edd-ba7bed5d7205
source-git-commit: ddbab603e4ac612a49a3853fcac428950def1d98
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 34%

---

# 匯入電子郵件內容 {#existing-content}

[!DNL Journey Optimizer]可讓您匯入現有的HTML內容，以設計您的電子郵件。 此內容可以是：

* **HTML檔案**，包含合併的樣式表；
* **.zip資料夾**&#x200B;包含HTML檔案、樣式表(.css)和影像。

  >[!NOTE]
  >
  >.zip 檔案結構沒有限制。不過，參照必須是相對參照，而且符合.zip資料夾的樹狀結構。

<!--DOCAC-13676
>[!TIP]
>
>If you have image designs (JPEG or PNG) instead of HTML files, you can use the [Template Accelerator](image-to-html.md) to automatically convert them into editable HTML email templates using AI.-->

若要匯入包含 HTML 內容的檔案，請依照以下步驟操作：

1. 從電子郵件Designer首頁，選取&#x200B;**[!UICONTROL 匯入HTML]**。

   ![](assets/import-html_2.png)

1. 拖放包含 HTML 內容的 HTML 或 .zip 檔案，然後按一下「**[!UICONTROL 匯入]**」。

   ![](assets/html-imported_2.png)

1. 上傳HTML內容後，您的內容將處於&#x200B;**[!UICONTROL 相容性模式]**。

   在此模式中，您只能個人化您的文字、新增連結或包含資產至您的內容。

1. 若要能夠利用電子郵件Designer內容元件，請存取&#x200B;**[!UICONTROL HTML轉換工具]**&#x200B;索引標籤，然後按一下&#x200B;**[!UICONTROL 轉換]**。

   ![](assets/html-imported.png)

   >[!NOTE]
   >
   > 在HTML檔案中使用`<table>`標籤做為第一個圖層可能會造成樣式遺失，包括上層圖層標籤中的背景和寬度設定。

1. 您現在可以根據需要，使用電子郵件Designer功能個人化匯入的檔案。 [了解更多](content-from-scratch.md)

## 操作說明影片 {#video}

瞭解如何匯入現有的 HTML 內容、調整設計、新增鏡像頁面和取消訂閱連結，以及如何編寫內容的程式碼。

>[!VIDEO](https://video.tv.adobe.com/v/334102?quality=12)
