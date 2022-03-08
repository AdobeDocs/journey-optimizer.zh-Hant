---
product: adobe campaign
title: notEqualIgnoreCase
description: 瞭解函式notEqualIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 13%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

檢查帶有第二個參數字串的第一個參數字串是否不同，忽略大小寫注意事項。

## 類別

字串

## 函式語法

`notEqualIgnoreCase(<parameters>)`

## 參數

* 字串

## 簽名和返回的類型

`notEqualIgnoreCase(<string>,<string>)`

返回布爾值。

## 範例

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
