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

* 請確認您使用的是最新版的&#x200B;**Adobe Experience Platform Web SDK**&#x200B;擴充功能。

* 在您的&#x200B;**標籤屬性**&#x200B;中安裝&#x200B;**Adobe Experience Platform Web SDK**&#x200B;擴充功能，並啟用&#x200B;**Personalization儲存空間**&#x200B;選項。

  此設定對於在使用者端上儲存事件歷史記錄是必要的，這是在規則產生器中實作頻率規則的先決條件。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

  ![](assets/configure_web_inapp_1.png)

## 設定傳送資料至平台規則 {#configure-sent-data-trigger}

1. 存取您的&#x200B;**Adobe Experience Platform Data Collection**&#x200B;執行個體，並導覽至以&#x200B;**Adobe Experience Platform Web SDK**&#x200B;擴充功能設定的&#x200B;**標籤屬性**。

1. 從&#x200B;**製作**&#x200B;功能表中，選取&#x200B;**規則**，然後&#x200B;**建立新規則**&#x200B;或&#x200B;**新增規則**。

   ![](assets/configure_web_inapp_2.png)

1. 在&#x200B;**事件**&#x200B;區段中，按一下&#x200B;**新增**，然後依照下列方式設定：

   * **延伸模組**：核心

   * **事件型別**：已載入程式庫（頁面頂端）。

   ![](assets/configure_web_inapp_3.png)

1. 按一下&#x200B;**保留變更**&#x200B;以儲存事件設定。

1. 在&#x200B;**動作**&#x200B;區段中，按一下&#x200B;**新增**，然後依照下列方式設定：

   * **擴充功能**： Adobe Experience Platform Web SDK

   * **動作型別**：傳送事件

   ![](assets/configure_web_inapp_4.png)

1. 在您&#x200B;**動作**&#x200B;型別的&#x200B;**Personalization**&#x200B;區段中，啟用&#x200B;**呈現視覺個人化決策**&#x200B;選項。

   ![](assets/configure_web_inapp_5.png)

1. 在&#x200B;**決定內容**&#x200B;區段中，定義決定要傳送哪個體驗的&#x200B;**索引鍵**&#x200B;和&#x200B;**值**&#x200B;配對。

   ![](assets/configure_web_inapp_6.png)

1. 按一下&#x200B;**保留變更**&#x200B;以儲存您的&#x200B;**動作**&#x200B;設定。

1. 導覽至&#x200B;**發佈流程**&#x200B;功能表。 建立新的&#x200B;**資料庫**&#x200B;或選取現有的&#x200B;**資料庫**，並將您新建立的&#x200B;**規則**&#x200B;新增至資料庫。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. 從您的&#x200B;**資料庫**，選取&#x200B;**儲存並建置至開發**。

   ![](assets/configure_web_inapp_7.png)

## 設定手動規則 {#configure-manual-trigger}

1. 存取您的&#x200B;**Adobe Experience Platform Data Collection**&#x200B;執行個體，並導覽至以&#x200B;**Adobe Experience Platform Web SDK**&#x200B;擴充功能設定的&#x200B;**標籤屬性**。

1. 從&#x200B;**製作**&#x200B;功能表中，選取&#x200B;**規則**，然後&#x200B;**建立新規則**&#x200B;或&#x200B;**新增規則**。

   ![](assets/configure_web_inapp_8.png)

1. 在&#x200B;**事件**&#x200B;區段中，按一下&#x200B;**新增**，然後依照下列方式設定：

   * **延伸模組**：核心

   * **事件型別**：按一下

   ![](assets/configure_web_inapp_9.png)

1. 在&#x200B;**Click設定**&#x200B;中，定義要評估的&#x200B;**選取器**。

   ![](assets/configure_web_inapp_10.png)

1. 按一下&#x200B;**保留變更**&#x200B;以儲存&#x200B;**事件**&#x200B;設定。

1. 在&#x200B;**動作**&#x200B;區段中，按一下&#x200B;**新增**，然後依照下列方式設定：

   * **擴充功能**： Adobe Experience Platform Web SDK

   * **動作型別**：評估規則集

   ![](assets/configure_web_inapp_11.png)

1. 在您&#x200B;**動作**&#x200B;型別的&#x200B;**評估規則集動作**&#x200B;區段中，啟用&#x200B;**呈現視覺個人化決定**&#x200B;選項。

   ![](assets/configure_web_inapp_13.png)

1. 在&#x200B;**決定內容**&#x200B;區段中，定義決定要傳送哪個體驗的&#x200B;**索引鍵**&#x200B;和&#x200B;**值**&#x200B;配對。

1. 存取&#x200B;**發佈流程**&#x200B;功能表、建立新的&#x200B;**資料庫**&#x200B;或選取現有的&#x200B;**資料庫**，並新增您新建立的&#x200B;**規則**。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. 從您的&#x200B;**資料庫**，選取&#x200B;**儲存並建置至開發**。

   ![](assets/configure_web_inapp_14.png)

