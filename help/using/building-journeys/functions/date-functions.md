---
product: journey optimizer
title: 日期函式
description: 瞭解日期函式
feature: Journeys
role: Developer
level: Experienced
keywords: 日期，函式，運算式，歷程，時間
version: Journey Orchestration
exl-id: 68c102c1-f1c7-44b7-893f-9a3b7e0854b6
TQID: https://experienceleague.adobe.com/C2Z5SufckUxCNf9TsloziZS-Q3KPzmgMVNGJGiwDQ08
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: []
source-git-commit: 52f7da843df1b3165aa6064efe893328413a7ad3
workflow-type: tm+mt
source-wordcount: 1135
ht-degree: 9%

---

# 日期函式 {#date-functions}

日期函式可讓您在歷程運算式中控制和使用日期和時間值。 這些功能對於客戶歷程中以時間為基礎的條件、排程和時間計算至關重要。

有以下需求時，請使用日期函式：

* 取得目前時間或具有特定時區處理的日期([now](#now)，[nowWithDelta](#nowWithDelta)，[currentTimeInMillis](#currentTimeInMillis))
* 根據引數型別([dateDiff](#dateDiff))，計算兩個日期或日期時間之間的差異（以天或毫秒為單位）
* 檢查日期是否落在特定時間範圍內([inLastDays](#inLastDays)，[inLastHours](#inLastHours)，[inLastMonths](#inLastMonths)，[inLastYears](#inLastYears)，[inNextDays](#inNextDays)，[inNextHours](#inNextHours)，[inNextMonths](#inNextMonths)，[inNextYears](#inNextYears))
* 修改日期和時間元件([setHours](#setHours)， [setDays](#setDays)， [updateTimeZone](#updateTimeZone))
* 執行以時間為基礎的計算和比較
* 在不同時間格式和表示之間轉換

日期函式可精確控制暫時邏輯，讓您建立對時間敏感的歷程路徑和條件，以回應特定時間範圍和排程。

>[!NOTE]
>
>此頁面上的函式可用於歷程運算式。 電子郵件內容的個人化編輯器中無法使用`now()`等某些函式。 [了解更多](../../personalization/functions/dates.md)

## currentTimeInMillis {#currentTimeInMillis}

傳回目前時間（以Epoch毫秒為單位）。

+++語法

`currentTimeInMillis()`

+++

+++參數

此函式不使用引數。

+++

+++簽章與傳回型別

`currentTimeInMillis()`

傳回整數。

+++

+++範例

`currentTimeInMillis()`

傳回「1544712617131」。

+++

## dateDiff {#dateDiff}

傳回相同型別的兩個日期或日期時間之間的差異。 結果的單位取決於引數型別： `dateOnly`引數傳回&#x200B;**天**&#x200B;的差異，而`dateTimeOnly`和`dateTime`引數傳回&#x200B;**毫秒**&#x200B;的差異。 如果任一引數為`null`，則傳回`null`。

>[!NOTE]
>
>這是與[個人化編輯器](../../personalization/functions/dates.md#date-diff)中可用的`dateDiff`不同的函式。 個人化編輯器版本只接受`dateTime`個引數，並一律傳回天數的差異。

+++語法

`dateDiff(<date1>,<date2>)`

+++

+++參數

| 參數 | 類型 |
|-----------|--------------------------------------|
| 日期1 | dateOnly、dateTimeOnly或dateTime |
| 日期2 | dateOnly、dateTimeOnly或dateTime |

兩個引數必須使用相同的資料型別；不支援混合型別（例如`dateOnly`搭配`dateTime`）。 引數可以是常值日期值、其他函式（例如`now()`）或內容屬性（事件裝載欄位、自訂動作回應欄位、設定檔或實體欄位以及變數），只要它們是`dateOnly`、`dateTimeOnly`或`dateTime`型別即可。

+++

+++簽章與傳回型別

`dateDiff(<dateOnly>,<dateOnly>)`

傳回整數，代表兩個日期之間的天數。

`dateDiff(<dateTimeOnly>,<dateTimeOnly>)`

傳回代表兩個日期時間之間的毫秒數的整數。

`dateDiff(<dateTime>,<dateTime>)`

傳回代表兩個日期時間之間的毫秒數的整數。

+++

+++範例

`dateDiff(toDateOnly('2023-12-15'), toDateOnly('2023-12-12'))`

傳回3 （天）。

`dateDiff(toDateTimeOnly('2023-12-15T00:00:00'), toDateTimeOnly('2023-12-12T00:00:00'))`

傳回259200000 （毫秒，等於3天）。

`dateDiff(now(), toDateTime('2024-12-25T00:00:00Z'))`

傳回今天和2024年12月25日之間的毫秒數。

`dateDiff(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate}, toDateOnly('2023-01-01'))`

傳回設定檔的`birthDate`欄位與2023年1月1日之間的天數，假設`birthDate`是輸入為`dateOnly`。

+++

## inLastDays {#inLastDays}

如果指定的dateTime介於現在與現在 — 差異天數之間，則傳回true。

+++語法

`inLastDays(<dateTime>,<delta>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

+++

+++簽章與傳回型別

`inLastDays(<dateTime>,<integer>)`

傳回布林值。

+++

+++範例

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回true。

+++

## inLastHours {#inLastHours}

如果指定的日期時間介於現在和現在之間 — 差異小時，則傳回true。

+++語法

`inLastHours(<dateTime>,<delta>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

+++

+++簽章與傳回型別

`inLastHours(<dateTime>,<integer>)`

傳回布林值。

+++

+++範例

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回true。

`inLastHours(@event{MyEvent.timestamp}, 4)`

傳回true。

+++

## inLastMonths {#inLastMonths}

如果指定的日期或dateTime介於現在和現在 — 差異月份之間，則傳回true。

+++語法

`inLastMonths(<dateTime>,<delta>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

+++

+++簽章與傳回型別

`inLastMonths(<dateTime>,<integer>)`

傳回布林值。

+++

+++範例

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回true。

+++

## inLastYears {#inLastYears}

如果指定的日期或dateTime介於現在和現在之間 — 差異年份，則傳回true。

+++語法

`inLastYears(<dateTime>,<delta>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

+++

+++簽章與傳回型別

`inLastYears(<dateTime>,<integer>)`

傳回布林值。

+++

+++範例

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回true。

+++

## inNextDays {#inNextDays}

如果指定的日期或日期時間介於現在和現在+差異天數之間，則傳回true。

+++語法

`inNextDays(<dateTime>,<delta>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

+++

+++簽章與傳回型別

`inNextDays(<dateTime>,<integer>)`

傳回布林值。

+++

+++範例

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回true。

+++

## inNextHours {#inNextHours}

如果指定的日期或日期時間介於現在和現在+差異小時之間，則傳回true。

+++語法

`inNextHours(<dateTime>,<delta>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

+++

+++簽章與傳回型別

`inNextHours(<dateTime>,<integer>)`

傳回布林值。

+++

+++範例

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回true。

+++

## inNextMonths {#inNextMonths}

如果指定的日期或dateTime介於現在和現在+差異月份之間，則傳回true。

+++語法

`inNextMonths(<dateTime>,<delta>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

+++

+++簽章與傳回型別

`inNextMonths(<dateTime>,<integer>)`

傳回布林值。

+++

+++範例

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

傳回true。

+++

## inNextYears {#inNextYears}

如果指定的日期或dateTime介於現在和現在+差異年度之間，則傳回true。

+++語法

`inNextYears(<dateTime>,<delta>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

+++

+++簽章與傳回型別

`inNextYears(<dateTime>,<integer>)`

傳回布林值。

+++

+++範例

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

傳回true。

+++

## now {#now}

以日期時間格式傳回目前日期。 如需資料型別的詳細資訊，請參閱[此頁面](../expression/data-types.md)。

>[!NOTE]
>
>此函式僅適用於歷程運算式。 對於電子郵件個人化與其他內容，請改用`getCurrentZonedDateTime()`。 [了解更多](../../personalization/functions/dates.md#get-current-zoned-date-time)

+++語法

`now(<parameter>)`

+++

+++參數

| 參數 | 說明 |
|--- |--- |
| 字串 | 時區識別碼（選擇性） |

+++

+++簽章與傳回型別

`now()`

`now("<timeZone id>")`

傳回日期時間。

+++

+++範例

`now()`

傳回2023-06-03T06:30Z。

`toString(now())`

傳回「2023-06-03T06:30Z」

`now("Europe/Paris")`

傳回2023-06-03T08:30+02:00。

+++

## nowWithDelta {#nowWithDelta}

傳回包含位移的目前日期時間。 如果指定了時區識別碼，則會套用時區位移。 如需資料型別的詳細資訊，請參閱[此頁面](../expression/data-types.md)。

+++語法

`nowWithDelta(<parameters>)`

+++

+++參數

| 參數 | 說明 |
|--- |--- |
| delta | 正或負整數值 |
| 日期部分 | 年、月、日、小時、分鐘或秒做為字串 |
| 時區id | 時區值的字串表示法。 如需詳細資訊，請參閱[資料型別](../expression/data-types.md)。 時區ID必須是字串常數。 它不能是欄位參考或運算式。 |

+++

+++簽章與傳回型別

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

傳回日期時間。

+++

+++範例

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

傳回2小時前的dateTime。

`nowWithDelta(1, "months", "Asia/Tokyo")`

在2026-01-31評估時，傳回2026-02-28T...；在2026-05-31評估時，傳回2026-06-30T...

`nowWithDelta()`使用行事曆月算術。 如果目標月份的天數少於當月當月，則結果會標準化為該月的最後一個有效日。 函式不會捲動至下個月。

+++

## setHours {#setHours}

僅設定日期時間或日期時間的小時。 例如，如果您要等到明天的特定小時，則可以強制該小時。

+++語法

`setHours(<parameter>)`

+++

+++參數

| 參數 | 類型 |
|--- |--- |
| 日期時間 | dateTime |
| 不考慮時區的日期時間 | dateTimeOnly |
| 小時 | 整數 |

+++

+++簽章與傳回型別

`setHours(<dateTime>,<hours>)`

傳回日期時間。

`setHours(<dateTimeOnly>,<hours>)`

傳回日期時間，不考慮時區。

+++

+++範例

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回2023-12-12T04:11:00Z。

`setHours(nowWithDelta(1, "days"), 20)`

傳回明天晚上8:XY，XY是目前時間評估的分鐘數。 如果評估在凌晨2:45進行，則傳回時間將會是晚上8:45。

+++

## setDays {#setDays}

僅設定日期時間或日期時間的日期。 例如，如果您要等到月份的某一天，則可以強制該天。

+++語法

`setDays(<parameter>)`

+++

+++參數

| 參數 | 類型 |
|--- |--- |
| 日期時間 | dateTime |
| 不考慮時區的日期時間 | dateTimeOnly |
| 天 | 整數 |

+++

+++簽章與傳回型別

`setDays(<dateTime>,<days>)`

傳回日期時間。

`setDays(<dateTimeOnly>,<days>)`

傳回日期時間，不考慮時區。

+++

+++範例

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

傳回2023-12-25T01:11:00Z。

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`

+++

## updateTimeZone {#updateTimeZone}

傳回新的日期時間，而在同一時間傳回新的時區。

+++語法

`updateTimeZone(<parameters>)`

+++

+++參數

* 時區id：字串
* dateTime

+++

+++簽章與傳回的型別

`updateTimeZone(<dateTime>,<timeZone id>)`

傳回日期時間。

+++

+++範例

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

傳回2023-08-28T17:15:30.123+02:00。

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

如果時間戳記欄位的值為`2021-11-16T16:55:12.939318+01:00`，則函式會傳回`2021-11-17T02:55:12.942115+11:00`。

+++

{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-functions-date-functions.md}}
