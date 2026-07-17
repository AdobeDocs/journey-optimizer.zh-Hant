---
solution: Journey Optimizer
product: journey optimizer
title: 事件轉換器指南
description: 瞭解如何在Adobe Journey Optimizer中設定忠誠度挑戰事件定義的結構描述和轉換器設定。
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="私人測試版" type="Informative"
mini-toc-levels: 1
exl-id: d3ad85f0-7f7e-40ab-b8c4-fc0c1234be87
feature_v2: []
subfeature_v2: []
source-git-commit: 762afe791cc1fa826b7a9f35f6f54591590bab7c
workflow-type: tm+mt
source-wordcount: 2015
ht-degree: 1%

---

# 事件轉換器指南 {#event-transformer-guide}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_event_transformer"
>title="事件轉換器指南"
>abstract="使用本指南來設定忠誠度挑戰事件定義的結構描述驗證和轉換器運算式。"

>[!BEGINSHADEBOX]

**目錄**

[開始應對忠誠度挑戰](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**建立和管理挑戰**

* [存取及管理挑戰與工作](access-loyalty-challenges.md)
* [創造挑戰](create-challenges.md)
* [建立任務](create-tasks.md)
* [監視忠誠度挑戰績效](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**設定並整合**

* [設定忠誠度挑戰](loyalty-admin.md)
* [獎勵定義指南](reward-definition-guide.md)
* **事件轉換器指南** ◀︎ **您在這裡**
* [熟客資料與資料集](loyalty-data-and-datasets.md)
* [忠誠度挑戰API參考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中。 如需[!DNL Journey Optimizer]中發行週期與可用性階段的完整詳細資訊，請參閱[發行週期](../rn/releases.md)。

在將客戶交易套用至忠誠度挑戰之前，必須採用「挑戰服務」可瞭解的&#x200B;**Adobe忠誠度事件**&#x200B;格式。 客戶事件（來自POS系統、行動應用程式、電子商務平台或任何其他來源）通常會使用客戶自己的資料結構。 **事件轉換器**&#x200B;會橋接此間隙，不需要變更上游系統。

## 概觀

**事件定義**&#x200B;會告訴平台兩件事：

* **要宣告哪些事件** — 如何識別傳入的事件屬於此定義（比對）
* **如何重新設定其形狀** — 將客戶的欄位對應至忠誠度事件格式（轉換）的[JSONata](https://docs.jsonata.org/overview)運算式

每個組織可以設定多個事件定義。 平台會依序評估這些變數，並套用符合的第一個變數。 不符合任何定義的事件會落入原生內嵌（請參閱[遞補 — 原生熟客活動](#fallback--native-loyalty-events)）。

## Adobe熟客活動格式

每個事件定義都必須產生以下格式的JSON物件。 這是「挑戰服務」處理的輸入。

```json
{
  "_id":              "string — optional; used for duplicate detection if enabled",
  "event_name":       "string — used for internal metrics and reporting only (e.g. 'purchase', 'visit')",
  "timestamp":        "ISO 8601 date-time string — when the event occurred",
  "utc_offset":       "string — UTC offset of the store or device (e.g. '-07:00'); required for daypart matching",
  "location_id":      "string — optional; store or location identifier",
  "transaction_id":   "string — optional; dedup key for the transaction",
  "loyalty_identity": {
    "id": "string — the member's loyalty ID"
  },
  "item_list": [
    {
      "item_set":   ["string", "..."],  // one or more identifiers — SKU, category, event code, etc.
      "item_name":  "string — optional human-readable label",
      "quantity":   1,                  // integer; how many units
      "unit_price": 4.99,               // float; price per unit
      "sub_total":  4.99                // float; line total (quantity × unit_price)
    }
  ]
}
```

### 欄位附註

| 欄位 | 必要 | 附註 |
|--------------------------------|--------------------|-------|
| `loyalty_identity` | **是** | 必須包含`id` — 成員的忠誠度識別碼。 |
| `item_list` | **是** | 必須至少包含一個專案。 空白`item_list`會導致事件因無效而被拒絕。 |
| `item_set` | **是** （每個專案） | 此陣列中的識別碼是挑戰任務包含/排除清單的相符專案。 包含每個相關的識別碼 — SKU、產品類別、部門代碼、事件名稱 — 以便任務篩選器可正確運作。 |
| `timestamp` | **是** | 用於日期視窗評估。 必須是ISO 8601。 |
| `utc_offset` | 建議 | 日時段比對和計算連續日連線時需要。 如果省略，則會略過時段評估和連續日期計數。 |
| `_id` | 無 | 如果已為組織啟用重複資料偵測，Challenge Service會拒絕已處理`_id`的事件。 |
| `sub_total` | 無 | 用於支出臨界值工作。 如果省略，則專案貢獻零支出。 |

## 事件定義欄位

| 欄位 | 類型 | 必要 | 說明 |
|--------------------------------|------------------|----------------------|-------------|
| `guid` | 字串 | 否（系統指派） | 建立時指派的唯一識別碼。 唯讀。 |
| `name` | 字串 | **是** | 人類可讀的標籤，例如`"Starbucks POS Purchase"`。 |
| `xdmSchemaId` | 字串 | 否* | XDM結構描述ID用於比對透過&#x200B;**DCCS擷取路由**&#x200B;到達的事件。 平台會讀取內嵌在傳入事件中的結構描述參考，並將其與此值比較。 |
| `identifierPath` | 字串 | 否* | 事件JSON中的點標籤法路徑，用來比對透過&#x200B;**直接HTTP路由(adobe.io)**&#x200B;到達的事件。 平台會讀取此路徑的值，並根據`identifier`檢查它。 |
| `identifier` | 字串陣列 | 無 | 預期值為`identifierPath`。 如果提供且非空白，則路徑上的值必須符合這些值之一。 如果為空，則路徑中具有值的任何事件都會相符。 |
| `schema` | 字串 | 否 | [JSON結構描述](https://json-schema.org/)檔案（作為JSON字串），用於在轉換之前驗證傳入的事件。 如果驗證失敗，則會以描述性錯誤拒絕事件。 |
| `transformer` | 字串 | **是** | 將傳入事件對應至Adobe忠誠度事件格式的JSONata運算式。 |

\*至少必須提供`xdmSchemaId`或`identifierPath`其中之一。

## 比對的運作方式

相符策略取決於事件到達平台的方式：

**DCCS擷取路由** — 透過資料收集核心服務(DCCS)到達的事件在其信封中附有XDM結構描述參考。 平台會從`/body/xdmMeta/schemaRef/id`讀取結構描述ID，並將其與每個定義的`xdmSchemaId`做比較。 針對此路由的定義設定`xdmSchemaId`。

**直接HTTP路由(adobe.io)** — 透過adobe.io API直接發佈至平台的事件不包含XDM結構描述參考。 平台改為使用`identifierPath`周遊事件JSON，並檢查在那裡找到的值：
* 如果`identifier`不是空的：值必須符合其中一個設定的字串。
* 如果`identifier`是空的：任何在路徑有非null值的事件都是相符的。

針對此路由的定義設定`identifierPath` （以及選擇性的`identifier`）。

平台會依順序&#x200B;**逐步執行組織的事件定義**&#x200B;並套用第一個相符專案。 找到相符專案後，`xdmEntity`內文（針對DCCS事件）或完整事件內文（針對直接HTTP事件）會傳遞至轉換器。

## 寫入轉換器

`transformer`欄位是[JSONata](https://docs.jsonata.org/overview)運算式。 它會接收傳入事件JSON作為其輸入，且必須傳回有效的Adobe忠誠度事件物件。

+++基本對應模式

將目標格式的每個最上層欄位對應至來源事件中的對應路徑：

```jsonata
{
  "_id":            sourceEvent._id,
  "event_name":     sourceEvent.eventType,
  "timestamp":      sourceEvent.timestamp,
  "utc_offset":     sourceEvent.storeInfo.utcOffset,
  "location_id":    sourceEvent.storeInfo.storeId,
  "transaction_id": sourceEvent.transaction.id,
  "loyalty_identity": {
    "id": sourceEvent.member.loyaltyId
  },
  "item_list": sourceEvent.transaction.items.{
    "item_set":   [itemSku, itemCategory],
    "item_name":  itemDescription,
    "quantity":   quantity,
    "unit_price": unitPrice,
    "sub_total":  lineTotal
  }
}
```

+++

+++以硬式編碼撰寫事件名稱

如果符合此定義的所有事件都代表相同的邏輯活動，請對`event_name`進行硬式編碼：

```jsonata
{
  "event_name": "in-store-purchase",
  ...
}
```

`event_name`用於內部量度和報告。 它不用作任務篩選 — 任務資格由`item_set`內容決定，而不是事件名稱。

+++

+++DCCS/XDM事件的對應身分識別

對於透過DCCS路由到達的事件，成員的身分通常會在標準XDM `identityMap`欄位中攜帶，而不是在自訂租使用者屬性中攜帶。 `identityMap`是由名稱空間輸入的對應 — 索引鍵本身就是名稱空間名稱，而值是身分識別物件的陣列。

```jsonata
"loyalty_identity": {
  "id": identityMap.Email[0].id
}
```

* **名稱空間替代：**&#x200B;以貴組織用於忠誠會員的任何名稱空間取代`Email` — `Loyalty`、`ECID`、`CRMID`等。永遠從儲存主要忠誠度設定檔身分的名稱空間讀取。

* **一律使用`[0]`：** `identityMap.Email`為陣列。 如果沒有索引，如果存在多個身分，則JSONata會傳回序列而不是單一值，並且`loyalty_identity.id`會成為清單。 將其釘選到第一個具有`[0]`的專案。

* **避免身分識別的自訂租使用者欄位：**&#x200B;自訂欄位群組有時會公開電子郵件形式的欄位（例如`_yourtenant.identification.core.email`）。 在範例資料中，這會傳回值且看起來是正確的，但在生產事件中，它通常是空的。 可靠的身分來源一律為`identityMap`。

+++

+++正在建置`item_set`

`item_set`是字串識別碼的陣列。 包含您的挑戰任務可能篩選的每個欄位：

```jsonata
"item_set": [itemSku, productCategory, departmentCode]
```

對於非交易事件（簽入、調查完成、自訂觸發器），單一識別碼就足夠了：

```jsonata
"item_set": [eventName]
```

+++

+++對應`unit_price`

`unit_price`應為單價。 有些來源結構描述會儲存明細總計（價格×數量）。 如果您的來源欄位是明細行總計，請除以數量以取得單價：

```jsonata
"unit_price": priceTotal / quantity
```

> 僅當來源欄位為行總計時除。 如果已經儲存單價，請直接對應 — 將單價除以數量將會自動產生錯誤值。

+++

+++衍生`transaction_id`

若您的來源事件不包含交易識別碼，則可從時間戳記衍生出穩定識別碼：

```jsonata
"transaction_id": "txn_" & $string($toMillis(timestamp))
```

這會將ISO時間戳記轉換為epoch毫秒，並為指定事件產生決定性的值。 使用您平台自己的ID產生函式（如有）。

+++

+++使用JSONata函式

提供完整的JSONata函式館。 有用的範例：

```jsonata
/* String concatenation */
"item_set": [skuId & ':' & categoryId]

/* Number formatting */
"item_set": ["spend:" & $formatNumber(totalAmount, '0.00')]

/* Conditional field */
"event_name": eventType ? eventType : "unknown"

/* Array transformation */
"item_list": items.{ "item_set": [sku], "quantity": qty, "sub_total": price * qty }
```

+++

## 範例

+++範例1 — 簡單自訂事件（非交易式）

**案例：**&#x200B;行動應用程式傳送簽到事件。 沒有條列專案 — 事件本身是符合資格的活動。

**傳入事件：**

```json
{
  "_id":       "evt-001",
  "eventName": "store-checkin",
  "timestamp": "2025-10-15T14:22:00Z",
  "storeId":   "STORE-042",
  "member": {
    "loyaltyId": "LM-8827361"
  }
}
```

**事件定義：**

```json
{
  "name":           "Mobile Store Check-In",
  "identifierPath": "eventName",
  "identifier":     ["store-checkin"],
  "transformer":    "{\"_id\": _id, \"event_name\": eventName, \"timestamp\": timestamp, \"location_id\": storeId, \"loyalty_identity\": {\"id\": member.loyaltyId}, \"item_list\": [{\"item_set\": [eventName], \"quantity\": 1}]}"
}
```

**格式化的轉換器（可讀性）：**

```jsonata
{
  "_id":        _id,
  "event_name": eventName,
  "timestamp":  timestamp,
  "location_id": storeId,
  "loyalty_identity": {
    "id": member.loyaltyId
  },
  "item_list": [
    {
      "item_set": [eventName],
      "quantity": 1
    }
  ]
}
```

**輸出Adobe忠誠度事件：**

```json
{
  "_id":        "evt-001",
  "event_name": "store-checkin",
  "timestamp":  "2025-10-15T14:22:00Z",
  "location_id": "STORE-042",
  "loyalty_identity": { "id": "LM-8827361" },
  "item_list": [{ "item_set": ["store-checkin"], "quantity": 1 }]
}
```

沒有包含/排除限制的挑戰任務會將此事件計為合格造訪 — 單一`item_set`專案`["store-checkin"]`符合允許所有專案的任何任務。

+++

+++範例2 — 包含條列專案的POS購買

**案例：**&#x200B;銷售點系統傳送交易裝載。 每個明細專案都有一個SKU且屬於類別。 挑戰任務使用SKU和類別來判斷符合條件。

**傳入事件：**

```json
{
  "_id":       "txn-20251015-4492",
  "timestamp": "2025-10-15T14:35:00Z",
  "storeInfo": {
    "storeId":   "STORE-042",
    "utcOffset": "-07:00"
  },
  "transaction": {
    "transactionId": "4492",
    "items": [
      { "sku": "COFFEE-001", "category": "BEVERAGE", "qty": 2, "unitPrice": 4.50, "lineTotal": 9.00 },
      { "sku": "MUFFIN-007", "category": "FOOD",     "qty": 1, "unitPrice": 3.25, "lineTotal": 3.25 }
    ]
  },
  "member": {
    "loyaltyId": "LM-8827361"
  }
}
```

**事件定義：**

```json
{
  "name":           "Retail POS Purchase",
  "identifierPath": "transaction.transactionId",
  "identifier":     [],
  "transformer":    "{\"_id\": _id, \"event_name\": \"purchase\", \"timestamp\": timestamp, \"utc_offset\": storeInfo.utcOffset, \"location_id\": storeInfo.storeId, \"transaction_id\": transaction.transactionId, \"loyalty_identity\": {\"id\": member.loyaltyId}, \"item_list\": transaction.items.{\"item_set\": [sku, category], \"quantity\": qty, \"unit_price\": unitPrice, \"sub_total\": lineTotal}}"
}
```

**格式化的轉換器：**

```jsonata
{
  "_id":            _id,
  "event_name":     "purchase",
  "timestamp":      timestamp,
  "utc_offset":     storeInfo.utcOffset,
  "location_id":    storeInfo.storeId,
  "transaction_id": transaction.transactionId,
  "loyalty_identity": {
    "id": member.loyaltyId
  },
  "item_list": transaction.items.{
    "item_set":   [sku, category],
    "quantity":   qty,
    "unit_price": unitPrice,
    "sub_total":  lineTotal
  }
}
```

**輸出Adobe忠誠度事件：**

```json
{
  "_id":            "txn-20251015-4492",
  "event_name":     "purchase",
  "timestamp":      "2025-10-15T14:35:00Z",
  "utc_offset":     "-07:00",
  "location_id":    "STORE-042",
  "transaction_id": "4492",
  "loyalty_identity": { "id": "LM-8827361" },
  "item_list": [
    { "item_set": ["COFFEE-001", "BEVERAGE"], "quantity": 2, "unit_price": 4.50, "sub_total": 9.00 },
    { "item_set": ["MUFFIN-007", "FOOD"],     "quantity": 1, "unit_price": 3.25, "sub_total": 3.25 }
  ]
}
```

具有`include: ["BEVERAGE"]`的挑戰任務會看到咖啡條列專案符合資格（其`item_set`包含`"BEVERAGE"`）並累積$9.00的支出用於該任務。 將會排除鬆餅條列專案。

+++

+++範例3 — AEP體驗事件（XDM結構描述比對）

**案例：**&#x200B;事件流經Adobe Journey Optimizer。 傳入事件是具有已知結構描述ID的XDM體驗事件。 平台使用結構描述ID進行比對，而非路徑/值檢查。

**傳入的XDM實體內文** （從AJO事件擷取的`xdmEntity`）：

```json
{
  "_brandname": {
    "identities": {
      "loyaltyId": "LM-8827361"
    },
    "transactions": {
      "transactionId": "TXN-9901",
      "storeNumber":   "042",
      "utcOffset":     "-07:00",
      "lineItems": [
        { "skuNumber": "11143053", "priceAmount": 345, "qty": 1, "category": "BEVERAGE" },
        { "skuNumber": "11161387", "priceAmount": 495, "qty": 1, "category": "FOOD" }
      ],
      "totalAmount": 840
    }
  },
  "_id":       "87c0cccf-5809-38e0-a703-3994e80173ab",
  "timestamp": "2025-07-04T16:03:32.000Z"
}
```

**事件定義：**

```json
{
  "name":        "AJO Brand Purchase",
  "xdmSchemaId": "https://ns.adobe.com/brandname/schemas/purchase-event-v1",
  "transformer":  "{\"_id\": _id, \"event_name\": \"purchase\", \"timestamp\": timestamp, \"utc_offset\": _brandname.transactions.utcOffset, \"location_id\": _brandname.transactions.storeNumber, \"transaction_id\": _brandname.transactions.transactionId, \"loyalty_identity\": {\"id\": _brandname.identities.loyaltyId}, \"item_list\": _brandname.transactions.lineItems.{\"item_set\": [skuNumber, category], \"quantity\": qty, \"unit_price\": priceAmount, \"sub_total\": priceAmount * qty}}"
}
```

**格式化的轉換器：**

```jsonata
{
  "_id":            _id,
  "event_name":     "purchase",
  "timestamp":      timestamp,
  "utc_offset":     _brandname.transactions.utcOffset,
  "location_id":    _brandname.transactions.storeNumber,
  "transaction_id": _brandname.transactions.transactionId,
  "loyalty_identity": {
    "id": _brandname.identities.loyaltyId
  },
  "item_list": _brandname.transactions.lineItems.{
    "item_set":   [skuNumber, category],
    "quantity":   qty,
    "unit_price": priceAmount,
    "sub_total":  priceAmount * qty
  }
}
```

> **注意：**&#x200B;當事件符合XDM結構描述ID時，轉換器只會接收事件的`xdmEntity`部分，而不是外部AJO信封。 您的轉換器運算式中的所有路徑都是相對於XDM實體本文。

+++

## 新增JSON結構描述驗證（選用）

如果您希望平台在嘗試轉換之前先驗證傳入事件的結構，請將`schema`欄位設定為編碼為JSON字串的[JSON結構描述](https://json-schema.org/draft-04)檔案。

結構描述驗證失敗的事件會在轉換執行前被拒絕。 錯誤回應包含特定驗證失敗，因此可輕鬆診斷格式錯誤的上游事件。

+++結構描述範例（例如上述範例2）

```json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "type": "object",
  "required": ["_id", "timestamp", "transaction", "member"],
  "properties": {
    "_id":       { "type": "string" },
    "timestamp": { "type": "string", "format": "date-time" },
    "member": {
      "type": "object",
      "required": ["loyaltyId"],
      "properties": {
        "loyaltyId": { "type": "string" }
      }
    },
    "transaction": {
      "type": "object",
      "required": ["items"],
      "properties": {
        "transactionId": { "type": "string" },
        "items": {
          "type": "array",
          "items": {
            "type": "object",
            "required": ["sku", "qty", "lineTotal"],
            "properties": {
              "sku":       { "type": "string" },
              "category":  { "type": "string" },
              "qty":       { "type": "number" },
              "unitPrice": { "type": "number" },
              "lineTotal": { "type": "number" }
            }
          }
        }
      }
    }
  }
}
```

+++

在事件定義的`schema`欄位中傳遞此結構描述作為縮制的JSON字串。

## 遞補 — 原生熟客活動

如果沒有任何事件定義符合傳入事件，平台會嘗試將其直接擷取為原生Adobe忠誠度事件。 如果裝載已符合上述的忠誠度事件格式，則不需要轉換器，事件會依原樣套用。 這可讓已預先格式化其事件的客戶完全略過轉換。

## API 參考

所有事件定義作業都使用基底路徑`/loyalty/metadata/config/events`。

+++建立事件定義

```http
POST /loyalty/metadata/config/events
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":           "Retail POS Purchase",
  "identifierPath": "transaction.transactionId",
  "identifier":     [],
  "transformer":    "{ ... }"
}
```

+++

+++清單事件定義

```http
GET /loyalty/metadata/config/events
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
```

+++

+++更新事件定義

```http
PUT /loyalty/metadata/config/events/{eventId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":        "Retail POS Purchase (v2)",
  "transformer": "{ ... updated expression ... }"
}
```

+++

+++刪除事件定義

```http
DELETE /loyalty/metadata/config/events/{eventId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
```

+++

## 轉換器驗證

儲存事件定義時，會驗證JSONata運算式的語法。 如果運算式無效，API會傳回`422`錯誤，其中包含剖析失敗的描述。

若要在部署之前測試轉換器，請使用[JSONata Exerciser](https://try.jsonata.org/) — 將您的來源事件貼上為輸入，並貼上轉換器運算式，以驗證輸出符合預期的熟客事件格式。

## 常見陷阱

這些錯誤都會在簡單的單一專案測試裝載上順利執行，這正是它們未偵測到的原因。 在部署之前，請務必根據包含兩個或多個產品的裝載測試您的轉換器。

+++建置一個物件，而不是在陣列上對應

最常見的錯誤。 將單一物件常值與`productListItems.SKU`搭配使用，會將每個SKU和每個數量拉入集中順序，而非針對每項產品產生一個條列專案。

**✗將所有專案摺疊為一個：**

```jsonata
"item_list": [
  {
    "item_set": [ productListItems.SKU ],
    "quantity": productListItems.quantity
  }
]
```

使用兩個產品時，`item_set`會同時儲存兩個SKU，`quantity`會變成類似`[1, 4]`的陣列。

**✓每個產品一個條列專案：**

```jsonata
"item_list": [
  productListItems.{
    "item_set": [SKU],
    "quantity": quantity
  }
]
```

每個產品會執行一次`.{ }`對應，因此每個產品都會成為自己的專案。

+++

+++忘記身分上的陣列索引

`identityMap.Email`是一個陣列。 若沒有`[0]`，如果設定檔在該名稱空間中有多個身分，`id`會變成值清單，而非單一字串。

**✗** `identityMap.Email.id`

**✓** `identityMap.Email[0].id`

+++

+++從自訂租使用者欄位取得身分

自訂欄位群組有時會公開電子郵件形式的欄位，例如`_yourtenant.identification.core.email`。 在範例資料中，它會傳回值且看起來是正確的，但在生產事件中，它經常是空的，而導致`loyalty_identity.id`傳出null。 一律使用`identityMap`做為身分來源。

+++

+++巢狀陣列漏入`item_set`

將類別欄位新增到`item_set`看起來很簡單，但如果`productCategories`本身是陣列，則結果會以無法預測的方式展開。

**✗可能會產生比預期更多的專案：**

```jsonata
"item_set": [SKU, productCategories.categoryID]
```

具有三個類別的產品會產生具有四個值的`item_set`。

**✓為巢狀陣列建立索引，以取得正好一個值：**

```jsonata
"item_set": [SKU, productCategories[0].categoryID]
```

+++

+++`item_list`為空白或遺失

具有空白或不存在`item_list`的事件會因無效而被拒絕。 對於非異動事件（簽入、自訂觸發器），沒有自然的條列專案，因此產生合成的專案：

```jsonata
"item_list": [{ "item_set": [eventName], "quantity": 1 }]
```

+++

+++`timestamp`作為Unix紀元整數，而非ISO 8601

平台必須有ISO 8601字串。 如果您的來源事件包含紀元以來的毫秒數，請將其轉換：

```jsonata
"timestamp": $fromMillis(timestamp)
```

+++

+++已省略`utc_offset`

如果沒有`utc_offset`，則會略過日時段比對和連續日連續連續計數。 將存放區或裝置UTC位移與來源事件對應到可用位置。

+++

+++DCCS事件中相對於AJO信封的轉換器路徑

對於DCCS事件，轉換器只會接收`xdmEntity`內文，而不會接收外部AJO信封。 所有路徑都必須相對於XDM實體根。 如果您的運算式參考位於外部信封中的欄位（例如`/body/xdmMeta/...`），將無法找到這些欄位，而且會無訊息地產生null。

+++
