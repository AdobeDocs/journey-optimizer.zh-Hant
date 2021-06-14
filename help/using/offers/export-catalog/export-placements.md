---
title: 位置資料集
description: 本區段列出匯出的版位資料集中使用的所有欄位。
feature: 優惠
topic: 整合
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 5%

---

# 位置資料集 {#placements-dataset}

每次修改選件時，都會更新版位的自動產生資料集。

![](../../assets/dataset-placements.png)

資料集中最新成功的批次資料會顯示在右側。 資料集的架構階層檢視會顯示在左窗格上。

>[!NOTE]
>
>了解如何在[本區段](../export-catalog/access-dataset.md)中存取Offer Library每個物件的匯出資料集。

以下是&#x200B;**[!UICONTROL Decision Object Repository - Placements]**&#x200B;資料集中可使用的所有欄位清單。

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## 識別碼

**欄位：** _id標
**題：** 識別
**碼說明：** 記錄的唯一識別碼。**類型:**&#x200B;字串

## _體驗

**欄位：** _experience 
**Type:** 物件

### _experience > decisioning

**欄位：** 決策
**類型：** 物件

#### _experience > decisioning >版位的管道識別碼

**欄位：** channelID
**標題：** 版位的管道識別
**碼說明：** 提出主張的管道。該值是有效的通道URI。 請參閱https://ns.adobe.com/xdm/channels/channel。
**類型:**&#x200B;字串

#### _experience > decisioning >內容元件類型

**欄位：** componentType 
**Title:** 內容元件類型
**說明：** 一組列舉的URI，其中每個值映射到為內容元件指定的類型。內容表示的某些使用者希望@type值能作為描述內容元件其他屬性的架構的參考。
**類型:**&#x200B;字串

#### _experience > decisioning > contentTypes

**欄位：** contentTypes 
**Type:** array

**_experience > decisioning > contentTypes > MIME Media Type**

**標題：** MIME媒體類
**型說明：** 該位置中預期之元件的媒體類型的限制。一個元件（如不同的影像格式）可能有多個媒體類型。
**類型:**&#x200B;字串

#### _experience > decisioning >版位說明

**欄位：** 說明
**標題：** 版位說明
**說明：** 此欄位可傳達人類可讀的意圖，了解如何在整體訊息傳送中使用動態內容。網頁中的特定空間是\&quot;Banner\&quot;通常是透過說明來傳達，而非透過正式方法。
**類型:**&#x200B;字串

#### _experience > decisioning >版位名稱

**欄位：** 名稱
**標題：** 版位名稱
**說明：** 在人類互動中參照該版位的指定名稱。**類型:**&#x200B;字串

## _repo

**欄位：** _repo 
**類型：** 物件

### _repo > Placement ETag

**欄位：** etag 
**標題：** 放置ETag
**說明：** 拍攝快照時決策選項物件所在的修訂。**類型:**&#x200B;字串
