---
title: 決定資料集
description: 本節列出用於決策的匯出資料集中的所有欄位
badge: label="舊版" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '1530'
ht-degree: 0%

---

# 決定資料集 {#decisions-dataset}

每次修改優惠時，都會更新自動產生的決定資料集。

![](../assets/dataset-activities.png)

資料集中最近成功的批次會顯示在右側。 資料集的結構描述階層檢視會顯示在左窗格中。

>[!NOTE]
>
>在[本節](../export-catalog/access-dataset.md)中瞭解如何存取選件資料庫中每個物件的匯出資料集。

以下是可以在&#x200B;**[!UICONTROL 決定物件存放庫 — 決定]**&#x200B;資料集（以前稱為決定物件存放庫 — 活動）中使用的所有欄位清單。

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

+++ 識別碼

**欄位：** _id
**標題：**&#x200B;識別碼
**描述：**&#x200B;記錄的唯一識別碼。
**型別：**&#x200B;字串

+++

+++ 體驗(_E)

**欄位：**&#x200B;體驗(_E)
**型別：**&#x200B;物件

+++

+++ 體驗>決策(_E)

**欄位：**&#x200B;決策
**型別：**&#x200B;物件

+++

+++ _experience >決策>條件

**欄位：**&#x200B;條件
**標題：**&#x200B;條件
**描述：**&#x200B;定義一組決定條件，每個條件都包含一組條件約束。
**型別：**&#x200B;陣列

+++

+++ _experience >決策>條件>說明

**欄位：**&#x200B;描述
**標題：**&#x200B;描述
**描述：**&#x200B;條件描述。 它可用來傳達人類可讀取的意圖，指出如何或為何建構此標準，以及此標準如何影響決策。
**型別：**&#x200B;字串

+++

+++_experience > decisioning >條件> optionSelection

**欄位：**&#x200B;選項選取
**標題：**&#x200B;選項選擇
**描述：**&#x200B;選項選取範圍定義此內容中選項的有效性/適用性。
**型別：**&#x200B;物件

* 說明

  **欄位：**&#x200B;描述
  **標題：**&#x200B;描述
  **描述：**&#x200B;選項選擇描述。 它可用來傳達人類可讀取的意圖，指出如何或為何建構此選項選擇，以及/或哪些選項將相符。
  **型別：**&#x200B;字串

* 選項篩選器

  **欄位：**&#x200B;篩選器
  **標題：**&#x200B;選項篩選器
  **說明：**&#x200B;參考以集合限定詞（先前稱為「標籤」）為基礎的篩選器，該篩選器使用附加的集合限定詞來比對來自詳細目錄的選項。 該值是被參考的決策規則的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/filter 。
  **型別：**&#x200B;字串

* 設定檔限制型別

  **欄位：** optionSelectionType
  **標題：**&#x200B;設定檔限制型別
  **描述：**&#x200B;決定目前是否設定任何條件約束，以及條件約束的表示方式。 可透過篩選查詢或一或多個對象成員資格進行。
  **型別：**&#x200B;字串
  **可能的值：** 「無」（預設）、「directList」、「篩選」

* 選項清單

  **欄位：**&#x200B;選項
  **標題：**&#x200B;選項清單
  **描述：**&#x200B;直接指定選項而不評估篩選查詢的清單。 可以指定選項清單或選項篩選規則。
  **型別：**&#x200B;陣列

<!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

+++

+++_experience >決策>條件>位置

**欄位：**&#x200B;位置
**標題：**&#x200B;位置限制
**說明：**&#x200B;位置限制指出此條件僅適用於列出的位置。 只有當目標位置在`xdm:placements`清單中時，才會考慮選項選擇。 否則，將跳過整個決定條件。 當&#39;xdm:placements&#39;清單被省略或為空白時，任何目標位置都會考量此條件。 此處列出的版位會強制套用選項選取的隱含條件。 要考慮的選項必須有目標位置的表示。
**型別：**&#x200B;陣列

* 位置識別碼

  **標題：**&#x200B;位置識別碼
  **描述：**&#x200B;位置實體的參考。 該值是被參考之位置的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/placement 。
  **型別：**&#x200B;字串

+++

+++_experience > decisioning >條件> profileConstraints

**欄位：**&#x200B;設定檔限制
**標題：**&#x200B;設定檔條件約束
**描述：**&#x200B;設定檔限制決定選項選取在此內容中目前是否符合此設定檔身分識別的資格。 如果設定檔限制不需要考慮每個選項的值（亦即，它不會改變選項選取範圍中的選項），則評估為「false」的設定檔限制會取消整個選項選取範圍。 另一方面，會針對選項選取的每個合格選項，評估將選項作為引數的設定檔限制規則。
**型別：**&#x200B;物件

+++

+++_experience >決策>條件> profileConstraints >說明

**欄位：**&#x200B;描述
**標題：**&#x200B;描述
**描述：**&#x200B;設定檔條件約束描述。 它用於傳達關於如何或為何建構此設定檔限制以及/或其將包含或排除哪些選項的可讀取意圖。
**型別：**&#x200B;字串

+++

+++ _experience >決策>條件> profileConstraints >適用性規則

**欄位：**&#x200B;適用性規則
**標題：**&#x200B;適用性規則
**描述：**&#x200B;對決定規則的參考，針對指定的設定檔和/或其他指定的內容XDM物件，其評估為true或false。 此規則用於決定選項是否符合指定設定檔的資格。 該值是被參考的決策規則的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/rule 。
**型別：**&#x200B;字串

+++

+++ _experience >決策>條件> profileConstraints >設定檔限制型別

**欄位：** profileConstraintType
**標題：**&#x200B;設定檔限制型別
**描述：**&#x200B;決定目前是否設定任何限制，以及限制如何表示。 可透過規則或一或多個對象會籍進行。
**型別：**&#x200B;字串
**可能的值：**

* 「無」（預設）
* &quot;eligibilityRule&quot;：&quot;設定檔限制表示為單一規則，在允許限製作業之前，必須評估為true。&quot;
* 「anySegments」：「設定檔限制會顯示為一個或多個對象，而且設定檔必須是至少一個對象的成員，才能允許限制動作。」
* 「allSegments」：「設定檔限制表示為一或多個對象，且在允許限制動作之前，設定檔必須是所有對象的成員。」
* &quot;rules&quot;：&quot;設定檔限制表示為許多不同的規則，例如，適用性、適用性、適用性，在允許限制動作之前，這些規則都必須評估為true。&quot;

+++

+++ _experience > decisioning >條件> profileConstraints > segmentIdentities

**欄位：** segmentIdentities
**標題：**&#x200B;區段識別碼
**描述：**&#x200B;對象的識別碼。
**型別：**&#x200B;陣列

* 識別碼

  **欄位：** _id
  **標題：**&#x200B;識別碼
  **描述：**&#x200B;相關名稱空間中的對象身分。
  **型別：**&#x200B;字串

* 名稱空間

  **欄位：**&#x200B;名稱空間
  **標題：**&#x200B;名稱空間
  **描述：**&#x200B;與`xid`屬性關聯的名稱空間。
  **型別：**&#x200B;物件
  **必要：** &quot;code&quot;

   * 程式碼

     **欄位：**&#x200B;代碼
     **標題：**&#x200B;代碼
     **描述：**&#x200B;此程式碼是名稱空間的人類可讀識別碼，可用來請求用於識別圖形處理的技術性名稱空間ID。
     **型別：**&#x200B;字串

* 體驗識別碼

  **欄位：** xid
  **標題：**&#x200B;體驗識別碼
  **描述：**&#x200B;當出現時，這個值代表跨名稱空間的識別碼，在所有名稱空間中都是唯一，也就是所有名稱空間中的範圍識別碼。
  **型別：**&#x200B;字串

+++

+++_experience >決策>條件>排名

**欄位：**&#x200B;排名
**標題：**&#x200B;排名詳細資料
**描述：**&#x200B;排名（優先順序）。 定義在決定標準內容中如何判斷\「最佳選項\」。 在所有符合設定檔限制的選取選項中，排名將決定要建議的前（或前N個）選項。
**型別：**&#x200B;物件

+++ 

+++_experience >決策>條件>排名>訂單

**欄位：**&#x200B;順序
**標題：**&#x200B;訂單評估
**描述：**&#x200B;評估一或多個決定選項的相對順序。 在順序值較低的選項上，會選取順序值較高的選項。 此方法確定的值可以排序，但無法測量它們之間的距離，也無法計算總和或產品。 中間值和模式是唯一可用於序數資料的中央趨勢測量值。
**型別：**&#x200B;物件

* 評分函式

  **欄位：**&#x200B;函式
  **標題：**&#x200B;評分函式
  **描述：**&#x200B;計算此決定選項之數值分數的函式參考。 決策選項便會依該分數排序（排名）。 此屬性的值是每次使用on選項叫用之函式的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/function 。
  **型別：**&#x200B;字串

* 訂單評估型別**

  **欄位：** orderEvaluationType
  **標題：**&#x200B;訂單評估型別
  **描述：**&#x200B;指定使用哪個順序評估機制、決定選項的靜態優先順序、計算每個選項數值的評分函式，或是接收排序清單的AI模型。
  **型別：**&#x200B;字串
  **可能的值：** 「靜態」、「scoringFunction」、「rankingStrategy」

* 排名策略

  **欄位：**&#x200B;排名策略
  **標題：**&#x200B;排名策略
  **描述：**&#x200B;對決定選項清單進行排名的策略參考。 決策選項將會以有序清單傳回。 此屬性的值是每次使用on選項叫用之函式的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/rankingStrategy 。
  **型別：**&#x200B;字串

+++

+++ _experience >決策>條件>排名>優先順序

**欄位：**&#x200B;優先順序
**標題：**&#x200B;優先順序
**描述：**&#x200B;單一決定選項相對於所有其他選項的優先順序。 未指定順序函式的選項會使用此屬性來排定優先順序。 優先順序值較高的選項會在優先順序較低的選項之前選取。 如果兩個或更多合格選項共用最高優先順序值，則會隨機選擇其中一個以用於決策主張。
**型別：**&#x200B;整數
**最小值：** 0
**預設值：** 0

+++

+++ _experience >決策>活動結束日期和時間

**欄位：** endTime
**標題：**&#x200B;活動結束日期和時間
**描述：**&#x200B;決定（先前稱為活動）結束日期和結束時間。 屬性具有在https://schema.org/Action上定義的schema.org的「endTime」屬性的語意。
**型別：**&#x200B;字串

+++

+++ _experience >決策>遞補選項

**欄位：**&#x200B;遞補
**標題：**&#x200B;遞補選項
**說明：**&#x200B;在此決定的內容中決策時使用的遞補選項參考不符合任何一般選項的資格（這通常發生在套用硬式限制時）。 此值是參考的遞補選項的URI (@id)。
**型別：**&#x200B;字串

+++

+++ 體驗>決策>活動名稱(_E)

**欄位：**&#x200B;名稱
**標題：**&#x200B;活動名稱
**描述：**&#x200B;決定（先前稱為活動）名稱，會顯示在各種使用者介面中。
**型別：**&#x200B;字串

+++

+++體驗>決策>活動開始日期和時間(_E)

**欄位：** startTime
**標題：**&#x200B;活動開始日期和時間
**描述：**&#x200B;決定（先前稱為活動）開始日期和結束時間。 屬性具有在https://schema.org/Action上定義的schema.org的「startTime」屬性的語意。
**型別：**&#x200B;字串

+++

+++ 存放庫(_R)

**欄位：** _repo
**型別：**&#x200B;物件

+++

+++ _repo >活動ETag

**欄位：** etag
**標題：**&#x200B;活動ETAG
**描述：**&#x200B;建立快照時決定（先前稱為活動）物件的修訂。
**型別：**&#x200B;字串

+++
