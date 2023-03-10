---
title: 日期時間函式程式庫
description: 日期時間函式程式庫
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

日期和時間函式可用來對Journey Optimizer內的值執行日期和時間操作。

## 年齡{#age}

此 `age` 函式可用來從指定日期擷取年齡。

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

## 當前時間（以毫秒為單位）{#current-time}

此 `currentTimeInMillis` 函式可用來擷取目前時間（以epoch毫秒為單位）。

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

此 `dateDiff` 函式可用來擷取兩個日期之間以天數表示的差異。

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

此 `dayOfWeek` 函式可用來擷取星期。

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

此 `dayOfYear` 函式可用來擷取一年當中的某天。

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

## 日期格式{#format-date}

此 `formatDate` 函式來設定日期時間值的格式。 格式應為有效的Java DateTimeFormat模式。

**語法**

```sql
{%= formatDate(datetime, format) %}
```

其中第一個字串是日期屬性，第二個值是您要如何轉換和顯示日期。

>[!NOTE]
>
> 如果日期模式無效，日期將回復為ISO標準格式。
>
> 您可以使用Java日期格式功能，如 [Oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**範例**

下列操作會以下列格式傳回日期：MM/DD/YY。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## 使用地區支援設定日期格式{#format-date-locale}

此 `formatDate` 函式用於將日期時間值格式化為其相應的語言敏感表示，即在所需地區中。 格式應為有效的Java DateTimeFormat模式。

**語法**

```sql
{%= formatDate(datetime, format, locale) %}
```

其中第一個字串是日期屬性，第二個值是要如何轉換和顯示日期，第三個值以字串格式表示地區。

>[!NOTE]
>
> 如果日期模式無效，日期將回復為ISO標準格式。
>
> 您可以使用Java日期格式功能，如 [Oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> 您可以使用格式設定和有效的地區設定，如 [Oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 和 [支援的地區設定](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).


**範例**

下列操作會以下列格式傳回日期：MM/DD/YY和地區法國。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## 設定天數{#set-days}

此 `setDays` 函式可用來設定指定日期時間的月中某天。

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

此 `setHours` 函式可用來設定日期時間的小時。

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

此 `toUTC` 函式用於將datetime轉換為UTC。


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

此 `weekOfYear` 函式可用來擷取一年中的某周。

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