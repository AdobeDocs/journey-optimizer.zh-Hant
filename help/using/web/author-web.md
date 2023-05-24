---
title: 製作網頁
description: 瞭解如何在Journey Optimizer建立網頁並編輯其內容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1623'
ht-degree: 14%

---

# 製作網頁 {#author-web}

一旦 [添加了Web操作](create-web.md#create-web-campaign) 在您的市場活動中，您可以使用web設計器編輯網站的內容。

在 [!DNL Journey Optimizer], Web創作由 **Adobe Experience Cloud視覺助手** chrome瀏覽器擴展。 [了解更多](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>能夠訪問和編寫 [!DNL Journey Optimizer] 用戶介面，確保遵循中列出的先決條件 [此部分](web-prerequisites.md)。

[瞭解如何在此視頻中建立Web活動](#video)

## 編輯網頁內容 {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="確認要編輯的 URL"
>abstract="確認特定網頁的 URL，以用於編輯將套用到上面定義的網頁表面的內容。必須使用此 Adobe Experience Platform Web SDK 實作此網頁。"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant" text="更多詳情"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="輸入要編輯的 URL"
>abstract="輸入特定網頁的 URL，以用於編輯將套用到符合規則的所有網頁的內容。必須使用 Adobe Experience Platform Web SDK 實作此網頁。"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant" text="更多詳情"

要開始建立Web促銷活動，請執行以下步驟。

1. 從 **[!UICONTROL 操作]** 頁籤 [活動](create-web.md#create-web-campaign)選中 **[!UICONTROL 編輯內容]**。<!--change screen with rule-->

   ![](assets/web-campaign-edit-content.png)

1. 如果建立了頁面匹配規則，則必須輸入與此規則匹配的任何URL:這些更改將應用於與規則匹配的所有頁面。 顯示頁面內容。

   >[!NOTE]
   >
   >如果您輸入單個URL作為Web表面，則要個性化的URL已填充。

   ![](assets/web-edit-enter-url.png)

   >[!CAUTION]
   >
   >網頁必須包括 [Adobe Experience PlatformWeb SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"}。 [了解更多](web-prerequisites.md#implementation-prerequisites)

1. 按一下 **[!UICONTROL 編輯網頁]** 開始創作。 將顯示Web設計器。

   ![](assets/web-designer.png)

   >[!NOTE]
   >
   >如果嘗試載入未能載入的網站，將顯示一條消息，建議您安裝 [Visual Editing Helper瀏覽器擴展](#install-visual-editing-helper)。 請參閱中的一些故障排除提示 [此部分](web-prerequisites.md#troubleshooting)。

1. 從畫布中選擇任何元素，如影像、按鈕、段落、文本、容器、標題、連結等。 [了解更多](#content-components)

1. 使用:

   * 用於編輯其內容、佈局、插入連結或個性化等的上下文菜單。

      ![](assets/web-designer-contextual-bar.png)

   * 右面板頂部的表徵圖可編輯、複製、刪除或隱藏每個元素。

      ![](assets/web-designer-right-panel-icons.png)

   * 根據所選元素動態更改的右面板。 例如，可以編輯元素的背景、排版、邊框、大小、位置、間距、效果或內聯樣式。

      ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>Web內容設計器與電子郵件設計器大體相似。 瞭解更多 [設計內容 [!DNL Journey Optimizer]](../email/get-started-email-design.md)。

## 使用元件 {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="將元件新增到您的網頁"
>abstract="您可以將許多元件新增到您的網頁並根據需要進行編輯。"

1. 從 **[!UICONTROL 元件]** 的子菜單。 您可以將以下元件添加到您的網頁中，並根據需要編輯它們：

   * [分隔線](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [影像](../email/content-components.md#image)
   * 標題 — 使用此元件與使用 **[!UICONTROL 文本]** 的子菜單。 [了解更多](../email/content-components.md#text)
   * 段落 — 使用此元件與使用 **[!UICONTROL 文本]** 的子菜單。 [了解更多](../email/content-components.md#text)
   * 連結
   * [提供決定](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. 懸停在頁面中，然後按一下 **[!UICONTROL 在前面插入]** 或 **[!UICONTROL 在後面插入]** 按鈕，將元件附加到頁面上的現有元素。

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >要取消選取元件，請按一下 **[!UICONTROL Esc]** 按鈕，將選定控制項在Tab鍵次序中下移一個位置。

1. 根據需要直接在頁面內容中編輯元件。

   ![](assets/web-designer-edit-header.png)

1. 調整從右側上下文窗格中顯示的樣式，如背景、文本顏色、邊框、大小、位置等。  — 取決於所選元件。

   ![](assets/web-designer-header-style.png)

## 添加個性化和優惠

要添加個性化設定，請選擇一個容器，然後從顯示的上下文菜單欄中選擇個性化設定表徵圖。 使用表達式編輯器添加更改。 [了解更多](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

使用 **[!UICONTROL 提供決定]** 插入元件 [提供](../offers/get-started/starting-offer-decisioning.md) 你的網頁。 該過程與 [向電子郵件添加優惠](../email/add-offers-email.md)。 它將利用決策管理來選擇向客戶提供的最佳服務。

![](assets/web-designer-offer.png)

## 管理修改 {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="輕鬆管理所有變更"
>abstract="使用此窗格，您可以瀏覽和管理您新增到網頁的所有調整和樣式。"

您可以輕鬆管理添加到網頁的所有元件、調整和樣式。

1. 選擇 **[!UICONTROL 修改]** 表徵圖以顯示左側的相應窗格。

   ![](assets/web-designer-modifications-pane.png)

1. 您可以查看對頁面所做的每項更改。

1. 選擇不需要的修改，然後按一下刪除表徵圖將其刪除。

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >刪除操作時請小心，因為該操作可能會影響後續操作。

1. 使用 **[!UICONTROL 更多操作]** 按鈕 **[!UICONTROL 修改]** 的子菜單。

   ![](assets/web-designer-delete-modifications.png)

1. 從 **[!UICONTROL 更多操作]** 菜單中，您也只能刪除無效的修改，這意味著其他更改覆蓋的更改。 例如，如果修改文本的顏色，然後刪除該文本，則顏色修改將變為無效，因為該文本已不存在。

1. 您還可以使用 **[!UICONTROL 撤消/重做]** 按鈕。

   ![](assets/web-designer-undo-redo.png)

   按一下並按住按鈕，在 **[!UICONTROL 撤消]** 和 **[!UICONTROL 重做]** 頁籤 然後按一下按鈕本身以應用所需的操作。

## 使用按一下跟蹤 {#use-click-tracing}

Web設計器中的此功能允許您選擇網站的任何元素並跟蹤該元素上的按一下。

市場活動開始後，您可以檢查市場活動Web報表中每個元素的點擊次數。 此資訊對改善您的網站用戶體驗非常有用。 例如，如果 [Web報告](../reports/campaign-global-report.md#web-tab) 顯示許多用戶按一下了實際上不可按一下的元素，您可能希望向該元素添加連結。

1. 在頁面中選擇元素，然後選擇 **[!UICONTROL 按一下跟蹤元素]** 的子菜單。

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >可以選擇任何項目，無論可按一下與否。

1. 相應的跟蹤操作自動顯示在 **[!UICONTROL 按一下跟蹤]** 的子菜單。

   ![](assets/web-designer-click-track-pane.png)

1. 添加有意義的標籤以管理所有跟蹤的元素，並在報告中輕鬆查找它們。 的 **[!UICONTROL CSS選擇器]** 欄位顯示查找選定元素的資訊。

1. 重複上述步驟，以根據需要選擇任意數量的其它元素進行按一下跟蹤。 相應的操作都列在左窗格中。

   ![](assets/web-designer-click-tracking-actions.png)

1. 要刪除元素上的按一下跟蹤，請選擇相應的刪除表徵圖。

活動激活後，您可以檢查市場活動報表 **[!UICONTROL Web]** 頁籤以比較印數，按一下按元素的點擊率和點擊次數。 [了解更多](../reports/campaign-global-report.md#web-tab)

## 在Web設計器中導航 {#navigate-web-designer}

### 使用麵包屑 {#breadcrumbs}

1. 從畫布中選擇任何元素。

1. 按一下 **[!UICONTROL 展開/折疊Breadcrumbs]** 按鈕，快速顯示有關選定元素的資訊。

   ![](assets/web-designer-breadcrumbs.png)

1. 當您懸停在麵包屑上時，相應的元素將在編輯器中加亮顯示。

1. 使用它，您可以輕鬆導航到可視編輯器中的任何父元素、同級元素或子元素。

### 切換到瀏覽模式 {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="使用瀏覽模式"
>abstract="在此模式下，您可以從要個人化的選取表面瀏覽到精準的頁面。"

可以從預設值進行交換 **[!UICONTROL 設計]** 模式 **[!UICONTROL 瀏覽]** 按鈕。

![](assets/web-designer-browse-mode.png)

從 **[!UICONTROL 瀏覽]** 模式下，您可以從要個性化的選定曲面導航到精確頁面。

在處理身份驗證後或從某個URL的起始處不可用的頁面時，它特別有用。 例如，您將能夠進行身份驗證、導航到帳戶頁或購物車頁，然後切換回 **[!UICONTROL 設計]** 的子菜單。

### 更改設備大小 {#change-device-size}

可以將Web設計器顯示的設備大小更改為預定義大小，如 **[!UICONTROL 平板電腦]** 或 **[!UICONTROL 移動環境]**，或通過輸入所需的像素數來定義自定義大小。

您還可以將縮放焦點從25%更改為400%。

![](assets/web-designer-device.png)

更改設備大小的功能是針對響應站點設計的，這些站點在各種設備、窗口和螢幕大小上呈現良好。 回應式網站會自動調整並適應任何螢幕大小，包括桌上型電腦、筆記型電腦、平板電腦或行動電話。

>[!CAUTION]
>
>您可以編輯具有特定設備大小的Web體驗。 但是，只要選擇器相同，這些更改就適用於所有大小和設備，而不僅適用於您正在使用的設備大小。 同樣，在普通案頭視圖中編輯體驗會將更改應用於所有螢幕大小，而不僅僅是案頭視圖。
>
>目前， [!DNL Journey Optimizer] 不支援設備大小特定的頁面更改。 這意味著，例如，如果您有一個單獨的移動網站，其站點結構是獨立的，則您應該在不同的市場活動中對移動網站進行特定更改。

## TestWeb活動 {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="預覽您的網頁體驗"
>abstract="取得您的網頁體驗的模擬。"

要顯示已修改的Web體驗的預覽，請執行以下步驟。

>[!CAUTION]
>
>您必須具有test配置檔案，以模擬將向其提供哪些優惠。 瞭解如何 [建立test配置檔案](../segment/creating-test-profiles.md)。

1. 從Web市場活動編輯內容螢幕中，選擇 **[!UICONTROL 模擬內容]**。

   <!--![](assets/web-designer-simulate.png)-->

   ![](assets/web-campaign-simulate.png)

1. 按一下 **[!UICONTROL 管理test配置檔案]** 選擇一個或多個test配置檔案。
1. 將顯示已修改網頁的預覽。

   ![](assets/web-designer-preview.png)

1. 您也可以在預設瀏覽器中開啟它，或複製testURL以在任何瀏覽器中貼上它。 這允許您與團隊和利益相關方共用連結，這些利益相關方將能夠在活動開始之前在任何瀏覽器中預覽新的Web體驗。

   >[!NOTE]
   >
   >複製testURL時，顯示的內容是生成內容模擬時使用的test配置檔案的個性化內容 [!DNL Journey Optimizer]。

## 操作說明影片{#video}

以下視頻顯示如何使用中的Web設計器創作Web體驗 [!DNL Journey Optimizer] 活動。

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)
