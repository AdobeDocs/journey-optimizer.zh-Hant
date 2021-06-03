---
title: '開始使用優惠方案目錄匯出  '
description: 本區段列出匯出資料集中用於決策的所有欄位。
source-git-commit: 95be47fbf6944f7e6a743056b6cc29b45ae291fe
workflow-type: tm+mt
source-wordcount: '1550'
ht-degree: 3%

---

# 決策資料集{#decisions-dataset}

每次修改選件時，都會更新自動產生的決策資料集（先前稱為活動）。

![](../../assets/dataset-activities.png)

資料集中最新成功的批次資料會顯示在右側。 資料集的架構階層檢視會顯示在左窗格上。

>[!NOTE]
>
>了解如何在[本區段](../export-catalog/access-dataset.md)中存取Offer Library每個物件的匯出資料集。

以下是可在&#x200B;**[!UICONTROL Decision Object Repository - Decisions]**&#x200B;資料集中使用的所有欄位清單（舊稱「決策物件存放庫 — 活動」）。

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

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

#### _experience >決策>條件

**欄位：** 條件
**標題：** 條件
**說明：** 定義一組決策條件，其中每個條件都包含一組限制。**類型：** 陣列

**「體驗>決策>條件>說明」**

**欄位：** 說明
**標題：** 說明
**說明：** 條件說明。它用於傳達人類可讀的意圖，以了解此標準如何構建、為何構建以及如何影響決策。
**類型:**&#x200B;字串

**_experience > decisioning >條件> optionSelection**

**欄位：** 選項選
**擇標題：** 選項選
**擇說明：** 選項選擇定義此上下文中選項的有效性/適用性。**類型：** 物件

* **說明**

   **欄位：** 說明
   **標題：** 說明
   **說明：** 選項選擇說明。它用於傳達人類可讀的意圖，了解此選項選項的構建方式或原因，和/或哪個選項將匹配。
   **類型:**&#x200B;字串

* **選項篩選**

   **欄位：** 篩選
   **標題：** 選項篩選
   **說明：** 參考標籤型篩選器，此篩選器會使用其附加的標籤來比對庫存中的選項。該值是引用的決策規則的URI(@id)。 請參閱結構https://ns.adobe.com/experience/decisioning/filter。
   **類型:**&#x200B;字串

* **輪廓約束類型**

   **欄位：** optionSelectionType
   **標題：** 設定檔限制類型
   **說明：** 判斷目前是否已設定任何限制，以及限制的表達方式。可透過篩選查詢或一或多個區段成員資格進行。
   **類型:**字串
   **可能的值：** 「無」（預設值）、「directList」、「篩選」

* **選項清單**

   **欄位：** 選項
   **標題：** 選項清單
   **說明：** 無需評估篩選查詢即可直接指定選項的清單。可以指定選項清單或選項篩選規則。
   **類型：** 陣列

   <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

**「體驗>決策>條件>版位」**

**欄位：** 版位
**標題：** 版位限制
**說明：** 版位限制表示此准則僅適用於列出的版位。只有在`xdm:placements`清單中有目標放置時，才會考慮選項選擇。 否則會略過整個決策標準。 省略「xdm:placement」清單或為空時，會針對任何目標位置考量條件。 此處列出的版位會加上選項選取的隱含條件。 要考慮的選項必須具有目標位置的表示。
**類型：** 陣列

* **版位識別碼**

   **標題：** 版位識別碼
   **說明：** 版位實體的參照。該值是所引用位置的URI(@id)。 請參閱結構https://ns.adobe.com/experience/decisioning/placement。
   **類型:**&#x200B;字串

**_experience > decisioning >條件> profileConstraints**

**欄位：** profileConstraints標
**題：** 設定檔限制說
**明：** 設定檔限制會決定在此情況下，某個選項選項是否適合此設定檔身分識別。如果配置檔案約束不需要考慮每個選項的值，即選項選項中的選項是不變的，則評估為&#39;false&#39;的配置檔案約束將取消整個選項選項。 另一方面，會針對選項選取的每個限定選項，評估以選項作為參數的設定檔約束規則。
**類型：** 物件

* **_experience > decisioning >條件>設定檔限制>說明**

   **欄位：** 說明
   **標題：** 說明
   **說明：** 設定檔限制說明。它用於傳達人類可讀的意圖，了解此設定檔限制是如何建構的，或為何建構，及/或將包含或排除哪個選項。
   **類型:**&#x200B;字串

* **_experience > decisioning >條件>設定檔限制>適用性規則**

   **欄位：** apilityRule
   **標題：** 適用性規則
   **說明：** 針對指定設定檔及/或其他指定內容XDM物件，評估為true或false之決策規則的參考。規則可用來決定選項是否符合指定設定檔的資格。 該值是引用的決策規則的URI(@id)。 請參閱結構https://ns.adobe.com/experience/decisioning/rule。
   **類型:**&#x200B;字串

* **_experience > decisioning >條件>設定檔限制>設定檔限制類型**

   **欄位：** profileConstraintType
   **標題：** 設定檔限制類型
   **說明：** 判斷目前是否已設定任何限制，以及限制的表達方式。可透過規則或一或多個區段成員資格。
   **類型:**字串
   **可能的值：**
   * &quot;none&quot;（預設）
   * &quot;apilityRule&quot;:「設定檔限制會以單一規則表示，在允許限制動作之前，必須評估為true。」
   * &quot;anySegments&quot;:&quot;配置檔案約束表示為一個或多個段，並且配置檔案必須是其中至少一個段的成員，才允許執行受約束操作。&quot;
   * &quot;allSegments&quot;:&quot;配置檔案約束以一個或多個段表示，配置檔案必須是所有段的成員，才允許執行受約束操作。&quot;
   * &quot;rules&quot;:「配置檔案約束被表示為許多不同的規則，例如資格、適用性、適用性，在允許約束操作之前，所有規則都必須評估為true。」

* **_experience > decisioning >條件> profileConstraints > segmentIdentities**

   **欄位：** segmentIdentities
   **標題：** 區段識別碼
   **說明：** 區段的識別碼。
   **類型：** 陣列

   * **識別碼**

      **欄位：** _id
      **標題：** 識別碼
      **說明：** 相關命名空間中區段的身分。
      **類型:**&#x200B;字串

   * **namespace**

      **欄位：** 命名空間
      **標題：** 命名空間
      **說明：** 與屬性相關聯的命 `xid` 名空間。
      **類型：** 物件
      **必要：**  &quot;code&quot;

      * **程式碼**

         **欄位：** 程式碼
         **標題：** 程式碼
         **說明：** 程式碼是人類看得懂的命名空間識別碼，可用來要求用於身分圖表處理的技術命名空間ID。
         **類型:**&#x200B;字串
   * **體驗識別碼**

      **欄位：** xid
      **標題：** 體驗識別碼
      **說明：** 如果存在，此值代表跨命名空間識別碼，在所有命名空間中所有命名空間範圍的識別碼中都是唯一的。
      **類型:**&#x200B;字串


**「體驗>決策>條件>排名」**

**欄位：** 排名
**標題：** 排名詳細資料
**說明：** 排名（優先順序）。定義在決策准則的內容下，如何判斷「最佳選項」。 在符合設定檔限制的所有選取選項中，排名將決定要建議的前N個選項。
**類型：** 物件

* **「體驗>決策>條件>排名」**

   **欄位：** 順序
   **標題：** 訂單評估
   **說明：** 評估一或多個決策選項的相對順序。對於具有較低序數值的任何選項，都會選擇具有較高序數值的選項。 該方法確定的值可以排序，但它們之間的距離不能測量，且不能計算和或積。 中值和模式是唯一可用於序數資料的中心趨勢度量。
   **類型：** 物件

   * **計分函式**

      **欄位：** 函式
      **標題：** 計分函式
      **說明：** 計算此決策選項之數值分數之函式的參考。然後，決策選項將依該分數排序（排名）。 此屬性的值是一次使用on選項調用的函式的URI(@id)。 請參閱結構https://ns.adobe.com/experience/decisioning/function。
      **類型:**&#x200B;字串

   * **訂單評估類型**

      **欄位：** orderEvaluationType
      **標題：** 訂單評估類型
      **說明：** 指定使用的訂單評估機制、決策選項的靜態優先順序、計算每個選項的數值的評分函式，或接收要訂購清單的排名策略。
      **類型:**字串
      **可能的值：** 「static」、「scoringFunction」、「rankingStrategy」

   * **排名策略**

      **欄位：** rankingStrategy
      **標題：** 排名策略
      **說明：** 對決策選項清單進行排名之策略的參考。決策選項將以有序清單返回。 此屬性的值是一次使用on選項調用的函式的URI(@id)。 請參閱結構https://ns.adobe.com/experience/decisioning/rankingStrategy。
      **類型:**&#x200B;字串

* **_experience > decisioning >條件>排名>優先順序**

   **欄位：** 優先順序
   **標題：** 優先順序
   **說明：** 單一決策選項相對於所有其他選項的優先順序。使用此屬性會排定不提供訂單函式的選項優先順序。 優先順序值較高的選項將優先於任何優先順序較低的選項。 如果兩個或多個合格期權具有最高優先順序值，則以統一隨機選擇一個期權並用於決策主張。
   **類型：** 整數
   **最小值：** 0
   **預設值：** 0

#### _experience > decisioning >活動結束日期和時間

**欄位：** endTime
**標題：** 活動結束日期和時間
**說明：** 決策（舊稱活動）結束日期和結束時間。該屬性具有schema.org在http://schema.org/Action上定義的「endTime」屬性的語義。
**類型:**&#x200B;字串

#### _experience >決策>備援選項

**欄位：** 後援
**標題：** 後援選項
**說明：** 在此決策中做出決策時，所使用的後援選項的參考不會符合任何一般選項（通常是在套用硬式限制時發生）。該值是引用的備援選項的URI(@id)。
**類型:**&#x200B;字串

#### _experience > decisioning >活動名稱

**欄位：** 名稱
**標題：** 活動名稱
**說明：** 顯示在各種使用者介面中的決策（舊稱活動）名稱。**類型:**&#x200B;字串

#### _experience > decisioning >活動開始日期和時間

**欄位：** startTime 
**Title:** 活動開始日期和時間
**說明：** 決策（舊稱為活動）開始日期和結束時間。該屬性在http://schema.org/Action上定義了schema.org的「startTime」屬性的語義。
**類型:**&#x200B;字串

## _repo

**欄位：** _repo 
**類型：** 物件

### _repo > Activity ETag

**欄位：** etag 
**標題：** 活動ETag
**說明：** 建立快照時決策（舊稱活動）物件所在的修訂。**類型:**&#x200B;字串
