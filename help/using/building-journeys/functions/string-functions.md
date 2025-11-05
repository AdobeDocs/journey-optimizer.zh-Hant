---
product: journey optimizer
title: 字串函式
description: 瞭解字串函式
feature: Journeys
role: Developer
level: Experienced
keywords: 字串，函式，運算式，歷程，文字，操控
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 15%

---

# 字串函式 {#string-functions}

字串函式可讓您操控和處理歷程運算式中的文字值。 這些功能對於客戶歷程中的文書處理、驗證、轉換和分析至關重要。

當您需要以下動作時，請使用字串函式：

* 串連並合併多個文字值([concat](#concat))
* 搜尋特定文字模式或子字串([contain](#contain)，[containIgnoreCase](#containIgnoreCase)，[indexOf](#indexOf)，[lastIndexOf](#lastIndexOf)，[matchRegExp](#matchRegExp))
* 比較具有區分大小寫或不區分大小寫相符專案([equalIgnoreCase](#equalIgnoreCase)， [notEqualIgnoreCase](#notEqualIgnoreCase))的字串
* 檢查字串開始和結束([startWith](#startWith)，[startWithIgnoreCase](#startWithIgnoreCase)，[endWith](#endWith)，[endWithIgnoreCase](#endWithIgnoreCase))
* 使用子字串作業擷取部分文字([substr](#substr))
* 將文字轉換為大寫或小寫([upper](#upper)， [lower](#lower)， [trim](#trim))
* 檢查字串是否為空白或包含特定值([isEmpty](#isEmpty)， [isNotEmpty](#isNotEmpty))
* 以新值取代文字模式([replace](#replace)，[replaceAll](#replaceAll))
* 將字串分割為陣列以供進一步處理（[分割](#split)）
* 取得字串長度([length](#length))或產生唯一識別碼([uuid](#uuid))

字串函式提供完整的文字操控功能，可讓您根據歷程運算式中的文字內容，進行複雜的資料處理和條件式邏輯。

## concat {#concat}

串連兩個字串引數或字串清單。

+++語法

`concat(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 清單 | listString |
| 字串 | 字串 |

+++

+++簽章與傳回的型別

`concat(<string>,<string>)`

`concat(<listString>)`

傳回字串。

+++

+++範例

`concat("Hello","World")`

傳回「HelloWorld」。

`concat(["Hello"," ","World"])`

傳回「Hello World」。

+++

## contain {#contain}

檢查第二個引數字串是否包含在第一個引數字串中。

+++語法

`contain(<parameters>)`

+++

+++參數

* 字串

+++

+++簽章與傳回的型別

`contain(<string>,<string>)`

傳回布林值。

+++

+++範例

`contain("rowing is great", "great")`

傳回true。

+++

## containIgnoreCase {#containIgnoreCase}

檢查第二個引數字串是否包含在第一個引數字串中，而不考慮大小寫。

+++語法

`containIgnoreCase(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 搜尋的字串 | 字串 |

+++

+++簽章與傳回的型別

`containIgnoreCase(<string>,<string>)`

傳回布林值。

+++

+++範例

`containIgnoreCase("rowing is great", "GREAT")`

傳回true。

+++

## endWith {#endWith}

如果第二個引數是第一個引數的尾碼，則傳回true。

+++語法

`endWith(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 尾碼 | 字串 |

+++

+++簽章與傳回的型別

`endWith(<string>,<string>)`

傳回布林值。

+++

+++範例

`endWith("Hello World", "World")`

傳回true。

`endWith("Hello World", "Hello")`

傳回false。

+++

## endWithIgnoreCase {#endWithIgnoreCase}

檢查第一個引數字串是否以特定字串（第二個引數字串）結尾，並未考慮大小寫。

+++語法

`endWithIgnoreCase(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 尾碼 | 字串 |

+++

+++簽章與傳回的型別

`endWithIgnoreCase(<string>,<string>)`

傳回布林值。

+++

+++範例

`endWithIgnoreCase("rowing is great", "AT")`

傳回true。

+++

## equalIgnoreCase {#equalIgnoreCase}

比較第一個引數字串與第二個引數字串，忽略大小寫考量。

+++語法

`equalIgnoreCase(<parameters>)`

+++

+++參數

* 字串

+++

+++簽章與傳回的型別

`equalIgnoreCase(<string>,<string>)`

傳回布林值。

+++

+++範例

`equalIgnoreCase("rowing is great", "rowing is GREAT")`

傳回true。

+++

## indexOf {#indexOf}

傳回第二個引數在第一個引數中第一次出現的位置。 如果沒有相符專案，則傳回–1。

+++語法

`indexOf(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 指定值 | 字串 |

+++

+++簽章與傳回的型別

`indexOf(<string>,<string>)`

傳回整數。

+++

+++範例

`indexOf("Hello", "l")`

傳回2。

說明：

在「Hello」中，「l」的第一次出現位置為位置2。

+++

## IsEmpty {#isEmpty}

如果引數中的字串沒有字元，則傳回true。

+++語法

`isEmpty(<parameters>)`

+++

+++參數

* 字串

+++

+++簽章與傳回的型別

`isEmpty(<string>)`

傳回布林值。

+++

+++範例

`isEmpty("")`

傳回true。

`isEmpty("Hello World")`

傳回false。

+++

## isNotEmpty {#isNotEmpty}

如果引數中的字串不是空的，則傳回true。

+++語法

`isNotEmpty(<parameters>)`

+++

+++參數

* 字串

+++

+++簽章與傳回的型別

`isNotEmpty(<string>)`

傳回布林值。

+++

+++範例

`isNotEmpty("")`

傳回false。

`isNotEmpty("hello")`

傳回true。

+++

## lastIndexOf {#lastIndexOf}

傳回第二個引數最後一次出現的位置（在第一個引數中）。 如果沒有相符專案，則傳回–1。

+++語法

`lastIndexOf(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 指定值 | 字串 |

+++

+++簽章與傳回的型別

`lastIndexOf(<string>,<string>)`

傳回整數。

+++

+++範例

`lastIndexOf("Hello", "l")`

傳回3。

說明：

在「Hello」中，「l」的最後一次出現位於位置3。

+++

## 長度 {#length}

傳回引數中字串運算式的字元數。

+++語法

`length(<parameters>)`

+++

+++參數

* 字串

+++

+++簽章與傳回的型別

`length(<string>)`

傳回整數。

+++

+++範例

`length("Hello World")`

傳回11。

+++

## lower {#lower}

傳回小寫版本的引數。

+++語法

`lower(<parameter>)`

+++

+++參數

* 字串

+++

+++簽章與傳回的型別

`lower(<string>)`

傳回字串。

+++

+++範例

`lower("A")`

傳回「a」。

+++

## matchRegExp {#matchRegExp}

如果第一個引數中的字串符合第二個引數中的規則運算式，則傳回true。 如需詳細資訊，請參閱[此頁面](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html)。

+++語法

`matchRegExp(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|--- |--- |
| 字串 | 字串 |
| regexp | 字串 |

+++

+++簽章與傳回的型別

`matchRegExp(<string>,<string>)`

傳回布林值。

+++

+++範例

`matchRegExp("12345", "\\d+")`

傳回true。

+++

## notEqualIgnoreCase {#notEqualIgnoreCase}

檢查第一個引數字串是否與第二個引數字串不同，忽略大小寫考量。

+++語法

`notEqualIgnoreCase(<parameters>)`

+++

+++參數

* 字串

+++

+++簽章與傳回的型別

`notEqualIgnoreCase(<string>,<string>)`

傳回布林值。

+++

+++範例

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`

+++

## replace {#replace}

以基礎字串中的取代字串取代符合目標字串的第一個專案。

例如，取代會從字串的開頭到結尾進行，將字串「aaa」中的「aa」取代為「b」將會產生「ba」而非「ab」。

+++語法

`replace(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|--------------|
| 基底 | 字串 |
| 目標 | 字串(RegExp) |
| 取代 | 字串 |

+++

+++簽章與傳回的型別

`replace(<base>,<target>,<replacement>)`

傳回字串。

+++

+++範例

`replace("Hello World", "l", "x")`

傳回「Hexlo World」。

具有RegExp的&#x200B;**範例：**

由於目標引數是RegExp，因此根據您要取代的字串，您可能需要將部分字元逸出。 其範例如下：

* 要評估的字串： `|OFFER_A|OFFER_B`
* 由設定檔屬性`#{ExperiencePlatform.myFieldGroup.profile.myOffers}`提供
* 要取代的字串： `|OFFER_A`
* 字串取代為： `''`
* 您必須在`\\`字元前新增`|`。

運算式為：

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

傳回的字串是： `|OFFER_B`

您也可以建置要由指定屬性取代的字串：

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`

+++

## replaceAll {#replaceAll}

以基礎字串中的取代字串取代所有符合目標字串的相符專案。

例如，取代會從字串的開頭到結尾進行，將字串「aaa」中的「aa」取代為「b」將會產生「ba」而非「ab」。

+++語法

`replaceAll(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|--------------|
| 基底 | 字串 |
| 目標 | 字串(RegExp) |
| 取代 | 字串 |

+++

+++簽章與傳回的型別

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

傳回字串。

+++

+++範例

`replaceAll("Hello World", "l", "x")`

傳回「Hexxo Worxd」。

由於目標引數是RegExp，因此根據您要取代的字串，您可能需要將部分字元逸出。 請參考[取代](#replace)函式中的範例。

+++

## split {#split}

以分隔字串分割第一個引數字串（第二個引數字串，可以是規則運算式），以產生字串（代號）清單。

+++語法

`split(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 輸入字串 | 字串 |
| 分隔符號字串 | 字串 |

+++

+++簽章與傳回型別

`split(<input string>, <separator string>)`

傳回listString。

+++

+++範例

`split("A_B_C", "_")`

傳回`["A","B","C"]`

具有下列值的事件欄位「event.appVersion」範例：「20.45.2.3434」

`split(@event{event.appVersion}, "\\.")`

傳回`["20", "45", "2", "3434"]`

+++

## startWith {#startWith}

如果第二個引數是第一個引數的前置詞，則傳回true。

+++語法

`startWith(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-------------|--------|
| 字串 | 字串 |
| 前置詞 | 字串 |

+++

+++簽章與傳回的型別

`startWith(<string>,<string>)`

傳回布林值。

+++

+++範例

`startWith("Hello World", "Hello")`

傳回true。

`startWith("Hello World", "World")`

傳回false。

+++

## startWithIgnoreCase {#startWithIgnoreCase}

如果第二個引數是第一個引數的前置詞，則傳回true，而不考慮大小寫。

+++語法

`startWithIgnoreCase(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-------------|--------|
| 字串 | 字串 |
| 前置詞 | 字串 |

+++

+++簽章與傳回的型別

`startWithIgnoreCase(<string>,<string>)`

傳回布林值。

+++

+++範例

`startWithIgnoreCase("rowing is great", "RO")`

傳回true。

+++

## substr {#substr}

傳回開始索引和結束索引之間的字串運算式的子字串。 如果未定義結束索引，則它介於開始索引和結束索引之間。

+++語法

`substr(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-------------|----------|
| 字串 | 字串 |
| beginindex | 整數 |
| endIndex | 整數 |

+++

+++簽章與傳回的型別

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

傳回字串。

+++

+++範例

`substr("Hello World",6)`

傳回「World」。

`substr("Hello World", 0, 5)`

傳回「Hello」。

+++

## trim {#trim}

移除開始和結束空格。

+++語法

`trim(<parameters>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |

+++

+++簽章與傳回的型別

`trim(<string>)`

傳回字串。

+++

+++範例

`trim(" Hello ")`

傳回「Hello」。

+++

## upper {#upper}

傳回引數的大寫版本。

+++語法

`upper(<parameters>)`

+++

+++簽章與傳回的型別

`upper(<string>)`

傳回字串。

+++

+++範例

`upper("b")`

傳回「B」。

+++

## UUID {#uuid}

產生隨機UUID （通用唯一識別碼）。

+++語法

`uuid()`

+++

+++參數 

此函式不需要引數。

+++

+++簽章與傳回的型別

`uuid()`

傳回字串。

+++

+++範例

`uuid()`

傳回「79e70b7f-8a85-400b-97a1-9f9826121553」。

+++

