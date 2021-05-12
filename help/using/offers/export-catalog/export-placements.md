---
title: 位置資料集
description: 此區段會列出匯出資料集中用於位置的所有欄位。
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 4%

---

# 位置資料集{#placements-dataset}

每次修改選件時，就會更新位置的自動產生資料集。

![](../../assets/dataset-placements.png)

資料集中最近成功的批次會顯示在右側。 資料集的架構階層檢視會顯示在左窗格上。

>[!NOTE]
>
>瞭解如何在[本節](../export-catalog/access-dataset.md)中存取選件程式庫每個物件的匯出資料集。

以下是&#x200B;**[!UICONTROL Decision Object Repository - Placements]**&#x200B;資料集中可使用的所有欄位清單。

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## 識別碼

**欄位：** _id標
**題：識** 別碼
**說明：記** 錄的唯一識別碼。**類型:**&#x200B;字串

## _體驗

**欄位：** _experience 
**Type：物** 件

### 決策

**欄位：決** 策類
**型：物** 件

#### 位置的頻道識別碼

**欄位：** channelID
**標題：** Placement的頻道識別
**碼說明：** 提出建議的頻道。該值是有效的渠道URI。 請參閱https://ns.adobe.com/xdm/channels/channel。
**類型:**&#x200B;字串

#### 內容元件類型

**Field:** componentType 
**Title:** Content Component Type 
**Description:** 列舉的URI集，其中每個值對應至內容元件的指定類型。內容表示法的某些使用者預期@type值會是描述內容元件其他屬性之架構的參考。
**類型:**&#x200B;字串

#### contentTypes

**欄位：** contentTypes 
**Type：陣** 列

* **MIME介質類型**

   **標題：** MIME媒體類型
   **說明：** 該位置中預期元件的媒體類型限制。一個元件（例如不同的影像格式）可能有多種媒體類型。
   **類型:**&#x200B;字串

#### 位置說明

**欄位：** 說明
**標題：位置說明** 說明：
**** 它用於傳達動態內容如何用於整體訊息傳送的人類可讀意圖。網頁中的某個空間是\&quot;橫幅\&quot;，通常是透過說明傳達，而非透過正式方法。
**類型:**&#x200B;字串

#### 位置名稱

**欄位：** 名稱
**標題：位置名** 稱說明：
**** 在人類互動中參照位置的指定名稱。**類型:**&#x200B;字串

## _repo

**欄位：** _repo 
**Type:** object

### Placement ETag

**Field:** etag 
**Title:** Placement ETag 
**Description:** 拍攝快照時決策選項對象所在的修訂版。**類型:**&#x200B;字串
