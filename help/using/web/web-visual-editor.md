---
title: 使用網頁設計工具編輯內容
description: 瞭解如何使用Journey Optimizer網頁編輯器編寫網頁及編輯其內容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
source-git-commit: 7cf58ae33c0b3e6d6b9ce19aa71ba105db40c602
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 8%

---


# 使用網頁設計工具 {#work-with-web-designer}

<!--
>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Confirm the URL to edit"
>abstract="Confirm the URL of the specific web page to use for editing the content that will be applied on the web configuration defined above. The web page must be implemented using the Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html" text="Learn more"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Enter the URL to edit"
>abstract="Enter the URL of a specific web page to use for editing the content that will be applied to all pages matching the rule. The web page must be implemented using Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html" text="Learn more"
-->

在[!DNL Journey Optimizer]中，視覺化網頁製作是由&#x200B;**Adobe Experience Cloud Visual Helper** Chrome瀏覽器擴充功能所支援。 [了解更多](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>若要能夠在[!DNL Journey Optimizer]使用者介面中存取及編寫網頁，請務必遵循[本節](web-prerequisites.md)中列出的必要條件。

## 開始編寫您的網頁體驗

若要開始使用視覺化網頁設計工具製作您的網頁體驗，請遵循下列步驟。

>[!CAUTION]
>
>[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"}必須包含在您的網頁中。 [了解更多](web-prerequisites.md#implementation-prerequisites)

1. **[!UICONTROL 在編輯內容]**&#x200B;屏幕中，按兩下編輯&#x200B;**[!UICONTROL 網頁頁面]**&#x200B;以打開網頁設計器。

   ![](assets/web-campaign-edit-web-page.png)

   <!--![](assets/web-designer.png)-->

   >[!NOTE]
   >
   >如果嘗試載入無法載入的網站，則會顯示一條消息，建議你安裝 [可視化編輯幫助程式瀏覽器擴展](#install-visual-editing-helper)。 請參閱本節](web-prerequisites.md#troubleshooting)中的[一些故障排除提示。
   >
   >您也可以在不載載視覺編輯者的情況下编辑網页內容。 為此，請取消選擇“ **[!UICONTROL 可視編輯者]** ”選項以改用非可視版本模式。 [了解更多](web-non-visual-editor.md)

1. 進入網頁設計器后，從畫布中選擇任何元素，例如圖像，按鈕，段落，文本，容器，標題，連結等。 [了解更多](#content-components)

1. 要編輯元素，您可以使用：

   * 上下文功能表，用于编辑其內容、佈局、插入連結或個人化等。

     ![](assets/web-designer-contextual-bar.png)

   * 右側面板頂端的圖示可編輯、重複、刪除或隱藏各元素。

     ![](assets/web-designer-right-panel-icons.png)

   * 根據所選取元素動態變更的右側面板。 例如，您可以編輯元素的背景、排版、邊框、大小、位置、間距、效果或內聯樣式。

     ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>Web 內容設計器通常與電子郵件設計器相似。 深入瞭解[使用 [!DNL Journey Optimizer]](../email/get-started-email-design.md)設計內容。

編輯網頁內容後，您就可以管理您的修改。 [了解更多](manage-web-modifications.md)

## 使用元件 {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="將元件新增到您的網頁"
>abstract="您可以將許多元件新增到您的網頁並根據需要進行編輯。"

1. 從左側的&#x200B;**[!UICONTROL 元件]**&#x200B;窗格中，選取專案。 您可以將下列元件新增至網頁，並視需要加以編輯：

   * [分隔線](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [影像](../email/content-components.md#image)
   * 標題 — 使用此元件類似於在電子郵件設計工具中使用&#x200B;**[!UICONTROL Text]**&#x200B;元件。 [了解更多](../email/content-components.md#text)
   * 段落 - 使用此元件類似於在 **[!UICONTROL 電子郵件設計器中使用文字]** 元件。 [了解更多](../email/content-components.md#text)
   * 連結

   ![](assets/web-designer-components.png)

1. 將滑鼠懸停在頁面中並按兩下 **[!UICONTROL “在前面]** 插入”或 **[!UICONTROL “在後]** 插入”按鈕以將元件附加到頁面上的現有元素。

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >要取消選擇元件，請按兩下 **[!UICONTROL 畫布頂部顯示的上下文藍色橫幅中的 ESC]** 按鈕。

1. 根據需要直接在頁面內容中編輯元件。

   ![](assets/web-designer-edit-header.png)

1. 調整從右側上下文窗格顯示的樣式，例如背景、文本顏色、邊框、大小、位置等。 - 取決於所選元件。

   ![](assets/web-designer-header-style.png)

## 新增個人化

若要添加個人化，請選擇一個容器，然後從顯示的上下文功能表中選擇個人化圖示。 使用 個人化 編輯者新增變更。 [了解更多](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

## 瀏覽網頁設計器 {#navigate-web-designer}

本節詳細說明您可以瀏覽Web設計工具的各種方式。 若要檢視和管理新增至您網頁體驗的修改，請參閱[本節](manage-web-modifications.md)。

### 使用階層連結 {#breadcrumbs}

1. 從畫布中選取任何元素。

1. 按一下畫面左下方的&#x200B;**[!UICONTROL 展開/摺疊階層連結]**&#x200B;按鈕，即可快速顯示所選專案的相關資訊。

   ![](assets/web-designer-breadcrumbs.png)

1. 當您將游標暫留在痕跡導航上時，編輯者中會反白顯示相應的元素。

1. 使用它可以輕鬆導航到可視化編輯者中的任何父元素、同層級元素或子元素。

### 切換到瀏覽模式 {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="使用瀏覽模式"
>abstract="在此模式下，您可以從要個人化的選取設定導覽至確切的頁面。"

您可以使用專用按鈕從默認 **[!UICONTROL 設計]** 模式 **[!UICONTROL 切換到瀏覽]** 模式。

![](assets/web-designer-browse-mode.png)

在 **[!UICONTROL 瀏覽]** 模式下，您可以從要個性化的選定配置中導航到確切的頁面。

在處理身份驗證後面的頁面或無法從特定URL的開始獲得的頁面時，它特別有用。 例如，您將能够進行身份驗證，導航到帳戶頁面或購物車頁面，然後切換回 **[!UICONTROL 設計]** 模式，以便對所需頁面執行更改。

使用瀏覽&#x200B;]**模式還可以**[!UICONTROL &#x200B;在創作單頁面應用程式時瀏覽網站的所有視圖。[了解更多](web-spa.md)

### 變更裝置大小 {#change-device-size}

您可以將 Web 設計器顯示器的裝置大小更改為預定義的大小，例如 **[!UICONTROL 平板電腦]** 或 **[!UICONTROL 行動裝置橫向]**，或透過輸入所需的像素數來定義自定義大小。

您也可以將縮放焦點從25%變更為400%。

![](assets/web-designer-device.png)

變更裝置大小的功能是專為可適當呈現在各種裝置、視窗和熒幕大小的回應式網站所設計。 回應式網站會自動調整並適應任何熒幕大小，包括桌上型電腦、筆記型電腦、平板電腦或行動電話。

>[!CAUTION]
>
>您可以編輯具有特定裝置大小的網頁體驗。 不過，只要選取器相同，這些變更就會套用至所有大小和裝置，而不只是您正在使用的裝置大小。 同樣地，在標準案頭檢視中編輯體驗時，會將變更套用至所有熒幕大小，而不僅僅是案頭檢視。
>
>目前不支持 [!DNL Journey Optimizer] 裝置大小特定的頁面變更。 這表示，舉例來說，如果您有另一個行動網站具有不同的網站結構，您應該針對不同促銷活動中的行動網站進行特定變更。

## 操作說明影片{#video}

以下影片說明如何在[!DNL Journey Optimizer]行銷活動中使用Web設計工具來撰寫Web體驗。

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)