---
product: journey optimizer
title: 轉換函式
description: 了解轉換函式
feature: Journeys
role: Developer
level: Experienced
keywords: 轉換，函式，運算式，歷程，型別，轉型
version: Journey Orchestration
source-git-commit: 451a9e1e5d5e6e1408849e8d1c5c9644a95359da
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 6%

---

# 轉換函式 {#conversion-functions}

轉換函式可讓您在歷程運算式中將資料從一種型別轉換為另一種型別。 這些函式對於在使用不同的資料來源和作業時確保資料相容性和正確型別處理至關重要。

當您需要以下工作時，請使用轉換函式：

* 將字串值轉換為數值、布林值或日期型別([toInteger](#toInteger)， [toDecimal](#toDecimal)， [toBool](#toBool))
* 轉換不同格式和表示之間的日期和時間([toDateTime](#toDateTime)，[toDateTimeOnly](#toDateTimeOnly)，[toDateOnly](#toDateOnly))
* 轉換介於整數與小數型別([toInteger](#toInteger)， [toDecimal](#toDecimal))之間的數值
* 將值轉換為字串格式([toString](#toString))或持續時間([toDuration](#toDuration))
* 確保比較和作業的型別相容性
* 處理來自可能具有不同型別格式的外部來源的資料

每個轉換函式都會自動處理型別特定規則和邊緣案例，讓資料轉換在歷程運算式中更加可靠且可預測。

## toBool {#toBool}

根據其型別，將引數值轉換為布林值。

* 從字串：嘗試將字串值轉換為布林值，如果字串值為「true」，則從「true」，否則為false
* 從數值：如果數值不等於0，則為true；否則為false

+++語法

`toBool(<parameter>)`

+++

+++參數

* 小數
* 布林值
* 字串
* 整數

+++

+++簽章與傳回的型別

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

傳回布林值。

+++

+++範例

`toBool("true")`

`toBool(1)`

傳回true。

`toBool("this is not a boolean")`

傳回false。

+++

## toDateOnly {#toDateOnly}

將引數轉換為dateOnly型別值。 若要深入瞭解資料型別，請參閱此[區段](../expression/data-types.md)。

+++語法

`toDateOnly(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 以「YYYY-MM-DD」（XDM格式）表示日期的字串表示法。 也支援ISO-8601格式：只考慮&#x200B;**完整日期**&#x200B;部分（請參閱[RFC 3339，第5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6)節） | 字串 |
| 日期時間 | dateTime |
| 沒有時區的日期時間 | dateTimeOnly |
| 紀元的整數值（以毫秒為單位） | 整數 |

+++

+++簽章與傳回的型別

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

傳回dateOnly型別值。

+++

+++範例

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

所有傳回代表2023-08-18的dateOnly物件。

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

傳回dateOnly。

+++

## toDateTime {#toDateTime}

根據引數的型別，將其轉換為日期時間值。

+++語法

`toDateTime(<parameters>)`

+++

+++參數

| 參數 | 說明 |
|--- |--- |
| 字串 | ISO-8601格式的日期時間。 日期時間的字串表示法，包含時區資訊 |
| 字串 | 時區ID。 時區識別碼（例如「UTC」、「歐洲/巴黎」） |
| dateOnly | 代表沒有時區的日期，以年 — 月 — 日檢視 |
| dateTimeOnly | 代表沒有時區的日期時間，以年 — 月 — 日 — 小時 — 分鐘 — 秒 — 毫秒的方式檢視 |
| 整數 | 紀元的整數值（以毫秒為單位） |

+++

+++簽章與傳回的型別

`toDateTime(<string>)`

`toDateTime(<string>, <dateOnly>)`

`toDateTime(<string>, <dateTimeOnly>)`

`toDateTime(<integer>)`

傳回&#x200B;**日期時間**。

+++

+++範例

`toDateTime("2023-08-18T23:17:59.123Z")`

傳回2023-08-18T23:17:59.123Z

ISO-8601字串已包含時區資訊。

`toDateTime("Europe/Paris", toDateOnly("2023-08-18"))`

傳回2023-08-18T00:00:00.000+02:00

這會將時區與僅限日期的值結合，以建立dateTime。 時間設定為指定時區的午夜(00:00:00)。

`toDateTime("UTC", toDateTimeOnly("2023-08-18T23:17:59.123"))`

傳回2023-08-18T23:17:59.123Z

這會透過將時區套用到dateTimeOnly值（沒有時區資訊）來建立dateTime。

`toDateTime(1560762190189)`

傳回2019-06-17T09:03:10.189Z

將以毫秒為單位的Unix時間戳記轉換為dateTime值。

+++

>[!NOTE]
>
>時區ID必須是字串常數。 它不能是欄位參考或運算式。 如需資料型別的詳細資訊，請參閱[此頁面](../expression/data-types.md)。

## toDateTimeOnly {#toDateTimeOnly}

將引數值轉換為僅日期時間值。

+++語法

`toDateTimeOnly(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| ISO-8601或&quot;YYYY-MM-DD&quot;格式的日期時間（XDM日期格式） | 字串 |
| 日期時間 | dateTime |

+++

+++簽章與傳回的型別

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`

傳回日期時間而不考慮時區。

+++

+++範例

`toDateTimeOnly ("2023-08-18")`

傳回代表2023-08-18T00:00:00.000的dateTime

`toDateTimeOnly(now())`

+++

## toDecimal {#toDecimal}

根據其型別，將引數值轉換為十進位值。

+++語法

`toDecimal(<parameter>)`

+++

+++參數

| 參數 | 說明 |
|--- |--- |
| 字串 | 將字串值轉換為小數 |
| dateTime | 將日期轉換為毫秒數（紀元毫秒） |
| 布林值 | 如果為true，則將布林值轉換為1，如果為false，則轉換為0 |
| 整數 | 轉換為小數（範例）。：1變為1.0) |

+++

+++簽章與傳回的型別

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

傳回小數。

+++

+++範例

`toDecimal("4.0")`

傳回4.0。

+++

## toDuration {#toDuration}

將引數值轉換為持續時間。 如需資料型別的詳細資訊，請參閱[此頁面](../expression/data-types.md)。

+++語法

`toDuration(<parameter>)`

+++

+++參數

| 參數 | 說明 |
|--- |--- |
| 字串 | 以ISO-8601持續時間格式PnDTnHnMn.nS為基礎的格式，將天數視為24小時 |
| 整數 | 毫秒數 |

如果字串運算式：接受的格式是以ISO-8601期間格式PnDTnHnMn.nS為基礎，而天數則視為24小時。

字串以選用的符號開頭，以ASCII負號或正號表示。 如果為負值，則整個期間都會被否定。 ASCII字母「P」是下一個大寫或小寫。 然後會有四個區段，每個區段包含一個數字和一個尾碼。 區段的ASCII尾碼為&quot;D&quot;、&quot;H&quot;、&quot;M&quot;及&quot;S&quot;，分別代表日、小時、分鐘及秒，可使用大寫或小寫。 尾碼必須依序出現。 ASCII字母「T」必須在小時、分鐘或秒區段的第一個專案（如果有的話）之前出現。 四個區段中的至少一個必須存在，如果存在「T」，則在「T」之後必須至少有一個區段。 每個區段的數字部分必須包含一個或多個ASCII數字。 數字可以以ASCII負號或正號為前置詞。 必須分析的天數、小時數和分鐘數。 秒數必須剖析為以及選用的分數。 小數點可以是點或逗號。 分數部分可能有0到9位數。

+++

+++簽章與傳回型別

`toDuration(<string>)`

`toDuration(<integer>)`

傳回持續時間。

+++

+++範例

`toDuration("PT10H")`

傳回10小時的持續時間。

`toDuration("PT4S")`

傳回4s的持續時間。

`toDuration(4000)`

傳回4s的持續時間。

+++

## toInteger {#toInteger}

將引數值轉換為整數。

+++語法

`toInteger(<parameter>)`

+++

+++參數

| 參數 | 說明 |
|--- |--- |
| 字串 | 將字串值轉換為整數 |
| dateTime | 將日期轉換為毫秒數（紀元毫秒） |
| 小數 | 透過移除小數部分轉換為整數（範例： 1.5變為1） |
| 布林值 | 如果為true，則將布林值轉換為1，如果為false，則轉換為0 |

+++

+++簽章與傳回型別

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

傳回整數。

+++

+++範例

`toInteger("4")`

傳回4。

+++

## toString {#toString}

根據其型別，將引數值轉換為字串值。 如需資料型別的詳細資訊，請參閱[此頁面](../expression/data-types.md)。

+++語法

`toString(<parameter>)`

+++

+++參數

| 參數 | 說明 |
|--- |--- |
| dateTime | 將日期轉換為UTC日期格式 |
| dateTimeOnly | 將日期轉換為UTC日期格式 |
| 期間 | 轉換為字串形式的對應毫秒數 |
| 整數 | 轉換為值的字串表示法（1會變成「1」） |
| 小數 | 轉換為值的字串表示法（1.5會變成&quot;1.5&quot;） |
| 布林值 | 將布林值轉換為&#39;true&#39; （如果為true），&#39;false&#39; （如果為false） |

+++

+++簽章與傳回型別

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

傳回字串。

+++

+++範例

`toString(4)`

傳回「4」。

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

傳回給定dateOnly欄位（XDM日期欄位）的字串表示法，例如「2023-08-18」。

`toString(toDuration(1520))`

傳回「PT1.52S」。

+++

