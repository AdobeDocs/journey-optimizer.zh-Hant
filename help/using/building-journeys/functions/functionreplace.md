---
product: adobe campaign
title: replace
description: 瞭解函式替換
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
source-git-commit: 87b8056d26fe91a71e92ca346a9811c609d41128
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 10%

---

# 替換 {#replace}

用基本字串中的替換字串替換與目標字串匹配的第一個匹配項。

替換從字串的開頭到結尾，例如，在字串&quot;aaa&quot;中將&quot;aa&quot;替換為&quot;b&quot;將導致&quot;ba&quot;而不是&quot;ab&quot;。

## 類別

字串

## 函式語法

`replace(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|--------------|
| 基礎 | 字串 |
| Target | 字串(RegExp) |
| 替換 | 字串 |

## 簽名和返回的類型

`replace(<base>,<target>,<replacement>)`

返回字串。

## 範例 1

`replace("Hello World", "l", "x")`

返回&quot;Hexlo World&quot;。

## 範例 2 {#example_2}

由於目標參數是RegExp，因此您可能需要轉義一些字元，具體取決於要替換的字串。 其範例如下：

* 要計算的字串： `|OFFER_A|OFFER_B`
* 由配置檔案屬性提供 `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* 要替換的字串： `|OFFER_A`
* 字串替換為： `''`
* 您需要添加 `\\` 在 `|` 字元。

表達式為：

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

返回的字串為： `|OFFER_B`

您還可以構建要從給定屬性替換的字串：

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`
