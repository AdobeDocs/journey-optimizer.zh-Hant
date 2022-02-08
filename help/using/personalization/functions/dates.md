---
title: 日期時間函式館
description: 日期時間函式館
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

日期和時間函式用於對Journey Optimizer內的值執行日期和時間操作。

## 年齡{#age}

的 `age` 函式用於從給定日期檢索年齡。

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

## 當前時間（毫秒）{#current-time}

的 `currentTimeInMillis` 函式用於檢索當前時間（以新紀元毫秒為單位）。

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

的 `dateDiff` 函式用於檢索兩個日期（天數）之間的差。

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

的 `dayOfWeek` 函式用於檢索星期幾。

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

的 `dayOfYear` 函式用於檢索年中的某一天。

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

## 格式日期{#format-date}

的 `formatDate` 函式用於格式化日期時間值。 格式應為有效的Java DateTimeFormat模式。

**格式**

```sql
{%= formatDate(date, format) %}
```

其中，第一個字串是date屬性，第二個值是要轉換和顯示日期的方式。

>[!NOTE]
>
> 如果日期模式無效，則日期將回退到ISO標準格式。
>
> 可以使用Java日期格式化函式（摘要） [在Oracle文檔中](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**範例**

以下操作將以下列格式返回日期：MM/DD/YY

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## 設定天數{#set-days}

的 `setDays` 函式用於設定給定日期時間的月份日。

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

的 `setHours` 函式用於設定日期時間的小時。

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

的 `toUTC` 函式用於將日期時間轉換為UTC。


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

的 `weekOfYear` 函式用於檢索年中的周。

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
