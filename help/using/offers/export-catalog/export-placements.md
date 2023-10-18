---
title: 位置資料集
description: 本節列出匯出的資料集中用於版位的所有欄位
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 5%

---

# 位置資料集 {#placements-dataset}

每次修改選件時，都會更新自動產生的刊登版位資料集。

![](../assets/dataset-placements.png)

資料集中最近成功的批次會顯示在右側。 資料集的結構描述階層檢視會顯示在左窗格中。

>[!NOTE]
>
>瞭解如何存取中選件資料庫每個物件的匯出資料集 [本節](../export-catalog/access-dataset.md).

以下為可用於的所有欄位清單 **[!UICONTROL 決定物件存放庫 — 位置]** 資料集。

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

+++ 識別碼

**欄位：** _id
**標題：** 識別碼
**說明：** 紀錄的唯一識別碼。
**類型:**&#x200B;字串

+++

+++ _體驗

**欄位：** 體驗(_E)
**型別：** 物件

+++

+++ 體驗>決策(_E)

**欄位：** 決策
**型別：** 物件

+++

+++ _experience > decisioning >刊登版位的頻道識別碼

**欄位：** channelid
**標題：** 刊登版位的頻道識別碼
**說明：** 提出主張的管道。 值為有效的管道URI。 請參閱https://ns.adobe.com/xdm/channels/channel。
**類型:**&#x200B;字串

+++

+++ _experience >決策>內容元件型別

**欄位：** componenttype
**標題：** 內容元件型別
**說明：** 一組URI的列舉，其中每個值都對應到指定給內容元件的型別。 內容表示的某些消費者期望@type值是描述內容元件其他屬性的結構描述的參考。
**類型:**&#x200B;字串

+++

+++ _experience >決策>內容型別

**欄位：** contentType
**型別：** 陣列

+++

+++_體驗>決策>內容型別> MIME媒體型別

**標題：** MIME媒體型別
**說明：** 該位置中預期元件的媒體型別限制。 一個元件可能有多種媒體型別，例如不同的影像格式。
**類型:**&#x200B;字串

+++

+++ _experience >決策>位置說明

**欄位：** 說明
**標題：** 位置說明
**說明：** 它可用來傳達人類對於如何在整體訊息傳遞中使用動態內容的可讀取意圖。 特定空間是網頁中的\「橫幅\」通常透過說明傳遞，而非透過正式方法傳遞。
**類型:**&#x200B;字串

+++

+++ 體驗>決策>版位名稱(_E)

**欄位：** 名稱
**標題：** 位置名稱
**說明：** 此位置的指定名稱，可在人類互動中參照。
**類型:**&#x200B;字串

+++

+++ 存放庫(_R)

**欄位：** 存放庫(_R)
**型別：** 物件

+++

+++ _repo >版位ETag

**欄位：** etag
**標題：** 刊登ETag
**說明：** 決定選項物件拍攝快照時的修訂版本。
**類型:**&#x200B;字串

+++
