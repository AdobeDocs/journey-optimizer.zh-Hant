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
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 9%

---

# Mobile 上線快速入門工作流程 {#mobile-wf}

新的 **行動入門快速入門工作流程** 是一項新產品功能，可快速設定Adobe Experience Platform Mobile SDK、開始收集及驗證行動事件資料，以及傳送推播通知 [!DNL Journey Optimizer].

此功能可透過 **[!DNL Adobe Experience Platform Data Collection]** 首頁以供所有客戶作為公開測試版使用。

## 快速入門{#gs-mobile-wf}

此新工作流程會透過減少總點按次數並加快Journey Optimizer的行動設定速度，使資料收集設定自動化。 此快速入門工作流程會帶您完成四個簡單步驟，以便 [設定](##setup-mobile-wf)， [實施](#implement-mobile-wf)， [驗證](#valid-mobile-wf)、和 [評論](#review-mobile-wf) 您的行動設定。

若要存取新的行動入門快速入門工作流程，請瀏覽 **[!DNL Data Collection]** 解決方案切換器中的。 然後選取 **[!DNL Start Collecting Mobile Data]** 卡片。

![](assets/mobile-wf-home.png)

以下是一些其他功能：

* 簡單的四步驟工作流程和使用者介面。
* 提供基本設定，以開始透過收集行動事件資料 [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} 幾分鐘內。
* 運用測試及驗證基本行動推送事件的功能 [Adobe Experience Platform保證](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html){target="_blank"}.
* 自動建立及設定所有必要的資料收集和Journey Optimizer資產。
* 在產品指引和工具提示中。
* 如有需要，可提供更進階實作的自然轉換。

## 設定 {#setup-mobile-wf}

此工作流程的第一步會自動建立及設定所有必要的資料收集和Journey Optimizer資產，例如行動屬性、行動擴充功能、Journey Optimizer擴充功能、規則、資料元素等。

接受測試版條款與條件後，請輸入行動應用程式的名稱，然後按一下 **[!DNL Next]**.

![](assets/mobile-wf-setup.png)

提供iOS和Android平台的資訊，包括應用程式ID和驗證金鑰或金鑰檔案。

## 實作{#implement-mobile-wf}

下一個步驟提供將程式碼安裝到行動應用程式的逐步指南。

![](assets/mobile-wf-add-code.png)


## 驗證{#valid-mobile-wf}

檢閱並檢查實作以驗證。 您可以傳送測試推播通知。

![](assets/mobile-wf-valid.png)


## 請檢閱 {#review-mobile-wf}

自動化設定已完成。 您現在可以造訪標籤行動屬性，設定規則或資料元素，並開始使用Adobe Journey Optimizer傳送推播通知。

![](assets/mobile-wf-done.png)


**相關主題**

* [開始使用推播通知](get-started-push.md)
* [推播通知資料流程和元件](push-gs.md)
* [設定推播通道](push-configuration.md)
* [推播通知報告](../reports/journey-global-report.md#push-global)
* [建立推播通知](create-push.md)
