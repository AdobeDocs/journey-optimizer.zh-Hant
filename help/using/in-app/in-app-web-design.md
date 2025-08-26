---
title: 設計您的網頁應用程式內內容
description: 瞭解如何設計您的網頁應用程式內內容
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 應用程式內、訊息、建立、開始
hide: true
hidefromtoc: true
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 7%

---

# 設計您的網頁應用程式內內容 {#in-app-web-design}

>[!BEGINSHADEBOX]

**目錄**

* [設定網頁應用程式內頻道](configure-in-app-web.md)
* [建立您的網頁應用程式內訊息行銷活動](create-in-app-web.md)
* 設計您的網頁應用程式內內容

>[!ENDSHADEBOX]

若要編輯應用程式內訊息內容，請從行銷活動的&#x200B;**[!UICONTROL 動作]**&#x200B;功能表按一下&#x200B;**[!UICONTROL 編輯內容]**&#x200B;按鈕。

![](assets/in_app_web_surface_7.png)

**[!UICONTROL 進階格式]**&#x200B;切換可啟動其他選項來自訂體驗。

建立應用程式內訊息，並定義內容與個人化後，您就可以檢閱並啟用該訊息。 然後，將根據行銷活動排程傳送通知。 請在[此頁面](send-in-app.md)了解更多。

## 訊息版面 {#message-layout}

從&#x200B;**[!UICONTROL 訊息配置]**&#x200B;區段中，選取四個不同的配置選項之一，以便根據您的訊息需求進行選擇。

![](assets/in_app_web_design_1.png)

* **[!UICONTROL 全熒幕]**：此型別的版麵包含對象裝置的整個熒幕。

  其支援媒體（影像、影片）、文字及按鈕元件。

* **[!UICONTROL 模型]**：此配置會顯示在大型警示樣式視窗中，而您的應用程式仍會顯示在背景中。

  其支援媒體（影像、影片）、文字及按鈕元件。

* **[!UICONTROL 橫幅]**：此型別的版面會顯示為原生作業系統警示訊息。

  您只能將&#x200B;**[!UICONTROL 標題]**&#x200B;和&#x200B;**[!UICONTROL 內文]**&#x200B;新增至您的訊息。

* **[!UICONTROL 自訂]**：自訂訊息模式可讓您直接匯入及編輯其中一個預先設定的HTML訊息。

   * 選取&#x200B;**[!UICONTROL 撰寫]**&#x200B;以輸入或貼上您的原始HTML程式碼。

     使用左窗格以運用Journey Optimizer個人化功能。 如需詳細資訊，請參閱[本章節](../personalization/personalize.md)。

   * 選取&#x200B;**[!UICONTROL 匯入]**&#x200B;以匯入包含HTML內容的HTML或.zip檔案。

## 內容索引標籤 {#content-tab}

您可以從&#x200B;**Content**&#x200B;索引標籤定義並個人化通知的內容和&#x200B;**關閉**&#x200B;按鈕的樣式。 您也可以新增媒體至應用程式內通知，並在此索引標籤新增動作按鈕。

### 關閉按鈕 {#close-button}

![](assets/in_app_web_design_2.png)

選擇&#x200B;**[!UICONTROL 關閉按鈕]**&#x200B;的&#x200B;**[!UICONTROL 樣式]**。

可用的樣式包括：

* **[!UICONTROL 簡單]**
* **[!UICONTROL 圓]**
* 來自媒體URL或您的Assets的&#x200B;**[!UICONTROL 自訂影像]**。

+++更多具有進階格式的選項

如果&#x200B;**[!UICONTROL 進階格式模式]**&#x200B;已開啟，您可以核取&#x200B;**[!UICONTROL 色彩]**&#x200B;選項來選擇按鈕的色彩和不透明度。

+++

### 媒體 {#add-media}

**[!UICONTROL 媒體]**&#x200B;欄位可讓您將媒體新增至應用程式內訊息，以為一般使用者建立引人入勝的體驗。

![](assets/in_app_web_design_3.png)

輸入您的媒體URL或按一下&#x200B;**[!UICONTROL 選取Assets]**&#x200B;圖示，直接將儲存在Assets資料庫中的資產新增至您的應用程式內訊息。 [進一步瞭解資產管理](../content-management/assets-essentials.md)。
您也可以為熒幕閱讀應用程式新增**[!UICONTROL 替代文字]**。

+++更多具有進階格式的選項

如果&#x200B;**[!UICONTROL 進階格式模式]**&#x200B;已開啟，您可以自訂媒體的&#x200B;**[!UICONTROL 最大高度]**&#x200B;和&#x200B;**[!UICONTROL 最大寬度]**。

+++

### 內容 {#title-body}

若要撰寫訊息，請在&#x200B;**[!UICONTROL 標題]**&#x200B;和&#x200B;**[!UICONTROL 內文]**&#x200B;欄位中輸入內容。

![](assets/in_app_web_design_4.png)

使用&#x200B;**[!UICONTROL Personalization]**&#x200B;圖示來新增個人化。 在本節[中進一步瞭解Adobe Journey Optimizer個人化編輯器](../personalization/personalize.md)中的個人化。

+++更多具有進階格式的選項

如果&#x200B;**[!UICONTROL 進階格式模式]**&#x200B;已開啟，您可以為&#x200B;**[!UICONTROL 標題]**&#x200B;和&#x200B;**[!UICONTROL 內文]**&#x200B;選擇：

* **[!UICONTROL 字型]**
* **[!UICONTROL Pt大小]**
* **[!UICONTROL 字型色彩]**
* **[!UICONTROL 對齊]**
+++

### 按鈕 {#add-buttons}

新增按鈕讓使用者可以和您的應用程式內訊息互動。

![](assets/in_app_web_design_5.png)

個人化您的按鈕：

1. 編輯按鈕#1文字（主要）欄位。 您也可以使用&#x200B;**[!UICONTROL Personalization]**&#x200B;圖示來定義內容和個人化資料。

1. 選擇您的&#x200B;**[!UICONTROL 互動事件]**，定義使用者與按鈕互動後的按鈕動作。

1. 在&#x200B;**[!UICONTROL 目標]**&#x200B;欄位中輸入您的網頁URL或深層連結。

1. 若要新增多個按鈕，請按一下[新增]按鈕&#x200B;****。

+++更多具有進階格式的選項

如果&#x200B;**[!UICONTROL 進階格式化模式]**&#x200B;已開啟，您可以為&#x200B;**[!UICONTROL 按鈕]**&#x200B;選擇：

* **[!UICONTROL 字型]**
* **[!UICONTROL Pt大小]**
* **[!UICONTROL 字型色彩]**
* **[!UICONTROL 對齊]**
* **[!UICONTROL 按鈕樣式]**
* **[!UICONTROL 半徑]**
* **[!UICONTROL 按鈕色彩]**

+++

## 設定標籤 {#settings-tab}

您可以從&#x200B;**設定**&#x200B;索引標籤定義訊息版面配置並預覽您的應用程式內訊息。 您也可以存取進階格式選項。

### 版面配置 {#layout-options}

![](assets/in_app_web_design_6.png)

**[!UICONTROL 背景影像]**&#x200B;欄位可讓您新增背景至應用程式內訊息：

* 來自URL連結的媒體。

* 背景顏色。

### 訊息 {#message-tab}

![](assets/in_app_web_design_7.png)

UI接管選項預設為啟用，可讓您讓應用程式內訊息背後的背景變暗，以強調對內容的關注。

+++更多具有進階格式的選項

如果&#x200B;**[!UICONTROL 進階格式化模式]**&#x200B;已開啟，您可以使用下列選項進一步個人化您的訊息：

* **[!UICONTROL 自訂UI接管]**：可讓您選取要在背景顯示的顏色及其不透明度。

* **[!UICONTROL 自訂大小]**：可讓您調整應用程式內通知的寬度和高度。

* **[!UICONTROL 自訂位置]**：可讓您自訂使用者熒幕上的應用程式內訊息位置。 您可以變更垂直和水平對齊。

* **[!UICONTROL 訊息圓角]**：可讓您變更&#x200B;**[!UICONTROL 圓角半徑]**，將圓角新增至應用程式內通知。

+++

**相關主題：**

* [測試並傳送您的應用程式內訊息](send-in-app.md)
* [應用程式內報告](../reports/campaign-global-report-cja-inapp.md)
* [應用程式內設定](inapp-configuration.md)