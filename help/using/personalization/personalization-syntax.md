---
solution: Journey Optimizer
product: journey optimizer
title: 個人化語法
description: 瞭解如何使用個人化語法。
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: 運算式，編輯器，語法，個人化
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
TQID: https://experienceleague.adobe.com/kZEw2lITdt8SMWMe-UT2vPzdoiAjB2vbItmK9zt-WJo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: ac5d9310-7772-40fb-9d78-864562e1bfd6
  - id: e51e8901-97d9-4f7d-a835-503025a90e32
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1979
ht-degree: 2%

---

# 個人化語法 {#personalization-syntax}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解Adobe Journey Optimizer中的Handlebars和PQL個人化語法，包括一般規則、保留關鍵字、型別強制執行、可用名稱空間和最佳實務。

>[!ENDSHADEBOX]

[!DNL Journey Optimizer]中的Personalization使用兩種互補語法，在相同的運算式中一起運作：

* **Handlebars** (`{{...}}`) — 用於轉譯設定檔屬性、陣列上的回圈，以及呼叫區塊協助程式。 如需完整參考，請參閱[HandlebarsJS檔案](https://handlebarsjs.com/)。
* **Profile Query Language (PQL)** (`{%= ... %}`) — 用於呼叫內建函式（例如`upperCase()`、`formatDate()`、`dateDiff()`）並評估條件運算式。

瞭解您所在的環境是避免執行階段錯誤的關鍵。 例如，置於`{{...}}`內的PQL函式呼叫將失敗，因為Handlebars會嘗試將其解析為協助程式，而不是將其評估為PQL運算式。

**範例:**

| 使用案例 | 語法 |
|----------|--------|
| 呈現設定檔屬性 | `{{profile.person.name.firstName}}` |
| 呼叫PQL函式 | `{%= upperCase(profile.person.name.firstName) %}` |
| 條件區塊 | `{%#if profile.loyalty.tier = "gold"%}...{%/if%}` |
| 在陣列上回圈 | `{{#each profile.orders}}...{{/each}}` |

屬性結構是在Adobe Experience Platform XDM結構描述中定義。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}。

>[!TIP]
>
>如需將這些語法套用至實際情況的現成運算式（日期格式、倒數、條件遞補等），請參閱&#x200B;**[Personalization配方](personalization-recipes.md)**&#x200B;頁面。

## 語法一般規則 {#general-rules}

* 識別碼可以是任何Unicode字元，但下列為Handlebars語法保留的特殊字元除外：

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* 語法區分大小寫。

* 字詞&#x200B;**true**、**false**、**null**&#x200B;和&#x200B;**未定義**&#x200B;只允許在路徑運算式的第一個部分中。

* 在Handlebars中，{{expression}}傳回的值是&#x200B;**HTML逸出**。 如果運算式包含`&`，則會產生傳回的HTML逸出輸出為`&amp;`。 如果您不希望Handlebars逸出值，請使用「三重儲存」。

  假設欄位`profile.person.name`的值為「Mark &amp; Mary」。 語法`{{profile.person.name}}`將顯示`Mark &amp; Mary`，而`{{{profile.person.name}}}`將顯示`Mark & Mary`。

* 關於常值函式引數，範本化語言剖析器不支援單一未逸出的反斜線(`\`)符號。 此字元必須使用額外的反斜線(`\`)符號逸出。 範例：

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

* 若要在字串值中包含&#x200B;**常值雙引號** （例如在產生JSON輸出時），請使用反斜線(`\"`)將其逸出：

  ```handlebars
  { "message": "Hello \"{{profile.person.name.firstName}}\"" }
  ```

  輸出： `{ "message": "Hello \"John\"" }`

  或者，當值本身包含您不想要以HTML編碼的特殊字元時，使用三重儲存`{{{ }}}`來輸出未逸出的HTML。

## 保留關鍵字 {#reserved-keywords}

某些關鍵字在Profile Query Language (PQL)中會保留，並且無法直接用作個人化運算式中的欄位或變數名稱。 如果您的XDM結構描述包含名稱符合保留關鍵字的欄位，您必須使用反引號(`` ` ``)將其逸出，以便在運算式中參照。

**保留的關鍵字包括：**

* `next`
* `last`
* `this`

**範例：**

如果您的設定檔結構描述有名為`next`的欄位，您必須以反引號將其換行：

```
{{profile.person.`next`.name}}
```

如果沒有反引號，個人化編輯器將會因錯誤而無法通過驗證。

>[!NOTE]
>
>保留關鍵字的反勾逸出同時適用於`{{...}}` Handlebars路徑和`{%= ... %}` PQL運算式，因為這些關鍵字是在路徑解析度層級保留。 這與連字欄位名稱不同，後者僅支援PQL運算式中的反勾字元逸出。 請參閱[連字屬性索引鍵](#hyphenated-keys)。

## 特殊屬性索引鍵的PQL語法規則 {#pql-special-keys}

除了保留的關鍵字之外，另有兩個案例需要在PQL運算式中執行反勾字元逸出。

### 連字屬性索引鍵 {#hyphenated-keys}

如果您的XDM結構描述包含具有連字型大小的欄位名稱（例如`my-field`、`event-type`），或是開頭為或包含數字的名稱，請在PQL運算式中以反引號將索引鍵換行：

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>只有PQL運算式(`{%= ... %}`)內支援反勾字元逸出。 Handlebars內插(`{{...}}`)不支援此功能。 不過，可以在`{{...}}`區塊中直接參考連字欄位名稱（例如`{{profile.my-custom-field}}`）；只有反勾語法會失敗。

若沒有PQL運算式中的反引號，連字型大小會解譯為減法運運算元，並導致PQL語法錯誤。

### 內容屬性中的數值事件ID {#numeric-event-ids}

當參考事件ID為數字（例如`1697323153`）的內容事件屬性時，請以反引號將其包裝。 這也適用於類似`formatDate()`的函式內部：

```handlebars
{% let ts = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy") %}
{{ts}}
```

## 輸入強制 {#type-coercion}

PQL是強型別。 比較或傳遞值時，兩邊的型別必須相同。 常見案例：

| 藍本 | 解決方案 |
|----------|----------|
| 儲存為字串的數值 | 在算術或比較前使用`stringToNumber()`： `{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}` |
| 儲存為字串的整數 | 在算術前使用`string_to_integer()`或`stringToNumber()` |
| 布林值儲存為字串 | 使用`toBool()`進行轉換： `{%= toBool(profile.consents.email.val) = true %}` |

## 可用的名稱空間 {#namespaces}

* **輪廓**

  此名稱空間可讓您參考[Adobe Experience Platform資料模型(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}中所述的設定檔結構描述中定義的所有屬性。

  屬性必須先在結構描述中定義，才能在[!DNL Journey Optimizer]個人化區塊中參考。

  如需如何在條件中運用設定檔屬性的詳細資訊，請參閱[本節](functions/helpers.md#if-function)。

  +++範例參考

   * `{{profile.person.name.fullName}}`
   * `{{profile.person.name.firstName}}`
   * `{{profile.person.gender}}`
   * `{{profile.personalEmail.address}}`
   * `{{profile.mobilePhone.number}}`
   * `{{profile.homeAddress.city}}`
   * `{{profile.faxPhone.number}}`

  +++

* **客群**

  若要深入瞭解細分服務，請參閱[此檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hant){target="_blank"}。

* **產品建議**

  此名稱空間可讓您參考現有的優惠決定。

  若要參照選件，您必須使用定義選件的不同資訊來宣告路徑。 此路徑的結構如下：

  `offers.Type.[Placement Id].[Activity Id].Attribute`

  其中：

   * `offers`會識別屬於優惠方案名稱空間的路徑運算式
   * `Type`決定優惠方案宣告的型別。 可能的值為： `image`、`html`和`text`
   * `Placement Id`和`Activity Id`是位置與活動識別碼
   * `Attributes`是優惠方案特定屬性，其取決於優惠方案型別。 範例： `deliveryUrl`影像

  如需有關Decisions API和優惠宣告的詳細資訊，請參閱[此頁面](../offers/api-reference/offer-delivery-api/decisioning-api.md)

  所有參考資料都是透過在[此頁面](../personalization/personalization-build-expressions.md)中說明的驗證機制針對優惠方案結構描述進行驗證

  +++範例參考

   * 影像的託管位置：

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

   * 按一下影像時的目標URL：

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

   * 來自決策引擎的優惠方案文字內容：

     `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

   * 來自決策引擎之優惠方案的HTML內容：

     `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

  +++

## 輔助程式 {#helpers-all}

Handlebars協助程式是簡單識別碼，後面可能會接著引數。 每個引數都是Handlebars運算式。 這些協助程式可從範本中的任何內容存取。

這些區塊協助程式由協助程式名稱前的`#`識別，並需要相同名稱的相符結尾`/`。

區塊是具有區塊開啟(`{{# }}`)和結束(`{{/}}`)的運算式。

如需協助程式函式的詳細資訊，請參閱[本節](functions/helpers.md)。

## 常值型別 {#literal-types}

[!DNL Adobe Journey Optimizer]支援下列常值型別：

| 常值 | 定義 |
| ------- | ---------- |
| 字串 | 由雙引號包住的字元所組成的資料型別。 <br>範例： `"prospect"`， `"jobs"`， `"articles"` |
| 布林值 | 為true或false的資料型別。 |
| 整數 | 代表整數的資料型別。 可以是正數、負數或零。 <br>範例： `-201`， `0`， `412` |
| 陣列 | 一種資料型別，由一組其他常值組成。 它使用方括弧將不同值分組，並使用逗號分隔不同值。<br> **注意：**&#x200B;您無法直接存取陣列中專案的屬性。<br> 範例： `[1, 4, 7]`， `["US", "FR"]` |

>[!CAUTION]
>
>個人化運算式無法使用&#x200B;**xEvent**&#x200B;變數。 對xEvent的任何參考都會導致驗證失敗。

## 最佳做法 {#best-practices}

在建立個人化運算式之前，請先檢閱這些語法規則。 大多數執行階段錯誤來自混合Handlebars和PQL內容。

**使用正確的條件區塊語法**

一律使用`{%#if%}` / `{%else if%}` / `{%else%}` / `{%/if%}`。 不支援`{% if %}` / `{% elseif %}` / `{% endif %}`語法。

```handlebars
{%#if profile.loyalty.tier = "gold"%}
Gold member content
{%else if profile.loyalty.tier = "silver"%}
Silver member content
{%else%}
Default content
{%/if%}
```

**請勿在`{{...}}` Handlebars區塊中呼叫PQL函式**

`{{...}}`僅解析Handlebars變數和協助程式 — 它不會評估PQL。 將`upperCase()`之類的PQL函式包裝在`{{...}}`內會導致「找不到協助程式」錯誤。 改用`{%= ... %}`：

| 不正確 | 正確 |
|-----------|---------|
| `{{upperCase(cleanName)}}` | `{%= upperCase(cleanName) %}` |

**結合`{{#each}}`與`{%#if%}`**&#x200B;時使用具名回圈別名

`this.field`是由Handlebars轉譯器解析，但不是由`{%#if%}`條件內的PQL評估器解析。 定義具有`as |item|`的具名別名，讓兩個內容都能解析欄位：

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending.
  {%/if%}
{{/each}}
```

**在循環之前，將PQL函式結果指派給變數**

無法直接在`{{#each}}`中呼叫PQL UDF （例如`topN`）。 先使用`{% let %}`評估它們，然後反複檢視結果：

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

**使用`{% let %}`以避免重複函式呼叫**

當計算值需要超過一次，請將其儲存在變數中。 這樣可改善可讀性，並防止重複評估：

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}}, your code is: WELCOME-{%= upperCase(cleanName) %}
```

**對`dateDiff`**&#x200B;使用正確的引數順序

`dateDiff(start, end)`會先採用較早的日期。 若要計算未來日期前的剩餘天數，請將目前日期傳入第一個引數：

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
```

**在PQL中使用`=`進行相等比較，而不是`==`**

PQL使用單一`=`運運算元來相等。 使用`==`會導致語法錯誤。

**在連字欄位名稱使用反引號 — 僅在PQL運算式中**

如果XDM結構描述欄位名稱包含連字型大小（例如`order-total`），請以反引號將其包裝，以防止將連字型大小剖析為減法運運算元。 這僅在`{%= ... %}`個PQL運算式中才受支援，在`{{...}}`個Handlebars區塊中則不受支援：

```sql
{%= profile.events.`order-total` > 100 %}
```

如需可直接複製到內容中的現成運算式，請參閱[Personalization配方](personalization-recipes.md)。

## 快速參考 {#quick-reference}

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

>[!BEGINTABS]

>[!TAB 概觀]

**TL；DR**

此頁面說明Journey Optimizer中的Handlebars和PQL個人化語法 — 其一般規則、保留關鍵字、名稱空間結構、型別系統，以及避免常見執行階段錯誤的最佳實務。

**個意圖**

* 瞭解何時使用Handlebars (`{{...}}`)與PQL (`{%= ... %}`)語法
* 套用一般語法規則：保留字元、區分大小寫、HTML逸出、反斜線處理
* 正確逸出保留關鍵字和特殊屬性索引鍵（連字名稱、數值事件ID）
* 比較或傳遞不相符型別的值時套用型別強制
* 從可用名稱空間參考個人化：設定檔、對象、選件
* 遵循最佳實務以避免最常見的執行階段和驗證錯誤

>[!TAB 字彙]

* **Handlebars**：用於轉譯屬性、在陣列上循環以及呼叫區塊協助程式的`{{...}}`範本語法；預設為HTML-escapes輸出。 *（產品特定）*
* **Profile Query Language (PQL)**：用於呼叫內建函式（例如`upperCase()`、`formatDate()`）和評估條件運算式的`{%= ... %}`運算式語法。 *（產品特定）*
* **三重儲存(`{{{ }}}`)**：輸出不含HTML逸出值的Handlebars語法變體，當值本身包含不應編碼的HTML字元時很有用。
* **保留關鍵字**：無法直接做為欄位或變數名稱使用的PQL識別碼(`next`、`last`、`this`)；當結構描述欄位使用這些名稱之一時，必須以反引號包住。
* **型別強制轉換**：在PQL中比較或算術之前，必須使用`stringToNumber()`或`toBool()`之類的函式，將值從一個資料型別明確轉換成另一個（例如字串→數字）。
* **名稱空間**：個人化資料的最上層群組 — 設定檔、對象、選件 — 每個群組都有自己的路徑結構和存取規則。
* **區塊協助程式**：由`#`在協助程式名稱和相符的結尾`/`之前識別的Handlebars協助程式，用於區塊建構，例如`{{#each}}`。

>[!TAB 術語]

* **正式名稱：** Handlebars — 針對`{{...}}`語法； PQL — 針對`{%= ... %}`語法
* **請勿混淆：** `{{...}}` （Handlebars — 轉譯變數和協助程式，HTML逸出） ≠ `{%= ... %}` （PQL — 評估函式和運算式） ≠ `{%#if%}` / `{%/if%}` （條件區塊語法，百分比大括弧）
* **請勿混淆：** `{{profile.person.name}}` （單一儲存 — HTML逸出的輸出）≠ `{{{profile.person.name}}}` （三重儲存 — 未逸出的輸出）
* **請勿混淆：**&#x200B;保留關鍵字反勾逸出（同時適用於`{{...}}`和`{%= ... %}`）≠連字鍵反勾逸出（僅支援`{%= ... %}`個PQL運算式中，不支援`{{...}}`）
* **請勿混淆：** `=` （PQL等式運運算元 — 正確） ≠ `==` （無效的PQL — 造成語法錯誤）

>[!TAB 護欄與限制]

* `xEvent`變數在個人化運算式中無法使用；對`xEvent`的任何參考都會導致驗證失敗。
* `{{...}}` Handlebars區塊內的PQL函式呼叫將失敗；請改用`{%= ... %}`。
* 不支援`{% if %}` / `{% elseif %}` / `{% endif %}`條件語法；請使用`{%#if%}` / `{%else if%}` / `{%/if%}`。
* 僅在PQL運算式(`{%= ... %}`)中支援連字欄位名稱的退格逸出。 在`{{...}}` Handlebars內插中，反勾語法失敗 — 但連字欄位名稱仍可直接參照（例如`{{profile.my-custom-field}}`）。
* 保留關鍵字(`next`， `last`， `this`)在做為結構描述欄位名稱時，必須用反引號括住；同時適用於`{{...}}`和`{%= ... %}`。
* 不支援單一反斜線`\`做為常值函式引數；請使用雙反斜線`\\`。
* PQL為強型別；比較或算術中不相符的型別需要使用`stringToNumber()`、`toBool()`或類似的強制函式進行明確轉換。

>[!TAB 常見問題集]

**問：何時應使用`{{...}}` （何時應使用`{%= ... %}`）？**

使用`{{...}}` (Handlebars)來轉譯屬性值、陣列上的回圈，以及呼叫區塊協助程式。 使用`{%= ... %}` (PQL)呼叫內建函式，例如`upperCase()`和`formatDate()`，並評估條件運算式。

**問：如何輸出不使用HTML編碼的值？**

使用三重儲存`{{{ }}}`而非`{{...}}`。 單大括弧Handlebars HTML-escapes輸出（例如，`&`變成`&amp;`）；三重棧疊略過逸出。

**問：什麼是PQL中的正確相等運運算元？**

在PQL中使用單一`=`進行相等比較。 使用`==`是語法錯誤。

**問：我如何參照名稱是保留關鍵字的結構描述欄位（例如`next`、`last`、`this`）？**

以反引號括住它： `{{profile.person.\`next\&#39;.name&rbrace;&rbrace;&#39;。 這同時適用於Handlebars路徑和PQL運算式。

**問：我可以在`{{...}}` Handlebars區塊中呼叫PQL函式嗎？**

沒有。 `{{...}}`僅解析Handlebars變數和協助程式。 `{{...}}`內的PQL函式造成「找不到協助程式」錯誤。 請改用`{%= functionName(...) %}`。

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 7fa07aa5 -->
