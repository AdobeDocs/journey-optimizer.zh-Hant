---
title: 字串函式庫
description: 字串函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 1d9fc184bb67362aac608e9816fe3afe64eb055c
workflow-type: tm+mt
source-wordcount: '1685'
ht-degree: 7%

---

# 字串函式 {#string}

了解如何在運算式編輯器中使用字串函式。

## 駝峰 {#camelCase}

此 `camelCase` 函式會大寫字串每個字詞的首字母。

**格式**

```sql
{%= camelCase(string)%}
```

**範例**

以下函式將大寫設定檔街道地址中的第一個字母。

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Concat {#concate}

此 `concat` 函式將兩個字串合併為一。

**格式**

```sql
{%= concat(string,string) %}
```

**範例**

下列函式會將設定檔城市和國家/地區合併為單一字串。

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## 包含 {#contains}

此 `contains` 函式來判斷字串是否包含指定的子字串。

**格式**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `STRING_1` | 要執行檢查的字串。 |
| `STRING_2` | 要在第一個字串內搜尋的字串。 |
| `CASE_SENSITIVE` | 可選參數，用於確定檢查是否區分大小寫。 可能的值：true（預設）/ false。 |

**範例**

* 下列函式將檢查設定檔名是否包含字母A（在上或下）。 如果是，則會傳回&#39;true&#39;，否則會傳回&#39;false&#39;。

   ```sql
   {%= contains(profile.person.name.firstName, "A", false) %}
   ```

* 下列查詢會區分大小寫，判斷人員的電子郵件地址是否包含字串「2010@gm」。

   ```sql
   {%= contains(profile.person.emailAddress,"2010@gm") %}
   ```

## 不包含{#doesNotContain}

此 `doesNotContain` 函式來判斷字串是否不包含指定的子字串。

**格式**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 引數 | 說明 |
| --------- | ----------- |
| `STRING_1` | 要執行檢查的字串。 |
| `STRING_2` | 要在第一個字串內搜尋的字串。 |
| `CASE_SENSITIVE` | 可選參數，用於確定檢查是否區分大小寫。 可能的值：true（預設）/ false。 |

**範例**

下列查詢會區分大小寫，判斷人員的電子郵件地址不包含字串「2010@gm」。

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## 結尾並非為{#doesNotEndWith}

此 `doesNotEndWith` 函式來判斷字串是否未以指定的子字串結尾。

**格式**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜尋的字串。 |
| `{CASE_SENSITIVE}` | 可選參數，用於確定檢查是否區分大小寫。 可能的值：true（預設）/ false。 |

**範例**

以下查詢會區分大小寫，判斷人員的電子郵件地址結尾不是「.com」。

```sql
doesNotEndWith(person.emailAddress,".com")
```

## 開頭非為{#doesNotStartWith}

此 `doesNotStartWith` 函式來判斷字串是否未以指定的子字串開頭。

**格式**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜尋的字串。 |
| `{CASE_SENSITIVE}` | 可選參數，用於確定檢查是否區分大小寫。 可能的值：true（預設）/ false。 |

**範例**

以下查詢會區分大小寫地確定人員的名稱不以「Joe」開頭。

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## 編碼64{#encode64}

此 `encode64` 函式可用來編碼字串，以保留個人資訊(PI)，例如包含在URL中。

**格式**

```sql
{%= encode64(string) %}
```

## 終止於{#endsWith}

此 `endsWith` 函式可用來判斷字串結尾是否為指定的子字串。

**格式**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜尋的字串。 |
| `{CASE_SENSITIVE}` | 可選參數，用於確定檢查是否區分大小寫。 可能的值：true（預設）/ false。 |

**範例**

下列查詢會區分大小寫，判斷人員的電子郵件地址結尾是「.com」。

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## 等於{#equals}

此 `equals` 函式可用來判斷字串是否等於指定的字串，且區分大小寫。

**格式**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串比較的字串。 |

**範例**

以下查詢區分大小寫確定人員的名稱是「John」。

```sql
{%=equals(profile.person.name,"John") %}
```

## 等於忽略大小寫{#equalsIgnoreCase}

此 `equalsIgnoreCase` 函式可用來判斷字串是否等於指定的字串，不區分大小寫。

**格式**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串比較的字串。 |

**範例**

以下查詢將不區分大小寫地確定人員的名稱是「John」。

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## 擷取電子郵件網域 {#extractEmailDomain}

此 `extractEmailDomain` 函式可用來擷取電子郵件地址的網域。

**格式**

```sql
{%= extractEmailDomain(string) %}
```

**範例**

以下查詢會擷取個人電子郵件地址的電子郵件網域。

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## 取得url主機 {#get-url-host}

此 `getUrlHost` 函式可用來擷取URL的主機名稱。

**格式**

```sql
{%= getUrlHost(string) %}: string
```

**範例**

```sql
{%= getUrlHost("http://www.myurl.com/contact") %}
```

傳回&quot;www.myurl.com&quot;

## 取得url路徑 {#get-url-path}

此 `getUrlPath` 函式可用來擷取URL網域名稱后面的路徑。

**格式**

```sql
{%= getUrlPath(string) %}: string
```

**範例**

```sql
{%= getUrlPath("http://www.myurl.com/contact.html") %}
```

傳回&quot;/contact.html&quot;

## 取得URL通訊協定 {#get-url-protocol}

此 `getUrlProtocol` 函式來擷取URL的通訊協定。

**格式**

```sql
{%= getUrlProtocol(string) %}: string
```

**範例**

```sql
{%= getUrlProtocol("http://www.myurl.com/contact.html") %}
```

傳回&quot;http&quot;

## 索引 {#index-of}

此 `indexOf` 函式可用來傳回第二參數首次出現的位置（在第一引數中）。 如果不匹配，則返回–1。

**格式**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個參數中搜尋的字串 |

**範例**

```sql
{%= indexOf("hello world","world" ) %}
```

返回6。

## Is empty {#isEmpty}

此 `isEmpty` 函式來判斷字串是否空白。

**格式**

```sql
{%= isEmpty(string) %}
```

**範例**

如果設定檔的行動電話號碼空白，下列函式會傳回&#39;true&#39;。 否則，會傳回&#39;false&#39;。

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## 非空白 {#is-not-empty}

此 `isNotEmpty` 函式來判斷字串是否非空。

**格式**

```sql
{= isNotEmpty(string) %}: boolean
```

**範例**

如果設定檔的行動電話號碼不為空，則下列函式會傳回&#39;true&#39;。 否則，會傳回&#39;false&#39;。

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## 上次索引 {#last-index-of}

此 `lastIndexOf` 函式可用來傳回第二個參數最後出現次數的位置（在第一個引數中）。 如果不匹配，則返回–1。

**格式**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個參數中搜尋的字串 |

**範例**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

返回7。

## 左修剪 {#leftTrim}

此 `leftTrim` 函式可用來從字串的開頭移除空格。

**格式**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

此 `length` 函式來取得字串或運算式中的字元數。

**格式**

```sql
{%= length(string) %}
```

**範例**

下列函式會傳回設定檔的城市名稱長度。

```sql
{%= length(profile.homeAddress.city) %}
```

## 贊{#like}

此 `like` 函式來判斷字串是否符合指定的模式。

**格式**

```sql
{%= like(STRING_1, STRING_2) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 比對第一個字串的運算式。 建立運算式時有兩個支援的特殊字元： `%` 和 `_`. <ul><li>`%` 用於表示零個或多個字元。</li><li>`_` 僅代表一個字元。</li></ul> |

**範例**

下列查詢會擷取所有使用包含模式「es」之設定檔的城市。

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## 小寫{#lower}

此 `lowerCase` 函式會將字串轉換為小寫字母。

**語法**

```sql
{%= lowerCase(string) %}
```

**範例**

此函式會將描述檔名轉換為小寫字母。

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## 符合{#matches}

此 `matches` 函式來判斷字串是否符合特定的規則運算式。 請參閱 [此文檔](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) ，以取得規則運算式中比對模式的詳細資訊。

**格式**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**範例**

以下查詢將不區分大小寫地確定人員的名稱以「John」開頭。

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## 遮色片 {#mask}

此 `Mask` 函式來將字串的一部分取代為「X」字元。

**格式**

```sql
{%= mask(string,integer,integer) %}
```

**範例**

下列查詢會以「X」字元取代「123456789」字串，但前兩個和後兩個字元除外。

```sql
{%= mask("123456789",1,2) %}
```

查詢會傳回 `1XXXXXX89`.

## MD5 {#md5}

此 `md5` 函式可用來計算並傳回字串的md5雜湊。

**格式**

```sql
{%= md5(string) %}: string
```

**範例**

```sql
{%= md5("hello world") %}
```

傳回&quot;5eb63bbbe01eeed093cb22bb8f5acdc3&quot;

## 不等於{#notEqualTo}

此 `notEqualTo` 函式來判斷字串是否不等於指定的字串。

**格式**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串比較的字串。 |

**範例**

以下查詢會區分大小寫地確定人員的名稱不是&quot;John&quot;。

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## 不等於忽略大小寫 {#not-equal-with-ignore-case}

此 `notEqualWithIgnoreCase` 函式來比較忽略大小寫的兩個字串。

**格式**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串比較的字串。 |

**範例**

以下查詢確定人員的名稱是否不是&quot;john&quot;，不區分大小寫。

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## 規則運算式群組{#regexGroup}

此 `Group` 函式用於根據提供的規則運算式來擷取特定資訊。

**格式**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING}` | 要執行檢查的字串。 |
| `{EXPRESSION}` | 比對第一個字串的規則運算式。 |
| `{GROUP}` | 要比對的運算式群組。 |

**範例**

以下查詢用於從電子郵件地址中提取域名。

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## Replace {#replace}

此 `replace` 函式，可將字串中的指定子字串取代為其他子字串。

**格式**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 必須替換子字串的字串。 |
| `{STRING_2}` | 要取代的子字串。 |
| `{STRING_3}` | 取代的子字串。 |

**範例**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

傳回「Hello Mark，這是您的每月電子報！」

## 全部替換{#replaceAll}

此 `replaceAll` 函式可用來將符合「target」的文字的所有子字串取代為指定的常值「取代」字串。 替換從字串的開頭到結尾，例如，將字串&quot;aaa&quot;中的&quot;aa&quot;取代為&quot;b&quot;將產生&quot;ba&quot;而非&quot;ab&quot;。

**格式**

```sql
{%= replaceAll(string,string,string) %}
```

## 右修剪 {#rightTrim}

此 `rightTrim` 函式會從字串的結尾移除空格。

**格式**

```sql
{%= rightTrim(string) %}
```

## Split {#split}

此 `split` 函式來依指定字元分割字串。

**格式**

```sql
{%= split(string,string) %}
```

## 開始於{#startsWith}

此 `startsWith` 函式可用來判斷字串是否以指定的子字串開頭。

**格式**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜尋的字串。 |
| `{CASE_SENSITIVE}` | 可選參數，用於確定檢查是否區分大小寫。 預設情況下，此值會設為true。 |

**範例**

以下查詢區分大小寫地確定人員的名稱是否以「Joe」開頭。

```sql
{%= startsWith(person.name,"Joe") %}
```

## 從字串轉換為整數 {#string-to-integer}

此 `string_to_integer` 函式將字串值轉換為整數值。

**格式**

```sql
{= string_to_integer(string) %}: int
```

## 字串至數字 {#string-to-number}

此 `stringToNumber` 函式將字串轉換為數字。 它會傳回與無效輸入的輸出相同的字串。

**格式**

```sql
{%= stringToNumber(string) %}: double
```

## 子字串 {#sub-string}

此 `Count string` 函式用於返回begin索引和end索引之間字串表達式的子字串。
**格式**

```sql
{= substr(string, integer, integer) %}: string
```

## 標題案例{#titleCase}

此 **titleCase** 函式可用來大寫字串每個字詞的前字母。

**語法**

```sql
{%= titleCase(string) %}
```

**範例**

如果這個人住在華盛頓高街，這個功能將返回華盛頓高街。

```sql
{%= titleCase(profile.person.location.Street) %}
```

## 到布爾 {#to-bool}

此 `toBool` 函式可用來將引數值轉換為布林值（視其類型而定）。

**格式**

```sql
{= toBool(string) %}: boolean
```

## 結束日期時間 {#to-date-time}

此 `toDateTime` 函式來將字串轉換為日期。 它會傳回紀元日期作為無效輸入的輸出。

**格式**

```sql
{%= toDateTime(string, string) %}: date-time
```

## 僅限截止時間 {#to-date-time-only}

此 `toDateTimeOnly` 函式用於將參數值轉換為僅限日期時間的值。 它會傳回紀元日期作為無效輸入的輸出。

**格式**

```sql
{%= toDateTimeOnly(string) %}: date-time
```

## 修剪{#trim}

此 **trim** 函式會從字串的開頭和結尾移除所有空格。

**語法**

```sql
{%= trim(string) %}
```

## 大寫{#upper}

此 **upperCase** 函式會將字串轉換為大寫字母。

**語法**

```sql
{%= upperCase(string) %}
```

**範例**

此函式會將描述檔姓氏轉換為大寫字母。

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## url解碼 {#url-decode}

此 `urlDecode` 函式來解碼url編碼字串。

**格式**

```sql
{%= urlDecode(string) %}: string
```

## Url編碼 {#url-encode}

此 `Count only null` 函式可用來將字串編碼為url。

**格式**

```sql
{%= urlEncode(string) %}: string
```
