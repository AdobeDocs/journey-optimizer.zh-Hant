---
product: adobe campaign
title: endWith
description: 瞭解函式endWith
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 25%

---

# 結尾 {#endWith}

如果第二個參數是第一個參數的尾碼，則返回true。

## 類別

字串

## 函式語法

`endWith(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 尾碼 | 字串 |

## 簽名和返回的類型

`endWith(<string>,<string>)`

返回布爾值。

## 範例

`endWith("Hello World", "World")`

返回true。

`endWith("Hello World", "Hello")`

返回false。
