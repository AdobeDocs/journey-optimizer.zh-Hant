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
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1275
ht-degree: 7%

---

# 日期函式 {#date-functions}

日期函式可讓您在歷程運算式中控制和使用日期和時間值。 這些功能對於客戶歷程中以時間為基礎的條件、排程和時間計算至關重要。

有以下需求時，請使用日期函式：

* 取得目前時間或具有特定時區處理的日期([now](#now)，[nowWithDelta](#nowWithDelta)，[currentTimeInMillis](#currentTimeInMillis))
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

傳回明天晚上8:XY，XY是目前時間評估的分鐘數。 如果評估發生在上午2:45，則傳回的時間將會是晚上8:45。

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

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面會記錄AJO歷程運算式中可用的所有日期和時間函式，包括如何取得目前時間、檢查日期是否在相對時間範圍內，以及修改日期/時間元件。

**意圖：**
* 使用`now`或`nowWithDelta`取得目前的日期時間（含選擇性的時區）
* 使用`currentTimeInMillis`以epoch整數擷取目前時間
* 使用`inLastDays`、`inLastHours`、`inLastMonths`、`inLastYears`檢查日期時間在過去N天、小時、月或年之內
* 使用`inNextDays`、`inNextHours`、`inNextMonths`、`inNextYears`檢查日期時間在接下來的N天、小時、月或年之內
* 使用`setHours`或`setDays`，在日期時間值上強制指定一小時或當月某日
* 將日期時間轉換為不同的時區，同時使用`updateTimeZone`保留相同的瞬間

**字彙表：**
* **dateTime**：包含時區位移資訊&#x200B;*（產品專用）*&#x200B;的日期時間值
* **dateTimeOnly**：沒有時區資訊的日期時間值&#x200B;*（產品特定）*
* **紀元毫秒**：代表自1970-01-01T00:00:00Z以來經過的毫秒數的整數
* **差異**：整數位移（正數或負數），與`nowWithDelta`搭配使用，將目前時間移動數年、月、日、小時、分鐘或秒

**護欄：**
* `now()`僅在歷程運算式中可用；對於電子郵件個人化，請使用`getCurrentZonedDateTime()`
* `nowWithDelta`中的時區ID必須是字串常數 — 不支援欄位參考和動態運算式
* `updateTimeZone`中的時區識別碼必須是字串常數

**術語：**
* 正式名稱：日期函式 — 首字母縮寫：none — 變體：日期時間函式，暫時函式
* 同義字： &quot;now()&quot; = &quot;current datetime&quot;； &quot;currentTimeInMillis()&quot; = &quot;current epoch milliseconds&quot;
* 請勿混淆：「inLastDays」（回顧時間）≠「inNextDays」（回顧時間）
* 請勿混淆：「setHours」（取代hour元件）≠「nowWithDelta」（位移目前時間）
* 請勿混淆：「updateTimeZone」（相同的即時、不同時區表示）≠「setHours」（變更時間值本身）

**常見問題集：**
* **問：我可以在電子郵件個人化內容中使用`now()`嗎？**  — 否，`now()`僅在歷程運算式中可用。 使用`getCurrentZonedDateTime()`進行電子郵件個人化。
* **問：如何檢查事件是否發生在過去24小時內？**  — 使用`inLastHours(@event{MyEvent.timestamp}, 24)`。
* **問：如何取得過去2小時內的目前時間位移？**  — 使用`nowWithDelta(-2, "hours")`。
* **問：`updateTimeZone`與`setHours`有何不同之處？** — `updateTimeZone`保持相同的即時時間，但以不同的時區表示，而`setHours`實際上會變更datetime值的小時元件。
* **問：`nowWithDelta`中的時區引數可以是設定檔欄位嗎？**  — 否，時區ID必須是字串常數；不支援欄位參考。

+++
