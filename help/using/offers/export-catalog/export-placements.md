---
title: 位置資料集
description: 本區段列出匯出的版位資料集中使用的所有欄位。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 5%

---

# 位置資料集 {#placements-dataset}

每次修改選件時，都會更新版位的自動產生資料集。

![](../../assets/dataset-placements.png)

資料集中最新成功的批次資料會顯示在右側。 資料集的架構階層檢視會顯示在左窗格上。

>[!NOTE]
>
>了解如何在 [本節](../export-catalog/access-dataset.md).

以下是可在 **[!UICONTROL Decision Object Repository - Placements]** 資料集。

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## 識別碼

**欄位：** _id
**標題：** 識別碼
**說明：** 記錄的唯一標識符。
**類型:**&#x200B;字串

## _體驗

**欄位：** _體驗
**類型：** 物件

### _experience > decisioning

**欄位：** 決策
**類型：** 物件

#### _experience > decisioning >版位的管道識別碼

**欄位：** channelID
**標題：** 版位的管道識別碼
**說明：** 提出建議的渠道。 該值是有效的通道URI。 請參閱https://ns.adobe.com/xdm/channels/channel。
**類型:**&#x200B;字串

#### _experience > decisioning >內容元件類型

**欄位：** componentType
**標題：** 內容元件類型
**說明：** 枚舉的URI集，其中每個值映射到為內容元件指定的類型。 內容表示的某些使用者希望@type值能作為描述內容元件其他屬性的架構的參考。
**類型:**&#x200B;字串

#### _experience > decisioning > contentTypes

**欄位：** contentTypes
**類型：** 陣列

**_experience > decisioning > contentTypes > MIME Media Type**

**標題：** MIME媒體類型
**說明：** 該位置中預期的元件的媒體類型的約束。 一個元件（如不同的影像格式）可能有多個媒體類型。
**類型:**&#x200B;字串

#### _experience > decisioning >版位說明

**欄位：** 說明
**標題：** 版位說明
**說明：** 它用於傳達人類可讀的意圖，以了解如何在整體訊息傳送中使用動態內容。 網頁中的特定空間是\&quot;Banner\&quot;通常是透過說明來傳達，而非透過正式方法。
**類型:**&#x200B;字串

#### _experience > decisioning >版位名稱

**欄位：** 名稱
**標題：** 版位名稱
**說明：** 在人類互動中參照該位置的指定名稱。
**類型:**&#x200B;字串

## _repo

**欄位：** _repo
**類型：** 物件

### _repo > Placement ETag

**欄位：** etag
**標題：** Placement ETag
**說明：** 建立快照時決策選項對象所在的修訂。
**類型:**&#x200B;字串
