---
product: journey optimizer
title: 清單函式
description: 瞭解清單函式
feature: Journeys
role: Developer
level: Experienced
keywords: 清單，函式，運算式，歷程，陣列，集合
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 9%

---

# 清單函式 {#list-functions}

清單函式可讓您操控和處理歷程運算式中的值集合。 這些功能對於篩選、排序、轉換和分析客戶歷程中的陣列和清單至關重要。

當您有以下需要時，請使用清單函式：

* 根據條件（[篩選](#filter)，[getListItem](#getListItem)）從集合中篩選及擷取特定專案
* 以遞增或遞減順序排序及組織清單專案（[排序](#sort)）
* 移除重複專案，並從清單([distinct](#distinct)， [distinctWithNull](#distinctWithNull))取得唯一值
* 檢查集合中是否存在值([in](#in))
* 限制從清單傳回的專案數([limit](#limit))
* 取得清單([listSize](#listSize))的大小，或將清單轉換為不同的格式([serializeList](#serializeList))
* 執行集合作業，例如在清單之間尋找共同元素（[相交](#intersect)）

清單函式提供強大的工具，用於處理複雜的資料結構，實現複雜的資料操作和根據收集內容的條件式邏輯。

## distinct {#distinct}

傳回給定清單的不同值或物件。 會忽略Null專案。

+++語法

`distinct(<parameters>)`

+++

+++參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要處理的清單。 對於listObject，它必須是欄位參考。 |
| keyAttributeName | 字串 | 此引數是選用專案，且僅適用於listObject。 如果未提供引數，如果所有屬性的值都相同，則會將物件視為重複。 否則，如果給定的屬性具有相同的值，則會將物件視為重複。 |

+++

+++簽章與傳回的型別

`distinct(<listInteger>)`

傳回整數清單。

`distinct(<listDecimal>)`

傳回小數點清單。

`distinct(<listString>)`

傳回字串清單。

`distinct(<listDateTimeOnly>)`

傳回日期時間清單，不考慮時區。

`distinct(<listDateTime>)`

傳回日期時間清單。

`distinct(<listDateOnly>)`

傳回日期清單。

`distinct(<listBoolean>)`

傳回布林值清單。

`distinct(<listDuration>)`

傳回持續時間清單。

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

傳回物件清單。

+++

+++範例

`distinct([10,2,10,null])`

傳回`[10, 2]`。

+++

## distinctWithNull {#distinctWithNull}

傳回給定清單的不同值或物件。 如果清單中至少有一個null專案，則傳回的清單中會出現null專案。

+++語法

`distinctWithNull(<parameters>)`

+++

+++參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString， listBoolean， listInteger， listDecimal， listDuration， listDateTime， listDateTimeOnly， listDateOnly | 要處理的清單。 |

+++

+++簽章與傳回的型別

`distinctWithNull(<listInteger>)`

傳回整數清單。

`distinctWithNull(<listDecimal>)`

傳回小數點清單。

`distinctWithNull(<listString>)`

傳回字串清單。

`distinctWithNull(<listDateTimeOnly>)`

傳回日期時間清單，不考慮時區。

`distinctWithNull(<listDateTime>)`

傳回日期時間清單。

`distinctWithNull(<listDateOnly>)`

傳回日期清單。

`distinctWithNull(<listBoolean>)`

傳回布林值清單。

`distinctWithNull(<listDuration>)`

傳回持續時間清單。

+++

+++範例

`distinctWithNull([10,2,10,null])`

傳回[10， 2， null]

+++

**注意：**&#x200B;此函式不支援引數`<listObject>`。

## 篩選 {#filter}

傳回listObject，其中物件的索引鍵屬性符合其中一個指定的索引鍵值。

+++語法

`filter(<parameters>)`

+++

+++參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToFilter | listObject | 要篩選的物件清單。 它必須是欄位參考。 |
| keyAttributeName | 字串 | 指定清單物件中的屬性名稱，用來作為篩選的索引鍵 |
| keyValueList | list | 用於篩選的索引鍵值陣列 |

+++

+++簽章與傳回的型別

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

傳回listObject。

+++

+++範例

以下是在傳入事件「myevent」中傳遞的裝載範例：

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

您可以使用下列運算式：

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

傳回listObject，其中包含以&quot;product2&quot;和&quot;product3&quot;作為ID的兩個物件。

+++

## getListItem {#getListItem}

傳回指定索引處的清單專案。

+++語法

`getListItem(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| 索引 | 整數 |

+++

+++簽章與傳回型別

`getListItem(<listInteger>,<index>)`

傳回整數。

`getListItem(<listDecimal>,<index>)`

傳回小數。

`getListItem(<listString>,<index>)`

傳回字串。

`getListItem(<listDateTimeOnly>,<index>)`

傳回日期時間，不考慮時區。

`getListItem(<listDateTime>,<index>)`

傳回日期時間。

`getListItem(<listDateOnly>,<index>)`

傳回日期清單。

`getListItem(<listBoolean>,<index>)`

傳回布林值。

`getListItem(<listDuration>,<index>)`

傳回持續時間。

+++

+++範例

`getListItem([10, 2, 3], 1)`

傳回「2」

`getListItem(["A", "B", "C"], 2)`

傳回「C」

具有事件欄位「event.appVersion」且值為「20.45.2.3434」的範例

`split(@event{event.appVersion}, "\\.")`

傳回`["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

傳回「20」

+++

## 在  {#in}

檢查第一個引數值是否在清單中。 檢查會透過每個引數值上的「等於」來執行。 如果找到引數值，則傳回true，否則傳回false。

`<expression>`的型別必須與清單的專案相符。 提醒清單的專案型別必須彼此相符。

+++語法

`in(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 布林值 | 布林值 |
| 整數 | 整數 |
| 小數 | 小數 |
| 持續時間 | 持續時間 |
| 日期時間 | 日期時間 |
| DateTimeOnly | DateTimeOnly |
| 清單 | listString |
| 清單 | listBoolean |
| 清單 | listInteger |
| 清單 | listDecimal |
| 清單 | listDuration |
| 清單 | listDateTime |
| 清單 | listDateTimeOnly |
| 清單 | listDateOnly |

+++

+++簽章與傳回的型別

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

傳回布林值。

+++

+++範例

`in(4,[4,5,3,4])`

傳回true。

`in(8,[4,5,3,4])`

傳回false。

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`

+++

## 相交 {#intersect}

傳回兩個輸入清單中的通用值。 如果兩個清單之一為空，則會傳回空白清單。

+++語法

`intersect(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 清單1 | list |
| 清單2 | list |

+++

+++簽章與傳回的型別

`intersect(listString,listString)`： listString

`intersect(listDecimal,listDecimal)`： listDecimal

`intersect(listInteger,listInteger)`： listInteger

`intersect(listDateTime,listDateTime)`： listDateTime

`intersect(listDateTimeOnly,listDateTimeOnly)`： listDateTimeOnly

`intersect(listDateOnly,listDateOnly)`： listDateOnly

`intersect(listDuration,listDuration)`： listDuration

`intersect(listBoolean,listBoolean)`：清單布林值

傳回清單。

+++

+++範例

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

傳回[&quot;sports&quot;，&quot;news&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

傳回設定檔屬性和指定類別清單之間的通用專案。

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

傳回設定檔屬性和指定事件欄位之間的通用專案。

+++

## limit {#limit}

傳回清單的第一個或最後的N個元素。

+++語法

`limit(<parameters>)`

+++

+++參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要考量的清單。 對於listObject，它必須是欄位參考。 |
| numberofItems | 整數 | 要從指定清單傳回的專案數。 |
| firstOrLastItems | 布林值 | 此引數為選用（預設為true）。 true會傳回第一個專案。 false會傳回最後一個專案。 |

+++

+++簽章與傳回的型別

`limit(<listString>,<integer>)`

`limit(<listString>,<integer>,<boolean>)`

傳回字串清單。

`limit(<listInteger>,<integer>)`

`limit(<listInteger>,<integer>,<boolean>)`

傳回整數清單。

`limit(<listDecimal>,<integer>)`

`limit(<listDecimal>,<integer>,<boolean>)`

傳回小數點清單。

`limit(<listBoolean>,<integer>)`

`limit(<listBoolean>,<integer>,<boolean>)`

傳回布林值清單。

`limit(<listDateOnly>,<integer>)`

`limit(<listDateOnly>,<integer>,<boolean>)`

傳回日期清單。

`limit(<listDateTimeOnly>,<integer>)`

`limit(<listDateTimeOnly>,<integer>,<boolean>)`

傳回日期時間清單，不考慮時區。

`limit(<listDateTime>,integer>)`

`limit(<listDateTime>,<integer>,<boolean>)`

傳回日期時間清單。

`limit(<listDuration>,<integer>)`

`limit(<listDuration>,<integer>,<boolean>)`

傳回持續時間清單。

`limit(<listObject>,<integer>)`

`limit(<listObject>,<integer>,<boolean>)`

傳回物件清單。

+++

+++範例

`limit(["A", "B", "C", "D", "E"], 3)`

傳回`["A","B","C"]`。

`limit(["A", "B", "C", "D", "E"], 3, false)`

傳回`["C","D","E"]`。

+++

## listSize {#listSize}

計算清單中的元素數量。

+++語法

`listSize(<parameters>)`

+++

+++參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要處理的清單。 對於listObject，它必須是欄位參考。 listObject不能包含null物件。 |

+++

+++簽章與傳回型別

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

傳回整數。

`listSize(<listObject>)`

+++

+++範例

`listSize([10,2,3])`

傳回3。

`listSize(@event{my_event.productListItems})`

傳回給定物件陣列（listObject型別）中的物件數目。

+++

## serializeList {#serializeList}

將指定清單（listObject以外的任何型別）轉換為字串。

+++語法

`serializeList(<parameters>)`

+++

+++參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString， listBoolean， listInteger， listDecimal， listDuration， listDateTime， listDateTimeOnly， listDateOnly | 要轉換為字串的清單。 |
| 分隔符號 | 字串 | 輸出字串中每個清單元素之間的分隔符號。 |
| addQuotes | 布林值 | 此引數指出輸出字串中的每個元素是否應該包含引號(true)。 |

+++

+++簽章與傳回的型別

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

傳回字串。

+++

+++範例

`serializeList(["Hello","World"], " ", false)`

傳回「Hello World」。

`serializeList(["Hello", "World"], ",", true)`

傳回&quot;Hello&quot;、&quot;World&quot;。

+++

## sort {#sort}

以自然順序排序值或物件清單。

+++語法

`sort(<parameters>)`

+++

+++參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToSort | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要排序的清單。 對於listObject，它必須是欄位參考。 |
| keyAttributeName | 字串 | 此引數僅適用於listObject。 指定清單物件中的屬性名稱會作為排序的索引鍵。 |
| sortingOrder | 布林值 | 遞增(true)或遞減(false) |

+++

+++簽章與傳回的型別

`sort(<listInteger>,<boolean>)`

傳回整數清單。

`sort(<listDecimal>,<boolean>)`

傳回小數點清單。

`sort(<listString>,<boolean>)`

傳回字串清單。

`sort(<listDateTimeOnly>,<boolean>)`

傳回日期時間清單，不考慮時區。

`sort(<listDateTime>,<boolean>)`

傳回日期時間清單。

`sort(<listDateOnly>,<boolean>)`

傳回日期清單。

`sort(<listBoolean>,<boolean>)`

傳回布林值清單。

`sort(<listObject>,<string>,<boolean>)`

傳回物件清單。

+++

+++範例

`sort(["A", "C", "B"], true)`

傳回`["A","B","C"]`。

`sort([1, 3, 2], false)`

傳回`[3, 2, 1]`。

`sort(@event{my_event.productListItems}, "SKU", true)`

傳回依SKU屬性排序的listObject （遞增順序）

+++

