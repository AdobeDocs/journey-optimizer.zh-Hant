---
title: 編寫單頁應用程式
description: 瞭解如何在Journey Optimizer中撰寫SPA及套用修改至不同的檢視
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: b33e4bca-d2e9-4610-9f04-008d47f686d0
source-git-commit: fb05b110fc1bd205810e7d85be4071644f52b191
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 25%

---

# 編寫單頁應用程式 {#web-author-spas}

## 關於檢視 {#about-views}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications_views"
>title="將變更套用到選取的視圖"
>abstract="變更將僅套用到選取的視圖。可以使用&#x200B;**瀏覽**&#x200B;模式找到並瀏覽到視圖。找不到您要尋找的視圖？"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant" text="更多詳情"

**單頁應用程式** (SPA)現在可以在網頁設計工具視覺編輯器中撰寫。 這可讓您選取要 **檢視** 您想要將網頁修改套用至。

[透過此影片瞭解如何編寫單頁應用程式](#video)

檢視可定義為整個網站或網站上一組視覺化元素，例如首頁、整個產品網站或所有結帳頁面上的傳遞偏好設定框架。 

需要一次性開發人員設定，才能定義Adobe Experience Platform Web SDK實作中的檢視。 這可讓您在SPA上建立並執行Adobe Journey Optimizer網路行銷活動。

## 在Web SDK實作中定義檢視 {#define-views}

可在Adobe中運用XDM檢視 [!DNL Journey Optimizer] 讓行銷人員透過網頁視覺化編輯器在SPA上執行網頁個人化和實驗行銷活動。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html){target="_blank"}

若要能夠存取及編寫中的檢視 [!DNL Journey Optimizer] 使用者介面，請務必遵循下列步驟操作 [本節](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html#implement-xdm-views){target="_blank"}.

## 在網頁設計工具中探索檢視 {#discover-views}

在Adobe Experience Platform Web SDK實作中完成SPA設定後，您必須導覽您要套用修改之網站的所有檢視。 請遵循下列步驟。

1. [建立網站行銷活動](create-web.md) 並存取 [網頁設計工具](edit-web-content.md).

   您目前所在的檢視畫面會顯示在左上方。

   ![](assets/web-designer-view-home.png)

1. 交換至 **[!UICONTROL 瀏覽]** 模式。 [了解更多](../web/edit-web-content.md#browse-mode)

   ![](assets/web-designer-view-browse.png)

1. 在網站的不同頁面之間導覽，以探索所有頁面。 當您瀏覽其他頁面時，最上方顯示的檢視名稱會變更。

   ![](assets/web-designer-other-view.png)

## 將修改套用至其他檢視 {#apply-modifications-views}

當您在特定檢視中新增修改後，即可將其套用至其他選取的檢視。 請遵循下列步驟。

>[!CAUTION]
>
>如果您尚未使用 **[!UICONTROL 瀏覽]** 模式，您將無法選取它們以套用您的修改。 [了解更多](#discover-views)

1. 選取 **[!UICONTROL 修改]** 圖示來在左側顯示對應的窗格。

   ![](assets/web-designer-view-modifications-pane.png)

1. 選取任何修改並按一下 **[!UICONTROL 更多動作]** 按鈕。 選取 **[!UICONTROL 套用至更多檢視]**.

   ![](assets/web-designer-modifications-more-actions.png)

1. 選取您要套用變更的檢視。

   ![](assets/web-designer-modifications-apply-to.png)

1. 按一下&#x200B;**[!UICONTROL 套用]**。

1. 交換至 **[!UICONTROL 瀏覽]** 用於檢查修改內容已套用至所需頁面的模式。

   ![](assets/web-designer-modifications-applied-view.png)

## 操作說明影片{#video}

此影片說明如何：

* 探索SPA檢視，使用 **[!UICONTROL 瀏覽]** 模式
* 在目前的檢視上進行製作
* 將網站修改套用至多個檢視或所有探索到的檢視
* 對修改執行大量動作

>[!VIDEO](https://video.tv.adobe.com/v/3424536/?quality=12&learn=on)
