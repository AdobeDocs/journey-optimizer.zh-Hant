---
solution: Journey Optimizer
product: journey optimizer
title: AJO訊息匯出綱要
description: 瞭解AJO訊息匯出資料集中可用的欄位
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 匯出，訊息，資料集，結構描述，電子郵件，簡訊
feature_v2: []
subfeature_v2: id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 420
ht-degree: 4%

---

# AJO訊息匯出綱要 {#ajo-message-export-schema}

在電子郵件或簡訊通道設定上啟用&#x200B;**訊息匯出**&#x200B;時，已傳送的訊息內容會寫入[!DNL Adobe Experience Platform]中的&#x200B;**AJO訊息匯出資料集**。

本節列出匯出資料集中的可用欄位。

## 資料集欄位

+++ 體驗(_E)

**欄位：** `_experience`\
**型別：**&#x200B;物件

+++

+++ _experience > customerJourneyManagement

**欄位：** `customerJourneyManagement`\
**型別：**&#x200B;物件

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata

**欄位：** `messageDeliveryMetadata`\
**型別：**&#x200B;物件

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > emailMetadata

**欄位：** `emailMetadata`\
**型別：**&#x200B;物件

* 收件者

  **欄位：** `recipient`\
  **型別：**&#x200B;物件

   * 密件副本

     **欄位：** `bcc`\
     **型別：**&#x200B;字串陣列

   * cc

     **欄位：** `cc`\
     **型別：**&#x200B;字串陣列

   * 電子郵件

     **欄位：** `email`\
     **型別：**&#x200B;字串

   * 名稱

     **欄位：** `name`\
     **型別：**&#x200B;字串

* 寄件者

  **欄位：** `sender`\
  **型別：**&#x200B;物件

   * 電子郵件

     **欄位：** `email`\
     **型別：**&#x200B;字串

   * errorEmail

     **欄位：** `errorEmail`\
     **型別：**&#x200B;字串

   * 名稱

     **欄位：** `name`\
     **型別：**&#x200B;字串

   * replyToEmail

     **欄位：** `replyToEmail`\
     **型別：**&#x200B;字串

   * replyToName

     **欄位：** `replyToName`\
     **型別：**&#x200B;字串

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > smsMetadata

**欄位：** `smsMetadata`\
**型別：**&#x200B;物件

* 收件者

  **欄位：** `recipient`\
  **型別：**&#x200B;物件

   * 數字

     **欄位：** `number`\
     **型別：**&#x200B;字串

* 寄件者

  **欄位：** `sender`\
  **型別：**&#x200B;物件

   * 數字

     **欄位：** `numbers`\
     **型別：**&#x200B;字串陣列

+++

+++ _experience > customerJourneyManagement > messageExecution

**欄位：** `messageExecution`\
**型別：**&#x200B;物件

* 客群

  **欄位：** `audience`\
  **型別：**&#x200B;物件

   * id

     **欄位：** `id`\
     **型別：**&#x200B;字串

   * 類型

     **欄位：** `type`\
     **型別：**&#x200B;字串

* fragmentPublicationIDs

  **欄位：** `fragmentPublicationIDs`\
  **型別：**&#x200B;字串陣列

* 中繼資料

  **欄位：** `metadata`\
  **型別：**&#x200B;對應

   * [對應索引鍵]

     **型別：**&#x200B;字串

* parentSourceMeta

  **欄位：** `parentSourceMeta`\
  **型別：**&#x200B;物件

   * sourceActionID

     **欄位：** `sourceActionID`\
     **型別：**&#x200B;字串

   * sourceID

     **欄位：** `sourceID`\
     **型別：**&#x200B;字串

   * sourceType

     **欄位：** `sourceType`\
     **型別：**&#x200B;字串

   * sourceVersionID

     **欄位：** `sourceVersionID`\
     **型別：**&#x200B;字串

* batchinstanceid

  **欄位：** `batchInstanceID`\
  **型別：**&#x200B;字串

* campaignActionID

  **欄位：** `campaignActionID`\
  **型別：**&#x200B;字串

* campaignID

  **欄位：** `campaignID`\
  **型別：**&#x200B;字串

* campaignVersionID

  **欄位：** `campaignVersionID`\
  **型別：**&#x200B;字串

* journeyActionID

  **欄位：** `journeyActionID`\
  **型別：**&#x200B;字串

* journeyVersionID

  **欄位：** `journeyVersionID`\
  **型別：**&#x200B;字串

* journeyVersionInstanceID

  **欄位：** `journeyVersionInstanceID`\
  **型別：**&#x200B;字串

* journeyVersionNodeID

  **欄位：** `journeyVersionNodeID`\
  **型別：**&#x200B;字串

* messageexecutidid

  **欄位：** `messageExecutionID`\
  **型別：**&#x200B;字串

* messageID

  **欄位：** `messageID`\
  **型別：**&#x200B;字串

* messagePublicationID

  **欄位：** `messagePublicationID`\
  **型別：**&#x200B;字串

* messageType

  **欄位：** `messageType`\
  **型別：**&#x200B;字串

* waveID

  **欄位：** `waveID`\
  **型別：**&#x200B;字串

+++

+++ _experience > customerJourneyManagement > messageProfile

**欄位：** `messageProfile`\
**型別：**&#x200B;物件

* 管道

  **欄位：** `channel`\
  **型別：**&#x200B;物件

   * contentType

     **欄位：** `contentTypes`\
     **型別：**&#x200B;字串陣列

   * locationtypes

     **欄位：** `locationTypes`\
     **型別：**&#x200B;字串陣列

   * metricTypes

     **欄位：** `metricTypes`\
     **型別：**&#x200B;字串陣列

   * _id

     **欄位：** `_id`\
     **型別：**&#x200B;字串

   * _type

     **欄位：** `_type`\
     **型別：**&#x200B;字串

   * mediaAction

     **欄位：** `mediaAction`\
     **型別：**&#x200B;字串

   * mediaType

     **欄位：** `mediaType`\
     **型別：**&#x200B;字串

   * 模式

     **欄位：** `mode`\
     **型別：**&#x200B;字串

   * referringSource

     **欄位：** `referringSource`\
     **型別：**&#x200B;字串

   * typeAtSource

     **欄位：** `typeAtSource`\
     **型別：**&#x200B;字串

* isSendTimeOptimized

  **欄位：** `isSendTimeOptimized`\
  **型別：**&#x200B;布林值

* isTestExecution

  **欄位：** `isTestExecution`\
  **型別：**&#x200B;布林值

* messageProfileID

  **欄位：** `messageProfileID`\
  **型別：**&#x200B;字串

* messageProfileTrackingID

  **欄位：** `messageProfileTrackingID`\
  **型別：**&#x200B;字串

* requestId

  **欄位：** `requestID`\
  **型別：**&#x200B;字串

* secondaryDimensionID

  **欄位：** `secondaryDimensionID`\
  **型別：**&#x200B;字串

* secondaryDimensionName

  **欄位：** `secondaryDimensionName`\
  **型別：**&#x200B;字串

* 變體

  **欄位：** `variant`\
  **型別：**&#x200B;字串

+++

+++ _experience > customerJourneyManagement > messageRendedContent

**欄位：** `messageRenderedContent`\
**型別：**&#x200B;物件

* 電子郵件內容

  **欄位：** `emailContent`\
  **型別：**&#x200B;物件

   * html

     **欄位：** `html`\
     **型別：**&#x200B;字串

   * 主旨

     **欄位：** `subject`\
     **型別：**&#x200B;字串

   * 文字

     **欄位：** `text`\
     **型別：**&#x200B;字串

* smsContent

  **欄位：** `smsContent`\
  **型別：**&#x200B;物件

   * 媒體

     **欄位：** `media`\
     **型別：**&#x200B;字串

   * 訊息

     **欄位：** `message`\
     **型別：**&#x200B;字串

   * 標題

     **欄位：** `title`\
     **型別：**&#x200B;字串

+++

+++ identityMap

**欄位：** `identityMap`\
**型別：**&#x200B;對應

* [對應索引鍵]

  **型別：**&#x200B;物件陣列

   * authenticatedState

     **欄位：** `authenticatedState`\
     **型別：**&#x200B;字串

   * id

     **欄位：** `id`\
     **型別：**&#x200B;字串

   * 主要

     **欄位：** `primary`\
     **型別：**&#x200B;布林值

+++

+++ eventType

**欄位：** `eventType`\
**型別：**&#x200B;字串

+++

+++ productedBy

**欄位：** `producedBy`\
**型別：**&#x200B;字串

+++

+++ 時間戳記

**欄位：** `timestamp`\
**型別：**&#x200B;日期時間

+++

