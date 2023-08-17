---
title: 個人化優惠資料集
description: 本節列出在匯出的優惠資料集中使用的所有欄位
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: f2174848c70610fc543ea9ddf766f0f7e579053a
workflow-type: tm+mt
source-wordcount: '2014'
ht-degree: 3%

---

# 個人化優惠資料集 {#offers-dataset}

每次修改優惠方案時，都會更新自動產生的個人化內容優惠方案資料集。

![](../assets/dataset-offers.png)

資料集中最近成功的批次會顯示在右側。 資料集的結構描述階層檢視會顯示在左窗格中。

>[!NOTE]
>
>瞭解如何存取中選件資料庫每個物件的匯出資料集 [本節](../export-catalog/access-dataset.md).

以下為可用於的所有欄位清單 **[!UICONTROL 決定物件存放庫 — 個人化優惠]** 資料集。

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

+++ 識別碼

**欄位：** _id
**標題：** 識別碼
**說明：** 紀錄的唯一識別碼。
**類型:**&#x200B;字串

+++

+++ _體驗 {#experience}

**欄位：** 體驗(_E)
**型別：** 物件

+++

+++ 體驗>決策(_E)

**欄位：** 決策
**型別：** 物件

+++

+++ 體驗>決策>行事曆限制(_E)

**欄位：** calendarConstraints
**標題：** 行事曆限制詳細資訊
**說明：** 行事曆限制會根據日期範圍來決定決定選項是否有效。 在該日期範圍外，無法建議選項。
**型別：** 物件

* **結束日期和時間**

  **欄位：** endDate
  **標題：** 結束日期和時間
  **說明：** 決定選項有效性的結束日期。 已超過結束日期的選項無法在決定程式中建議。
  **類型:**&#x200B;字串

* **開始日期和時間**

  **欄位：** startDate
  **標題：** 開始日期和時間
  **說明：** 決定選項有效性的開始日期。 尚未到達開始日期的選項無法在決策程式中建議。
  **類型:**&#x200B;字串

+++

+++ 體驗>決策>特性(_E)

**欄位：** 特性
**標題：** 決定選項特性
**說明：** 屬於此特定決定選項的其他特性或屬性。 不同的執行個體可以有不同的特性（地圖中的索引鍵）。 特性是名稱值配對，用來區分不同決定選項。 特性會用作內容中的值，代表此決定選項，並作為分析和最佳化選項效能的功能。 當每個執行個體都有相同的屬性或屬性時，該方面應該被模型化為衍生自決定選項詳細資訊的擴充功能結構描述。
**型別：** 物件

+++

+++ 體驗>決策>內容(_E)

**欄位：** 內容
**標題：** 內容詳細資料
**說明：** 在不同內容中呈現決定專案的內容專案。 單一決定選項可以有多個內容變體。 內容是導向對象以在（數位）體驗中消費的資訊。 內容會透過管道傳送到特定位置。
**型別：** 陣列

+++

+++_體驗>決策>內容>元件

**欄位：** 元件
**說明：** 代表決定選項的內容元件，包括其所有語言變體。 特定元件可由「dx：format」、「dc：subject」和「dc：language」或其組合找到。 此中繼資料用於尋找或表示與優惠方案相關聯的內容，並根據刊登版位合約加以整合。
**型別：** 陣列
**必填：** &quot;_type&quot;， &quot;_dc&quot; <!--TBC?-->

* **體驗>決策>內容>元件>內容元件型別**

  **欄位：** _type
  **標題：** 內容元件型別
  **說明：** 一組URI的列舉，其中每個值都對應到指定給內容元件的型別。 內容表示的某些消費者期望@type值是描述內容元件其他屬性的結構描述的參考。
  **類型:**&#x200B;字串

* **_experience >決策>內容>元件> _dc**

  **欄位：** _dc
  **型別：** 物件
  **必填：** &quot;format&quot;

   * **格式**

     **欄位：** 格式
     **標題：** 格式
     **說明：** 資源的實體或數位表現形式。 通常，格式應該包含資源的媒體型別。 格式可用於決定顯示或操作資源所需的軟體、硬體或其他裝置。 建議的最佳作法是從受控辭彙表中選取值(例如 [網際網路媒體型別](https://www.iana.org/assignments/media-types/) 定義電腦媒體格式)。
     **類型:**字串
     **範例：** &quot;application/vnd.adobe.photoshop&quot;

   * **語言**
     **欄位：** 語言
     **標題：** 語言
     **說明：** 資源的語言。 \n語言是依照中定義的語言代碼指定的 [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)，這是BCP 47的一部分，用於XDM的其他地方。
     **型別：** 陣列
     **範例：** &quot;\n&quot;， &quot;pt-BR&quot;， &quot;es-ES&quot;

* **_experience > decisioning >內容>元件> _repo**

  **欄位：** 存放庫(_R)
  **型別：** 物件

   * **id**

     **欄位：** id
     **說明：** 選用的唯一識別碼，可參照內容存放庫中的資產。 當使用Platform API擷取表示時，使用者端可預期額外的屬性\&quot;repo：resolveUrl\&quot;來擷取資產。
     **類型:**字串
     **範例：** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e」

   * **名稱**

     **欄位：** 名稱
     **說明：** 關於要透過\&quot;repo：id\&quot;找到儲存外部資產的存放庫的位置，有一些提示。
     **類型:**&#x200B;字串

   * **repositoryID**

     **欄位：** repositoryID
     **說明：** 選用的唯一識別碼，可參照內容存放庫中的資產。 當使用Platform API擷取表示時，使用者端可預期額外的屬性\&quot;repo：resolveUrl\&quot;來擷取資產。
     **類型:**字串
     **範例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

     **欄位：** resolveURL
     **說明：** 選用的唯一資源定位器，可讀取內容存放庫中的資產。 這將讓使用者端更容易取得資產，而無需瞭解資產的管理位置以及要呼叫的API。 這類似於HAL連結，但語意較簡單且目的性較強。
     **類型:**字串
     **範例：** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;

* **_experience >決策>內容>元件>內容**

  **欄位：** 內容
  **說明：** 直接保留內容的選用欄位。 元件可以直接儲存簡單的內容，而不是在資產存放庫中參照內容。 此欄位不適用於複合、複雜和二進位內容資產。
  **類型:**&#x200B;字串

* **_experience >決策>內容>元件> deliveryURL**

  **欄位：** deliveryURL
  **說明：** 選用的唯一資源定位器，可從內容傳遞網路或服務端點取得資產。 使用者代理會使用此URL來公開存取資產。
  **類型:**字串
  **範例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience >決策>內容>元件> linkURL**

  **欄位：** linkURL
  **說明：** 選擇性唯一資源定位器，用於使用者互動。 此URL用於在使用者代理中將一般使用者引薦至，並且可被追蹤。
  **類型:**字串
  **範例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

+++_體驗>決策>內容>版位

**欄位：** 刊登
**標題：** 刊登
**說明：** 要遵循的位置。 該值是被參考之優惠方案位置的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/placement 。
**類型:**&#x200B;字串

+++

+++ _experience >決策>生命週期狀態

**欄位：** lifecycleStatus
**標題：** 生命週期狀態
**說明：** 生命週期狀態允許使用物件執行工作流程。 在物件可見或被視為相關的位置，狀態可能會受到影響。 狀態變更是由使用物件的使用者端或服務所驅動。
**型別：** 字串
**可能的值：** 「草稿」（預設）、「已核准」、「即時」、「已完成」、「已封存」

+++

+++ _experience >決策>決策選項名稱

**欄位：** 名稱
**標題：** 決定選項名稱
**說明：** 顯示在各種使用者介面中的選項名稱。
**類型:**&#x200B;字串

+++

+++ _experience > decisioning > profileConstraints

**欄位：** profileConstraints
**標題：** 設定檔限制詳細資訊
**說明：** 在此情況下，設定檔限制會決定某個選項是否適用於此設定檔識別。 如果設定檔限制不需要考慮每個選項的值（亦即，它不會改變選項選取範圍中的選項），則評估為「false」的設定檔限制會取消整個選項選取範圍。 另一方面，會針對選項選取的每個合格選項，評估將選項作為引數的設定檔限制規則。
**型別：** 物件

+++

+++_體驗>決策> profileConstraints >說明

**欄位：** 說明
**標題：** 說明
**說明：** 設定檔限制說明。 它用於傳達關於如何或為何建構此設定檔限制以及/或其將包含或排除哪些選項的可讀取意圖。
**類型:**&#x200B;字串

+++

+++_體驗>決策> profileConstraints >適用性規則

**欄位：** 適用性規則
**標題：** 適用性規則
**說明：** 決策規則的參考，對於指定的設定檔和/或其他指定的內容XDM物件，其評估為true或false。 此規則用於決定選項是否符合指定設定檔的資格。 該值是被參考的決策規則的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/rule 。
**類型:**&#x200B;字串

+++

+++_體驗>決策> profileConstraints >設定檔限制型別

**欄位：** profileConstrainttype
**標題：** 設定檔限制型別
**說明：** 決定目前是否設定任何限制，以及限制如何表示。 可透過規則或一或多個對象會籍進行。
**型別：** 字串
**可能的值：**
* 「無」（預設）
* &quot;eligibilityRule&quot;：&quot;設定檔限制表示為單一規則，在允許限製作業之前，必須評估為true。&quot;
* 「anySegments」：「設定檔限制會顯示為一個或多個對象，而且設定檔必須是至少一個對象的成員，才能允許限制動作。」
* 「allSegments」：「設定檔限制表示為一或多個對象，且在允許限制動作之前，設定檔必須是所有對象的成員。」
* &quot;rules&quot;：&quot;設定檔限制表示為許多不同的規則，例如，適用性、適用性、適用性，在允許限制動作之前，這些規則都必須評估為true。&quot;

+++

+++_體驗>決策> profileConstraints >區段識別碼

**欄位：** segmentIdentities
**標題：** 區段識別碼
**說明：** 對象的識別碼
**型別：** 陣列

* **識別碼**

  **欄位：** _id
  **標題：** 識別碼
  **說明：** 相關名稱空間中的對象身分。
  **類型:**&#x200B;字串

* **命名空間**

  **欄位：** 名稱空間
  **標題：** 名稱空間
  **說明：** 與關聯的名稱空間 `xid` 屬性。
  **型別：** 物件
  **必填：** &quot;code&quot;

   * **程式碼**

     **欄位：** 程式碼
     **標題：** 程式碼
     **說明：** 此代碼是適用於名稱空間的可讀取識別碼，可用於請求技術性的名稱空間ID （用於識別圖形處理）。
     **類型:**&#x200B;字串

* **體驗識別碼**

  **欄位：** xid
  **標題：** 體驗識別碼
  **說明：** 當出現時，這個值代表跨名稱空間的識別碼，在所有名稱空間中都是唯一，也就是所有名稱空間中的範圍識別碼。
  **類型:**&#x200B;字串

+++

+++ _experience >決策>排名

**欄位：** 排名
**標題：** 排名詳細資料
**說明：** 排名（優先順序）。 根據決策標準的內容，定義視為\「最佳動作\」的專案。 在符合資格限制的所有選取選項中，排名順序將決定要建議的前（或前N個）選項。
**型別：** 物件

+++

+++_體驗>決策>排名>訂單評估

**欄位：** 訂購
**標題：** 訂單評估
**說明：** 評估一或多個決定選項的相對順序。 在順序值較低的選項上，會選取順序值較高的選項。 此方法確定的值可以排序，但無法測量它們之間的距離，也無法計算總和或產品。 中間值和模式是唯一可用於序數資料的中央趨勢測量值。
**型別：** 物件

* **評分函式**

  **欄位：** 函式
  **標題：** 評分函式
  **說明：** 計算此決定選項之數值分數的函式參照。 決策選項便會依該分數排序（排名）。 此屬性的值是每次使用on選項叫用之函式的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/function 。
  **類型:**&#x200B;字串

* **訂單評估型別**

  **欄位：** orderEvaluationType
  **標題：** 訂單評估型別
  **說明：** 指定使用的順序評估機制、決定選項的靜態優先順序、計算每個選項數值的評分函式，或接收排序清單的AI模型。
  **類型:**字串
  **可能的值：** &quot;static&quot;、&quot;scoringFunction&quot;、&quot;rankingStrategy&quot;

* **排名策略**

  **欄位：** 排名策略
  **標題：** 排名策略
  **說明：** 對決定選項清單進行排名的策略參考。 決策選項將會以有序清單傳回。 此屬性的值是每次使用on選項叫用之函式的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/rankingStrategy 。
  **類型:**&#x200B;字串

+++

+++_體驗>決策>排名>優先順序

**欄位：** 優先順序
**標題：** 優先順序
**說明：** 相對於所有其他選項的單一決定選項優先順序。 未指定順序函式的選項會使用此屬性來排定優先順序。 優先順序值較高的選項會在優先順序較低的選項之前選取。 如果兩個或更多合格選項共用最高優先順序值，則會隨機選擇其中一個以用於決策主張。
**型別：** 整數
**最小值：** 0
**預設值：** 0

+++

+++ _experience >決策>標籤

**欄位：** 標籤
**標題：** 標籤
**說明：** 與此實體相關聯的集合限定詞集（先前稱為「標籤」）。 集合限定詞用於篩選運算式，以將整體詳細目錄限製為子集（類別）。
**型別：** 陣列

+++

<!--Field without name under tags: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++_repo

**欄位：** 存放庫(_R)
**型別：** 物件

+++

+++ _repo >決定選項ETag

**欄位：** etag
**標題：** 決定選項ETag
**說明：** 決定選項物件拍攝快照時的修訂版本。
**類型:**&#x200B;字串

+++
