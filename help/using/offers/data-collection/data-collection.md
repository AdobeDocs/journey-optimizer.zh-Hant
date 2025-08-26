---
title: 資料彙集
description: 進一步了解決策管理意見反應資料收集
badge: label="舊版" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer, Developer
level: Experienced
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 1%

---

# 決策管理資料收集 {#data-collection}

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

不過，**大部分的管道**&#x200B;都需要曝光數和點按數資料，才能以&#x200B;**體驗事件**&#x200B;的形式傳送到Adobe Experience Platform。 其中包括：

* 使用[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"}呈現選件的網頁

* 使用[Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}呈現選件的行動應用程式 — [深入瞭解](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
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
