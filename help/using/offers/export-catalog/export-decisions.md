---
title: '開始使用優惠方案目錄匯出  '
description: 本節列出匯出資料集中用於決策的所有欄位。
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '1483'
ht-degree: 3%

---

# 決策資料集{#decisions-dataset}

每次修改選件時，就會更新自動產生的決策資料集。

![](../../assets/dataset-activities.png)

資料集中最近成功的批次會顯示在右側。 資料集的架構階層檢視會顯示在左窗格上。

>[!NOTE]
>
>瞭解如何在[本節](../export-catalog/access-dataset.md)中存取選件程式庫每個物件的匯出資料集。

以下是&#x200B;**[!UICONTROL Decision Object Repository - Decisions]**&#x200B;資料集（先前稱為Decision Object Repository - Activities）中可使用的所有欄位清單。

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

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

#### 准則

**欄位：** 條件
**標題：條** 件說明：
**** 定義一組決策標準，每個標準都包含一組約束。**類型：陣** 列

* **描述**

   **欄位：說** 明
   **標題：說** 明
   **說明：** 准則說明。它用於傳達人類可讀意圖，以瞭解如何構建或為何構建此標準以及它如何影響決策。
   **類型:**&#x200B;字串

* **選項選擇**

   **欄位：選** 項選擇
   **標題：選** 項選擇
   **說明：選** 項選擇定義了選項在此上下文中的有效性／適用性。
   **類型：對** 像

   * **說明**

      **欄位：說** 明
      **標題：說** 明
      **說明：選** 項選擇說明。它用於傳達人類可讀意圖，瞭解如何或為何構建此選項選擇和／或哪個選項匹配。
      **類型:**&#x200B;字串

   * **選項篩選**

      **欄位：篩** 選
      **標題：選** 項篩選
      **說明：** 對基於標籤的篩選器的參考，該篩選器使用其附加的標籤來比對庫存的選項。該值是所引用決策規則的URI(@id)。 請參閱架構https://ns.adobe.com/experience/decisioning/filter。
      **類型:**&#x200B;字串

   * **描述檔約束類型**

      **欄位：** optionSelectionType
      **標題：描** 述檔約束類型
      **說明：** 確定當前是否設定了約束以及約束的表達方式。它可透過篩選查詢或一或多個區段成員資格。
      **類型:**字串
      **可能的值：** &quot;directList&quot;、&quot;filter&quot;
      **預設值：** 「無」

   * **選項清單**

      **欄位：選** 項
      **標題：選** 項清單
      **說明：** 直接指定選項而不評估篩選查詢的清單。可以指定選項清單或選項篩選規則。
      **類型：陣** 列

      <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

* **位置**

   **欄位：位** 置
   **標題：位** 置限制
   **說明：** 放置約束表示此准則僅適用於列出的位置。只有當目標位置位於`xdm:placements`清單中時，才會考慮選項選擇。 否則，將跳過整個決策標準。 當省略或空白「xdm:lactions」清單時，任何定位的位置都會考慮標準。 此處列出的位置會為選項選擇加上隱含標準。 要考慮的選項必須具有目標放置的表示法。
   **類型：陣** 列

   * **位置識別碼**

   **標題：位** 置識別碼
   **說明：** 放置圖元的參考。該值是所引用位置的URI(@id)。 請參閱架構https://ns.adobe.com/experience/decisioning/placement。
   **類型:**&#x200B;字串

* **profileConstraints**

   **欄位：** profileConstraints
   **標題：描** 述檔約束
   **說明：** 描述檔約束會決定此時，在此上下文中，某個選項選擇是否適合此描述檔身份。如果描述檔約束不需要考慮每個選項的值，即選項選擇中的選項不變，則評估為&#39;false&#39;的描述檔約束會取消整個選項選擇。 另一方面，系統會針對選項選擇的每個限定選項評估以選項作為參數的配置檔案約束規則。
   **類型：對** 像

   * **說明**

      **欄位：說** 明
      **標題：說** 明
      **說明：描** 述檔約束說明。它用於傳達人類可讀意圖，瞭解如何或為何構建此配置檔案約束和／或該約束將包含或排除哪個選項。
      **類型:**&#x200B;字串

   * **資格規則**

      **欄位：資格** 規則
      **標題：資** 格規則
      **說明：** 對於特定描述檔和／或其他特定上下文XDM物件，評估為true或false之決策規則的參考。此規則用於決定選項是否符合指定描述檔的資格。 該值是所引用決策規則的URI(@id)。 請參閱架構https://ns.adobe.com/experience/decisioning/rule。
      **類型:**&#x200B;字串

   * **描述檔約束類型**

      **欄位：** profileConstraintType
      **標題：描** 述檔約束類型
      **說明：** 確定當前是否設定了約束以及約束的表達方式。可透過規則或一或多個區段成員資格進行。
      **類型:**字串
      **可能的值：**
      * &quot;無&quot;
      * &quot;agilibilityRule&quot;:「描述檔約束表示為單一規則，必須在允許限制動作前評估為true。」
      * &quot;anySegments&quot;:「描述檔約束表示為一或多個區段，且描述檔必須是其中至少一個區段的成員，才能允許受約束動作。」
      * &quot;allSegments&quot;:「描述檔約束表示為一或多個區段，且描述檔必須是所有區段的成員，才能允許受約束動作。」
      * 「規則」:「描述檔約束是以多種不同的規則來表示，例如資格、適用性、適用性，所有規則都必須在允許限制動作前評估為true。」
         **預設值：** 「無」
   * **區段識別碼**

      **欄位：** segmentIdentities
      **標題：區** 段識別碼
      **說明：** 區段的識別碼。
      **類型：陣** 列

      * **識別碼**

         **欄位：** _id
         **標題：識** 別碼
         **說明：** 相關命名空間中區段的識別。
         **類型:**&#x200B;字串

      * **命名空間**

         **欄位：命名** 空間
         **標題：命名** 空間
         **說明：** 與屬性關聯的命名 `xid` 空間。
         **類型：對** 像
         **必要：** 「程式碼」

         * **程式碼**

            **欄位：程** 式碼
            **標題：程** 式碼
            **說明：** 代碼是名稱空間的人類可讀識別碼，可用來請求用於身份圖形處理的技術名稱空間ID。
            **類型:**&#x200B;字串
      * **體驗識別碼**

         **欄位：** xid
         **標題：體** 驗識別碼
         **說明：** 當存在時，此值表示跨名稱空間標識符，該標識符在所有名稱空間中的所有命名空間範圍內標識符中都是唯一的。
         **類型:**&#x200B;字串



* **排名**

   **欄位：排** 名
   **標題：排名** 詳細資訊
   **說明：** 排名（優先順序）。定義在決策標準的上下文下如何確定\&quot;最佳選項\&quot;。 在符合描述檔約束的所有選取選項中，排名將決定要建議的頂端（或前N個）選項。
   **類型：對** 像

   * **訂單**

      **欄位：順** 序
      **標題：訂** 單評估
      **說明：** 評估一或多個決策選項的相對順序。對於具有較低序數值的任何選項，都會選擇具有較高序數值的選項。 該方法所確定的值可以排序，但是它們之間的距離不能測量，且不能求和或求積。 中值和模式是唯一可用於順序資料的中心趨勢度量。
      **類型：對** 像

      * **計分函式**

         **欄位：函** 數
         **標題：計** 分函式
         **說明：** 計算此決策選項數值分數的函式的參考。然後，將依該分數排序（排名）決策選項。 此屬性的值是一次使用on選項調用的函式的URI(@id)。 請參閱架構https://ns.adobe.com/experience/decisioning/function。
         **類型:**&#x200B;字串

      * **訂單評估類型**

         **欄位：** orderEvaluationType
         **標題：訂** 單評估類型
         **說明：** 指定使用哪種訂單評估機制、決策選項的靜態優先順序、計算每個選項的數值的評分函式或接收排序清單的排名策略。
         **類型:**字串
         **可能的值：** 「static」、「scoringFunction」、「rankingStrategy」

      * **排名策略**

         **欄位：** rankingStrategy
         **標題：排** 名策略
         **說明：** 對決策選項清單排名的策略的參考。決策選項將在有序清單中返回。 此屬性的值是一次使用on選項調用的函式的URI(@id)。 請參閱架構https://ns.adobe.com/experience/decisioning/rankingStrategy。
         **類型:**&#x200B;字串
   * **優先順序**

      **欄位：優** 先
      **標題：優** 先順序
      **說明：** 單一決策選項相對於所有其他選項的優先順序。使用此屬性，不提供訂單函式的選項會排定優先順序。 優先順序值較高的選項會在任何優先順序較低的選項之前選取。 如果兩個或兩個以上符合資格的期權具有最高的優先順序值，則會以一致的隨機方式選擇一個期權，用於決策建議。
      **類型：整** 數
      **最小值：** 0
      **預設值：** 0


#### 活動結束日期和時間

**欄位：** endTime標
**題：活** 動結束日期和時間
**說明：** 決定結束日期和結束時間。該屬性在http://schema.org/Action上定義schema.org&#39;endTime&#39;屬性的語義。
**類型:**&#x200B;字串

#### 備援選項

**欄位：備** 援
**標題：備援選** 項說明：
**** 在此決策中進行決策時所使用的備援選項參考，不會限定任何一般選項（通常在套用硬式限制時發生）。該值是引用的備援選項的URI(@id)。
**類型:**&#x200B;字串

#### 活動名稱

**欄位：** 名稱
**標題：活動名** 稱說明：
**** 顯示於各種使用者介面中的決策名稱。**類型:**&#x200B;字串

#### 活動開始日期和時間

**欄位：** startTime 
**Title:** Activity Start Date and Time 
**Description:** Decision start date and end time.該屬性在http://schema.org/Action上定義schema.org的&#39;startTime&#39;屬性的語義。
**類型:**&#x200B;字串

## _repo

**欄位：** _repo 
**Type:** object

### Activity ETag

**Field:** etag 
**Title:** Activity 
**Etag Description:** 拍攝快照時決策對象所在的修訂版。**類型:**&#x200B;字串
