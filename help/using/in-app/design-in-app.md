---
title: 設計您的應用程式內內容
description: 瞭解如何在Journey Optimizer中設計您的應用程式內內容
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 應用程式內、訊息、設計、格式
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 4899dbe71243184b6283a32a4fe7eb2edb82f872
workflow-type: tm+mt
source-wordcount: '1148'
ht-degree: 28%

---

# 設計您的應用程式內內容 {#design-content}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_content"
>title="定義應用程式內的內容"
>abstract="自訂應用程式內訊息的內容與樣式。您也可以新增媒體與動作按鈕，讓您的訊息更引人入勝且更有成效。"

您可以編輯應用程式內內容以設定體驗選項：

* 在 **[!UICONTROL Campaign]**，來自 **[!UICONTROL 動作]** 功能表，若要設定訊息內容，請按一下 **[!UICONTROL 編輯內容]** 按鈕。

  ![](assets/edit-in-app-content.png)

* 在 **[!UICONTROL 歷程]**，從應用程式內的進階功能表 **[!UICONTROL 動作]**，您就可以開始使用設計內容 **[!UICONTROL 編輯內容]** 按鈕。

  ![](assets/design_inapp_journey.png)

此 **[!UICONTROL 進階格式]** 切換可啟動其他選項來自訂體驗。

建立應用程式內訊息，並定義內容與個人化後，您就可以檢閱並啟用該訊息。 然後，將根據行銷活動排程傳送通知。 在[本頁](send-in-app.md)中瞭解更多。

## 訊息版面 {#message-layout}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_message_layout"
>title="定義應用程式內的內容"
>abstract="此訊息版面提供您常用的範本以設定訊息的框架。自訂版面提供上傳或撰寫自訂 HTML 訊息的選項。"

從 **[!UICONTROL 訊息配置]** 區段，根據您的訊息傳送需求，選取四個不同的版面配置選項之一。

![](assets/in_app_content_1.png)

* **[!UICONTROL 全熒幕]**：此型別的版麵包含對象裝置的整個熒幕。

  其支援媒體（影像、影片）、文字及按鈕元件。

* **[!UICONTROL 強制回應]**：此版面會顯示在大型警報樣式視窗中，而您的應用程式仍會顯示在背景中。

  其支援媒體（影像、影片）、文字及按鈕元件。

* **[!UICONTROL 橫幅]**：此型別的版面會以原生作業系統警報訊息的形式顯示。

  您只能新增 **[!UICONTROL 頁首]** 和 **[!UICONTROL 內文]** 至您的訊息。

* **[!UICONTROL 自訂]**：自訂訊息模式可讓您直接匯入及編輯其中一個預先設定的HTML訊息。

   * 選取 **[!UICONTROL 撰寫]** 以輸入或貼上您的原始HTML程式碼。

     使用左窗格以運用Journey Optimizer個人化功能。 如需詳細資訊，請參閱[本章節](../personalization/personalize.md)。

   * 選取 **[!UICONTROL 匯入]** 以匯入包含HTML內容的HTML或.zip檔案。

## 內容索引標籤 {#content-tab}

從 **內容** 標籤內，您可以定義並個人化通知的內容和樣式 **關閉** 按鈕。 您也可以新增媒體至應用程式內通知，並在此索引標籤新增動作按鈕。

### 關閉按鈕 {#close-button}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_close"
>title="選擇關閉按鈕的樣式。"
>abstract="關閉按鈕部分提供選項讓您選取訊息關閉按鈕的變化，以及上傳自訂影像的選項。"

![](assets/in_app_content_2.png)

選擇 **[!UICONTROL 樣式]** 的 **[!UICONTROL 關閉按鈕]**.

可用的樣式包括：

* **[!UICONTROL 簡單]**
* **[!UICONTROL 圓形]**
* **[!UICONTROL 自訂影像]** 來自媒體URL或您的資產。

+++更多具有進階格式的選項

如果 **[!UICONTROL 進階格式化模式]** 開啟，您可以檢查 **[!UICONTROL 顏色]** 選項來選擇按鈕的顏色和不透明度。

+++

### 媒體 {#add-media}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_media"
>title="新增媒體至您的應用程式內訊息，以建立令一般使用者信服的體驗。"
>abstract="提供至內容的直接連結，或使用資產選擇器從 Asset Essentials 挑選要新增至訊息的媒體。"

此 **[!UICONTROL 媒體]** 欄位可讓您將媒體新增至應用程式內訊息，為一般使用者建立引人入勝的體驗。

![](assets/in_app_content_3.png)

輸入您的媒體URL或按一下 **[!UICONTROL 選取資產]** 圖示可將儲存在「資產」程式庫中的資產直接新增至應用程式內訊息。 [進一步瞭解資產管理](../content-management/assets.md).
您也可以新增 **[!UICONTROL 替代文字]** 適用於熒幕閱讀應用程式。

+++更多具有進階格式的選項

如果 **[!UICONTROL 進階格式化模式]** 開啟，您可以自訂 **[!UICONTROL 最大高度]** 和 **[!UICONTROL 最大寬度]** 媒體的。

+++

### 標題和本文 {#title-body}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_content"
>title="若要撰寫訊息，請在「標題」與「本文」欄位輸入內容。"
>abstract="此處可以新增標題與內容文字。若要納入個人化語彙基元，請開啟個人化對話框。"

若要撰寫訊息，請在 **[!UICONTROL 頁首]** 和 **[!UICONTROL 內文]** 欄位。

![](assets/in_app_content_4.png)

使用 **[!UICONTROL 個人化]** 圖示以新增個人化。 進一步瞭解Adobe Journey Optimizer運算式編輯器中的個人化 [在本節中](../personalization/personalize.md).

+++更多具有進階格式的選項

如果 **[!UICONTROL 進階格式化模式]** 已開啟，您可以為以下專案選擇 **[!UICONTROL 頁首]** 和 **[!UICONTROL 內文]**：

* 此 **[!UICONTROL 字型]**
* 此 **[!UICONTROL Pt大小]**
* 此 **[!UICONTROL 字型顏色]**
* 此 **[!UICONTROL 對齊方式]**
+++

### 按鈕 {#add-buttons}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_buttons"
>title="新增按鈕讓使用者可以和您的應用程式內訊息互動。"
>abstract="本部份可讓您在訊息中新增召喚行動按鈕。您也可以針對每個按鈕納入自訂的文字與目標。"

新增按鈕讓使用者可以和您的應用程式內訊息互動。

![](assets/in_app_content_5.png)

個人化您的按鈕：

1. 編輯按鈕#1文字（主要）欄位。 您也可以使用 **[!UICONTROL 個人化]** 圖示來定義內容和個人化資料。

1. 選擇您的 **[!UICONTROL 互動事件]** 會定義使用者與按鈕互動後的按鈕動作。

1. 在「 」中輸入您的網頁URL或深層連結 **[!UICONTROL Target]** 欄位。

1. 若要新增多個按鈕，請按一下 **[!UICONTROL 新增按鈕]**.

+++更多具有進階格式的選項

如果 **[!UICONTROL 進階格式化模式]** 已開啟，您可以為以下專案選擇 **[!UICONTROL 按鈕]**：

* 此 **[!UICONTROL 字型]**
* 此 **[!UICONTROL Pt大小]**
* 此 **[!UICONTROL 字型顏色]**
* 此 **[!UICONTROL 對齊方式]**
* 此 **[!UICONTROL 按鈕樣式]**
* 此 **[!UICONTROL 半徑]**
* 此 **[!UICONTROL 按鈕顏色]**

+++

## 設定標籤 {#settings-tab}

從 **設定** 索引標籤上，您可以定義訊息版面並預覽應用程式內訊息。 您也可以存取進階格式選項。

### 預覽 {#preview-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_preview"
>title="預覽您的應用程式內訊息。"
>abstract="這是預覽影像，將會在訊息傳送至裝置的訊息摘要時顯示。"

![](assets/in_app_content_6.png)

此 **[!UICONTROL 應用程式預覽]** 可讓您在應用程式內訊息後面新增背景：

* 來自URL連結的媒體。

* 資產庫中的資產。

* 背景顏色。

### 版面配置 {#layout-options}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_layout"
>title="定義應用程式內訊息的訊息版面。"
>abstract="本部份可讓您在應用程式內訊息中新增背景。這需要 UI 接管才能啟用。"

![](assets/in_app_content_7.png)

此 **[!UICONTROL 背景影像]** 欄位可讓您將背景新增至應用程式內訊息：

* 來自URL連結的媒體。

* 背景顏色。

### 訊息 {#message-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_message_advanced"
>title="定義訊息進階設定。"
>abstract="本部份讓您可以強化應用程式內的內容個人化，尤其是在啟用「進階格式化」時。"

![](assets/in_app_content_8.png)

UI接管選項預設為啟用，可讓您讓應用程式內訊息背後的背景變暗，以強調對內容的關注。

+++更多具有進階格式的選項

如果 **[!UICONTROL 進階格式化模式]** 開啟，您就可以使用下列選項進一步個人化您的訊息：

* **[!UICONTROL 自訂手勢]**：可讓您自訂使用者滑動互動的內容。 如果選取了關閉，您可以新增自訂互動事件和/或目標目的地。

* **[!UICONTROL 自訂使用者介面接管]**：可讓您選取要在背景顯示的顏色及其不透明度。

* **[!UICONTROL 自訂大小]**：可讓您調整應用程式內通知的寬度和高度。

* **[!UICONTROL 自訂位置]**：可讓您自訂應用程式內訊息在使用者畫面上的位置。 您可以變更垂直和水平對齊。

* **[!UICONTROL 自訂動畫]**：可讓您自訂顯示和解除動畫，例如從使用者裝置的左側或頂端出現應用程式內通知時。

* **[!UICONTROL 訊息圓角]**：可讓您透過變更 **[!UICONTROL 圓角半徑]**.

+++

**相關主題：**

* [建立應用程式內訊息](create-in-app.md)
* [應用程式內報告](../reports/campaign-global-report.md#inapp-report)
* [應用程式內設定](inapp-configuration.md)

## 操作說明影片{#video}

以下影片說明如何編寫和測試您的應用程式內訊息。

>[!VIDEO](https://video.tv.adobe.com/v/3410471?quality=12&learn=on)
