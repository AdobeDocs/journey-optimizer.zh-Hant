---
product: journey optimizer
title: toDateTime
description: 瞭解函式toDateTime
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateTime，函式，運算式，歷程
exl-id: 2b487e60-593e-4bf7-9639-f469ba0f5cdc
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 10%

---

# toDateTime {#toDateTime}

根據引數的型別，將其轉換為日期時間值。

## 類別

轉換

## 函式語法

`toDateTime(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| ISO-8601格式的日期時間 | 字串 |
| 時區id | 字串 |
| 沒有時區的日期時間 | dateTimeOnly |
| 紀元的整數值（以毫秒為單位） | 整數 |

>[!NOTE]
>
>時區ID必須是字串常數。 它不能是欄位參考或運算式。 如需資料型別的詳細資訊，請參閱[此頁面](../expression/data-types.md)。

## 簽章與傳回的型別

`toDateTime(<string>)`

`toDateTime(<stringified time zone id>, <dateTimeOnly>)`

`toDateTime(<integer>)`

傳回&#x200B;**日期時間**。

<!--`toDateTime(<year>,<month>,<dayOfMonth>,<hour>,<minute>,<second>)`

Returns a date time with default time zone UTC.

`toDateTime(<year>,<month>,<dayOfMonth>)`
`toDateTime(<stringified timeZone>,<year>,<month>,<dayOfMonth>)`
`toDateTime(<timeZone>,<year>,<month>,<dayOfMonth>)`

Return a datetime where hour, minute and second set to 0.

`toDateTime(<stringified timeZone>,<year>,<month>,<dayOfMonth>,<hour>,<minute>,<second>)`
`toDateTime(<string>)`
`toDateTime(<string>,<integer>)`
`toDateTime(<stringified timeZone>,<dateTimeOnly)`

`toDateTime(<timeZone>,<integer>)`

Return a datetime.

-->

## 範例

`toDateTime ("2023-08-18T23:17:59.123Z")`

傳回2023-08-18T23:17:59.123Z

`toDateTime(toDateTimeOnly("UTC", "2023-08-18T23:17:59.123"))`

傳回2023-08-18T23:17:59.123Z

`toDateTime(1560762190189)`

傳回2023-06-17T09:03:10.189Z

<!--`toDateTime ("2016-08-18T23:17:59.123", "UTC")`

Returns 2016-08-18T23:17:59.123Z.

`toDateTime("Z",2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000Z.

`toDateTime("Z",2016,8,18)`

Returns 2016-08-18T00:00:00.000Z.-->
