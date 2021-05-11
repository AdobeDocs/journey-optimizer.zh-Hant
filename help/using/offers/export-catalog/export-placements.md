---
title: 位置資料集
description: 此區段會列出匯出資料集中用於位置的所有欄位。
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 4%

---

# 位置資料集{#placements-dataset}

每次修改選件時，就會更新位置的自動產生資料集。

![](../assets/dataset-placements.png)

資料集中最近成功的批次會顯示在右側。 資料集的架構階層檢視會顯示在左窗格上。

>[!NOTE]
>
>瞭解如何在[本節](../export-catalog/access-dataset.md)中存取選件程式庫每個物件的匯出資料集。

位置描述個人化訊息中的位置或位置。 它用於為個人化決策提供的內容設定技術限制。 位置也代表當產生涉及此位置的體驗事件時，產生特定類型量度的請求。 例如，該位置有助於向最終用戶顯示的電子郵件中的個人化可點選影像。 例如，位置可能會要求組合體驗在體驗事件中報告點按其影像的要求，其度量為https://ns.adobe.com/xdm/data/metrics/web/linkclicks，並參考此位置。

以下是&#x200B;**[!UICONTROL Decision Object Repository - Placements]**&#x200B;資料集中可使用的所有欄位清單。

## 識別碼

記錄的唯一識別碼。

類型: 字串

## _體驗

### 決策

#### 位置的頻道識別碼

提出建議的渠道。 該值是有效的渠道URI。 請參閱https://ns.adobe.com/xdm/channels/channel。

類型: 字串

#### 內容元件類型

列舉的URI集，其中每個值對應至指定給內容元件的類型。 內容表示法的某些使用者預期@type值會是描述內容元件其他屬性之架構的參考。

類型: 字串

#### MIME介質類型

該位置中預期元件的介質類型的約束。 一個元件（例如不同的影像格式）可能有多種媒體類型。

類型: 字串

#### 位置說明

它用於傳達動態內容在整體訊息傳遞中的使用方式，以傳達人類可讀的意圖。 網頁中的某個空間是\&quot;橫幅\&quot;，通常是透過說明傳達，而非透過正式方法。

類型: 字串

#### 位置名稱

在人類互動中參照位置的指定名稱。

類型: 字串

## _repo

### Placement ETag

拍攝快照時決策選項對象所在的修訂版本。

類型: 字串
