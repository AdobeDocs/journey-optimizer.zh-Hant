---
product: journey optimizer
title: replace
description: 了解函式取代
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: replace，函式，表達式，歷程
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 10%

---

# replace {#replace}

以基本字串中的取代字串取代與目標字串相符的第一個出現次數。

替換從字串的開頭到結尾，例如，將字串&quot;aaa&quot;中的&quot;aa&quot;取代為&quot;b&quot;將產生&quot;ba&quot;而非&quot;ab&quot;。

## 類別

字串

## 函式語法

`replace(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|--------------|
| 基礎 | 字串 |
| Target | 字串(RegExp) |
| 更換 | 字串 |

## 簽名和返回類型

`replace(<base>,<target>,<replacement>)`

傳回字串。

## 範例 1

`replace("Hello World", "l", "x")`

返回&quot;Hexlo World&quot;。

## 範例 2 {#example_2}

由於目標參數為RegExp，因此根據您要取代的字串，您可能需要逸出某些字元。 其範例如下：

* 要評估的字串： `|OFFER_A|OFFER_B`
* 由設定檔屬性提供 `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* 要替換的字串： `|OFFER_A`
* 字串取代為： `''`
* 您需要新增 `\\` 在 `|` 字元。

運算式為：

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

傳回的字串為： `|OFFER_B`

您也可以建立要從指定屬性取代的字串：

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`
