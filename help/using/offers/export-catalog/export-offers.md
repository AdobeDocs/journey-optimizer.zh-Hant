---
title: 個人化優惠資料集
description: 此區段會列出選件匯出資料集中使用的所有欄位。
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '1943'
ht-degree: 3%

---

# 個人化選件資料集{#offers-dataset}

每次修改選件時，更新用於個人化內容選件的自動產生的資料集。

![](../../assets/dataset-offers.png)

資料集中最近成功的批次會顯示在右側。 資料集的架構階層檢視會顯示在左窗格上。

>[!NOTE]
>
>瞭解如何在[本節](../export-catalog/access-dataset.md)中存取選件程式庫每個物件的匯出資料集。

以下是&#x200B;**[!UICONTROL Decision Object Repository - Personalized Offers]**&#x200B;資料集中可使用的所有欄位清單。

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

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

#### calendarConstraints

**欄位：** calendarConstraints標
**題：Calendar Constraint Details** Description:
**** Calendar約束決定決策選項是否在給定日期範圍內有效。在該日期範圍以外，無法建議選項。
**類型：對** 像

* **結束日期與時間**

   **欄位：** endDate
   **標題：** 結束日期與時間
   **說明：** 決策選項有效性的結束日期。在決策過程中，已過其結束日期的選項無法再建議。
   **類型:**&#x200B;字串

* **開始日期和時間**

   **欄位：** startDate
   **標題：** 開始日期與時間
   **說明：** 決策選項有效性的開始日期。尚未到達其開始日期的選項仍無法在決策程式中建議。
   **類型:**&#x200B;字串

#### 特徵

**欄位：特** 性
**標題：決策選** 項特性說明：屬
**** 於此特定決策選項的附加屬性或屬性。不同的例項可以有不同的特性（地圖中的鍵）。 這些特徵是用於區分一個決策選項和其他決策選項的名稱值對。 特徵用作代表此決策選項的內容值，以及用於分析和最佳化選項效能的功能。 當每個實例具有相同的屬性或屬性時，應將該方面建模為擴展方案，該擴展方案源自決策選項詳細資訊。
**類型：對** 像

#### 內容

**欄位：內** 容
**標題：內容詳細** 資訊說明：
**** 內容項目，可在不同的上下文中呈現決策項目。單一決策選項可包含多個內容變體。 內容是指針對受眾的資訊，以便在（數位）體驗中消費。 內容透過通道傳遞至特定位置。
**類型：陣** 列

* **元件**

   **欄位：元** 件
   **說明：** 代表決策選項的內容元件，包括其所有語言變體。特定元件由「dx:format」、「dc:subject」和「dc:language」或其組合找到。 此中繼資料可用來尋找或表示與選件相關的內容，並根據位置合約加以整合。
   **類型：陣** 列
   **必要：** &quot;_type&quot;, &quot;_dc&quot;  <!--TBC?-->

   * **內容元件類型**

      **欄位：** _type
      **標題：內** 容元件類型
      **說明：** 一組列舉的URI，其中每個值對應至指定給內容元件的類型。內容表示法的某些使用者預期@type值會是描述內容元件其他屬性之架構的參考。
      **類型:**&#x200B;字串

   * **_dc**

      **欄位：** _dc
      **類型：對** 像
      **必要：** 「格式」

      * **格式**

         **欄位：格** 式
         **標題：格** 式
         **說明：** 資源的物理或數位表現。通常，格式應包括資源的媒體類型。 該格式可用於確定顯示或操作該資源所需的軟體、硬體或其它設備。 建議的最佳實務是從受控辭彙中選取值（例如，定義電腦媒體格式的[網際網路媒體類型](http://www.iana.org/assignments/media-types/)清單）。
         **類型:**字串
         **範例：** 「application/vnd.adobe.photoshop」

      * **語言**
         **欄位：語** 言
         **標題：語** 言
         **說明：** 資源的語言或語言。\n語言在[IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)中定義的語言代碼中指定，該代碼是BCP 47的一部分，BCP 47在XDM中的其他位置使用。
         **類型：陣** 列
         **範例：** &quot;\n&quot;、&quot;pt-BR&quot;、&quot;es-ES&quot;
   * **_repo**

      **欄位：** _repo
      **類型：對** 像

      * **id**

         **欄位：** id
         **說明：可** 選的唯一識別碼，可參考內容儲存庫中的資產。當使用平台API來擷取表示法時，用戶端可能會預期有其他屬性\&quot;repo:resolveUrl\&quot;來擷取資產。
         **類型:**字串
         **範例：** &quot;urn:aid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

      * **名稱**

         **欄位：名** 稱
         **說明：** 有關使用\&quot;repo:id\&quot;查找儲存外部資產的儲存庫的位置的提示。
         **類型:**&#x200B;字串

      * **repositoryID**

         **欄位：** repositoryID
         **說明：可** 選的唯一識別碼，可參考內容儲存庫中的資產。當使用平台API來擷取表示法時，用戶端可能會預期有其他屬性\&quot;repo:resolveUrl\&quot;來擷取資產。
         **類型:**字串
         **範例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

      * **resolveURL**

         **欄位：** resolveURL
         **說明：用** 於讀取內容儲存庫中資產的可選唯一資源定位器。這可讓用戶端更輕鬆地取得資產，而不需瞭解資產的管理位置以及要呼叫的API。 這類似於HAL連結，但語義更簡單、更有針對性。
         **類型:**字串
         **範例：** 「https://plaftform.adobe.io/resolveByPath?path=」「/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3」
   * **content**

      **欄位：內** 容
      **說明：** 可直接保留內容的選用欄位。該元件可以直接保存簡單內容，而不是引用資產儲存庫中的內容。 此欄位不用於複合、複雜和二進位內容資產。
      **類型:**&#x200B;字串

   * **deliveryURL**

      **欄位：** deliveryURL
      **說明：可** 選的唯一資源定位器，可從內容傳送網路或服務端點取得資產。此URL可供使用者代理公開存取資產。
      **類型:**字串
      **範例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

   * **linkURL**

      **欄位：** linkURL
      **說明：用** 戶交互的可選唯一資源定位器。此URL用於將使用者引薦至使用者代理中，並可加以追蹤。
      **類型:**字串
      **範例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;



* **版位**

   **欄位：位** 置
   **標題：位** 置
   **說明：** 要符合的位置。此值是參考之選件位置的URI(@id)。 請參閱架構https://ns.adobe.com/experience/decisioning/placement。
   **類型:**&#x200B;字串

#### 生命週期狀態

**Field:** lifecycleStatus 
**Title:** Lifecycle Status 
**Description:** Lifecycle status允許使用對象執行工作流。狀態可能會影響對象可見或被認為相關的位置。 狀態更改由使用對象的客戶端或服務驅動。
**類型：字** 串
**可能的值：** &quot;Draft&quot;、&quot;Approved&quot;、&quot;Live&quot;、&quot;Completed&quot;、&quot;Archived&quot;預設值：
**** &quot;Draft&quot;

#### 決策選項名稱

**欄位：** 名稱
**標題：決** 策選項名稱說
**明：** 顯示於各種使用者介面中的選項名稱。**類型:**&#x200B;字串

#### profileConstraints

**欄位：** profileConstraints 
**Title:** Profile Constraint Details 
**Description:** 配置檔案約束決定了此上下文中的選項是否適用於此配置檔案標識。如果描述檔約束不需要考慮每個選項的值，即選項選擇中的選項不變，則評估為&#39;false&#39;的描述檔約束會取消整個選項選擇。 另一方面，系統會針對選項選擇的每個限定選項評估以選項作為參數的配置檔案約束規則。
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
   **說明：** 區段的識別碼
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


#### 排名

**欄位：排** 名
**標題：排** 名詳細資
**訊說明：** 排名（優先順序）。定義在判定准則的上下文下，將什麼視為「最佳動作」。 在符合資格限制的所有選取選項中，排名順序將決定要建議的前N個選項。
**類型：對** 像

* **訂單評估**

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

#### 標籤

**Field:** tags 
**Title:** Tags 
**Description:** 與此實體關聯的標籤集。這些標籤用於篩選運算式，以將整體庫存限制為子集（類別）。
**類型：陣** 列

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

**欄位：** _repo 
**Type:** object

### 決策選項ETag

**欄位：** etag 
**Title:** Decision Option ETag 
**Description:** 拍攝快照時決策選項對象所在的修訂版。**類型:**&#x200B;字串



