---
solution: Journey Optimizer
product: journey optimizer
title: 與其他解決方案整合
description: 進一步了解如何整合Journey Optimizer與其他解決方案
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: f635c6995c453ed6d1042ef3e699d977e824f01e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 與其他解決方案整合 {#integration}

使用Adobe Journey Optimizer，您可以輕鬆管理、保留這些資料，並將其匯出至屬於您技術堆疊一部分的平台或系統。 這些整合可協助您處理特定使用案例，並延伸Adobe Journey Optimizer功能範圍。

>[!NOTE]
>
> Adobe Journey Optimizer以Adobe Experience Platform為基礎，以原生方式連線至 [Adobe即時客戶個人檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。 此內建資料來源已預先設定，且設計為從即時客戶設定檔中擷取和使用資料（例如，檢查進入歷程的人員是否為客戶）。 它可讓您使用設定檔資料和體驗事件資料。 [了解更多](../datasource/adobe-experience-platform-data-source.md)。

## Adobe Customer Journey Analytics{#integration-cja}

您可以匯出Journey Optimizer產生的資料，以在Customer Journey Analytics中執行進階分析。

Journey Optimizer與Customer Journey Analytics的整合提供您所有歷程、行銷活動和選件的全方位檢視，並提供自動化報表分送和資料的自訂視覺效果。

在Journey Optimizer中建立您的歷程後，您可以將客戶資料匯入Customer Journey Analytics，以開始報告並了解客戶與您歷程的每次互動的影響。

深入了解 [Journey Optimizer +Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics{#integration-aa}

您可以運用您已擷取並串流至Adobe Experience Platform的所有Adobe Analytics行為事件資料，以觸發即時歷程，並為客戶自動化體驗。

深入了解 [Journey Optimizer + Analytics](../event/about-analytics.md).

## AdobeIntelligent Services{#integration-intelligent-service}

與Adobe智慧服務的整合可讓您在客戶體驗使用案例中運用人工智慧和機器學習的強大功能。 這可讓行銷分析人員使用業務層級設定，針對公司的需求設定專屬預測，而不需要資料科學的專業知識。 例如，Adobe智慧服務可讓品牌建立流失率或轉換機器學習的分數，這些分數將在Adobe Experience Platform中以描述檔屬性的形式提供，並可用於個人化歷程。 [了解更多](../building-journeys/ai-services-overview.md)。


## Adobe Campaign{#integration-ac}

如果您有Adobe Campaign v7或v8，則可使用整合。 使用此整合，使用Adobe Campaign交易訊息功能來傳送電子郵件、推播通知和簡訊。

深入了解 [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md).

您也可以設定與Adobe Campaign Standard的整合，以在歷程中傳送訊息。

深入了解 [Journey Optimizer +Campaign Standard](../building-journeys/ajo-ac.md).

## 自訂通道{#integration-custom}

如果您使用協力廠商系統來傳送訊息，或想要歷程將API呼叫傳送至協力廠商系統，請使用自訂動作來設定其與歷程的連線。 例如，您可以使用自訂動作連線至下列系統：ε,Slack, [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;}、Firebase等

自訂動作是技術使用者定義的其他動作，可供行銷人員使用。 設定後，它們會顯示在歷程的左側浮動視窗中，位於 **[!UICONTROL 動作]** 類別。 在[本頁](../building-journeys/about-journey-activities.md#action-activities)中瞭解更多。

深入了解 [自訂動作](../action/about-custom-action-configuration.md).

## 外部資料來源{#integration-external-systems}

Journey Optimizer可讓您透過自訂資料來源和自訂動作來設定與外部系統的連線。 舉例來說，這可讓您透過來自外部訂房系統的資料，讓您的歷程更為豐富。

了解如何使用外部資料來源來定義與協力廠商系統的連線，位於 [本節](../datasource/external-data-sources.md).
