---
product: journey optimizer
title: replace
description: 瞭解函式取代
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 取代，函式，運算式，歷程
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 10%

---

# replace {#replace}

以基礎字串中的取代字串取代符合目標字串的第一個專案。

取代會從字串的開頭到結尾進行，例如，將字串「aaa」中的「aa」取代為「b」將會產生「ba」而不是「ab」。

## 類別

字串

## 函式語法

`replace(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|--------------|
| 基底 | 字串 |
| Target | 字串(RegExp) |
| 取代 | 字串 |

## 簽章和傳回的型別

`replace(<base>,<target>,<replacement>)`

傳回字串。

## 範例 1

`replace("Hello World", "l", "x")`

傳回「Hexlo World」。

## 範例 2 {#example_2}

由於目標引數是RegExp，因此根據您要取代的字串，您可能需要逸出部分字元。 其範例如下：

* 要評估的字串： `|OFFER_A|OFFER_B`
* 由設定檔屬性提供 `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* 要取代的字串： `|OFFER_A`
* 字串取代為： `''`
* 您需要新增 `\\` 早於 `|` 字元。

運算式為：

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

傳回的字串是： `|OFFER_B`

您也可以建置要由指定屬性取代的字串：

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`
