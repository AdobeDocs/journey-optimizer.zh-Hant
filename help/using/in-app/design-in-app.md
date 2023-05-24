---
title: 設計您的應用程式內內容
description: 瞭解如何在Journey Optimizer設計應用程式內容
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 應用內、消息、設計、格式
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 5%

---

# 設計您的應用程式內內容 {#design-content}

您可以編輯應用內內容以配置體驗選項：

* 在 **[!UICONTROL 活動]**，也請參見Wiki頁。 **[!UICONTROL 操作]** 菜單，要配置消息內容，請按一下 **[!UICONTROL 編輯內容]** 按鈕

   ![](assets/edit-in-app-content.png)

* 在 **[!UICONTROL 旅程]**，從應用內的高級菜單 **[!UICONTROL 操作]**，您可以開始設計內容 **[!UICONTROL 編輯內容]** 按鈕

   ![](assets/design_inapp_journey.png)

的 **[!UICONTROL 高級格式]** 切換激活其他選項以自定義體驗。

建立In-app消息並定義和個性化其內容後，您可以查看並激活它。 然後，根據活動計畫發送通知。 在[本頁](send-in-app.md)中瞭解更多。

## 消息佈局 {#message-layout}

從 **[!UICONTROL 消息佈局]** 選項。

![](assets/in_app_content_1.png)

* **[!UICONTROL 全屏]**:此類型的佈局涵蓋您的觀眾設備的整個螢幕。

   其支援媒體（影像、影片）、文字及按鈕元件。

* **[!UICONTROL 模式]**:此佈局顯示在大型警報樣式窗口中，您的應用程式仍在後台顯示。

   其支援媒體（影像、影片）、文字及按鈕元件。

* **[!UICONTROL 橫幅]**:此類型的佈局將顯示為本機OS警報消息。

   只能添加 **[!UICONTROL 標題]** 和 **[!UICONTROL 身體]** 你的留言。

* **[!UICONTROL 自定義]**:自定義消息模式允許您直接導入和編輯預配置的HTML消息之一。

   * 選擇 **[!UICONTROL 合成]** 輸入或貼上原始HTML代碼。

      使用左窗格利用Journey Optimizer個性化功能。 如需詳細資訊，請參閱[本章節](../personalization/personalize.md)。

   * 選擇 **[!UICONTROL 導入]** 導入包含HTML內容的HTML或.zip檔案。

## 內容頁籤 {#content-tab}

從 **內容** 頁籤，您可以定義並個性化：通知的內容和 **關閉** 按鈕 您還可以將媒體添加到應用程式內通知中，並從此頁籤添加操作按鈕。

### 關閉按鈕 {#close-button}

![](assets/in_app_content_2.png)

選擇 **[!UICONTROL 樣式]** 你 **[!UICONTROL 關閉按鈕]**。

可用樣式有：

* **[!UICONTROL 簡單]**
* **[!UICONTROL 圓]**
* **[!UICONTROL 自定義映像]** 的子菜單。

+++更多具有高級格式的選項

如果 **[!UICONTROL 高級格式模式]** 開啟，你可以檢查 **[!UICONTROL 顏色]** 的子菜單。

+++

### 媒體 {#add-media}

的 **[!UICONTROL 媒體]** 欄位允許您將媒體添加到應用內消息中，以為最終用戶建立引人注目的體驗。

![](assets/in_app_content_3.png)

鍵入媒體URL或按一下 **[!UICONTROL 選擇資產]** 表徵圖，將儲存在資產庫中的資產直接添加到應用內消息。 [瞭解有關資產管理的更多資訊](../email/assets-essentials.md)。
也可以添加 **[!UICONTROL 備選文本]** 用於螢幕讀取應用程式。

+++更多具有高級格式的選項

如果 **[!UICONTROL 高級格式模式]** 開啟時，您可以 **[!UICONTROL 最大高度]** 和 **[!UICONTROL 最大寬度]** 你的媒體。

+++

### 標題和正文 {#title-body}

要撰寫郵件，請在 **[!UICONTROL 標題]** 和 **[!UICONTROL 身體]** 的子菜單。

![](assets/in_app_content_4.png)

使用 **[!UICONTROL 個性化]** 表徵圖以添加個性化設定。 瞭解有關Adobe Journey Optimizer表達式編輯器中個性化設定的詳細資訊 [此部分](../personalization/personalize.md)。

+++更多具有高級格式的選項

如果 **[!UICONTROL 高級格式模式]** 開啟，你可以選擇 **[!UICONTROL 標題]** 和 **[!UICONTROL 身體]**:

* 這樣 **[!UICONTROL 字型]**
* 這樣 **[!UICONTROL Pt大小]**
* 這樣 **[!UICONTROL 字型顏色]**
* 這樣 **[!UICONTROL 對齊]**
+++

### 按鈕 {#add-buttons}

為用戶添加按鈕以與您的應用內消息交互。

![](assets/in_app_content_5.png)

要個性化按鈕：

1. 編輯按鈕#1文本（主）欄位。 您還可以使用 **[!UICONTROL 個性化]** 表徵圖，定義內容和個性化資料。

1. 選擇 **[!UICONTROL 交互事件]** 它定義了用戶與按鈕交互後的操作。

1. 在 **[!UICONTROL 目標]** 的子菜單。

1. 要添加多個按鈕，請按一下 **[!UICONTROL 「添加」按鈕]**。

+++更多具有高級格式的選項

如果 **[!UICONTROL 高級格式模式]** 開啟，你可以選擇 **[!UICONTROL 按鈕]**:

* 這樣 **[!UICONTROL 字型]**
* 這樣 **[!UICONTROL Pt大小]**
* 這樣 **[!UICONTROL 字型顏色]**
* 這樣 **[!UICONTROL 對齊]**
* 這樣 **[!UICONTROL 按鈕樣式]**
* 這樣 **[!UICONTROL 半徑]**
* 這樣 **[!UICONTROL 按鈕顏色]**

+++

## 「設定」頁籤 {#settings-tab}

從 **設定** 頁籤，您可以定義消息佈局並預覽應用內消息。 您還可以訪問高級格式設定選項。

### 預覽 {#preview-tab}

![](assets/in_app_content_6.png)

的 **[!UICONTROL 應用預覽]** 允許您在In-app消息後添加背景：

* 來自URL連結的媒體。

* 資產庫中的資產。

* 背景色。

### 版面配置 {#layout-options}

![](assets/in_app_content_7.png)

的 **[!UICONTROL 背景影像]** 欄位允許您向In-app消息添加背景：

* 來自URL連結的媒體。

* 背景色。

### 訊息 {#message-tab}

![](assets/in_app_content_8.png)

預設情況下啟用的UI接管選項允許您對In-app消息背景進行變暗，以強調對內容的關注。

+++更多具有高級格式的選項

如果 **[!UICONTROL 高級格式模式]** 開啟時，您可以使用以下選項進一步個性化您的消息：

* **[!UICONTROL 自定義手勢]**:允許您自定義用戶刷卡交互。 如果選擇「消除」，則可以添加自定義交互事件和/或目標目標。

* **[!UICONTROL 自定義UI接管]**:允許您選擇要在背景及其不透明度中顯示的顏色。

* **[!UICONTROL 自定義大小]**:允許您調整應用內通知的寬度和高度。

* **[!UICONTROL 自定義職位]**:允許您在用戶螢幕上自定義In-app消息的位置。 可以更改「垂直」(Vertical)和「水準」(Horizontal)對齊方式。

* **[!UICONTROL 自定義動畫]**:允許您自定義「顯示」和「取消」動畫，例如，如果您的「應用內」通知從用戶設備的左側或頂部顯示。

* **[!UICONTROL 消息圓角]**:允許您通過更改應用內通知添加圓角 **[!UICONTROL 角半徑]**。

+++

**相關主題：**

* [建立應用程式內訊息](create-in-app.md)
* [應用程式內報告](../reports/campaign-global-report.md#inapp-report)
* [應用內配置](inapp-configuration.md)

## 操作說明影片{#video}

以下視頻顯示如何製作和test您的應用內消息。

>[!VIDEO](https://video.tv.adobe.com/v/3410471?quality=12&learn=on)
