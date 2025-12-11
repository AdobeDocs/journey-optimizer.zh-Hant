---
solution: Journey Optimizer
product: journey optimizer
title: 反複運算內容資料
description: 瞭解如何使用Handlebars語法，從各種內容來源反複處理陣列
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
hide: true
hidefromtoc: true
keywords: 運算式，編輯器， handlebars，反複專案，陣列，內容，個人化
source-git-commit: 20421485e354b0609dd445f2db2b7078ee81d891
workflow-type: tm+mt
source-wordcount: '3008'
ht-degree: 0%

---

# 反複運算內容資料 {#personalization-contexts}

瞭解如何使用Handlebars反複運算語法來顯示訊息中各種來源的動態資料清單，包括事件、自訂動作回應和其他內容資料。

## 概觀 {#overview}

在[訊息個人化](personalize.md)期間，Journey Optimizer可讓您存取來自多個來源的內容資料。 您可以使用原生管道（[電子郵件](../email/get-started-email-design.md)、[推播](../push/create-push.md)、[簡訊](../sms/create-sms.md)）中的Handlebars語法，從這些來源重複處理陣列，以顯示動態內容，例如產品清單、建議或其他重複元素。

**可用的內容來源：**

* **[事件](#event-data)**：歷程事件（商業事件、單一事件）的資料
* **[自訂動作回應](#custom-action-responses)**：透過自訂動作從外部API呼叫傳回的資料
* **[資料集查詢](#dataset-lookup)**：從Adobe Experience Platform資料集擷取的擴充資料
* **[技術屬性](#technical-properties)**：歷程中繼資料，例如歷程ID和補充識別碼
* **[歷程內容](#other-contexts)**：執行期間可存取的其他歷程相關資料

本指南會說明如何在訊息中逐一檢視陣列，以及如何在設定歷程活動時使用陣列。 從[Handlebars反複專案語法](#syntax)開始，以瞭解訊息個人化基本概念，或跳至[使用歷程運算式中的陣列](#arrays-in-journeys)，以瞭解如何將陣列資料傳遞至自訂動作和資料集查詢。

## Handlebars反複專案語法 {#syntax}

Handlebars提供`{{#each}}` [協助程式](functions/helpers.md)來反複處理陣列。 基本語法為：

```handlebars
{{#each arrayPath as |item|}}
  <!-- Access item properties here -->
  {{item.property}}
{{/each}}
```

**關鍵點：**

* 將`arrayPath`取代為您的陣列資料路徑
* 將`item`取代為您偏好的任何變數名稱（例如，`product`、`response`、`element`）
* 使用`{{item.propertyName}}`存取每個專案的屬性
* 您可以巢狀內嵌多重層級陣列的多個`{{#each}}`區塊

## 反複處理事件資料 {#event-data}

當您的歷程由[事件](../event/about-events.md)觸發時，事件資料可供使用。 這對於顯示歷程開始時所擷取的資料非常有用，例如購物車內容、訂單專案或表單提交。

>[!TIP]
>
>您可以將事件資料與其他來源結合。 如需範例，請參閱[結合多個內容來源](#combine-sources)。

### 事件的內容路徑

```handlebars
context.journey.events.<event_ID>.<fieldPath>
```

* `<event_ID>`：您在歷程中設定的事件唯一ID
* `<fieldPath>`：事件結構描述中欄位或陣列的路徑

### 範例：來自事件的購物車專案

如果您的[事件結構描述](../event/experience-event-schema.md)包含`productListItems`陣列（標準[XDM格式](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html?lang=zh-Hant){target="_blank"}），您可以顯示購物車內容，如下列範例所詳述。

+++ 檢視範常式式碼

```handlebars
{{#each context.journey.events.event_ID.productListItems as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}
```

+++

### 範例：事件中的巢狀陣列

對於巢狀結構，請使用巢狀`{{#each}}`區塊。

+++ 檢視範常式式碼

```handlebars
{{#each context.journey.events.event_ID.categories as |category|}}
  <h2>{{category.name}}</h2>
  <ul>
    {{#each category.items as |item|}}
      <li>{{item.title}}</li>
    {{/each}}
  </ul>
{{/each}}
```

+++

深入瞭解[最佳實務](#best-practices)中的巢狀結構。

## 反複處理自訂動作回應 {#custom-action-responses}

[自訂動作](../action/about-custom-action-configuration.md)回應包含從外部API呼叫傳回的資料。 這對於顯示您系統中的即時資訊非常有用，例如忠誠度點數、產品推薦、詳細目錄狀態或個人化優惠。

>[!NOTE]
>
>自訂動作必須設定回應裝載，才能使用此功能。 在[本節](../action/action-response.md#config-response)中瞭解更多資訊。 您也可以結合自訂動作回應與事件資料或資料集查詢 — 請參閱[結合多個內容來源](#combine-sources)以取得範例。

### 自訂動作的內容路徑

```handlebars
context.journey.actions.<actionName>.<fieldPath>
```

* `<actionName>`：您在歷程中設定的[自訂動作](../action/about-custom-action-configuration.md)名稱
* `<fieldPath>`：回應承載中欄位或陣列的路徑

### 範例：來自API的產品建議

若要反複運算自訂動作傳回的一系列產品建議，並將它們顯示為訊息中的個別卡片，請參閱下列範例。

+++ 檢視範常式式碼

**API回應：**

```json
{
  "recommendations": [
    {
      "productId": "12345",
      "productName": "Summer Jacket",
      "price": 89.99,
      "imageUrl": "https://example.com/jacket.jpg"
    },
    {
      "productId": "67890",
      "productName": "Running Shoes",
      "price": 129.99,
      "imageUrl": "https://example.com/shoes.jpg"
    }
  ]
}
```

**訊息個人化：**

```handlebars
<h2>Recommended for You</h2>
<div class="recommendations">
  {{#each context.journey.actions.GetRecommendations.recommendations as |item|}}
    <div class="product-card">
      <img src="{{item.imageUrl}}" alt="{{item.productName}}" />
      <h3>{{item.productName}}</h3>
      <p class="price">${{item.price}}</p>
    </div>
  {{/each}}
</div>
```

+++

### 範例：自訂動作的巢狀陣列

若要反複處理包含巢狀陣列（一個物件陣列，其中每個物件都包含另一個陣列）的自訂動作回應，請參閱以下範例。 此示範使用巢狀`{{#each}}`回圈來存取多個層級的資料。

+++ 檢視範常式式碼

**API回應：**

```json
{    
  "id": "84632848268632",    
  "responses": [
    { "productIDs": [1111, 2222, 3333] },
    { "productIDs": [4444, 5555, 6666] },
    { "productIDs": [7777, 8888, 9999] }
  ]
}
```

**訊息個人化：**

```handlebars
<h2>Product Groups</h2>
{{#each context.journey.actions.GetProducts.responses as |response|}}
  <div class="product-group">
    <ul>
      {{#each response.productIDs as |productID|}}
        <li>Product ID: {{productID}}</li>
      {{/each}}
    </ul>
  </div>
{{/each}}
```

+++

如需更複雜的巢狀模式，請參閱[最佳實務](#best-practices)。

### 範例：忠誠度層級優點

若要根據忠誠度狀態顯示動態福利，請參閱以下範例。

+++ 檢視範常式式碼

**API回應：**

```json
{
  "loyaltyTier": "gold",
  "benefits": [
    { "name": "Free shipping", "icon": "truck" },
    { "name": "20% discount", "icon": "percent" },
    { "name": "Priority support", "icon": "headset" }
  ]
}
```

**訊息個人化：**

```handlebars
<h2>Your {{context.journey.actions.GetLoyaltyInfo.loyaltyTier}} Member Benefits</h2>
<ul class="benefits">
  {{#each context.journey.actions.GetLoyaltyInfo.benefits as |benefit|}}
    <li>
      <span class="icon-{{benefit.icon}}"></span>
      {{benefit.name}}
    </li>
  {{/each}}
</ul>
```

+++

## 反複處理資料集查詢結果 {#dataset-lookup}

[資料集查詢活動](../building-journeys/dataset-lookup.md)可讓您在歷程執行階段期間，從[Adobe Experience Platform資料集](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh-Hant){target="_blank"}擷取資料。 擴充的資料會以陣列形式儲存，並可在訊息中反複顯示。

>[!AVAILABILITY]
>
>「資料集查詢」活動僅適用於一組有限的組織。 若想取得存取權，請聯絡您的 Adobe 代表。

在[本節](../building-journeys/dataset-lookup.md)中進一步瞭解設定資料集查詢活動。 結合事件資料時，資料集查詢特別強大 — 如需實際使用案例，請參閱[範例：使用資料集查詢](#combine-sources)擴充的事件資料。

### 資料集查詢的內容路徑

```handlebars
context.journey.datasetLookup.<activityID>.entities
```

* `<activityID>`：資料集查詢活動的唯一ID
* `entities`：從資料集擷取的擴充資料陣列

### 範例：資料集中的產品詳細資料

如果您使用資料集查詢活動根據SKU擷取產品資訊，請參閱以下範例。

+++ 檢視範常式式碼

**資料集查詢組態：**

* 查閱金鑰： `list(@event{purchase_event.products.sku})`
* 要傳回的欄位： `["SKU", "category", "price", "name"]`

**訊息個人化：**

```handlebars
<h2>Product Details</h2>
<table>
  <thead>
    <tr>
      <th>Product Name</th>
      <th>Category</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    {{#each context.journey.datasetLookup.3709000.entities as |product|}}
      <tr>
        <td>{{product.name}}</td>
        <td>{{product.category}}</td>
        <td>${{product.price}}</td>
      </tr>
    {{/each}}
  </tbody>
</table>
```

+++

### 範例：使用資料集資料篩選反複專案

若要在反複專案期間篩選資料集查詢結果，並僅顯示符合特定條件的專案（例如，來自特定類別的產品），請在`{{#if}}`回圈中使用條件`{{#each}}`陳述式。 請參閱下列範例。

+++ 檢視範常式式碼

```handlebars
<h2>Household Products</h2>
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {{#if product.category = "household"}}
    <div class="product">
      <h3>{{product.name}}</h3>
      <p>Price: ${{product.price}}</p>
    </div>
  {{/if}}
{{/each}}
```

+++

進一步瞭解[最佳實務](#best-practices)中的條件式篩選。

### 範例：從資料集查詢計算總計

若要在疊代資料集查閱結果時計算並顯示總計，請參閱以下範例。

+++ 檢視範常式式碼

```handlebars
{% let householdTotal = 0 %}
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {%#if product.category = "household"%}
    {% let householdTotal = householdTotal + product.price %}
  {%/if%}
{{/each}}

<p>Your household products total: ${{householdTotal}}</p>
```

+++

## 使用歷程技術屬性 {#technical-properties}

歷程技術屬性可讓您存取有關歷程執行的中繼資料，例如歷程ID和補充識別碼。 在與反複專案模式結合時，這些功能可能會很有用，尤其是根據特定歷程例項篩選陣列時。

### 可用的技術屬性

```handlebars
context.journey.technicalProperties.journeyUID
context.journey.technicalProperties.supplementalId
```

### 範例：使用補充識別碼篩選陣列專案

在事件觸發的具有陣列的歷程中使用補充識別碼時，您可以篩選以僅顯示目前歷程執行個體的相關專案。 進一步瞭解[本指南](../building-journeys/supplemental-identifier.md)中的補充識別碼。

**案例**：歷程是由多個預訂所觸發，但您只想要顯示觸發此歷程執行個體之特定預訂（以補充ID識別）的資訊。

+++ 檢視範常式式碼

```handlebars
{{#each context.journey.events.event_ID.bookingList as |booking|}}
  {%#if booking.bookingInfo.bookingNum = context.journey.technicalProperties.supplementalId%}
    <div class="booking-details">
      <h3>Your Booking: {{booking.bookingInfo.bookingNum}}</h3>
      <p>Destination: {{booking.bookingInfo.bookingCountry}}</p>
      <p>Date: {{booking.bookingInfo.bookingDate}}</p>
    </div>
  {%/if%}
{{/each}}
```

+++

### 範例：包含用於追蹤的歷程ID

若要在您的訊息中包含歷程ID以進行追蹤，請參閱下列範例。

+++ 檢視範常式式碼

```handlebars
<footer>
  <p>Journey Reference: {{context.journey.technicalProperties.journeyUID}}</p>
</footer>
```

+++

## 合併多個內容來源 {#combine-sources}

您可以將不同來源的資料合併成相同訊息，以建立豐富的個人化體驗。 本節顯示一起使用多個內容來源的實際範例。

**您可以合併的內容來源：**

* [事件資料](#event-data) + [自訂動作回應](#custom-action-responses)
* [事件資料](#event-data) + [資料集查詢](#dataset-lookup)
* [多個來源](#combine-sources) + [技術屬性](#technical-properties)

### 範例：具有即時詳細目錄的購物車專案

若要結合事件資料（購物車內容）與自訂動作資料（詳細目錄狀態），請檢視下列範例。

+++ 檢視範常式式碼

```handlebars
<h2>Your Cart</h2>
{{#each context.journey.events.cartEvent.productListItems as |product|}}
  <div class="cart-item">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}

<h2>We Also Recommend</h2>
{{#each context.journey.actions.GetRecommendations.items as |recommendation|}}
  <div class="recommendation">
    <h4>{{recommendation.name}}</h4>
    <p>${{recommendation.price}}</p>
    {{#if recommendation.inStock}}
      <span class="badge">In Stock</span>
    {{else}}
      <span class="badge out-of-stock">Out of Stock</span>
    {{/if}}
  </div>
{{/each}}
```

+++

### 範例：使用資料集查詢擴充了事件資料

若要結合[事件SKU](#event-data)與[資料集查詢](#dataset-lookup)的詳細產品資訊，請檢視下列範例。

+++ 檢視範常式式碼

```handlebars
<h2>Your Order Details</h2>
{{#each context.journey.events.orderEvent.productListItems as |item|}}
  <div class="order-item">
    <p><strong>SKU:</strong> {{item.SKU}}</p>
    <p><strong>Quantity:</strong> {{item.quantity}}</p>
    
    <!-- Enrich with dataset lookup data -->
    {{#each context.journey.datasetLookup.1234567.entities as |enrichedProduct|}}
      {{#if enrichedProduct.SKU = item.SKU}}
        <p><strong>Product Name:</strong> {{enrichedProduct.name}}</p>
        <p><strong>Category:</strong> {{enrichedProduct.category}}</p>
        <img src="{{enrichedProduct.imageUrl}}" alt="{{enrichedProduct.name}}" />
      {{/if}}
    {{/each}}
  </div>
{{/each}}
```

+++

### 範例：將多個來源與技術屬性結合

若要將多個內容來源（設定檔資料、事件資料、自訂動作和技術屬性）合併為單一訊息，請檢視下列範例。

+++ 檢視範常式式碼

```handlebars
<div class="personalized-content">
  <!-- Profile data -->
  <h1>Hello {{profile.person.name.firstName}},</h1>
  
  <!-- Event data iteration -->
  <h2>Your Recent Purchases</h2>
  {{#each context.journey.events.purchaseEvent.items as |purchase|}}
    <div class="purchase">
      <p>{{purchase.productName}} - ${{purchase.price}}</p>
    </div>
  {{/each}}
  
  <!-- Custom action response iteration -->
  <h2>Recommended for You</h2>
  {{#each context.journey.actions.GetPersonalizedRecs.recommendations as |rec|}}
    <div class="recommendation">
      <h3>{{rec.title}}</h3>
      <p>{{rec.description}}</p>
    </div>
  {{/each}}
  
  <!-- Technical properties -->
  <footer>
    <p class="fine-print">Journey ID: {{context.journey.technicalProperties.journeyUID}}</p>
  </footer>
</div>
```

+++

## 其他內容型別 {#other-contexts}

雖然本指南著重於陣列的疊代，但其他內容型別可用於個人化，通常不需要疊代。 您可以直接存取這些連結，而非透過下列連結：

* **[設定檔屬性](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}** (`profile.*`)：來自Adobe Experience Platform的個別設定檔欄位
* **[對象](../audience/about-audiences.md)** (`inAudience()`)：對象成員資格檢查
* **[優惠決定](../offers/get-started/starting-offer-decisioning.md)**：決定管理優惠
* **[Target屬性](../orchestrated/activities/channels.md#add-personalization)** （僅限協調的行銷活動）：在行銷活動畫布中計算的屬性
* **權杖** (`context.token`)：工作階段或驗證權杖

如需使用這些來源的完整個人化語法和範例，請參閱：

* [新增個人化](personalization-build-expressions.md)
* [個人化語法](personalization-syntax.md)

## 在歷程運算式中使用陣列 {#arrays-in-journeys}

雖然上一節著重於使用Handlebars在訊息個人化中反複處理陣列，您也可以在設定歷程活動時使用陣列。 本節說明如何在Journey運算式中使用來自事件的陣列資料，尤其是將資料傳遞至自訂動作或使用具有資料集查詢的陣列時。

>[!IMPORTANT]
>
>歷程運算式使用與Handlebars個人化不同的語法。 在歷程組態（例如自訂動作引數或條件）中，您會將[歷程運算式編輯器](../building-journeys/expression/expressionadvanced.md)與`first`、`all`和`serializeList`之類的函式搭配使用。 在訊息內容中，您使用Handlebars語法搭配`{{#each}}`回圈。

### 傳遞陣列值至自訂動作引數 {#arrays-to-custom-actions}

設定[自訂動作](../action/about-custom-action-configuration.md)時，您通常需要從事件陣列擷取值，並將它們當成引數傳遞。 本節說明常見模式。

深入瞭解如何在[傳遞集合至自訂動作引數](../building-journeys/collections.md#passing-collection)。

#### 從陣列擷取單一值

**使用案例**：從事件陣列取得特定欄位，以作為查詢引數傳遞至GET要求。

+++ 檢視範常式式碼

**範例案例**：從產品清單中擷取價格大於0的第一個SKU。

**事件結構描述範例**：

```json
{
  "commerce": {
    "productListItems": [
      { "SKU": "SKU-1", "priceTotal": 10.0 },
      { "SKU": "SKU-2", "priceTotal": 0.0 },
      { "SKU": "SKU-3", "priceTotal": 20.0 }
    ]
  }
}
```

**自訂動作組態**：

1. 在您的自訂動作中，使用型別`sku`設定查詢引數（例如`string`）
2. 將其標籤為`Variable`以允許動態值

**動作引數中的歷程運算式**：

```javascript
@event{YourEventName.commerce.productListItems.first(currentEventField.priceTotal > 0).SKU}
```

**說明**：

* `@event{YourEventName}`：參考您的歷程事件
* `.first(currentEventField.condition)`：傳回符合條件的第一個陣列專案
* `currentEventField`：代表事件陣列中的每個專案，因為您會在其中重複執行
* `.SKU`：從相符的專案中擷取SKU欄位
* 結果： `"SKU-1"` （適用於動作引數的字串）

深入瞭解`first`集合管理函式[中的](../building-journeys/expression/collection-management-functions.md)函式。

+++

#### 從陣列建立值清單

**使用案例**：建立以逗號分隔的ID清單，以作為查詢引數傳遞（例如，`/products?ids=sku1,sku2,sku3`）。

+++ 檢視範常式式碼

**自訂動作組態**：

1. 使用型別`ids`設定查詢引數（例如`string`）
2. 將其標籤為`Variable`

**歷程運算式**：

```javascript
serializeList(
  @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0).SKU},
  ",",
  true
)
```

**說明**：

* `.all(currentEventField.condition)`：傳回符合條件的所有陣列專案（傳回清單）
* `currentEventField`：代表事件陣列中的每個專案，因為您會在其中重複執行
* `.SKU`：專案清單以僅包含SKU值
* `serializeList(list, delimiter, addQuotes)`：將清單加入字串
   * `","`：使用逗號做為分隔符號
   * `true`：在每個字串元素周圍加上引號
* 結果： `"SKU-1,SKU-3"` （適用於查詢引數）

進一步瞭解：

* [&#39;所有&#39;](../building-journeys/expression/collection-management-functions.md)
* [&#39;serializeList&#39;](../building-journeys/functions/list-functions.md#serializeList)

自訂動作的集合處理包含在[將集合傳遞至自訂動作引數](../building-journeys/collections.md#passing-collection)中。

+++

#### 傳遞物件陣列至自訂動作

**使用案例**：傳送要求內文中的完整物件陣列(針對POST或具有內文的GET)。

+++ 檢視範常式式碼

**要求內文範例**：

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "Product A",
        "price": 20.1,
        "color": "blue"
      }
    ]
  }
}
```

**自訂動作組態**：

1. 在要求內文中將`products`定義為型別`listObject`
2. 將其標籤為`Variable`
3. 定義物件欄位： `id`、`name`、`price`、`color` （每個欄位都可以對應）

**歷程畫佈設定**：

1. 在進階模式中，設定集合運算式：

   ```javascript
   @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0)}
   ```

1. 在集合對應UI中：
   * 將`id`對應→`productListItems.SKU`
   * 將`name`對應→`productListItems.name`
   * 將`price`對應→`productListItems.priceTotal`
   * 將`color`對應→`productListItems.color`

Journey Optimizer會建構符合動作裝載結構的物件陣列。

>[!NOTE]
>
>使用事件陣列時，請使用`currentEventField`來參考每個專案。 對於資料來源集合(Adobe Experience Platform)，請使用`currentDataPackField`。 對於自訂動作回應集合，請使用`currentActionField`。

深入瞭解[將集合傳遞至自訂動作引數](../building-journeys/collections.md#passing-collection)。

+++

### 使用陣列進行資料集查詢 {#arrays-with-dataset-lookup}

使用[資料集查詢活動](../building-journeys/dataset-lookup.md)時，您可以傳遞一組值作為查詢索引鍵，以擷取擴充的資料。

**範例**：查詢事件陣列中所有SKU的產品詳細資料。

+++ 檢視範常式式碼

**資料集查詢組態**：

在查閱索引鍵欄位中，使用`list()`將陣列路徑轉換為清單：

```javascript
list(@event{purchaseEvent.productListItems.SKU})
```

這會建立要在資料集中查詢的所有SKU值清單。 結果可在`context.journey.datasetLookup.<activityID>.entities`以陣列形式提供，您可以在訊息中反複查詢（請參閱[反複查詢資料集查詢結果](#dataset-lookup)）。

+++

### 限制和模式 {#array-limitations}

在歷程中使用陣列時，請注意下列限制：

#### 在歷程流程中陣列上無動態回圈

歷程無法建立動態回圈，因為陣列中的每個專案會多次執行一個動作節點。 這是刻意為防止出現失控的效能問題。

**您無法執行的動作**：

* 為每個陣列專案動態執行一次自訂動作
* 根據陣列長度建立多個歷程分支

**改為建議的模式**：

1. **一次傳送所有專案**：將整個陣列或序列化清單傳遞給處理所有專案的單一自訂動作。 請參閱[從陣列](#arrays-to-custom-actions)建置值清單。

2. **使用外部彙總**：讓您的外部API接受多個ID，並在單一呼叫中傳回合併的結果。

3. **在AEP中預先計算**：使用[計算屬性](../audience/computed-attributes.md)從設定檔層級的陣列預先計算值。

4. **單一值擷取**：如果您只需要一個值，請使用`first`或`head`擷取它。 請參閱[從陣列](#arrays-to-custom-actions)擷取單一值。

深入瞭解[護欄和限制](../start/guardrails.md)。

#### 陣列大小考量

大型陣列可能會影響歷程效能：

* **事件陣列**：將事件裝載總數保持在50KB以下
* **自訂動作回應**：回應裝載應小於100KB
* **資料集查閱結果**：限制查閱金鑰和傳回實體的數目

### 完成範例：自訂動作的事件陣列 {#complete-example}

以下是完整的工作流程，說明如何將事件陣列與自訂動作搭配使用。

**案例**：當使用者放棄購物車時，請將購物車資料傳送至外部建議API以取得個人化建議，然後在電子郵件中顯示這些建議。

+++ 檢視範常式式碼

**步驟1：設定自訂動作**

建立自訂動作「GetCartRecommendations」：

* **方法**： POST
* **URL**： `https://api.example.com/recommendations`
* **要求內文**：

```json
{
  "cartItems": [
    {
      "sku": "string",
      "price": 0,
      "quantity": 0
    }
  ]
}
```

* 將`cartItems`標示為型別`listObject`和`Variable`
* 定義欄位： `sku` （字串）、`price` （數字）、`quantity` （整數）

深入瞭解[設定自訂動作](../action/about-custom-action-configuration.md)。

**步驟2：設定回應承載**

在自訂動作中設定回應：

```json
{
  "recommendations": [
    {
      "productId": "string",
      "productName": "string",
      "price": 0,
      "imageUrl": "string"
    }
  ]
}
```

深入瞭解[使用API呼叫回應](../action/action-response.md)。

**步驟3：在歷程中連線動作**

1. 在購物車放棄事件後，新增自訂動作
1. 在`cartItems`集合的進階模式中：

   ```javascript
   @event{cartAbandonment.commerce.productListItems.all(currentEventField.quantity > 0)}
   ```

1. 對應集合欄位：
   * `sku` → `productListItems.SKU`
   * `price` → `productListItems.priceTotal`
   * `quantity` → `productListItems.quantity`

**步驟4：在電子郵件中使用回應**

在您的電子郵件內容中，重複建議：

```handlebars
<h2>We noticed you left these items in your cart</h2>
{{#each context.journey.events.cartAbandonment.productListItems as |item|}}
  <div class="cart-item">
    <p>{{item.name}} - Quantity: {{item.quantity}}</p>
  </div>
{{/each}}

<h2>You might also like</h2>
{{#each context.journey.actions.GetCartRecommendations.recommendations as |rec|}}
  <div class="recommendation">
    <img src="{{rec.imageUrl}}" alt="{{rec.productName}}" />
    <h3>{{rec.productName}}</h3>
    <p>${{rec.price}}</p>
  </div>
{{/each}}
```

**步驟5：測試您的設定**

在執行即時歷程之前，請使用動作設定中的「傳送測試請求」功能來測試自訂動作，以驗證建置的請求和值。

1. 使用[歷程測試模式](../building-journeys/testing-the-journey.md)
2. 以包含`productListItems`陣列的範例事件資料觸發
3. 確認自訂動作收到正確的陣列結構
4. 檢查[動作測試記錄](../action/action-response.md#test-mode-logs)
5. 預覽電子郵件以確認兩個陣列皆正確顯示

深入瞭解[疑難排解您的自訂動作](../action/troubleshoot-custom-action.md)。

+++

## 最佳做法 {#best-practices}

重複上下文資料時，請遵循這些最佳實務，以建立可維護、高效能的個人化。

### 使用描述性變數名稱

選擇可清楚指出您正在反複處理的專案的變數名稱。 這可讓您的程式碼更容易閱讀及維護。 深入瞭解[個人化語法](personalization-syntax.md)：

+++ 檢視範常式式碼

```handlebars
<!-- Good -->
{{#each products as |product|}}
{{#each users as |user|}}
{{#each recommendations as |recommendation|}}

<!-- Less clear -->
{{#each items as |item|}}
{{#each array as |element|}}
```

+++

### 回圈中的運算式片段

在[回圈中使用](use-expression-fragments.md)運算式片段`{{#each}}`時，請注意，您無法傳遞回圈範圍的變數做為片段引數。 不過，片段可以存取在片段以外的訊息內容中定義的全域變數。

+++ 檢視範常式式碼

**支援的模式 — 使用全域變數：**

```handlebars
{% let globalDiscount = 15 %}

{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    {{fragment id='ajo:fragment123/variant456' mode='inline'}}
  </div>
{{/each}}
```

片段可以參照`globalDiscount`，因為它已在訊息中全域定義。

**不支援 — 傳遞回圈變數：**

```handlebars
{{#each products as |product|}}
  <!-- This will NOT work as expected -->
  {{fragment id='ajo:fragment123/variant456' currentProduct=product}}
{{/each}}
```

**因應措施**：將個人化邏輯直接包含在回圈中，而非使用片段，或呼叫回圈外的片段。

+++

深入瞭解如何在回圈[中使用運算式片段](use-expression-fragments.md#fragments-in-loops)，包括詳細範例和其他因應措施。



### 處理空白陣列

當陣列為空時，請使用`{{else}}`子句來提供遞補內容。 深入瞭解[協助程式函式](functions/helpers.md)：

+++ 檢視範常式式碼

```handlebars
{{#each context.journey.actions.GetRecommendations.items as |item|}}
  <div>{{item.name}}</div>
{{else}}
  <p>No recommendations available at this time.</p>
{{/each}}
```

+++

### 與條件式協助程式結合

在條件式內容的回圈中使用`{{#if}}`。 深入瞭解[條件式規則](create-conditions.md)，並檢視[自訂動作回應](#custom-action-responses)與[資料集查詢](#dataset-lookup)區段中的範例。

+++ 檢視範常式式碼

```handlebars
{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    {{#if product.onSale}}
      <span class="badge">On Sale!</span>
    {{/if}}
    {{#if product.newArrival}}
      <span class="badge">New</span>
    {{/if}}
  </div>
{{/each}}
```

+++

### 限制效能的反複專案

對於大型陣列，請考慮限制迭代次數：

+++ 檢視範常式式碼

```handlebars
<!-- Display only first 5 items -->
{{#each context.journey.actions.GetProducts.items as |product|}}
  {{#if @index < 5}}
    <div>{{product.name}}</div>
  {{/if}}
{{/each}}
```

+++

### 存取陣列中繼資料

Handlebars在回圈中提供特殊變數，有助於進階反複運算模式：

* `@index`：目前的反複專案索引（0型）
* `@first`：第一個反複專案為True
* `@last`：最後一個反複專案為True

+++ 檢視範常式式碼

```handlebars
{{#each products as |product|}}
  <div class="product {{#if @first}}featured{{/if}}">
    {{@index}}. {{product.name}}
  </div>
{{/each}}
```

+++

>[!NOTE]
>
>這些Handlebars變數(`@index`、`@first`、`@last`)只能在訊息個人化的`{{#each}}`回圈中使用。 若要在Journey運算式中使用陣列（例如在傳遞至自訂動作之前從陣列取得第一個專案），請使用陣列函式，例如[`head`](../personalization/functions/arrays-list.md#head)、[`first`](../building-journeys/expression/collection-management-functions.md)或[`all`](../building-journeys/expression/collection-management-functions.md)。 如需詳細資訊，請參閱[在歷程運算式中使用陣列](#arrays-in-journeys)。

## 疑難排解 {#troubleshooting}

反複專案發生問題？ 本節涵蓋常見問題和解決方案。

### 未顯示陣列

**問題**：您的陣列反複專案未顯示任何內容。

+++ 檢視可能的原因和解決方案

**可能的原因和解決方案**：

1. **不正確的路徑**：根據內容來源驗證您陣列的正確路徑：
   * 針對[個事件](#event-data)： `context.journey.events.<event_ID>.<fieldPath>`
   * 針對[自訂動作](#custom-action-responses)： `context.journey.actions.<actionName>.<fieldPath>`
   * 針對[資料集查詢](#dataset-lookup)： `context.journey.datasetLookup.<activityID>.entities`

2. **陣列是空的**：新增`{{else}}`子句以檢查陣列是否沒有資料。 如需範例，請參閱[最佳實務](#best-practices)。

3. **資料尚不可用**：請確保已在歷程流程中的訊息活動之前執行自訂動作、事件或資料集查詢活動。

+++

### 語法錯誤

**問題**：運算式驗證失敗或未轉譯訊息。

+++ 檢視常見錯誤

**常見錯誤**：

* 遺失結尾標籤：每個`{{#each}}`都必須有`{{/each}}`。 請檢閱[Handlebars反複專案語法](#syntax)以取得正確結構。
* 不正確的變數名稱：請確定在整個區塊中一律使用變數名稱。 如需命名慣例，請參閱[最佳實務](#best-practices)。
* 不正確的路徑分隔符號：使用點(`.`)而不使用斜線或其他字元

+++

### 運算式片段無法在回圈中運作

**問題**：運算式片段在`{{#each}}`回圈中使用時未顯示預期的內容，或顯示空白/未預期的輸出。

+++ 檢視可能的原因和解決方案

**可能的原因和解決方案**：

1. **嘗試傳遞回圈變數做為引數**：運算式片段無法接收回圈範圍的變數（例如目前的反複專案等）做為引數。 這是已知的限制。

   **解決方案**：使用下列變通方法之一：

   * 在訊息中定義片段可存取的全域變數
   * 直接在回圈中包含個人化邏輯，而非使用片段
   * 如果不需要回圈特定的資料，請呼叫回圈外部的片段

2. **片段需要無法使用的引數**：如果您的片段設計來接收特定的輸入引數，當這些引數無法從回圈中傳遞時，將無法正常運作。

   **解決方案**：重新建構您的方法，以使用片段可以存取的全域變數。 如需範例，請參閱[最佳實務 — 回圈中的運算式片段](#best-practices)。

3. **不正確的變數範圍**：片段可能正在嘗試參考只存在於回圈範圍內的變數。

   **解決方案**：定義片段在訊息層級（回圈外）需要的任何變數，讓這些變數可全域存取。

深入瞭解如何在回圈[中使用運算式片段](use-expression-fragments.md#fragments-in-loops)，包括詳細的說明、範例和建議的模式。

+++

### 測試您的反複專案

使用[歷程測試模式](../building-journeys/testing-the-journey.md)驗證您的反複專案。 使用[自訂動作](#custom-action-responses)或[資料集查詢](#dataset-lookup)時，這一點尤其重要：

+++ 檢視測試步驟

1. 以[測試模式](../building-journeys/testing-the-journey.md)開始您的歷程
2. 使用範例資料觸發事件或自訂動作
3. 檢查[訊息預覽](../content-management/preview.md)以驗證反複專案是否正確顯示
4. 檢閱測試模式記錄檔是否有任何錯誤（請參閱[自訂動作測試模式記錄檔](../action/action-response.md#test-mode-logs)）

+++

## 相關主題 {#related-topics}

**Personalization基本知識：** [開始使用個人化](personalize.md) | [新增個人化](personalization-build-expressions.md) | [Personalization語法](personalization-syntax.md) | [輔助函式](functions/helpers.md) | [建立條件式規則](create-conditions.md)

**歷程組態：** [關於事件](../event/about-events.md) | [設定自訂動作](../action/about-custom-action-configuration.md) | [將集合傳遞至自訂動作引數](../building-journeys/collections.md#passing-collection) | [在自訂動作中使用API呼叫回應](../action/action-response.md) | [疑難排解您的自訂動作](../action/troubleshoot-custom-action.md) | [在歷程中使用Adobe Experience Platform資料](../building-journeys/dataset-lookup.md) | [在歷程中使用補充識別碼](../building-journeys/supplemental-identifier.md) | [護欄和限制](../start/guardrails.md) | [測試您的歷程](../building-journeys/testing-the-journey.md)

**歷程運算式函式：** [進階運算式編輯器](../building-journeys/expression/expressionadvanced.md) | [集合管理函式](../building-journeys/expression/collection-management-functions.md) （第一個、全部、最後一個） | [列出函式](../building-journeys/functions/list-functions.md) （serializeList、篩選、排序） | [陣列函式](../personalization/functions/arrays-list.md) （頭、尾）

**Personalization使用案例：** [購物車放棄電子郵件](personalization-use-case-helper-functions.md) | [訂單狀態通知](personalization-use-case.md)

**郵件設計：** [開始使用電子郵件設計](../email/get-started-email-design.md) | [建立推播通知](../push/create-push.md) | [建立SMS訊息](../sms/create-sms.md) | [預覽和測試您的內容](../content-management/preview-test.md)

