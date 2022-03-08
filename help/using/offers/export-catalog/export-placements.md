---
title: 位置資料集
description: 此部分列出導出資料集中用於放置的所有欄位
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 5%

---

# 位置資料集 {#placements-dataset}

每次修改要約時，更新用於放置的自動生成的資料集。

![](../assets/dataset-placements.png)

資料集中最近成功的批處理顯示在右側。 資料集的架構的分層視圖顯示在左窗格中。

>[!NOTE]
>
>瞭解如何訪問中提供庫的每個對象的導出資料集 [此部分](../export-catalog/access-dataset.md)。

下面是可在 **[!UICONTROL Decision Object Repository - Placements]** 資料集。

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## 識別碼 {#identifier}

**欄位：** _id
**標題：** 標識符
**描述：** 記錄的唯一標識符。
**類型:**&#x200B;字串

## _體驗 {#experience}

**欄位：** 體驗
**類型：** 對象

### 經驗>決策

**欄位：** 決定
**類型：** 對象

#### _experience >決策>放置的通道標識符

**欄位：** 通道ID
**標題：** 放置的通道標識符
**描述：** 提出建議的渠道。 該值是有效的通道URI。 請參閱https://ns.adobe.com/xdm/channels/channel。
**類型:**&#x200B;字串

#### 經驗>決策>內容元件類型

**欄位：** 元件類型
**標題：** 內容元件類型
**描述：** 枚舉的一組URI，其中每個值映射到給定給內容元件的類型。 內容表示的一些使用者希望@type值是對描述內容元件附加屬性的架構的引用。
**類型:**&#x200B;字串

#### _experience >決策>內容類型

**欄位：** 內容類型
**類型：** 陣列

**_experience >決策>內容類型> MIME媒體類型**

**標題：** MIME媒體類型
**描述：** 該位置中預期的元件的介質類型的約束。 對於一個元件（如不同的影像格式），可能有多種介質類型。
**類型:**&#x200B;字串

#### _experience >決策>放置說明

**欄位：** 描述
**標題：** 放置說明
**描述：** 它用於傳達關於動態內容如何在整體消息傳遞中使用的人類可讀意圖。 網頁中的某個空間是\ &quot;Banner\&quot;，通常通過說明而不是正式方法來傳達。
**類型:**&#x200B;字串

#### _experience >決策>放置名稱

**欄位：** 名稱
**標題：** 放置名稱
**描述：** 在人類交互中引用位置的指定名稱。
**類型:**&#x200B;字串

## _repo {#repo}

**欄位：** _repo
**類型：** 對象

### _repo >放置ETag

**欄位：** etag
**標題：** 放置ETag
**描述：** 拍攝快照時決策選項對象所在的修訂版本。
**類型:**&#x200B;字串
