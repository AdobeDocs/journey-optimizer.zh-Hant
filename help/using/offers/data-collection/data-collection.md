---
title: 資料收集
description: 深入了解決策管理意見資料收集
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 1%

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

1. 一方面，有些管道 **自動** 追蹤曝光次數和點按次數。 具體如下：

   * 由撰寫的電子郵件 [!DNL Journey Optimizer]
   * 由製作的行動推播通知 [!DNL Journey Optimizer]
   * 使用 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} 或行動SDK<!--TBC--> 呈現選件 <!--need more info + link-->

   >[!NOTE]
   >
   >如果Adobe以視覺化方式將選件轉譯給管道上的一般使用者，您可以假設Adobe會自動傳入意見。

1. 另一方面，有些管道需要將曝光數和點按資料以 **體驗事件**.

   除了使用 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} 或行動SDK<!--TBC-->，所有使用決策API請求來接收選件的管道都需要以體驗事件的形式傳送意見。 其中包括:

   * 網頁
   * 資訊站
   * 透過協力廠商應用程式傳送的訊息

   >[!NOTE]
   >
   >如果選件需要有關如何呈現的指示，您可以假設您應將意見傳入作為體驗事件。

### 自訂事件

根據您自己的偏好設定，可將與優惠方案相連結之自訂事件的意見傳送至Adobe Experience Platform。 例如，如果選件有多個按鈕，例如 *興趣*, *不感興趣*，以此類推，您可能想要個別傳入這些事件，但也可以以體驗事件的形式傳入。 <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## 傳送意見資料

若要傳入意見資料，您需要建立資料集以收集事件，並針對每種事件類型定義要傳送至Adobe Experience Platform的體驗事件。

* 了解如何建立要在中收集體驗事件的資料集 [本節](create-dataset.md).

* 了解如何定義體驗事件，以便在 [本節](schema-requirement.md).

