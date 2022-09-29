---
product: adobe campaign
title: toDateOnly
description: 了解函式toDateOnly
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: cca94d15da5473aa9890c67af7971f2e745d261e
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 9%

---

# toDateOnly{#toDateOnly}

將引數轉換為dateOnly類型值。 若要進一步了解資料類型，請參閱 [節](../expression/data-types.md).

## 類別

轉換

## 函式語法

`toDateOnly(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期的字串表示方式為「YYYY-MM-DD」（XDM格式）。 也支援ISO-8601格式：僅限 **完整日期** 部分(請參閱 [RFC 3339，第5.6節](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | 字串 |
| 日期時間 | dateTime |
| 無時區的日期時間 | dateTimeOnly |
| 以毫秒為單位的整數值 | 整數 |

## 簽名和返回的類型

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

傳回dateOnly類型值。

## 範例

`toDateOnly("2016-08-18")`

`toDateOnly("2016-08-18T00:00:00.000Z")`

`toDateOnly("2016-08-18T00:00:00")`

所有報表都會傳回代表2016-08-18的dateOnly物件。

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

傳回dateOnly。
