---
title: 日期時間函式程式庫
description: 日期時間函式程式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: f0c5b42984b76fee005fe0c0e10312d47f9d10e8
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 6%

---

# 日期時間函式{#date-time}

日期和時間函式可用來對Journey Optimizer內的值執行日期和時間操作。

## 年齡{#age}

此 `age` 函式可用來從指定日期擷取年齡。

**格式**

```sql
 {%= age(date) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(date) %}
```
-->

## 當前時間（以毫秒為單位）{#current-time}

此 `currentTimeInMillis` 函式可用來擷取目前時間（以epoch毫秒為單位）。

**格式**

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

此 `dateDiff` 函式可用來擷取兩個日期之間以天數表示的差異。

**格式**

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


## 週中的日{#day-week}

此 `dayOfWeek` 函式可用來擷取星期。

**格式**

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

此 `dayOfYear` 函式可用來擷取一年當中的某天。

**格式**

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

## 日期格式{#format-date}

此 `formatDate` 函式來設定日期時間值的格式。 格式應為有效的Java DateTimeFormat模式。

**格式**

```sql
{%= formatDate(date, format) %}
```

其中第一個字串是日期屬性，第二個值是您要如何轉換和顯示日期。

>[!NOTE]
>
> 如果日期模式無效，日期將回復為ISO標準格式。
>
> 您可以使用Java日期格式化函式，如摘要 [在Oracle檔案中](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**範例**

下列操作會以下列格式傳回日期：MM/DD/YY。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## 設定天數{#set-days}

此 `setDays` 函式可用來設定指定日期時間的月中某天。

**格式**

```sql
{%= setDays(date, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 設定小時數{#set-hours}

此 `setHours` 函式可用來設定日期時間的小時。

**格式**

```sql
{%= setHours(date, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## 到UTC{#to-utc}

此 `toUTC` 函式用於將datetime轉換為UTC。


**格式**

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


## 每年的周UTC{#week-of-year}

此 `weekOfYear` 函式可用來擷取一年中的某周。

**格式**

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
