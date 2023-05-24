---
title: 資料收集
description: 瞭解有關決策管理反饋資料收集的詳細資訊
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 3%

---

# 決策管理資料收集 {#data-collection}

## 瞭解資料收集

您可以在Adobe Experience Platform收集offer decisioning反饋，包括顯示哪些優惠以及用戶如何與其交互。 此資料可用於：
* 合成 [決策管理報告](../reports/get-started-events.md);
* 使用 [頻率封蓋](../offer-library/add-constraints.md#capping) 規則；
* 大樓 [AI模型](../ranking/create-ranking-strategies.md) 可用作排名方法。

## 事件類型

收集資料的方式會因您要捕獲的事件類型而異。

### 決策事件

每次決策管理做出決策時，與該決策事件相關的資訊 **自動** 發到Adobe Experience Platform，所有頻道。 [了解更多](../reports/get-started-events.md)

### 印象和按一下事件

決策管理印象和點擊定義如下：

* 安 **印象** 事件是向用戶顯示要約時。

* A **按一下** 事件是用戶按一下或與聘用交互時。

根據 [!DNL Journey Optimizer] 所使用的通道。

**電子郵件** 創作者 [!DNL Journey Optimizer] **自動** 跟蹤觀感和點擊量。

但是， **最多頻道** 需要將印象和點擊資料作為 **體驗活動**。 其中包括:

* 使用 [Adobe Experience PlatformWeb SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant){target="_blank"} 提供優惠

* 使用 [Adobe Experience Platform移動SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* 亭
* 通過第三方應用程式發送的消息
   <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>使用決定API請求來接收服務的通道需要將反饋作為體驗事件發送到。 換句話說，如果服務需要有關如何呈現的說明，您可以假定您應將反饋作為體驗事件發送。

### 自訂事件

根據您自己的偏好，可將與優惠掛鈎的定製事件反饋發送到Adobe Experience Platform。 例如，如果聘用具有多個按鈕，如 *感興趣*。 *不感興趣*，等等，您可能希望單獨發送這些事件，但這些事件也可以作為體驗事件發送。

## 發送反饋資料

要發送反饋資料，您需要建立一個資料集以收集事件，並為每個事件類型定義一個將發送到Adobe Experience Platform的體驗事件。

* 瞭解如何建立將在中收集體驗事件的資料集 [此部分](create-dataset.md)。

* 瞭解如何定義要在中發送反饋資料的體驗事件 [此部分](schema-requirement.md)。
