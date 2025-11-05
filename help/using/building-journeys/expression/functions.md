---
solution: Journey Optimizer
product: journey optimizer
title: 函式
description: 瞭解函式
feature: Journeys
role: Developer
level: Experienced
keywords: 函式，運算式，編輯器，歷程
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: d58319d687d113ce680c415524fdea0400cb38f0
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 69%

---

# 函式 {#functions}

函式可以有不同的簽章（不同的有序引數集）。 函式簽章可以有0-N個運算式做為排序引數。

`<function name>`(`<expression as param 1>`， `<expression as param 2>`， ... ，`<expression as param N>`)

每個函式都有特定的傳回型別。

以下是支援的函式清單。

## 主要函式

| 類別 | 函數 |
|-------------|-----------------------|
| Adobe Experience Platform | [inAudience](../functions/functioninaudience.md) |
| 彙總 | [avg](../functions/aggregation-functions.md#avg) |
| 彙總 | [count](../functions/aggregation-functions.md#count) |
| 彙總 | [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) |
| 彙總 | [countWithNull](../functions/aggregation-functions.md#countWithNull) |
| 彙總 | [distinctCount](../functions/aggregation-functions.md#distinctCount) |
| 彙總 | [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) |
| 彙總 | [max](../functions/aggregation-functions.md#max) |
| 彙總 | [min](../functions/aggregation-functions.md#min) |
| 彙總 | [sum](../functions/aggregation-functions.md#sum) |
| 轉換 | [toBool](../functions/conversion-functions.md#toBool) |
| 轉換 | [toDateOnly](../functions/conversion-functions.md#toDateOnly) |
| 轉換 | [toDateTime](../functions/conversion-functions.md#toDateTime) |
| 轉換 | [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) |
| 轉換 | [toDecimal](../functions/conversion-functions.md#toDecimal) |
| 轉換 | [toDuration](../functions/conversion-functions.md#toDuration) |
| 轉換 | [toInteger](../functions/conversion-functions.md#toInteger) |
| 轉換 | [toString](../functions/conversion-functions.md#toString) |
| 日期 | [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) |
| 日期 | [inLastDays](../functions/date-functions.md#inLastDays) |
| 日期 | [inLastHours](../functions/date-functions.md#inLastHours) |
| 日期 | [inLastMonths](../functions/date-functions.md#inLastMonths) |
| 日期 | [inLastYears](../functions/date-functions.md#inLastYears) |
| 日期 | [inNextDays](../functions/date-functions.md#inNextDays) |
| 日期 | [inNextHours](../functions/date-functions.md#inNextHours) |
| 日期 | [inNextMonths](../functions/date-functions.md#inNextMonths) |
| 日期 | [inNextYears](../functions/date-functions.md#inNextYears) |
| 日期 | [now](../functions/date-functions.md#now) |
| 日期 | [nowWithDelta](../functions/date-functions.md#nowWithDelta) |
| 日期 | [setHours](../functions/date-functions.md#setHours) |
| 日期 | [setDays](../functions/date-functions.md#setDays) |
| 日期 | [updateTimeZone](../functions/date-functions.md#updateTimeZone) |
| 清單 | [distinct](../functions/list-functions.md#distinct) |
| 清單 | [distinctWithNull](../functions/list-functions.md#distinctWithNull) |
| 清單 | [篩選器](../functions/list-functions.md#filter) |
| 清單 | [getListItem](../functions/list-functions.md#getListItem) |
| 清單 | [in](../functions/list-functions.md#in) |
| 清單 | [相交](../functions/list-functions.md#intersect) |
| 清單 | [限制](../functions/list-functions.md#limit) |
| 清單 | [listSize](../functions/list-functions.md#listSize) |
| 清單 | [serializeList](../functions/list-functions.md#serializeList) |
| 清單 | [sort](../functions/list-functions.md#sort) |
| 數學 | [random](../functions/functionrandom.md) |
| 數學 | [round](../functions/functionround.md) |
| 字串 | [concat](../functions/string-functions.md#concat) |
| 字串 | [contain](../functions/string-functions.md#contain) |
| 字串 | [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) |
| 字串 | [endWith](../functions/string-functions.md#endWith) |
| 字串 | [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) |
| 字串 | [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) |
| 字串 | [indexOf](../functions/string-functions.md#indexOf) |
| 字串 | [isEmpty](../functions/string-functions.md#isEmpty) |
| 字串 | [isNotEmpty](../functions/string-functions.md#isNotEmpty) |
| 字串 | [lastIndexOf](../functions/string-functions.md#lastIndexOf) |
| 字串 | [length](../functions/string-functions.md#length) |
| 字串 | [lower](../functions/string-functions.md#lower) |
| 字串 | [matchRegExp](../functions/string-functions.md#matchRegExp) |
| 字串 | [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) |
| 字串 | [replace](../functions/string-functions.md#replace) |
| 字串 | [replaceAll](../functions/string-functions.md#replaceAll) |
| 字串 | [split](../functions/string-functions.md#split) |
| 字串 | [startWith](../functions/string-functions.md#startWith) |
| 字串 | [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) |
| 字串 | [substr](../functions/string-functions.md#substr) |
| 字串 | [trim](../functions/string-functions.md#trim) |
| 字串 | [upper](../functions/string-functions.md#upper) |
| 字串 | [uuid](../functions/string-functions.md#uuid) |
