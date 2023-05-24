---
product: journey optimizer
title: toDateOnly
description: 瞭解函式toDateOnly
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateOnly，函式，表達式，旅程
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 10%

---

# toDateOnly{#toDateOnly}

將參數轉換為dateOnly類型值。 要瞭解有關資料類型的詳細資訊，請參閱此 [節](../expression/data-types.md)。

## 類別

轉換

## 函式語法

`toDateOnly(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期的字串表示形式為「YYYY-MM-DD」（XDM格式）。 還支援ISO-8601格式：僅 **全日期** 已考慮部件(請參閱 [RFC 3339，第5.6節](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | 字串 |
| 日期時間 | 日期時間 |
| 無時區的日期時間 | 日期僅時間 |
| 時元的整數值（毫秒） | 整數 |

## 簽名和返回的類型

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

返回dateOnly類型值。

## 範例

`toDateOnly("2016-08-18")`

`toDateOnly("2016-08-18T00:00:00.000Z")`

`toDateOnly("2016-08-18T00:00:00")`

全部返回表示2016-08-18的dateOnly對象。

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

返回dateOnly。
