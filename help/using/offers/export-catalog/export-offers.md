---
title: 個人化優惠資料集
description: 本區段列出匯出的選件資料集中所使用的所有欄位。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '2003'
ht-degree: 3%

---

# 個人化優惠資料集 {#offers-dataset}

每次修改選件時，都會更新個人化內容選件的自動產生資料集。

![](../../assets/dataset-offers.png)

資料集中最新成功的批次資料會顯示在右側。 資料集的架構階層檢視會顯示在左窗格上。

>[!NOTE]
>
>了解如何在 [本節](../export-catalog/access-dataset.md).

以下是可在 **[!UICONTROL Decision Object Repository - Personalized Offers]** 資料集。

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

## 識別碼

**欄位：** _id
**標題：** 識別碼
**說明：** 記錄的唯一標識符。
**類型:**&#x200B;字串

## _體驗

**欄位：** _體驗
**類型：** 物件

### _experience > decisioning

**欄位：** 決策
**類型：** 物件

#### _experience > decisioning > calendarConstraints

**欄位：** calendarConstraints
**標題：** 日曆約束詳細資訊
**說明：** 日曆限制會決定決定選項在某個日期範圍內是否有效。 在該日期範圍外，無法建議選項。
**類型：** 物件

* **結束日期和時間**

   **欄位：** endDate
   **標題：** 結束日期和時間
   **說明：** 決定選項有效的結束日期。 在決策程式中，已過其結束日期的選項無法再建議。
   **類型:**&#x200B;字串

* **開始日期和時間**

   **欄位：** startDate
   **標題：** 開始日期和時間
   **說明：** 決策選項有效的開始日期。 尚未達到開始日期的選項在決策程式中尚無法建議。
   **類型:**&#x200B;字串

#### 「體驗>決策>特性」

**欄位：** 特徵
**標題：** 決策選項特徵
**說明：** 屬於此特定決策選項的其他屬性或屬性。 不同的例項可能具有不同的特性（地圖中的索引鍵）。 特徵是用於區分一個決策選項與其他決策選項的名稱值組。 特徵用作表示此決策選項的內容中的值，以及用於分析和優化選項效能的功能。 當每個例項都有相同的屬性或屬性時，該方面應該建模為衍生自決策選項詳細資料的擴充架構。
**類型：** 物件

#### 「體驗>決策>內容」

**欄位：** 內容
**標題：** 內容詳細資料
**說明：** 內容項目，以在不同內容中呈現決策項目。 單一決策選項可以有多種內容變體。 內容是指針對受眾以在（數位）體驗中消費的資訊。 內容會透過管道傳遞至特定版位。
**類型：** 陣列

**「體驗>決策>內容>元件」**

**欄位：** 元件
**說明：** 代表決策選項的內容元件，包括其所有語言變體。 特定元件由「dx:format」、「dc:subject」和「dc:language」或其組合找到。 此中繼資料可用來尋找或呈現與優惠方案相關聯的內容，並根據版位合約加以整合。
**類型：** 陣列
**必要：** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > decisioning > contents > components >內容元件類型**

   **欄位：** _type
   **標題：** 內容元件類型
   **說明：** 枚舉的URI集，其中每個值映射到為內容元件指定的類型。 內容表示的某些使用者希望@type值能作為描述內容元件其他屬性的架構的參考。
   **類型:**&#x200B;字串

* **「體驗>決策>內容>元件> _dc」**

   **欄位：** _dc
   **類型：** 物件
   **必要：** &quot;format&quot;

   * **格式**

      **欄位：** 格式
      **標題：** 格式
      **說明：** 資源的物理或數字表現。 通常，格式應包含資源的媒體類型。 可使用格式來確定顯示或操作資源所需的軟體、硬體或其它設備。 建議的最佳實務是從受控辭匯中選取值(例如 [Internet媒體類型](http://www.iana.org/assignments/media-types/) 定義電腦媒體格式)。
      **類型:**字串
      **範例：** &quot;application/vnd.adobe.photoshop&quot;

   * **語言**
      **欄位：** 語言
      **標題：** 語言
      **說明：** 資源的語言或語言。 \n語言是在語言代碼中指定的，如 [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)，此為BCP47的一部分，而BCP47會用於XDM的其他位置。
      **類型：** 陣列
      **範例：** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **「體驗>決策>內容>元件>_repo」**

   **欄位：** _repo
   **類型：** 物件

   * **id**

      **欄位：** id
      **說明：** 可選的唯一識別碼，用於參考內容存放庫中的資產。 當使用Platform API擷取表示法時，用戶端可能會預期其他屬性\&quot;repo:resolveUrl\&quot;來擷取資產。
      **類型:**字串
      **範例：** &quot;urn&quot;:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e」

   * **名稱**

      **欄位：** 名稱
      **說明：** 透過\&quot;repo:id\&quot;提供存放外部資產的存放庫位置相關提示。
      **類型:**&#x200B;字串

   * **repositoryID**

      **欄位：** repositoryID
      **說明：** 可選的唯一識別碼，用於參考內容存放庫中的資產。 當使用Platform API擷取表示法時，用戶端可能會預期其他屬性\&quot;repo:resolveUrl\&quot;來擷取資產。
      **類型:**字串
      **範例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **欄位：** resolveURL
      **說明：** 可選的唯一資源定位器，用於讀取內容存放庫中的資產。 如此一來，若客戶不了解資產的管理位置以及要呼叫的API，就能更輕鬆取得資產。 這類似於HAL連結，但語義更簡單、更有針對性。
      **類型:**字串
      **範例：** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **「體驗>決策>內容>元件」**

   **欄位：** 內容
   **說明：** 直接保留內容的選用欄位。 元件可直接保留簡單內容，而非參考資產存放庫中的內容。 此欄位不適用於複合、複雜和二進位內容資產。
   **類型:**&#x200B;字串

* **_experience > decisioning > contents > components > deliveryURL**

   **欄位：** deliveryURL
   **說明：** 可選的唯一資源定位器，用於從內容傳送網路或服務端點取得資產。 此URL可供使用者代理公開存取資產。
   **類型:**字串
   **範例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning > contents > components > linkURL**

   **欄位：** linkURL
   **說明：** 用戶交互的可選唯一資源定位器。 此URL用於將使用者引用至使用者代理中，且可加以追蹤。
   **類型:**字串
   **範例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_experience > decisioning >內容>位置**

**欄位：** 刊登
**標題：** 版位
**說明：** 符合的位置。 值是所參考之優惠方案版位的URI(@id)。 請參閱結構https://ns.adobe.com/experience/decisioning/placement。
**類型:**&#x200B;字串

#### _experience > decisioning >生命週期狀態

**欄位：** lifecycleStatus
**標題：** 生命週期狀態
**說明：** 生命週期狀態可讓工作流程與物件一起執行。 狀態可能會影響對象可見或被認為相關的位置。 狀態更改由使用對象的客戶端或服務驅動。
**類型：** 字串
**可能的值：** 「草稿」（預設）、「已核准」、「已上線」、「已完成」、「已封存」

#### _experience > decisioning >決策選項名稱

**欄位：** 名稱
**標題：** 決策選項名稱
**說明：** 顯示在各種用戶介面中的選項名稱。
**類型:**&#x200B;字串

#### _experience > decisioning > profileConstraints

**欄位：** profileConstraints
**標題：** 配置檔案約束詳細資訊
**說明：** 設定檔限制會決定在此情境下，某個選項是否符合此設定檔身分識別的資格。 如果配置檔案約束不需要考慮每個選項的值，即選項選項中的選項是不變的，則評估為&#39;false&#39;的配置檔案約束將取消整個選項選項。 另一方面，會針對選項選取的每個合格選項評估以選項作為參數的設定檔約束規則。
**類型：** 物件

**_experience > decisioning > profileConstraints >說明**

**欄位：** 說明
**標題：** 說明
**說明：** 設定檔限制說明。 它用於傳達人類可讀的意圖，了解此設定檔限制是如何建構的，或為何建構，及/或將包含或排除哪個選項。
**類型:**&#x200B;字串

**_experience > decisioning > profileConstraints >適用性規則**

**欄位：** 適用性規則
**標題：** 適用性規則
**說明：** 針對指定設定檔和/或其他指定情境式XDM物件，評估為true或false之決策規則的參考。 規則可用來決定選項是否符合指定設定檔的資格。 該值是引用的決策規則的URI(@id)。 請參閱結構https://ns.adobe.com/experience/decisioning/rule。
**類型:**&#x200B;字串

**_experience > decisioning > profileConstraints >設定檔約束類型**

**欄位：** profileConstraintType
**標題：** 輪廓約束類型
**說明：** 確定當前是否設定了任何約束以及約束的表達方式。 可透過規則或一或多個區段成員資格。
**類型：** 字串
**可能的值：**
* &quot;none&quot;（預設）
* &quot;apilityRule&quot;:「設定檔限制會以單一規則表示，在允許限制動作之前，必須評估為true。」
* &quot;anySegments&quot;:&quot;配置檔案約束表示為一個或多個段，並且配置檔案必須是其中至少一個段的成員，才允許執行受約束操作。&quot;
* &quot;allSegments&quot;:&quot;配置檔案約束以一個或多個段表示，配置檔案必須是所有段的成員，才允許執行受約束操作。&quot;
* &quot;rules&quot;:「配置檔案約束被表示為許多不同的規則，例如資格、適用性、適用性，在允許約束操作之前，所有規則都必須評估為true。」

**_experience > decisioning > profileConstrants >區段識別碼**

**欄位：** segmentIdentities
**標題：** 區段識別碼
**說明：** 區段的識別碼
**類型：** 陣列

* **識別碼**

   **欄位：** _id
   **標題：** 識別碼
   **說明：** 相關命名空間中區段的身分。
   **類型:**&#x200B;字串

* **命名空間**

   **欄位：** 命名空間
   **標題：** 命名空間
   **說明：** 與 `xid` 屬性。
   **類型：** 物件
   **必要：** &quot;code&quot;

   * **程式碼**

      **欄位：** 代碼
      **標題：** 程式碼
      **說明：** 該代碼是命名空間人類看得懂的識別碼，可用來要求用於身分圖表處理的技術命名空間ID。
      **類型:**&#x200B;字串

* **體驗識別碼**

   **欄位：** xid
   **標題：** 體驗識別碼
   **說明：** 如果存在，此值代表跨命名空間識別碼，此識別碼在所有命名空間中所有命名空間範圍的識別碼中都是唯一的。
   **類型:**&#x200B;字串

#### _experience >決策>排名

**欄位：** 排名
**標題：** 排名詳細資料
**說明：** 排名（優先順序）。 定義在決策准則的情境下，視為「最佳動作」的項目。 在符合資格限制的所有選取選項中，排名順序將決定要建議的前N個選項。
**類型：** 物件

**_experience > decisioning >排名>訂購評估**

**欄位：** 訂購
**標題：** 訂單評估
**說明：** 評估一個或多個決策選項的相對順序。 對於具有較低序數值的任何選項，都會選擇具有較高序數值的選項。 該方法確定的值可以排序，但它們之間的距離不能測量，且不能求和或求積。 中值和模式是唯一可用於序數資料的中心趨勢度量。
**類型：** 物件

* **計分函式**

   **欄位：** 函式
   **標題：** 計分函式
   **說明：** 對函式的引用，該函式計算此決策選項的數值分數。 然後，決策選項將依該分數排序（排名）。 此屬性的值是一次使用on選項調用的函式的URI(@id)。 請參閱結構https://ns.adobe.com/experience/decisioning/function。
   **類型:**&#x200B;字串

* **訂單評估類型**

   **欄位：** orderEvaluationType
   **標題：** 訂單評估類型
   **說明：** 指定使用的順序評估機制、決策選項的靜態優先順序、計算每個選項的數值的評分函式或接收清單以進行排序的排名策略。
   **類型:**字串
   **可能的值：** &quot;static&quot;、&quot;scoringFunction&quot;、&quot;rankingStrategy&quot;

* **排名策略**

   **欄位：** rankingStrategy
   **標題：** 排名策略
   **說明：** 對決策選項清單進行排名的策略的引用。 決策選項將以有序清單返回。 此屬性的值是一次使用on選項調用的函式的URI(@id)。 請參閱結構https://ns.adobe.com/experience/decisioning/rankingStrategy。
   **類型:**&#x200B;字串

**_experience > decisioning >排名>優先順序**

**欄位：** 優先順序
**標題：** 優先順序
**說明：** 單一決策選項相對於所有其他選項的優先順序。 使用此屬性會排定未指定順序函式的選項優先順序。 優先順序值較高的選項將優先於任何優先順序較低的選項。 如果兩個或多個合格期權具有最高優先順序值，則以統一隨機選擇一個期權並用於決策主張。
**類型：** 整數
**最小值：** 0
**預設值：** 0

#### _experience > decisioning >標籤

**欄位：** 標籤
**標題：** 標籤
**說明：** 與此實體相關聯的標籤集。 標籤用於篩選運算式，以將整體清點限制為子集（類別）。
**類型：** 陣列

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

**欄位：** _repo
**類型：** 物件

### _repo >決策選項ETag

**欄位：** etag
**標題：** 決策選項ETag
**說明：** 建立快照時決策選項對象所在的修訂。
**類型:**&#x200B;字串
