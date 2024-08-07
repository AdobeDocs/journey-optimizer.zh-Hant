---
title: 日期時間函式庫
description: 日期時間函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3a4a58f8601c67e8e9a2b606a47c6b4bcc2dab05
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 7%

---

# 日期時間函式{#date-time}

日期和時間函式可用來對Journey Optimizer中的值執行日期和時間作業。

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


## 星期幾{#day-week}

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
> 您可以使用[Oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html)和[支援的語言環境](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html)中概述的格式設定和有效語言環境。


**範例**

下列作業將傳回下列格式的日期： MM/DD/YY和locale FRANCE。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

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


## UTC年周{#week-of-year}

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