---
title: 編輯網頁內容
description: 瞭解如何在Journey Optimizer中編寫網頁及編輯其內容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1069'
ht-degree: 18%

---

# 編輯網頁內容 {#edit-web-content}

在您[將網頁體驗](create-web.md#create-web-experience)新增到歷程或行銷活動後，您可以使用網頁設計工具編輯您網站的內容。

[透過此影片瞭解如何創作網路行銷活動](#video)

在[!DNL Journey Optimizer]中，網頁製作是由&#x200B;**Adobe Experience Cloud Visual Helper** Chrome瀏覽器擴充功能所支援。 [了解更多](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>若要能夠在[!DNL Journey Optimizer]使用者介面中存取及編寫網頁，請務必遵循[本節](web-prerequisites.md)中列出的必要條件。

存取下列章節以深入瞭解每個主題：

* [管理修改](manage-web-modifications.md)

* [監視網路行銷活動](monitor-web-experiences.md)

## 使用網頁設計工具 {#work-with-web-designer}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="確認要編輯的 URL"
>abstract="確認特定網頁的 URL，以用於編輯套用到上方定義之網頁設定的內容。必須使用此 Adobe Experience Platform Web SDK 實作此網頁。"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant" text="了解更多"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="輸入要編輯的 URL"
>abstract="輸入特定網頁的 URL，以用於編輯將套用到符合規則的所有網頁的內容。必須使用 Adobe Experience Platform Web SDK 實作此網頁。"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant" text="了解更多"

若要開始編寫您的Web體驗，請遵循下列步驟。

1. 從歷程中行銷活動或網頁體驗活動的&#x200B;**[!UICONTROL 動作]**&#x200B;索引標籤，選取&#x200B;**[!UICONTROL 編輯內容]**。<!--change screen with rule-->

   ![](assets/web-campaign-edit-content.png)

1. 如果您已建立符合規則的頁面，則必須輸入符合此規則的任何URL：變更將套用至符合規則的所有頁面。 頁面內容隨即顯示。

   >[!NOTE]
   >
   >如果您輸入單一URL作為網頁設定，則會填入要個人化的URL。

   ![](assets/web-edit-enter-url.png)

   >[!CAUTION]
   >
   >網頁必須包含[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"}。 [了解更多](web-prerequisites.md#implementation-prerequisites)

1. 按一下&#x200B;**[!UICONTROL 編輯網頁]**&#x200B;以開始編寫它。 網頁設計工具隨即顯示。

   ![](assets/web-designer.png)

   >[!NOTE]
   >
   >如果您嘗試載入無法載入的網站，則會顯示一則訊息，建議您安裝[Visual Editing Helper瀏覽器擴充功能](#install-visual-editing-helper)。 請參閱[本節](web-prerequisites.md#troubleshooting)中疑難排解的一些提示。

1. 從畫布中選取任何元素，例如影像、按鈕、段落、文字、容器、標題、連結等。 [了解更多](#content-components)

1. 使用：

   * 上下文選單可編輯其內容、配置、插入連結或個人化等。

     ![](assets/web-designer-contextual-bar.png)

   * 右側面板頂端的圖示可編輯、複製、刪除或隱藏每個元素。

     ![](assets/web-designer-right-panel-icons.png)

   * 根據所選元素動態變更的右側面板。 例如，您可以編輯元素的背景、印刷樣式、框線、大小、位置、間距、效果或內嵌樣式。

     ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>網頁內容設計工具大多與電子郵件Designer類似。 深入瞭解[使用 [!DNL Journey Optimizer]](../email/get-started-email-design.md)設計內容。

## 使用元件 {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="將元件新增到您的網頁"
>abstract="您可以將許多元件新增到您的網頁並根據需要進行編輯。"

1. 從左側的&#x200B;**[!UICONTROL 元件]**&#x200B;窗格中，選取專案。 您可以將下列元件新增至網頁，並視需要加以編輯：

   * [分隔線](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [影像](../email/content-components.md#image)
   * 標題 — 使用此元件類似於在電子郵件Designer中使用&#x200B;**[!UICONTROL Text]**&#x200B;元件。 [了解更多](../email/content-components.md#text)
   * 段落 — 使用此元件類似於在電子郵件Designer中使用&#x200B;**[!UICONTROL 文字]**&#x200B;元件。 [了解更多](../email/content-components.md#text)
   * 連結

   ![](assets/web-designer-components.png)

1. 將游標停留在頁面上，然後按一下&#x200B;**[!UICONTROL 插入在前]**&#x200B;或&#x200B;**[!UICONTROL 插入在後]**&#x200B;按鈕，將元件附加至頁面上的現有元素。

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >若要取消選取元件，請按一下畫布頂端所顯示內容藍色橫幅中的&#x200B;**[!UICONTROL ESC]**&#x200B;按鈕。

1. 視需要直接在頁面的內容中編輯元件。

   ![](assets/web-designer-edit-header.png)

1. 調整從右邊內容窗格顯示的樣式，例如背景、文字顏色、邊框、大小、位置等。  — 視選取的元件而定。

   ![](assets/web-designer-header-style.png)

## 新增個人化

若要新增個人化，請選取容器，然後從顯示的內容功能表列中選取個人化圖示。 使用個人化編輯器新增變更。 [了解更多](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

## 瀏覽網頁設計工具 {#navigate-web-designer}

本節詳細說明您可以瀏覽Web設計工具的各種方式。 若要檢視和管理新增至您網頁體驗的修改，請參閱[本節](manage-web-modifications.md)。

### 使用階層連結 {#breadcrumbs}

1. 從畫布中選取任何元素。

1. 按一下畫面左下方的&#x200B;**[!UICONTROL 展開/摺疊階層連結]**&#x200B;按鈕，即可快速顯示所選專案的相關資訊。

   ![](assets/web-designer-breadcrumbs.png)

1. 當您將游標停留在階層連結上時，編輯器中會反白顯示對應的元素。

1. 您可以使用它輕鬆導覽至視覺編輯器中的任何父項、同層級專案或子項元素。

### 切換到瀏覽模式 {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="使用瀏覽模式"
>abstract="在此模式下，您可以從要個人化的選取設定導覽至確切的頁面。"

您可以使用專用按鈕，將預設&#x200B;**[!UICONTROL 設計]**&#x200B;模式切換至&#x200B;**[!UICONTROL 瀏覽]**&#x200B;模式。

![](assets/web-designer-browse-mode.png)

從&#x200B;**[!UICONTROL 瀏覽]**&#x200B;模式中，您可以瀏覽至您想要個人化之所選組態的正確頁面。

在處理經過驗證或無法從特定URL開始使用的頁面時，此外掛程式特別有用。 例如，您將能夠驗證、導覽至您的帳戶頁面或購物車頁面，然後切換回&#x200B;**[!UICONTROL 設計]**&#x200B;模式，以在您想要的頁面上執行變更。

使用&#x200B;**[!UICONTROL 瀏覽]**&#x200B;模式，您也可以在編寫單頁應用程式時，瀏覽您網站的所有檢視。 [了解更多](web-spa.md)

### 變更裝置大小 {#change-device-size}

您可以將網頁設計工具顯示的裝置大小變更為預先定義的大小，例如&#x200B;**[!UICONTROL 平板電腦]**&#x200B;或&#x200B;**[!UICONTROL 行動裝置橫向]**，或輸入所需的畫素數來定義自訂大小。

您也可以將縮放焦點從25%變更為400%。

![](assets/web-designer-device.png)

變更裝置大小的功能是專為可適當呈現在各種裝置、視窗和熒幕大小的回應式網站所設計。 回應式網站會自動調整並適應任何螢幕大小，包括桌上型電腦、筆記型電腦、平板電腦或行動電話。

>[!CAUTION]
>
>您可以編輯具有特定裝置大小的網頁體驗。 不過，只要選取器相同，這些變更就會套用至所有大小和裝置，而不只是您正在使用的裝置大小。 同樣地，在標準案頭檢視中編輯體驗時，會將變更套用至所有熒幕大小，而不僅僅是案頭檢視。
>
>目前，[!DNL Journey Optimizer]不支援裝置大小特定的頁面變更。 這表示，舉例來說，如果您有另一個行動網站具有不同的網站結構，您應該針對不同促銷活動中的行動網站進行特定變更。

## 作法影片{#video}

以下影片說明如何在[!DNL Journey Optimizer]行銷活動中使用Web設計工具來撰寫Web體驗。

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)