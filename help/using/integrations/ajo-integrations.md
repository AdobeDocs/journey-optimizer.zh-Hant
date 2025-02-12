---
solution: Journey Optimizer
product: journey optimizer
title: 與其他解決方案整合
description: 進一步了解如何整合 Journey Optimizer 與其他解決方案
feature: Integrations
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: ccfc0870a8d59d16c7f5b6b02856785aa28dd307
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 100%

---

# 與其他解決方案整合 {#integration}

透過 Adobe Journey Optimizer，您可以輕鬆管理、保留這些資料，並將其匯出至屬於您技術堆疊一部分的平台或系統。 這些整合可協助您處理特定使用案例，並延伸 Adobe Journey Optimizer 功能範圍。

>[!NOTE]
>
> Adobe Journey Optimizer 以 Adobe Experience Platform 為基礎，以原生方式連線至 [Adobe 即時客戶輪廓](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}。此內建資料來源已預先設定，且設計旨在從即時客戶輪廓擷取並使用資料 (例如，檢查進入歷程的人員是否為客戶)。 其可讓您使用個人檔資料與體驗事件資料。 [了解更多](../datasource/adobe-experience-platform-data-source.md)。
>

## Adobe Customer Journey Analytics {#integration-cja}

在 Journey Optimizer 產生資料之後，您可利用 Customer Journey Analytics 對該資料執行進階分析。

Journey Optimizer 會將資料儲存在 Adobe Experience Platform，並利用 Customer Journey Analytics，透過自動化報告分送與資料的自訂視覺效果，全面掌握您的所有歷程、行銷活動及產品建議。

在 Journey Optimizer 建立您的歷程之後，Customer Journey Analytics 可從平台擷取資料以開始報告，並了解客戶與您歷程每次互動的影響。

深入了解 [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md)。

## Adobe Analytics {#integration-aa}

您現在可運用您已擷取並串流至 Adobe Experience Platform 的所有 Adobe Analytics 行為事件資料，以觸發即時歷程並自動化客戶體驗。此資料也可用來建立客群，後者可利用 Journey Optimizer 參與。

深入了解 [Journey Optimizer + Analytics](../event/about-analytics.md)。


## Adobe Experience Manager Assets {#integration-assets}

利用 [!DNL Adobe Experience Manager Assets] 將行銷與創意內容工作流程結合在一起。與 [!DNL Adobe Journey Optimizer] 進行本機整合，存取 [!DNL Adobe Experience Manager Assets] 來儲存、管理、探索及分發數位資產。提供了可用於填入訊息的單一、集中式資產存放庫。

可以透過左側選單 **[!UICONTROL Assets]** 區段直接從 [!DNL Adobe Journey Optimizer] 存取 [!DNL Adobe Experience Manager Assets]。

進一步了解 [Journey Optimizer + Adobe Experience Manager Assets](../integrations/assets.md)。


## Adobe Stock {#integration-stock}

[!DNL Adobe Stock] 和 [!DNL Adobe Journey Optimizer] 電子郵件設計工具整合外掛程式，為客戶提供了用於訊息製作的導覽、授權和儲存影像的簡單方法。

使用 [!DNL Adobe Journey Optimizer]，您可直接從 [!DNL Adobe Stock] 將影像上傳到電子郵件，並使用&#x200B;**[!UICONTROL 尋找 Adobe Stock 照片]**&#x200B;選項將其新增到 **[!UICONTROL Assets]** 資料夾。此外，**[!UICONTROL 尋找類似 Stock 照片]**&#x200B;選項可協助您尋找符合傳送中所用資產的內容、顏色與組成的影像。

深入了解 [Journey Optimizer + Stock](../integrations/stock.md)。


## Adobe Intelligent Services {#integration-intelligent-service}

Adobe Intelligent Services 是即時客戶資料平台的原生功能，可讓您在客戶體驗使用案例中運用人工智慧與機器學習的強大功能。 這可讓行銷分析人員利用業務層級設定，針對公司需求設定專屬預測，而無需資料科學的專業知識。

Customer AI 可讓品牌建立流失率或轉換機器學習型分數，這些分數將在 Adobe Experience Platform 以輪廓屬性形式提供，且可用來個人化歷程。

[了解更多](../building-journeys/ai-services-overview.md)。


## Adobe Campaign {#integration-ac}

如果您有 Adobe Campaign v7 或 v8，則可整合。 透過整合，您可使用 Adobe Campaign 異動訊息功能來傳送電子郵件、推播通知與簡訊。

深入瞭解 [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md)。

您也可設定整合至 Adobe Campaign Standard，以在歷程中傳送訊息。

深入了解 [Journey Optimizer + Campaign Standard](../building-journeys/using-adobe-campaign-standard.md)。


## Adobe Workfront {#integration-workfront}

使用 Adobe Workfront 中的 Adobe Journey Optimizer 模組來建立、讀取、更新或刪除記錄，或對 Adobe Journey Optimizer API 執行自訂 API 呼叫。

[這篇部落格文章中](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/accelerating-go-to-market-how-workfront-workfront-fusion-aep-and/ba-p/653685){target="_blank"}提供了此整合關鍵步驟的概觀。

了解更多有關 Journey Optimizer + Adobe Workfront [的資訊，請參閱 Adobe Workfront 文件](https://experienceleague.adobe.com/docs/workfront/using/adobe-workfront-fusion/fusion-apps-and-modules/adobe-journey-optimizer-modules.html?lang=zh-Hant){target="_blank"}。

## 自訂通道 {#integration-custom}

如果您使用協力廠商系統來傳送訊息，或想要歷程傳送 API 呼叫至協力廠商系統，請使用自訂動作來連線至您的歷程。 例如，您可利用自訂動作連線至下列系統：Epsilon、Slack、[Adobe Developer](https://developer.adobe.com){target="_blank"}、Firebase 等等。

自訂動作是技術使用者定義的其他動作，可供行銷人員使用。 在設定之後，其會顯示在您歷程的左側浮動視窗，位於&#x200B;**[!UICONTROL 動作]**&#x200B;類別。 在[本頁](../building-journeys/about-journey-activities.md#action-activities)中瞭解更多。

深入了解[自訂動作](../action/about-custom-action-configuration.md)。

## 外部資料來源 {#integration-external-systems}

Journey Optimizer 可讓您透過自訂資料來源與自訂動作來設定與外部系統的連線。 舉例來說，這可讓您利用來自外部訂房系統的資料，讓您的歷程更為豐富。

請參見[本節](../datasource/external-data-sources.md)，了解如何利用外部資料來源以定義與協力廠商系統的連線。
