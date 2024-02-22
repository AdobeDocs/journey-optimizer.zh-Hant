---
title: 在Journey Optimizer中建立網頁應用程式內訊息
description: 瞭解如何在Journey Optimizer中建立網頁應用程式內訊息
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 應用程式內、訊息、建立、開始
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 2%

---


# 設定網頁應用程式內頻道 {#configure-in-app-web}

## 先決條件 {#prerequisites}

* 確保您使用的是最新版本的 **Adobe Experience Platform Web SDK** 副檔名。

* 安裝 **Adobe Experience Platform Web SDK** 擴充功能在您的中 **標籤屬性** 並啟用 **個人化儲存** 選項。

  此設定對於在使用者端上儲存事件歷史記錄是必要的，這是在規則產生器中實作頻率規則的先決條件。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

  ![](assets/configure_web_inapp_1.png)

## 設定傳送資料至平台規則 {#configure-sent-data-trigger}

1. 存取您的 **Adobe Experience Platform資料彙集** 執行個體並導覽至 **標籤屬性** 已使用 **Adobe Experience Platform Web SDK** 副檔名。

1. 從 **製作** 功能表，選取 **規則** 則 **建立新規則** 或 **新增規則**.

   ![](assets/configure_web_inapp_2.png)

1. 在 **活動** 區段，按一下 **新增** 並依照以下方式設定：

   * **副檔名**：核心

   * **事件型別**：程式庫已載入（頁面頂端）。

   ![](assets/configure_web_inapp_3.png)

1. 按一下 **保留變更** 以儲存事件設定。

1. 在 **動作** 區段，按一下 **新增** 並依照以下方式設定：

   * **副檔名**：Adobe Experience Platform Web SDK

   * **動作型別**：傳送事件

   ![](assets/configure_web_inapp_4.png)

1. 在 **個人化** 部分 **動作** 型別，啟用 **呈現視覺個人化決定** 選項。

   ![](assets/configure_web_inapp_5.png)

1. 在 **決定內容** 區段，定義 **索引鍵** 和 **值** 決定要提供哪個體驗的配對。

   ![](assets/configure_web_inapp_6.png)

1. 儲存您的 **動作** 設定，按一下 **保留變更**.

1. 導覽至 **發佈流程** 功能表。 建立新的 **資料庫** 或選取現有的 **資料庫** 並新增您新建立的 **規則** 轉換至此。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. 從您的 **資料庫**，選取 **儲存並建置到開發環境**.

   ![](assets/configure_web_inapp_7.png)

## 設定手動規則 {#configure-manual-trigger}

1. 存取您的 **Adobe Experience Platform資料彙集** 執行個體並導覽至 **標籤屬性** 已使用 **Adobe Experience Platform Web SDK** 副檔名。

1. 從 **製作** 功能表，選取 **規則** 則 **建立新規則** 或 **新增規則**.

   ![](assets/configure_web_inapp_8.png)

1. 在 **活動** 區段，按一下 **新增** 並依照以下方式設定：

   * **副檔名**：核心

   * **事件型別**：按一下

   ![](assets/configure_web_inapp_9.png)

1. 在 **按一下設定**，定義 **選擇器** 將會進行評估的物件。

   ![](assets/configure_web_inapp_10.png)

1. 按一下 **保留變更** 儲存 **事件** 設定。

1. 在 **動作** 區段，按一下 **新增** 並依照以下方式設定：

   * **副檔名**：Adobe Experience Platform Web SDK

   * **動作型別**：評估規則集

   ![](assets/configure_web_inapp_11.png)

1. 在 **評估規則集動作** 部分 **動作** 型別，啟用 **呈現視覺個人化決定** 選項。

   ![](assets/configure_web_inapp_13.png)

1. 在 **決定內容** 區段，定義 **索引鍵** 和 **值** 決定要提供哪個體驗的配對。

1. 存取 **發佈流程** 功能表，建立新的 **資料庫** 或選取現有的 **資料庫** 並新增您新建立的 **規則**. [了解更多](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. 從您的 **資料庫**，選取 **儲存並建置到開發環境**.

   ![](assets/configure_web_inapp_14.png)

