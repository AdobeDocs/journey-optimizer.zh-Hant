---
product: journey optimizer
title: notEqualIgnoreCase
description: 了解函式notEqualIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 0%

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
