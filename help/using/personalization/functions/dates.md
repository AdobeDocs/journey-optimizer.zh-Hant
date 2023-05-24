---
title: 日期時間函式館
description: 日期時間函式館
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 2444d8fbe3a86feb0497d754b4f57f234fa29e49
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 4%

---

# 日期時間函式{#date-time}

日期和時間函式用於對Journey Optimizer內的值執行日期和時間操作。

## 年齡{#age}

的 `age` 函式用於從給定日期檢索年齡。

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

## 當前時間（毫秒）{#current-time}

的 `currentTimeInMillis` 函式用於檢索當前時間（以新紀元毫秒為單位）。

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

的 `dateDiff` 函式用於檢索兩個日期（天數）之間的差。

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


## 週中的日{#day-week}

的 `dayOfWeek` 函式用於檢索星期幾。

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

的 `dayOfYear` 函式用於檢索年中的某一天。

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

## 格式日期{#format-date}

的 `formatDate` 函式用於格式化日期時間值。 格式應為有效的Java DateTimeFormat模式。

**語法**

```sql
{%= formatDate(datetime, format) %}
```

其中，第一個字串是date屬性，第二個值是要轉換和顯示日期的方式。

>[!NOTE]
>
> 如果日期模式無效，則日期將回退到ISO標準格式。
>
> 可以使用Java日期格式化函式，如中所概述 [Oracle文檔](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**範例**

以下操作將以下列格式返回日期：MM/DD/YY

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## 使用區域設定支援設定日期格式{#format-date-locale}

的 `formatDate` 函式用於將日期時間值格式化為其相應的語言敏感表示，即在所需語言環境中。 格式應為有效的Java DateTimeFormat模式。

**語法**

```sql
{%= formatDate(datetime, format, locale) %}
```

其中，第一個字串是date屬性，第二個值是您希望轉換和顯示日期的方式，第三個值以字串格式表示區域設定。

>[!NOTE]
>
> 如果日期模式無效，則日期將回退到ISO標準格式。
>
> 可以使用Java日期格式化函式，如中所概述 [Oracle文檔](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html)。
>
> 可以使用格式設定和有效語言環境，如中所概述 [Oracle文檔](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 和 [支援的語言環境](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html)。


**範例**

以下操作將以下列格式返回日期：MM/DD/YY和法國地區。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## 設定天數{#set-days}

的 `setDays` 函式用於設定給定日期時間的月份日。

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

## 設定小時數{#set-hours}

的 `setHours` 函式用於設定日期時間的小時。

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


## 到UTC{#to-utc}

的 `toUTC` 函式用於將日期時間轉換為UTC。


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


## 每年的周UTC{#week-of-year}

的 `weekOfYear` 函式用於檢索年中的周。

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