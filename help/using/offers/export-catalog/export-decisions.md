---
title: '開始使用優惠目錄匯出  '
description: 此部分列出導出資料集中用於決策的所有欄位
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1550'
ht-degree: 3%

---

# 決定資料集 {#decisions-dataset}

每次修改提供時，更新自動生成的決策資料集（以前稱為活動）。

![](../assets/dataset-activities.png)

資料集中最近成功的批處理顯示在右側。 資料集的架構的分層視圖顯示在左窗格中。

>[!NOTE]
>
>瞭解如何訪問中提供庫的每個對象的導出資料集 [此部分](../export-catalog/access-dataset.md)。

下面是可在 **[!UICONTROL Decision Object Repository - Decisions]** 資料集（以前稱為Decision Object Repository - Activities）。

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

## 識別碼 {#identifier}

**Field:** _id
**Title:** Identifier
**Description:** A unique identifier for the record.
**類型:**&#x200B;字串

## _體驗 {#experience}

**欄位：** 體驗
**類型：** 對象

### 經驗>決策

**欄位：** 決定
**類型：** 對象

#### 經驗>決策>條件

**欄位：** 標準
**標題：** 標準
**描述：** 定義一組決策標準，其中每個標準都包含一組約束。
**類型：** 陣列

**經驗>決定>條件>說明**

**欄位：** 描述
**標題：** 說明
**描述：** 條件說明。 它用於傳達人類可讀的意圖，說明如何構建或為什麼構建此標準以及它如何影響決策。
**類型:**&#x200B;字串

**_experience >決策>條件>選項選擇**

**欄位：** 選項選擇
**標題：** 選項選擇
**描述：** 選項選擇定義選項在此上下文中的有效性/適用性。
**類型：** 對象

* **說明**

   **Field:** description
   **標題：** 說明
   **描述：** 選項選擇說明。 它用於傳達人類可讀的意圖，說明如何構建此選項選擇和/或將匹配哪些選項。
   **類型:**&#x200B;字串

* **選項篩選器**

   **欄位：** 濾波器
   **標題：** 選項篩選器
   **描述：** 對基於標籤的篩選器的引用，該篩選器使用其附加的標籤匹配庫存中的選項。 The value is the URI (@id) of the decision rule that is referenced. 請參見架構https://ns.adobe.com/experience/decisioning/filter。
   **類型:**&#x200B;字串

* **配置檔案約束類型**

   **欄位：** 選項SelectionType
   **Title:** Profile Constraint Type
   **Description:** Determines if any constraints are currently set and how the constraints are expressed. 它可以通過篩選器查詢或通過一個或多個段成員身份。
   **類型:**字串
   **Possible values:** &quot;none&quot; (default), &quot;directList&quot;, &quot;filter&quot;

* **選項清單**

   **欄位：** 選項
   **Title:** Option List
   **Description:** A list that directly specifies the options without evaluating a filter query. Either an option list or an option filter rule can be specified.
   **類型：** 陣列

   <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

**經驗>決定>條件>放置**

**欄位：** 植入
**標題：** 放置限制
**描述：** 放置約束表示此條件僅適用於列出的放置。 僅當目標放置位於 `xdm:placements` 清單是所考慮的選項選擇。 否則，將跳過整個決策標準。 當省略或空「xdm:placements」清單時，將考慮任何目標放置的條件。 此處列出的位置為選項選擇強加隱式條件。 An option to be considered must have a representation for the targeted placement.
**類型：** 陣列

* **放置標識符**

   **標題：** 放置標識符
   **描述：** 對放置圖元的參照。 The value is the URI (@id) of the placement that is referenced. 請參見架構https://ns.adobe.com/experience/decisioning/placement。
   **類型:**&#x200B;字串

**_experience >決策>條件>配置檔案約束**

**Field:** profileConstraints
**Title:** Profile Constraint
**Description:** The profile constraint decides if an option selection is eligible for this profile identity at this moment, in this context. If the profile constraint does not need to consider values of each of the option, i.e. it is invariant of the options from the option selection, the profile constraint that evaluates to &#39;false&#39; cancels out the entire option selection. 另一方面，將選項作為參數的配置檔案約束規則會針對選項選擇的每個限定選項進行評估。
**Type:** object

* **_experience >確定>條件>配置檔案約束>說明**

   **Field:** description
   **Title:** Description
   **描述：** 配置檔案約束描述。 它用於傳達人類可讀的意圖，說明如何構建此配置檔案約束和/或該約束將包含或排除哪些選項。
   **類型:**&#x200B;字串

* **_experience >決策>標準>配置檔案約束>資格規則**

   **欄位：** 資格規則
   **標題：** 資格規則
   **描述：** 對給定配置檔案和/或其它給定上下文XDM對象的判定規則的引用，該判定規則計算為true或false。 該規則用於確定該選項是否符合給定配置檔案的條件。 該值是引用的決策規則的URI(@id)。 See schema https://ns.adobe.com/experience/decisioning/rule.
   **類型:**&#x200B;字串

* **_experience >確定>條件>配置檔案約束>配置檔案約束類型**

   **欄位：** profileConstraintType
   **標題：** 配置檔案約束類型
   **描述：** 確定當前是否設定了任何約束以及如何表示約束。 它可通過規則或通過一個或多個段成員身份。
   **類型:**字串
   **可能的值：**
   * &quot;無&quot;（預設）
   * &quot;資格規則&quot;:&quot;配置檔案約束表示為一個規則，在允許約束操作之前，必須計算為true。&quot;
   * &quot;anySegments&quot;:「配置檔案約束被表示為一個或多個段，在允許約束操作之前，配置檔案必須是其中至少一個段的成員。」
   * &quot;所有段&quot;:「配置檔案約束表示為一個或多個段，並且配置檔案必須是所有段的成員，然後才能允許約束操作。」
   * &quot;rules&quot;: &quot;The profile constraint is expressed as a number of different rules, e.g. eligibility, applicability, suitability, which all must evaluate to true before the constrained action is allowed.&quot;

* **_experience >決策>條件>配置檔案約束>段標識**

   **欄位：** 段標識
   **標題：** 段標識符
   **描述：** 段的標識符。
   **Type:** array

   * **識別碼**

      **Field:** _id
      **標題：** 標識符
      **描述：** 相關命名空間中段的標識。
      **類型:**&#x200B;字串

   * **namespace**

      **Field:** namespace
      **Title:** Namespace
      **Description:** The namespace associated with the `xid` attribute.
      **Type:** object
      **必需：** &quot;代碼&quot;

      * **程式碼**

         **Field:** code
         **標題：** 代碼
         **描述：** 該代碼是命名空間的可讀標識符，可用於請求用於標識圖形處理的技術命名空間ID。
         **類型:**&#x200B;字串
   * **體驗標識符**

      **Field:** xid
      **標題：** 體驗標識符
      **描述：** 當存在時，此值表示跨命名空間標識符，該標識符在所有命名空間中所有命名空間範圍內的標識符之間都是唯一的。
      **類型:**&#x200B;字串


**_experience > decisioning > criteria > ranking**

**欄位：** 排名
**標題：** 排名詳細資訊
**描述：** 等級（優先順序）。 定義給定決策標準的上下文如何確定「最佳選項\」。 Among all the selected options that meet the profile constraints, the ranking will decide the top (or top N) option(s) to be proposed.
**Type:** object

* **_experience > decisioning > criteria > ranking > order**

   **欄位：** 訂單
   **標題：** 訂單評估
   **Description:** Evaluation of a relative order of one or more decision options. 在具有較低序號值的任何選項上選擇具有較高序號值的選項。 The values determined by this method can be ordered but distances between them cannot be measured and neither can sums nor products be calculated. 中值和模式是唯一可用於有序資料的中心趨勢度量。
   **類型：** 對象

   * **評分函式**

      **Field:** function
      **標題：** 評分函式
      **Description:** A reference to a function that computes a numerical score for this decision option. 然後，將按該分數對決策選項進行排序（排序）。 此屬性的值是一次使用on選項調用的函式的URI(@id)。 請參見架構https://ns.adobe.com/experience/decisioning/function。
      **類型:**&#x200B;字串

   * **訂單評估類型**

      **欄位：** orderEvaluationType
      **標題：** 訂單評估類型
      **描述：** 指定使用哪個排序評估機制、決策選項的靜態優先順序、計算每個選項的數值的評分函式或接收清單對其排序的排序策略。
      **類型:**字串
      **可能的值：** &quot;static&quot;、&quot;scoringFunction&quot;、&quot;rankingStrategy&quot;

   * **排名策略**

      **欄位：** 排名策略
      **標題：** 排名策略
      **描述：** 對對決策選項清單進行排序的策略的引用。 決策選項將在有序清單中返回。 此屬性的值是一次使用on選項調用的函式的URI(@id)。 請參見架構https://ns.adobe.com/experience/decisioning/rankingStrategy。
      **類型:**&#x200B;字串

* **經驗>決策>標準>排名>優先順序**

   **欄位：** 優先順序
   **標題：** 優先順序
   **描述：** 單個決策選項相對於所有其他選項的優先順序。 沒有為其提供訂單函式的選項使用此屬性優先化。 優先順序值較高的選項在任何優先順序較低的選項之前被選中。 如果兩個或多個合格期權共用最高優先順序值，則以統一隨機方式選擇其中一個期權並用於決策命題。
   **Type:** integer
   **最小值：** 0
   **Default value:** 0

#### _experience > decisioning > Activity End Date and Time

**欄位：** 結束時間
**標題：** 活動結束日期和時間
**描述：** 決定（以前稱為活動）結束日期和結束時間。 該屬性在http://schema.org/Action上定義了schema.org的「endTime」屬性的語義。
**類型:**&#x200B;字串

#### _experience >決策>回退選項

**欄位：** 回退
**標題：** 回退選項
**描述：** 對回退選項的引用在此決策的上下文中進行決策時使用，但不會限定任何常規選項（通常在應用硬約束時發生這種情況）。 該值是引用的回退選項的URI(@id)。
**類型:**&#x200B;字串

#### 經驗>決策>活動名稱(_E)

**欄位：** 名稱
**標題：** 活動名稱
**描述：** 顯示在各種用戶介面中的決策（以前稱為活動）名稱。
**類型:**&#x200B;字串

#### _experience >決策>活動開始日期和時間

**欄位：** 開始時間
**標題：** 活動開始日期和時間
**描述：** 決定（以前稱為活動）開始日期和結束時間。 該屬性在http://schema.org/Action上定義了schema.org的「startTime」屬性的語義。
**類型:**&#x200B;字串

## _repo {#repo}

**欄位：** _repo
**類型：** 對象

### _repo >活動ETag

**欄位：** etag
**標題：** 活動ETag
**描述：** 拍攝快照時決策（以前稱為活動）對象所在的修訂版本。
**類型:**&#x200B;字串
