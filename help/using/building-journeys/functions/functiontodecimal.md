---
product: adobe campaign
title: toDecimal
description: 瞭解函式toDecimal
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 14%

---

# 到十進位 {#toDecimal}

根據參數值的類型將參數值轉換為小數值。

## 類別

轉換

## 函式語法

`toDecimal(<parameter>)`

## 參數

| 參數 | 說明 |
|--- |--- |
| 字串 | 將字串值轉換為小數 |
| 日期時間 | 將日期轉換為毫秒數（新紀元毫秒） |
| 布林值 | 如果為true，則將布爾值轉換為1；如果為false，則將布爾值轉換為0 |
| 整數 | 轉換為小數（示例）。:1變為1.0) |

## 簽名和返回的類型

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

返回小數。

## 範例

`toDecimal("4.0")`

返回4.0。
