---
solution: Journey Optimizer
product: journey optimizer
title: 操作者
description: 瞭解進階運算式中的運運算元
feature: Journeys
role: Developer
level: Experienced
keywords: 運算式，語法，運運算元，編輯器，歷程
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sK2GNHkkiJ4M5V99Uucc-b68iESNW7kCNBjHVNT-dMs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1001
ht-degree: 3%

---

# 操作者 {#operators}

運運算元有兩種型別：一元運運算元和二進位運運算元。 有左一元運運算元和右一元運運算元。

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@event{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## 重要備註{#important-notes}

* 使用乘法(`*`)時，兩個作業欄位必須具有相同的型別，可以是整數或小數。 範例：
   * 下列範例是正確的： `3.0 * 4.0`
   * `3 * 4.0`將導致錯誤

* 使用`+`運運算元時，運算式必須封裝在括弧中。 範例：
   * `toDateTimeOnly(toDateTime((currentTimeInMillis()) + 1))`正確
   * `toDateTimeOnly(toDateTime(currentTimeInMillis() + 1))`將導致錯誤

## 邏輯  {#logical}

### 和

```json
<expression1> and <expression2>
```

&lt;expression1>和&lt;expression2>都必須是布林值。 結果是布林值。

範例：

```json
3.14 > 2 and 3.15 < 1
```

### 或

```json
<expression1> or <expression2>
```

&lt;expression1>和&lt;expression2>都必須是布林值。 結果是布林值。

範例：

```json
3.14 > 2 or 3.15 < 1
```

### 非

```json
not <expression>
```

&lt;expression>必須為布林值。 結果是布林值。

範例：

```json
not 3.15 < 1
```

## 比較 {#comparison}

### 為null

```json
<expression> is null
```

結果是布林值。

請注意，null表示運算式沒有評估值。

範例：

```json
@event{BarBeacon.location} is null
```

### 不是null

```json
<expression> is not null
```

結果是布林值。

請注意，null表示運算式沒有評估值。

範例：

```json
@event{BarBeacon.location} is not null
```

### 具有null

```json
<expression> has null
```

&lt;expression>必須是清單。 結果是布林值。

用於識別清單是否包含至少一個Null值。

範例：

```json
["foo", "bar", null] has null
```

傳回true

```json
["foo", "bar", ""] has null
```

傳回false，因為「」不視為null。

### ==

```json
<expression1> == <expression2>
```

>[!NOTE]
>
>&lt;expression1>和&lt;expression2>沒有資料型別控制項。

範例：

```json
3.14 == 42
```

```json
"foo" == "bar"
```

### !=

```json
<expression1> != <expression2>
```

>[!NOTE]
>
>&lt;expression1>和&lt;expression2>沒有資料型別控制項。

結果是布林值。

範例：

```json
3.14 != 42
```

```json
"foo" != "bar"
```

### >

```json
<expression1> > <expression2>
```

日期時間可以與日期時間比較。

Datetimeonly可以與Datetimeonly比較。

整數或小數點都可以與整數或小數點進行比較。

禁止任何其他組合。

結果是布林值。

範例：

```json
3.14 > 42
```

### >=

```json
<expression1> >= <expression2>
```

日期時間可以與日期時間比較。

Datetimeonly可以與Datetimeonly比較。

整數或小數點都可以與整數或小數點進行比較。

禁止任何其他組合。

結果是布林值。

範例：

```json
42 >= 3.14
```

### &lt;

```json
<expression1> < <expression2>
```

日期時間可以與日期時間比較。

Datetimeonly可以與Datetimeonly比較。

整數或小數點都可以與整數或小數點進行比較。

禁止任何其他組合。

結果是布林值。

範例：

```json
42 < 3.14
```

### &lt;=

```json
<expression1> <= <expression2>
```

日期時間可以與日期時間比較。

Datetimeonly可以與Datetimeonly比較。

整數或小數點都可以與整數或小數點進行比較。

禁止任何其他組合。

結果是布林值。

範例：

```json
42 <= 3.14
```

## 算術 {#arithmetic}

### +

```json
<expression1> + <expression2>
```

這兩個運算式都必須是數值（整數或小數）。

結果也是數字。

範例：

```json
1 + 2
```

傳回3

### -

```json
<expression1> - <expression2>
```

這兩個運算式都必須是數值（整數或小數）。

結果也是數字。

範例：

```json
2 - 1 
```

傳回1

### /

```json
<expression1> / <expression2>
```

這兩個運算式都必須是數值（整數或小數）。

結果也是數字。

&lt;expression2>不可以等於0 （傳回0）。

範例：

```json
4 / 2
```

傳回2

### *

```json
<expression1> * <expression2>
```

這兩個運算式都必須是數值（整數或小數）。

結果也是數字。

範例：

```json
3 * 4
```

傳回12

### %

```json
<expression1> % <expression2>
```

這兩個運算式都必須是數值（整數或小數）。

結果也是數字。

範例：

```json
3 % 2
```

傳回1。

## 數學 {#math}

### 是數值

```json
<expression> is numeric
```

運算式的型別是整數或小數。

範例：

```json
@ is numeric
```

### 為整數

```json
<expression> is integer
```

運算式的型別是整數。

範例：

```json
@ is integer
```

### 為小數

```json
<expression> is decimal
```

運算式的型別是十進位。

範例：

```json
@ is decimal
```

## 字串 {#string}

### +

```json
<string> + <expression>
```

```json
<expression> + <string>
```

它會串連兩個運算式。

一個運算式必須是鏈結字串。

範例：

```json
"the current time is " + (now())
```

傳回「目前時間是2023-09-23T09:30:06.693Z」

```json
(now()) + " is the current time"
```

傳回「2023-09-23T09:30:06.693Z為目前時間」

```json
"a" + "b" + "c" + 1234
```

傳回「abc1234」。

## 日期 {#date}

### +

```json
<expression> + <duration>
```

將期間附加至dateTime、dateTimeOnly或duration。

範例：

```json
(toDateTime("2023-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

傳回&#x200B;_dateTime_ 2023-12-03T15:30:30Z

```json
(toDateTimeOnly("2023-12-03T15:15:30")) + (toDuration("PT15M"))
```

傳回&#x200B;_dateTimeOnly_ 2023-12-03T15:30:30

```json
(now()) + (toDuration("PT1H"))
```

從目前時間後一小時傳回&#x200B;_dateTime_ （含UTC時區）

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

傳回&#x200B;_持續時間_ PT2H

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面是歷程進階運算式編輯器中可用運運算元的完整參考，涵蓋邏輯(`and`、`or`、`not`)、比較(`==`、`!=`、`>`、`>=`、`<`、`<=`、`is null`、`is not null`、`has null`)、算術(`+`、`-`、`/`、`*`、`%`)、數學型別檢查(`is numeric`、`is integer`、`is decimal`)、字串串連和日期算術運算子。

**意圖：**

* 使用邏輯運運算元`and`、`or`和`not`結合布林條件
* 使用`is null` / `is not null`檢查欄位或運算式值是否為Null或不為Null
* 使用`has null`運運算元偵測清單中的null值
* 使用`>`、`>=`、`<`、`<=`、`==`和`!=`比較數值、日期時間和日期時間值
* 使用`+`、`-`、`/`、`*`和`%`對數值執行算術
* 使用`+`運運算元將期間新增至dateTime、dateTimeOnly或duration值

**字彙表：**

* **一元運運算元**：套用至單一運算元的運運算元；可以是左側（例如`not`）或右側（例如`is null`） *（產品特定）*
* **二進位運運算元**：在兩個運算元（例如`and`， `==`， `+`） *（產品特定）*&#x200B;之間套用的運運算元
* **具有null**：如果清單包含至少一個null專案&#x200B;*（產品特定）*，右邊一元運運算元會傳回true
* **是數值/是整數/是十進位**：根據運算式&#x200B;*（產品特定）*&#x200B;的數值子型別傳回布林值的型別檢查運運算元

**護欄：**

* 使用乘法(`*`)時，兩個運算元必須是相同的數值型別（整數或兩個小數） — 混合型別會導致錯誤
* 使用`+`運運算元進行日期算術時，運算式必須用括弧括住，以避免剖析錯誤
* 比較運運算元(`>`、`>=`、`<`、`<=`)只在相容型別之間有效：具有Datetime的Datetime、具有DatetimeOnly的DatetimeOnly或具有數值的numeric — 禁止任何其他組合
* 空白字串`""`不視為Null — `has null`會針對包含`""`的清單傳回False
* `==`和`!=`運運算元在運算元之間不執行任何資料型別控制

**術語：**

* 正式名稱：運運算元 — 縮寫：無 — 變體：運算式運運算元、歷程運運算元
* 同義字： `and` = &quot;logical AND&quot;；`or` = &quot;logical OR&quot;；`not` = &quot;logical NOT&quot;；`%` = &quot;modulo&quot;
* 請勿混淆： `is null` （運算式沒有評估值） ≠ `== null` （不是有效的語法）； `has null` （清單包含null） ≠ `is null` （運算式本身為null）

**常見問題集：**

* **問：我可以直接將整數乘以十進位嗎？** — No； `*`的兩個運算元都必須是相同型別。 使用`3.0 * 4.0` （小數）或`3 * 4` （整數）。
* **問：如何新增15分鐘至dateTime？**  — 使用`(toDateTime("...")) + (toDuration("PT15M"))`。
* **問：`is null`與`has null`之間有何差異？** — `is null`檢查單一運算式是否沒有評估值；`has null`檢查清單是否包含至少一個null專案。
* **問：`"" has null`是否傳回True？** — No；空白字串不會視為Null，因此結果為false。
* **問：為什麼`3 * 4.0`會造成錯誤？** — `*`運運算元要求兩個運算元必須是相同的數值型別；不允許混合整數與小數。

+++
