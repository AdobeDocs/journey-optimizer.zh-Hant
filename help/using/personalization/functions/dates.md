---
title: 日期時間函式庫
description: 日期時間函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3eab04f28b1daab556c4b4395d67f28d292fc52b
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 13%

---

# 日期時間函式{#date-time}

日期和時間函式可用來對Journey Optimizer中的值執行日期和時間作業。

## 增加天數 {#add-days}

`addDays`函式會依指定的天數調整指定日期，使用正值增加值，使用負值減少值。

**語法**

```sql
{%= addDays(date, number) %}
```

+++範例

* 輸入： `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* 輸出： `2024-11-11T17:19:51Z`

+++

## 增加小時數 {#add-hours}

`addHours`函式會依指定的小時數調整指定日期，使用正值增加值，使用負值減少值。

**語法**

```sql
{%= addHours(date, number) %}
```

+++範例

* 輸入： `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* 輸出： `2024-11-01T18:19:51Z`

+++

## 增加分鐘數 {#add-minutes}

`addMinutes`函式會以指定的分鐘數調整指定日期，使用正值增加值，使用負值減少值

**語法**

```sql
{%= addMinutes(date, number) %}
```

+++範例

* 輸入： `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* 輸出： `2024-11-01T18:09:51Z`

+++

## 增加月數 {#add-months}

`addMonths`函式會依指定的月數調整指定日期，使用正值增加值，使用負值減少值。

**語法**

```sql
{%= addMonths(date, number) %}
```

+++範例

* 輸入： `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* 輸出： `2025-01-01T17:19:51Z`

+++

## 增加秒數 {#add-seconds}

`addSeconds`會以指定的秒數來調整指定日期，使用正值來遞增，使用負值來遞減。

**語法**

```sql
{%= addSeconds(date, number) %}
```

+++範例

* 輸入： `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* 輸出： `2024-11-01T17:20:01Z`

+++

## 增加年數 {#add-years}

`addYears`會依指定的年數來調整指定日期，使用正值來遞增，使用負值來遞減。

**語法**

```sql
{%= addYears(date, number) %}
```

+++範例

* 輸入： `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* 輸出： `2026-11-01T17:19:51Z`

+++

## 年齡{#age}

`age`函式用於從給定日期擷取年齡。

**語法**

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

## 年齡 (以天為單位) {#age-days}

`ageInDays`函式會以天數計算指定日期的存留期，即指定日期與目前日期之間經過的天數，未來日期為負數，過去日期為正數。

**語法**

```sql
{%= ageInDays(date) %}
```

+++範例

currentDate = 2025-01-07T12:17:10.720122+05:30 （亞洲/加爾各答）

* 輸入： `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* 輸出： `5`

+++

## 年齡 (以月為單位) {#age-months}

`ageInMonths`函式會以月為單位計算指定日期的年齡，也就是指定日期和目前日期之間經過的月數，未來日期的負數與過去日期的正數。

**語法**

```sql
{%= ageInMonths(date) %}
```

+++範例

currentDate = 2025-01-07T12:22:46.993748+05:30（亞洲/加爾各答）

* 輸入： `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* 輸出： `12`

+++

## 比較日期 {#compare-dates}

`compareDates`函式會比較第一個輸入日期與另一個輸入日期。 如果date1等於date2，則傳回0；如果date1在date2之前，則傳回–1；如果date1在date2之後，則傳回1。

**語法**

```sql
{%= compareDates(date1, date2) %}
```

+++範例

* 輸入： `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* 輸出： `-1`

+++

## 轉換分區日期時間 {#convert-zoned-date-time}

`convertZonedDateTime`函式將日期時間轉換為指定的時區。

**語法**

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

+++範例

* 輸入： `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* 輸出： `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

## 目前時間 (以毫秒為單位){#current-time}

`currentTimeInMillis`函式用於擷取目前時間（以Epoch毫秒為單位）。

**語法**

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

## 日期差異{#date-diff}

`dateDiff`函式用於擷取兩個日期之間的天數差異。

**語法**

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 當月的第幾天 {#day-month}

`dayOfWeek`會傳回代表該月某日的數字。

**語法**

```sql
{%= dayOfMonth(datetime) %}
```

+++範例

* 輸入： `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* 輸出： `5`

+++


## 星期幾 {#day-week}

`dayOfWeek`函式用於擷取星期幾。

**語法**

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 年中的日{#day-year}

`dayOfYear`函式用於擷取一年當中的第幾天。

**語法**

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 差異 (以秒為單位) {#diff-seconds}

`diffInSeconds`函式傳回兩個日期之間的秒數差。

**語法**

```sql
{%= diffInSeconds(endDate, startDate) %}
```

+++範例

* 輸入： `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* 輸出： `50`

+++

## 擷取小時 {#extract-hours}

`extractHours`函式會從指定的時間戳記中擷取時數元件。

**語法**

```sql
{%= extractHours(date) %}
```

+++範例

* 輸入： `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* 輸出： `17`

+++

## 擷取分鐘 {#extract-minutes}

`extractMinutes`函式會從指定的時間戳記中擷取分鐘元件。

**語法**

```sql
{%= extractMinutes(date) %}
```

+++範例

* 輸入： `{%= extractMinute(stringToDate("2024-11-01T17:19:51Z"))%}`
* 輸出： `19`

+++

## 擷取月份 {#extract-months}

`extractMonth`函式會從指定的時間戳記中擷取月份元件。

**語法**

```sql
{%= extractMonths(date) %}
```

+++範例

* 輸入： `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* 輸出： `11`

+++

## 擷取秒 {#extract-seconds}

`extractSeconds`函式會從指定的時間戳記中擷取第二個元件。

**語法**

```sql
{%= extractSeconds(date) %}
```

+++範例

* 輸入： `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* 輸出： `51`

+++

## 格式化日期{#format-date}

`formatDate`函式用來格式化日期時間值。 格式應為有效的Java DateTimeFormat模式。

**語法**

```sql
{%= formatDate(datetime, format) %}
```

其中第一個字串是日期屬性，第二個值是您想要轉換和顯示日期的方式。

>[!NOTE]
>
> 如果日期模式無效，該日期將回覆為ISO標準格式。
>
> 您可以使用[Oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}中摘要的Java日期格式函式

**範例**

下列作業將傳回下列格式的日期：MM/DD/YY。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

## 支援地區設定的日期格式{#format-date-locale}

`formatDate`函式可用來將日期時間值格式化成對應的語言敏感表示法，亦即所需的地區設定。 格式應為有效的Java DateTimeFormat模式。

**語法**

```sql
{%= formatDate(datetime, format, locale) %}
```

其中第一個字串是日期屬性，第二個值是您轉換和顯示日期的方式，第三個值代表字串格式的地區設定。

>[!NOTE]
>
> 如果日期模式無效，該日期將回覆為ISO標準格式。
>
> 您可以使用[Oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html)中摘要的Java日期格式函式。
>
> 您可以使用[Oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html)和[支援的地區設定](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html)中概述的格式設定和有效地區設定。

**範例**

下列作業將傳回下列格式的日期： MM/DD/YY和locale FRANCE。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## 取得目前分區日期時間 {#get-current-zoned-date-time}

`getCurrentZonedDateTime`函式傳回目前日期和時間，並附上時區資訊。

**語法**

```sql
{%= getCurrentZonedDateTime() %}
```

+++範例

* 輸入： `{%= getCurrentZonedDateTime() %}`
* 輸出： `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

## 小時差 {#hours-difference}

`diffInHours`函式傳回兩個日期之間的時數差。

**語法**

```sql
{%= diffInHours(endDate, startDate) %}
```

+++範例

* 輸入： `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* 輸出： `10`

+++

## 分鐘差{#diff-minutes}

`diffInMinutes`函式用來傳回兩個日期之間的差異（以分鐘為單位）。

**語法**

```sql
{%= diffInMinutes(endDate, startDate) %}
```

+++範例

* 輸入： `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* 輸出： `60`

+++

## 月差 {#months-difference}

`diffInMonths`函式傳回兩個日期之間的月差。

**語法**

```sql
{%= diffInMonths(endDate, startDate) %}
```

+++範例

* 輸入： `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* 輸出： `3`

+++

## 設定天數{#set-days}

`setDays`函式用來設定指定日期時間的月份日期。

**語法**

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 設定時數{#set-hours}

`setHours`函式是用來設定日期時間的小時。

**語法**

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 至日期時間 {#to-date-time}

`ToDateTime`函式將字串轉換為日期。 針對無效輸入會傳回epoch日期作為輸出。

**語法**

```sql
{%= toDateTime(string, string) %}
```

+++範例

* 輸入： `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* 輸出： `2024-11-01T17:19:51Z`

+++

## 到 UTC{#to-utc}

`toUTC`函式用於將日期時間轉換為UTC。

**語法**

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 截斷至當天的開始 {#truncate-day}

`truncateToStartOfDay`函式是用來修改指定的日期時間，方法是將其設定為當天的開始，而時間設定為00:00。

**語法**

```sql
{%= truncateToStartOfDay(date) %}
```

+++範例

* 輸入： `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* 輸出： `2024-11-01T00:00Z`

+++

## 截斷至季的開始 {#truncate-quarter}

`truncateToStartOfQuarter`函式用於將日期時間截斷為其季度的第一天（例如，1月1日、4月1日、7月1日、10月1日），截斷時間為00:00。

**語法**

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

+++範例

* 輸入： `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* 輸出： `2024-10-01T00:00Z`

+++

## 截斷至週的開始 {#truncate-week}

`truncateToStartOfWeek`函式將指定日期時間設定為一週的開始（星期一為00:00），以修改指定的日期時間。

**語法**

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

+++範例

* 輸入： `truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* 輸出： `2024-11-18T00:00Z // monday`

+++

## 截斷至年的開始 {#truncate-year}

`truncateToStartOfYear`函式是用來修改指定的日期時間，方法是將其截斷至一年的第一天（1月1日），網址為00:00。

**語法**

```sql
{%= truncateToStartOfYear(dateTime) %}
```

+++範例

* 輸入： `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* 輸出： `2024-01-01T00:00Z`

+++

## 年中的週 {#week-of-year}

`weekOfYear`函式用於擷取該年的周數。

**語法**

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 年差 {#diff-years}

`diffInYears`函式是用來傳回兩個日期之間的年差。

**語法**

```sql
{%= diffInYears(endDate, startDate) %}: int
```

+++範例

* 輸入： `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* 輸出： `5`

+++
