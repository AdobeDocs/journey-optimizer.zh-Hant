---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 資料收集
description: 進一步了解決策管理意見反應資料收集
badge: label="舊版" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Experienced
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-xLnILnYeTkebBswLoIyVxKl61aaOWqX1vp6GaAoG0A
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 433
ht-degree: 7%

---

# 決策管理資料收集 {#data-collection}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！ [了解更多](../../experience-decisioning/gs-experience-decisioning.md)

## 瞭解資料彙集

您可以在Adobe Experience Platform中收集Offer Decisioning意見回饋，包括顯示哪些優惠方案以及使用者如何與其互動。 此資料可用於：

* 構成[決定管理報告](../reports/get-started-events.md)；
* 使用[頻率限定](../offer-library/add-constraints.md#capping)規則；
* 正在建置可以做為排名方法的[AI模型](../ranking/create-ranking-strategies.md)。

## 事件型別

資料收集方式因您要擷取的事件型別而異。

### 決定事件

每次決策管理做出決策時，該決策事件的相關資訊都會自動&#x200B;**傳送**&#x200B;至所有管道的Adobe Experience Platform。 [了解更多](../reports/get-started-events.md)

### 曝光和點選事件

決定管理曝光次數和點按次數定義如下：

* 向使用者顯示選件時發生&#x200B;**印象**&#x200B;事件。

* **click**&#x200B;事件是使用者點按或互動選件時。

系統會根據使用的[!DNL Journey Optimizer]管道，擷取曝光數與點按數的回饋。

**電子郵件**&#x200B;由[!DNL Journey Optimizer]編寫&#x200B;**自動**&#x200B;追蹤閱聽和點按。

不過，**大部分的管道**&#x200B;都需要曝光數和點按數資料，才能以&#x200B;**體驗事件**&#x200B;的形式傳送到Adobe Experience Platform。 其中包括:

* 使用[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant){target="_blank"}呈現選件的網頁

* 使用[Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=zh-Hant){target="_blank"}呈現選件的行動應用程式 — [深入瞭解](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* 資訊站
* 透過協力廠商應用程式傳送的訊息
  <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>使用決策API請求接收優惠的管道需要以體驗事件的形式傳送意見回應。 換言之，如果選件需要有關如何轉譯的指示，您可以假設您應將意見作為體驗事件傳送。

### 自訂事件

與您優惠相連結的自訂事件回饋，可根據您自己的偏好設定傳送到Adobe Experience Platform。 例如，如果選件有多個按鈕，例如&#x200B;*感興趣*、*不感興趣*&#x200B;等，您可能想要分別傳送這些事件，但這些事件也可以以體驗事件的形式傳送。

## 傳送意見回饋資料

若要傳送意見反應資料，您必須建立資料集以收集事件，並針對每種事件型別定義要傳送至Adobe Experience Platform的體驗事件。

* 瞭解如何建立將在[此區段](create-dataset.md)中收集體驗事件的資料集。

* 在[本節](schema-requirement.md)中瞭解如何定義要傳送意見回饋資料的體驗事件。
