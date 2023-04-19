---
title: 資料收集
description: 深入了解決策管理意見資料收集
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 3%

---

# 決策管理資料收集 {#data-collection}

## 了解資料收集

您可以在Adobe Experience Platform中收集offer decisioning意見，包括顯示哪些優惠方案以及使用者與這些優惠方案的互動方式。 此資料可用於：
* 合成 [決策管理報告](../reports/get-started-events.md);
* 使用 [頻率限定](../offer-library/add-constraints.md#capping) 規則；
* 建置 [AI模型](../ranking/create-ranking-strategies.md) 可作為排名方法。

## 事件類型

收集資料的方式會根據您要擷取的事件類型而有所不同。

### 決策事件

每次決策管理作出決策時，與該決策事件相關的資訊為 **自動** 已傳送至Adobe Experience Platform（所有通道）。 [了解更多](../reports/get-started-events.md)

### 曝光次數和點按事件

決策管理曝光次數和點按次數的定義如下：

* 安 **印象** 事件是向使用者顯示選件的時機。

* A **按一下** 事件是使用者點按或與選件互動時。

會根據 [!DNL Journey Optimizer] 使用的通道。

**電子郵件** 由 [!DNL Journey Optimizer] **自動** 追蹤曝光次數和點按次數。

不過， **最多通道** 需要將曝光次數和點按次數資料以 **體驗事件**. 其中包括:

* 網頁使用 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant){target="_blank"} 呈現選件

* 使用 [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* 資訊站
* 透過協力廠商應用程式傳送的訊息
   <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>使用決策API請求來接收選件的管道需要以體驗事件的形式傳送意見。 換言之，如果選件需要有關如何呈現的指示，您可以假設您應將意見以體驗事件的形式傳入。

### 自訂事件

根據您自己的偏好設定，可將與優惠方案相連結之自訂事件的意見傳送至Adobe Experience Platform。 例如，如果選件有多個按鈕，例如 *興趣*, *不感興趣*，以此類推，您可能想要個別傳入這些事件，但也可以以體驗事件的形式傳入。 <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## 傳送意見資料

若要傳入意見資料，您需要建立資料集以收集事件，並針對每種事件類型定義要傳送至Adobe Experience Platform的體驗事件。

* 了解如何建立要在中收集體驗事件的資料集 [本節](create-dataset.md).

* 了解如何定義體驗事件，以便在 [本節](schema-requirement.md).
