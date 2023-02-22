---
title: 製作網頁
description: 了解如何在Journey Optimizer中撰寫網頁及編輯其內容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 4%

---

# 製作網頁 {#author-web}

>[!AVAILABILITY]
>
>網路頻道功能目前僅供選取使用者的測試版使用。

在 [!DNL Journey Optimizer] Adobe Experience Cloud Visual Helper chrome瀏覽器擴充功能提供網頁編寫功能。 [了解更多](visual-editing-helper.md)

若要存取及編寫 [!DNL Journey Optimizer] 使用者介面，遵循 [本節](create-web.md#prerequesites).

## 編輯網頁內容 {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="確認要編輯的URL"
>abstract="確認特定網頁的URL，以用於編輯將套用至上述定義之Web表面的內容。 網頁必須使用Adobe Experience Platform Web SDK實作。"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant" text="更多詳情"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="輸入要編輯的URL"
>abstract="輸入要用於編輯內容的特定網頁的URL，該內容將應用於符合規則的所有頁面。 網頁必須使用Adobe Experience Platform Web SDK實作。"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant" text="更多詳情"

<!--Confirm the URL to use for authoring content on the surface. Typically the Authoring URL will be the surface URL itself, but you may include extra parameters if required. The page must include the Adobe Experience Platform Web SDK.-->

從促銷活動建立網頁動作後，您就可以使用網頁設計工具來編輯內容。 若要這麼做，請遵循下列步驟。

>[!CAUTION]
>
>要在 [!DNL Journey Optimizer]，您的網頁必須使用 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"}.

1. 從 **[!UICONTROL 動作]** 選取 **[!UICONTROL 編輯內容]** 開始編寫網頁行銷活動。

1. 如果您建立的頁面符合規則，則必須輸入任何符合此規則的URL。 變更會套用至符合規則的所有頁面。

   >[!NOTE]
   >
   >如果您輸入單一URL作為Web表面，則已填入要個人化的URL。

   ![](assets/web-edit-enter-url.png)

1. 頁面內容隨即顯示。

   >[!CAUTION]
   >
   >網頁必須包含 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"}.

1. 按一下 **[!UICONTROL 開啟網頁設計工具]** 來編輯。 [了解更多](author-web.md)

   ![](assets/web-open-designer.png)

1. 網頁設計器隨即顯示。

   ![](assets/web-designer.png)

1. 從畫布中選取任何元素，例如影像、按鈕、段落、文字、容器、標題、連結等。 和使用：

   * 內容功能表，可編輯其內容、版面、插入連結或個人化等。

      ![](assets/web-designer-contextual-bar.png)

   * 右側面板上方的圖示可編輯、複製、刪除或隱藏每個元素。

      ![](assets/web-designer-right-panel-icons.png)

   * 會根據所選元素動態變更的右側面板。 例如，您可以編輯元素的背景、印刷樣式、邊框、大小、位置、間距、效果或內嵌樣式。

      ![](assets/web-designer-right-panel.png)

## 使用內容元件 {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="將內容元件新增至網頁"
>abstract="您可以新增許多元件至您的網頁，並視需要加以編輯。"

1. 從 **[!UICONTROL 元件]** 窗格，您可以將下列元件新增至您的網頁，並視需要加以編輯：

   * [除法器](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [影像](../email/content-components.md#image)
   * 標題 — 使用此元件類似於使用 **[!UICONTROL 文字]** 元件。 [了解更多](../email/content-components.md#text)
   * 段落 — 使用此元件類似於使用 **[!UICONTROL 文字]** 元件。 [了解更多](../email/content-components.md#text)
   * 連結 — 了解如何在 [本節](../email/styling-links.md)
   * [優惠方案決策](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. 將滑鼠指標暫留在頁面中，按一下 **[!UICONTROL 插入在前]** 或 **[!UICONTROL 插入在後]** 按鈕，將元件附加至頁面上的現有元素。

   ![](assets/web-designer-insert-components.png)

1. 從針對此元件顯示的容器中，視需要編輯元件內容。

   ![](assets/web-designer-edit-html.png)

1. 調整從 **[!UICONTROL 容器]** 窗格，如背景、文字顏色、邊框、大小、位置等。 取決於所選元件。

   ![](assets/web-designer-html-style.png)

## 瀏覽網頁設計工具

### 使用階層連結

1. 從畫布選取任何元素。

1. 按一下 **[!UICONTROL 展開/折疊階層連結]** 按鈕，快速顯示所選元素的相關資訊。

   ![](assets/web-designer-breadcrumbs.png)

1. 當您將游標暫留在階層連結上時，編輯器中會強調顯示對應的元素。

1. 使用它，您可以輕鬆導覽至視覺編輯器中的任何父元素、同層級元素或子元素。

### 切換為瀏覽模式 {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="使用瀏覽模式"
>abstract="在此模式中，您可以從您要個人化的選定曲面導覽至確切頁面。"

您可以從預設值交換 **[!UICONTROL 設計]** 模式 **[!UICONTROL 瀏覽]** 模式。

![](assets/web-designer-browse-mode.png)

從 **[!UICONTROL 瀏覽]** 模式中，您可以從要個性化的選定曲面導航到確切頁面。

在處理驗證後面的頁面，或從某個URL開始就無法使用的頁面時，它特別有用。 例如，您將能夠驗證、導覽至您的帳戶頁面或購物車頁面，然後切換回 **[!UICONTROL 設計]** 模式，以在您想要的頁面上執行變更。

### 更改設備大小

您可以將裝置大小變更為預先定義的大小，例如 **[!UICONTROL 平板電腦]** 或 **[!UICONTROL 行動橫向]**，或定義自訂大小。 輸入要定義自訂大小的像素數。

您也可以將縮放焦點從25%變更為400%。

![](assets/web-designer-device.png)

## 管理修改 {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="輕鬆管理您的所有變更"
>abstract="使用此窗格，您可以瀏覽並管理您添加到網頁的所有調整和樣式。"

您可以輕鬆管理新增至網頁的所有元件、調整和樣式。

1. 選取 **[!UICONTROL 修改]** 按鈕，在左側顯示相應的窗格。

   ![](assets/web-designer-modifications-pane.png)

1. 您可以檢閱您對頁面所做的每項變更。

1. 選取不需要的修改，然後按一下刪除圖示加以移除。

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >刪除動作可能會影響後續動作時，請謹慎處理。

1. 您也可以使用 **[!UICONTROL 還原/重做]** 按鈕。

   ![](assets/web-designer-undo-redo.png)

   按一下並按住按鈕，以在 **[!UICONTROL 還原]** 和 **[!UICONTROL 取消復原]** 選項。 然後按一下按鈕本身以套用所需的動作。

## 新增個人化和選件

若要新增個人化，請選取容器，然後從顯示的內容功能表列中選取個人化圖示。 使用運算式編輯器新增變更。 [了解更多](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

使用 **[!UICONTROL 優惠方案決策]** 插入元件 [優惠](../offers/get-started/starting-offer-decisioning.md) 填入您的網頁。 程式與 [將優惠方案新增至電子郵件](../email/add-offers-email.md). 它將利用決策管理來挑選最適合客戶的優惠方案。

![](assets/web-designer-offer.png)

## 測試網路促銷活動 {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="預覽您的網路體驗"
>abstract="取得網路體驗的模擬外觀。"

若要顯示已修改之網路體驗的預覽，請遵循下列步驟。

>[!CAUTION]
>
>您必須有可用的測試設定檔，以模擬將會提供哪些選件給他們。 了解如何 [建立測試設定檔](../segment/creating-test-profiles.md).

1. 從 **[!UICONTROL 編輯內容]** 螢幕或Web設計器，選擇 **[!UICONTROL 模擬內容]**.

   ![](assets/web-designer-simulate.png)

1. 按一下 **[!UICONTROL 管理測試設定檔]** 來選取一或多個測試設定檔。
1. 將顯示已修改網頁的預覽。

   ![](assets/web-designer-preview.png)

1. 您也可以複製測試URL以貼到任何瀏覽器中，或在預設瀏覽器中開啟。
