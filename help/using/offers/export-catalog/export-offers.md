---
title: 個人化優惠資料集
description: 本區段列出匯出的選件資料集中所使用的所有欄位。
feature: 優惠
topic: 整合
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '2007'
ht-degree: 3%

---

# 個人化優惠資料集 {#offers-dataset}

每次修改選件時，都會更新個人化內容選件的自動產生資料集。

![](../../assets/dataset-offers.png)

資料集中最新成功的批次資料會顯示在右側。 資料集的架構階層檢視會顯示在左窗格上。

>[!NOTE]
>
>了解如何在[本區段](../export-catalog/access-dataset.md)中存取Offer Library每個物件的匯出資料集。

以下是&#x200B;**[!UICONTROL Decision Object Repository - Personalized Offers]**&#x200B;資料集中可使用的所有欄位清單。

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

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

#### _experience > decisioning > calendarConstraints

**欄位：** calendarConstraints標
**題：** 日曆約束詳細資
**訊說明：** 日曆約束決定在給定日期範圍內決策選項是否有效。在該日期範圍外，無法建議選項。
**類型：** 物件

* **結束日期和時間**

   **欄位：** endDate
   **標題：** 結束日期和時間
   **說明：** 決策選項有效性的結束日期。在決策程式中，已過其結束日期的選項無法再建議。
   **類型:**&#x200B;字串

* **開始日期和時間**

   **欄位：** startDate
   **標題：** 開始日期與時間
   **說明：** 決策選項有效性的開始日期。尚未達到開始日期的選項在決策程式中尚無法建議。
   **類型:**&#x200B;字串

#### 「體驗>決策>特性」

**欄位：** 特性
**標題：** 決策選項特性
**說明：** 屬於此特定決策選項的其他屬性或屬性。不同的例項可能具有不同的特性（地圖中的索引鍵）。 特徵是用於區分一個決策選項與其他決策選項的名稱值組。 特徵用作表示此決策選項的內容中的值，以及用於分析和優化選項效能的功能。 當每個例項都有相同的屬性或屬性時，該方面應該建模為衍生自決策選項詳細資料的擴充架構。
**類型：** 物件

#### 「體驗>決策>內容」

**欄位：** 內容
**標題：** 內容詳細資
**料說明：** 在不同內容中呈現決策項目的內容項目。單一決策選項可以有多種內容變體。 內容是指針對受眾以在（數位）體驗中消費的資訊。 內容會透過管道傳遞至特定版位。
**類型：** 陣列

**「體驗>決策>內容>元件」**

**欄位：** 元
**件說明：** 代表決策選項的內容元件，包括其所有語言變體。特定元件由「dx:format」、「dc:subject」和「dc:language」或其組合找到。 此中繼資料可用來尋找或呈現與優惠方案相關聯的內容，並根據版位合約加以整合。
**類型：** 陣
**列必要：** &quot;_type&quot;, &quot;_dc&quot;  <!--TBC?-->

* **_experience > decisioning > contents > components >內容元件類型**

   **欄位：** _type
   **標題：** 內容元件類型
   **說明：** 一組列舉的URI，其中每個值映射到為內容元件指定的類型。內容表示的某些使用者希望@type值能作為描述內容元件其他屬性的架構的參考。
   **類型:**&#x200B;字串

* **「體驗>決策>內容>元件> _dc」**

   **欄位：** _dc
   **類型：** 物件
   **必要：**  &quot;format&quot;

   * **格式**

      **欄位：** 格式
      **標題：** 格式
      **說明：** 資源的物理或數位形式。通常，格式應包含資源的媒體類型。 可使用格式來確定顯示或操作資源所需的軟體、硬體或其它設備。 建議的最佳實務是從受控辭匯中選取值（例如，定義電腦媒體格式的[網際網路媒體類型](http://www.iana.org/assignments/media-types/)清單）。
      **類型:**字串
      **範例：**  &quot;application/vnd.adobe.photoshop&quot;

   * **語言**
      **欄位：** 語言
      **標題：** 語言
      **說明：** 資源的語言或語言。\n語言在語言代碼中指定，如[IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)中所定義，該代碼是BCP 47的一部分，BCP 47用於XDM的其他位置。
      **類型：** 陣列
      **範例：** &quot;\n&quot;、&quot;pt-BR&quot;、&quot;es-ES&quot;

* **「體驗>決策>內容>元件>_repo」**

   **欄位：** _repo
   **類型：** 物件

   * **id**

      **欄位：** id
      **說明：** 可參考內容存放庫中資產的選用唯一識別碼。當使用Platform API擷取表示法時，用戶端可能會預期其他屬性\&quot;repo:resolveUrl\&quot;來擷取資產。
      **類型:**字串
      **範例：** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **名稱**

      **欄位：** 名稱
      **說明：** 透過\&quot;repo:id\&quot;，說明如何找出儲存外部資產之存放庫的相關位置。
      **類型:**&#x200B;字串

   * **repositoryID**

      **欄位：** repositoryID
      **說明：** 可參考內容存放庫中資產的選用唯一識別碼。當使用Platform API擷取表示法時，用戶端可能會預期其他屬性\&quot;repo:resolveUrl\&quot;來擷取資產。
      **類型:**字串
      **範例：**  &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **欄位：** resolveURL
      **說明：** 內容存放庫中讀取資產的選用唯一資源定位器。這可讓用戶端更輕鬆取得資產，同時了解資產的管理位置以及要呼叫的API。 這類似於HAL連結，但語義更簡單、更有針對性。
      **類型:**字串
      **範例：**  &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **「體驗>決策>內容>元件」**

   **欄位：** 內容
   **說明：** 可直接保留內容的選用欄位。元件可直接保留簡單內容，而非參考資產存放庫中的內容。 此欄位不適用於複合、複雜和二進位內容資產。
   **類型:**&#x200B;字串

* **_experience > decisioning > contents > components > deliveryURL**

   **欄位：** deliveryURL
   **說明：** 可選的唯一資源定位器，用於從內容傳送網路或服務端點取得資產。此URL可供使用者代理公開存取資產。
   **類型:**字串
   **範例：**  &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning > contents > components > linkURL**

   **欄位：** linkURL
   **說明：** 使用者互動的選用唯一資源定位器。此URL用於將使用者引用至使用者代理中，且可加以追蹤。
   **類型:**字串
   **範例：**  &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_experience > decisioning >內容>位置**

**欄位：** 版位
**標題：** 版位
**說明：** 版位以符合。值是所參考之優惠方案版位的URI(@id)。 請參閱結構https://ns.adobe.com/experience/decisioning/placement。
**類型:**&#x200B;字串

#### _experience > decisioning >生命週期狀態

**欄位：** 生命周
**期狀態標題：** 生命週期狀
**態說明：** 生命週期狀態可讓工作流程透過物件執行。狀態可能會影響對象可見或被認為相關的位置。 狀態更改由使用對象的客戶端或服務驅動。
**類型：** 字
**串可能的值：** 「草稿」（預設值）、「已核准」、「即時」、「已完成」、「已封存」

#### _experience > decisioning >決策選項名稱

**欄位：** 名稱
**標題：** 決策選項名稱
**說明：** 顯示在各種使用者介面中的選項名稱。**類型:**&#x200B;字串

#### _experience > decisioning > profileConstraints

**欄位：** profileConstraints標
**題：** 設定檔限制詳細資
**料說明：** 設定檔限制會決定選項是否適用於此設定檔身分識別，目前是在此情境中。如果配置檔案約束不需要考慮每個選項的值，即選項選項中的選項是不變的，則評估為&#39;false&#39;的配置檔案約束將取消整個選項選項。 另一方面，會針對選項選取的每個限定選項，評估以選項作為參數的設定檔約束規則。
**類型：** 物件

**_experience > decisioning > profileConstraints >說明**

**欄位：** 說明
**標題：** 說明
**說明：** 設定檔限制說明它用於傳達人類可讀的意圖，了解此設定檔限制是如何建構的，或為何建構，及/或將包含或排除哪個選項。
**類型:**&#x200B;字串

**_experience > decisioning > profileConstraints >適用性規則**

**欄位：** 適用性
**規則標題：** 適用性規
**則說明：** 針對特定設定檔和/或其他特定情境XDM物件，評估為true或false之決策規則的參考。規則可用來決定選項是否符合指定設定檔的資格。 該值是引用的決策規則的URI(@id)。 請參閱結構https://ns.adobe.com/experience/decisioning/rule。
**類型:**&#x200B;字串

**_experience > decisioning > profileConstraints >設定檔約束類型**

**欄位：** profileConstraintType
**標題：** 設定檔限制類型
**說明：** 決定目前是否設定了任何限制以及如何表示限制。可透過規則或一或多個區段成員資格。
**類型：** 字串
**可能的值：**
* &quot;none&quot;（預設）
* &quot;apilityRule&quot;:「設定檔限制會以單一規則表示，在允許限制動作之前，必須評估為true。」
* &quot;anySegments&quot;:&quot;配置檔案約束表示為一個或多個段，並且配置檔案必須是其中至少一個段的成員，才允許執行受約束操作。&quot;
* &quot;allSegments&quot;:&quot;配置檔案約束以一個或多個段表示，配置檔案必須是所有段的成員，才允許執行受約束操作。&quot;
* &quot;rules&quot;:「配置檔案約束被表示為許多不同的規則，例如資格、適用性、適用性，在允許約束操作之前，所有規則都必須評估為true。」

**_experience > decisioning > profileConstrants >區段識別碼**

**欄位：** segmentIdentities 
**Title:** 區段識別
**碼說明：** 區段的識別碼類
**型：** 陣列

* **識別碼**

   **欄位：** _id
   **標題：** 識別碼
   **說明：** 相關命名空間中區段的身分。
   **類型:**&#x200B;字串

* **命名空間**

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

#### _experience >決策>排名

**欄位：** 排名
**標題：** 排名詳細資料
**說明：** 排名（優先順序）。定義在決策准則的情境下，視為「最佳動作」的項目。 在符合資格限制的所有選取選項中，排名順序將決定要建議的前N個選項。
**類型：** 物件

**_experience > decisioning >排名>訂購評估**

**欄位：** 訂單
**標題：** 訂單評估
**說明：** 評估一個或多個決策選項的相對順序。對於具有較低序數值的任何選項，都會選擇具有較高序數值的選項。 該方法確定的值可以排序，但它們之間的距離不能測量，且不能計算和或積。 中值和模式是唯一可用於序數資料的中心趨勢度量。
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

**_experience > decisioning >排名>優先順序**

**欄位：** 優
**先順序標題：** 優先
**順序說明：** 單一決策選項相對於所有其他選項的優先順序。使用此屬性會排定不提供訂單函式的選項優先順序。 優先順序值較高的選項將優先於任何優先順序較低的選項。 如果兩個或多個合格期權具有最高優先順序值，則以統一隨機選擇一個期權並用於決策主張。
**類型：** 整數
**最小值：** 0預
**設值：** 0

#### _experience > decisioning >標籤

**欄位：** 標
**題：** 標
**題：** 與此實體相關聯的標籤集。標籤用於篩選運算式，以將整體清點限制為子集（類別）。
**類型：** 陣列

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

**欄位：** _repo 
**類型：** 物件

### _repo >決策選項ETag

**欄位：** etag 
**標題：** 決策選項ETag
**說明：** 建立快照時決策選項物件所在的修訂。**類型:**&#x200B;字串



