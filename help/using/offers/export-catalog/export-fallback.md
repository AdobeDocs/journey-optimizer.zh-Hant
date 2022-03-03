---
title: 回退提供資料集
description: 此部分列出導出資料集中用於回退聘用的所有欄位
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 14ab70aa32f4f7978b8c72b3981d3b55f56fd08b
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 3%

---

# 回退提供資料集 {#fallback-dataset}

每次修改優惠時，更新自動生成的備用優惠資料集。

![](../assets/dataset-fallback.png)

資料集中最近成功的批處理顯示在右側。 資料集的架構的分層視圖顯示在左窗格中。

>[!NOTE]
>
>瞭解如何訪問中提供庫的每個對象的導出資料集 [此部分](../export-catalog/access-dataset.md)。

下面是可在 **[!UICONTROL Decision Object Repository - Fallback Offers]** 資料集。

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

#### 經驗>決策>特性

**欄位：** 特徵
**標題：** 決策選項特徵
**描述：** 屬於此特定決策選項的其他屬性或屬性。 不同的實例可以具有不同的特徵（映射中的鍵）。 這些特徵是用於區分一個決策選項和其他決策選項的名稱值對。 特徵用作表示此決策選項的內容中的值，並用作分析和優化選項效能的特徵。 當每個實例具有相同的屬性或屬性時，應將該方面建模為從決策選項詳細資訊派生的擴展架構。
**類型：** 對象

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### 經驗>決定>內容

**欄位：** 內容
**標題：** 內容詳細資訊
**描述：** 內容項，用於在不同上下文中呈現決策項。 單個決策選項可以具有多個內容變型。 內容是指面向受眾的資訊，以便在（數字）體驗中消費。 內容通過渠道被遞送到特定的位置。
**類型：** 陣列

**經驗>決定>內容>元件**

**欄位：** 元件
**描述：** 代表決策選項的內容的元件，包括其所有語言變體。 通過「dx:format」、「dc:subject」和「dc:language」或其組合找到特定元件。 此元資料用於定位或表示與要約相關聯的內容並根據放置合同將其整合。
**類型：** 陣列
**必需：** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience >決定>內容>元件>內容元件類型**

   **欄位：** 類型
   **標題：** 內容元件類型
   **描述：** 枚舉的一組URI，其中每個值映射到給定給內容元件的類型。 內容表示的一些使用者希望@type值是對描述內容元件附加屬性的架構的引用。
   **類型:**&#x200B;字串

* **經驗>決定>內容>元件>dc**

   **欄位：** _dc
   **類型：** 對象
   **必需：** &quot;格式&quot;

   * **格式**

      **欄位：** 格式
      **標題：** 格式
      **描述：** 資源的物理或數字表示。 通常，格式應包括資源的媒體類型。 可使用格式來確定顯示或操作資源所需的軟體、硬體或其它設備。 建議的最佳做法是從受控辭彙中選擇一個值(例如， [Internet媒體類型](http://www.iana.org/ assignments/media-types/)定義電腦媒體格式。
      **類型:**字串
      **示例：** &quot;application/vnd.adobe.photoshop&quot;

   * **語言**

      **欄位：** 語言
      **標題：** 語言
      **描述：** 資源的語言或語言。 \n語言是在定義的語言代碼中指定的 [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)BCP47的一部分，在XDM的其他部分使用。
      **類型：** 陣列
      **示例：** &quot;\n&quot;、&quot;pt-BR&quot;、&quot;es-ES&quot;

* **經驗>決定>內容>元件>回收**

   **欄位：** _repo
   **類型：** 對象

   * **id**

      **欄位：** ID
      **描述：** 用於引用內容儲存庫中資產的可選唯一標識符。 當使用平台API來檢索表示法時，客戶端可以期望有附加屬性\&quot;repo:resolveUrl\&quot;來檢索資產。
      **類型:**字串
      **示例：** 「urn」:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **名稱**

      **欄位：** 名稱
      **描述：** 有關通過「repo:id\」在何處查找儲存外部資產的儲存庫的一些提示。
      **類型:**&#x200B;字串

   * **資料庫ID**

      **欄位：** 資料庫ID
      **描述：** 用於引用內容儲存庫中資產的可選唯一標識符。 當使用平台API來檢索表示法時，客戶端可以期望有附加屬性\&quot;repo:resolveUrl\&quot;來檢索資產。
      **類型:**字串
      **示例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **解析URL**

      **欄位：** 解析URL
      **描述：** 用於在內容儲存庫中讀取資產的可選唯一資源定位器。 這樣，在客戶不瞭解資產管理位置和要調用的API的情況下，獲取資產就更容易了。 這類似於HAL連結，但語義更簡單、更有針對性。
      **類型:**字串
      **示例：** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **體驗>決定>內容>元件>內容**

   **欄位：** 內容
   **描述：** 可選欄位，用於直接保存內容。 該元件可以直接保存簡單內容，而不是引用資產儲存庫中的內容。 此欄位不用於複合、複雜和二進位內容資產。
   **類型:**&#x200B;字串

* **_experience >決策>內容>元件>交付URL**

   **欄位：** 傳遞URL
   **描述：** 從內容傳送網路或服務端點獲取資產的可選唯一資源定位器。 此URL用於由用戶代理公開訪問資產。
   **類型:**字串
   **示例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience >決策>內容>元件>連結URL**

   **欄位：** 連結URL
   **描述：** 用於用戶交互的可選唯一資源定位器。 此URL用於將最終用戶引用到用戶代理中，並可以進行跟蹤。
   **類型:**字串
   **示例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_experience >決策>內容>放置**

**欄位：** 放置
**標題：** 放置
**描述：** 要遵守的位置。 該值是引用的要約放置的URI(@id)。 請參見架構https://ns.adobe.com/experience/decisioning/placement。
**類型:**&#x200B;字串

#### 體驗>決策>生命週期狀態(_E)

**欄位：** 生命週期狀態
**標題：** 生命週期狀態
**描述：** 生命週期狀態允許使用對象執行工作流。 該狀態可能會影響對象可見或被視為相關的位置。 狀態更改由使用對象的客戶端或服務驅動。
**類型：** 字串
**可能的值：** &quot;草稿&quot;（預設）、&quot;已批准&quot;、&quot;即時&quot;、&quot;已完成&quot;、&quot;已存檔&quot;

#### _experience >決策>決策選項名稱

**欄位：** 名稱
**標題：** 決策選項名稱
**描述：** 顯示在各種用戶介面中的選項名稱。
**類型:**&#x200B;字串

#### 體驗>決定>標籤

**欄位：** 標籤
**標題：** 標籤
**描述：** 與此實體關聯的標籤集。 標籤用於篩選表達式中，以將整體清單限制為子集（類別）。
**類型：** 陣列

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo {#repo}

**欄位：** _repo
**類型：** 對象

### _repo >決策選項ETag

**欄位：** etag
**標題：** 決策選項ETag
**描述：** 拍攝快照時決策選項對象所在的修訂版本。
**類型:**&#x200B;字串
