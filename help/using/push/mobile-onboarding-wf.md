---
solution: Journey Optimizer
product: journey optimizer
title: Mobile 上線快速入門工作流程
description: 瞭解如何使用行動入門快速入門工作流程
topic: Mobile
feature: Push
role: Admin
level: Intermediate
badge: label="Beta" type="Informative"
exl-id: 364ef926-3f92-4297-acbd-a283668106ac
source-git-commit: 4d7ad2c3ed71801298f1afe31d0e29d7bb1d5c7f
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 9%

---

# Mobile 上線快速入門工作流程 {#mobile-wf}

新的&#x200B;**行動入門快速入門工作流程**&#x200B;是新的產品功能，可快速設定Adobe Experience Platform Mobile SDK、開始收集和驗證行動事件資料，以及透過[!DNL Journey Optimizer]傳送推播通知。

此功能可透過&#x200B;**[!DNL Adobe Experience Platform Data Collection]**&#x200B;首頁以公用Beta的形式供所有客戶存取。

## 快速入門{#gs-mobile-wf}

此新工作流程會透過減少總點按次數並加快Journey Optimizer的行動設定速度，使資料收集設定自動化。 此快速入門工作流程將帶您進行四個簡單的步驟，以[設定](##setup-mobile-wf)、[實作](#implement-mobile-wf)、[驗證](#valid-mobile-wf)以及[檢閱](#review-mobile-wf)您的行動設定。

若要存取新的行動入門快速入門工作流程，請從解決方案切換器瀏覽至&#x200B;**[!DNL Data Collection]**。 然後在首頁上選取&#x200B;**[!DNL Start Collecting Mobile Data]**&#x200B;卡片。

![](assets/mobile-wf-home.png)

以下是一些其他功能：

* 簡單的四步驟工作流程和使用者介面。
* 提供基本設定，以便在幾分鐘內開始透過[Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"}收集行動事件資料。
* 能夠利用[Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=zh-Hant){target="_blank"}測試及驗證基本行動推播事件。
* 自動建立及設定所有必要的資料收集和Journey Optimizer資產。
* 在產品指引和工具提示中。
* 如有需要，可提供更進階實作的自然轉換。

## 設定 {#setup-mobile-wf}

此工作流程的第一步會自動建立及設定所有必要的資料收集和Journey Optimizer資產，例如行動屬性、行動擴充功能、Journey Optimizer擴充功能、規則、資料元素等。

接受Beta條款與條件後，請輸入行動應用程式的名稱，然後按一下&#x200B;**[!DNL Next]**。

![](assets/mobile-wf-setup.png)

提供iOS和Android平台的資訊，包括應用程式ID和驗證金鑰或金鑰檔案。

## 實作{#implement-mobile-wf}

下一個步驟提供將程式碼安裝到行動應用程式的逐步指南。

![](assets/mobile-wf-add-code.png)


## 驗證{#valid-mobile-wf}

檢閱並檢查實作以驗證。 您可以傳送測試推播通知。

![](assets/mobile-wf-valid.png)


## 審閱 {#review-mobile-wf}

自動化設定已完成。 您現在可以造訪標籤行動屬性，設定規則或資料元素，並開始使用Adobe Journey Optimizer傳送推播通知。

![](assets/mobile-wf-done.png)


**相關主題**

* [開始使用推播通知](../../rp_landing_pages/push-landing-page.md)
* [推播通知資料流程和元件](push-gs.md)
* [設定推播通道](push-configuration.md)
* [推播通知報告](../reports/journey-global-report-cja-push.md#push-global)
* [建立推播通知](create-push.md)
