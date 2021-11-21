---
product: adobe campaign
title: notEqualIgnoreCase
description: 了解函式notEqualIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 13%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

檢查包含第二個引數字串的第一個引數字串是否不同，忽略大小寫考量事項。

## 類別

字串

## 函式語法

`notEqualIgnoreCase(<parameters>)`

## 參數

* 字串

## 簽名和返回類型

`notEqualIgnoreCase(<string>,<string>)`

傳回布林值。

## 範例

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
