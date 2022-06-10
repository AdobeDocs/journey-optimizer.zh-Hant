---
title: 字串函式館
description: 字串函式館
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 7%

---

# 字串函式 {#string}

瞭解如何在表達式編輯器中使用字串函式。

## 駝峰 {#camelCase}

的 `camelCase` 函式將字串中每個單詞的第一個字母大寫。

**格式**

```sql
{%= camelCase(string)%}
```

**範例**

以下函式將大寫配置檔案的街道地址中的首字母。

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## 孔卡 {#concate}

的 `concat` 函式。

**格式**

```sql
{%= concat(string,string) %}
```

**範例**

以下函式將配置式城市和國家/地區合併為一個字串。

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## 包含 {#contains}

的 `contains` 函式用於確定字串是否包含指定的子字串。

**格式**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `STRING_1` | 要執行檢查的字串。 |
| `STRING_2` | 要在第一個字串內搜索的字串。 |
| `CASE_SENSITIVE` | 用於確定檢查是否區分大小寫的可選參數。 可能的值：true（預設）/false。 |

**範例**

* 以下函式將檢查配置檔案的名字是否包含字母A（在大寫或小寫中）。 如果是，則返回「true」，否則返回「false」。

   ```sql
   {%= contains(profile.person.name.firstName, "A", false) %}
   ```

* 以下查詢以區分大小寫的方式確定人員的電子郵件地址是否包含字串&quot;2010@gm&quot;。

   ```sql
   {%= contains(profile.person.emailAddress,"2010@gm") %}
   ```

## 不包含{#doesNotContain}

的 `doesNotContain` 函式用於確定字串是否不包含指定的子字串。

**格式**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 引數 | 說明 |
| --------- | ----------- |
| `STRING_1` | 要執行檢查的字串。 |
| `STRING_2` | 要在第一個字串內搜索的字串。 |
| `CASE_SENSITIVE` | 用於確定檢查是否區分大小寫的可選參數。 可能的值：true（預設）/false。 |

**範例**

以下查詢以區分大小寫的方式確定人員的電子郵件地址不包含字串「2010@gm」。

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## 不以{#doesNotEndWith}

的 `doesNotEndWith` 函式用於確定字串是否以指定的子字串結尾。

**格式**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜索的字串。 |
| `{CASE_SENSITIVE}` | 用於確定檢查是否區分大小寫的可選參數。 可能的值：true（預設）/false。 |

**範例**

以下查詢以區分大小寫的方式確定人員的電子郵件地址是否以&quot;。com&quot;結尾。

```sql
doesNotEndWith(person.emailAddress,".com")
```

## 不以開頭{#doesNotStartWith}

的 `doesNotStartWith` 函式用於確定字串是否不以指定的子字串開頭。

**格式**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜索的字串。 |
| `{CASE_SENSITIVE}` | 用於確定檢查是否區分大小寫的可選參數。 可能的值：true（預設）/false。 |

**範例**

以下查詢以區分大小寫的方式確定人員姓名是否不以「Joe」開頭。

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## 編碼64{#encode64}

的 `encode64` 函式用於對字串進行編碼以保留個人資訊(PI)（如果要包括在URL中）。

**格式**

```sql
{%= encode64(string) %}
```

## 終止於{#endsWith}

的 `endsWith` 函式用於確定字串是否以指定的子字串結尾。

**格式**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜索的字串。 |
| `{CASE_SENSITIVE}` | 用於確定檢查是否區分大小寫的可選參數。 可能的值：true（預設）/false。 |

**範例**

以下查詢以「.com」結尾，並區分大小寫。

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## 等於{#equals}

的 `equals` 函式用於確定字串是否等於指定的字串（區分大小寫）。

**格式**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串進行比較的字串。 |

**範例**

以下查詢以區分大小寫的方式確定人員的姓名是否為「John」。

```sql
{%=equals(profile.person.name,"John") %}
```

## 等於忽略大小寫{#equalsIgnoreCase}

的 `equalsIgnoreCase` 函式用於確定字串是否等於指定的字串，而不區分大小寫。

**格式**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串進行比較的字串。 |

**範例**

以下查詢確定人員的姓名是否為「John」（不區分大小寫）。

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## 提取電子郵件域 {#extractEmailDomain}

的 `extractEmailDomain` 函式用於提取電子郵件地址的域。

**格式**

```sql
{%= extractEmailDomain(string) %}
```

**範例**

以下查詢提取個人電子郵件地址的電子郵件域。

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## 獲取URL主機 {#get-url-host}

的 `getUrlHost` 函式用於檢索URL的主機名。

**格式**

```sql
{%= getUrlHost(string) %}: string
```

**範例**

```sql
{%= getUrlHost("http://www.myurl.com/contact") %}
```

返回&quot;www.myurl.com&quot;

## 獲取URL路徑 {#get-url-path}

的 `getUrlPath` 函式用於檢索URL的域名後的路徑。

**格式**

```sql
{%= getUrlPath(string) %}: string
```

**範例**

```sql
{%= getUrlPath("http://www.myurl.com/contact.html") %}
```

返回&quot;/contact.html&quot;

## 獲取URL協定 {#get-url-protocol}

的 `getUrlProtocol` 函式用於檢索URL的協定。

**格式**

```sql
{%= getUrlProtocol(string) %}: string
```

**範例**

```sql
{%= getUrlProtocol("http://www.myurl.com/contact.html") %}
```

返回&quot;http&quot;

## 索引 {#index-of}

的 `indexOf` 函式用於返回（在第一參數中）第一參數出現的位置。 如果沒有匹配項，則返回–1。

**格式**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個參數中搜索的字串 |

**範例**

```sql
{%= indexOf("hello world","world" ) %}
```

返回6。

## Is empty {#isEmpty}

的 `isEmpty` 函式用於確定字串是否為空。

**格式**

```sql
{%= isEmpty(string) %}
```

**範例**

如果配置檔案的手機號碼為空，則以下函式將返回「true」。 否則，它將返回「false」。

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## 不為空 {#is-not-empty}

的 `isNotEmpty` 函式用於確定字串是否不為空。

**格式**

```sql
{= isNotEmpty(string) %}: boolean
```

**範例**

如果配置檔案的行動電話號碼不為空，則以下函式將返回「true」。 否則，它將返回「false」。

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## 上次索引 {#last-index-of}

的 `lastIndexOf` 函式用於返回（在第一參數中）第二參數最後出現的位置。 如果沒有匹配項，則返回–1。

**格式**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個參數中搜索的字串 |

**範例**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

返回7。

## 左修剪 {#leftTrim}

的 `leftTrim` 函式用於從字串開頭刪除空格。

**格式**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

的 `length` 函式用於獲取字串或表達式中的字元數。

**格式**

```sql
{%= length(string) %}
```

**範例**

以下函式返回配置檔案的城市名稱的長度。

```sql
{%= length(profile.homeAddress.city) %}
```

## 像{#like}

的 `like` 函式用於確定字串是否與指定的模式匹配。

**格式**

```sql
{%= like(STRING_1, STRING_2) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串匹配的表達式。 建立表達式時支援兩個特殊字元： `%` 和 `_`。 <ul><li>`%` 用於表示零個或多個字元。</li><li>`_` 只表示一個字元。</li></ul> |

**範例**

以下查詢將檢索包含模式「es」的配置檔案所在的所有城市。

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## 小寫{#lower}

的 `lowerCase` 函式將字串轉換為小寫字母。

**語法**

```sql
{%= lowerCase(string) %}
```

**範例**

此函式將配置檔案的名字轉換為小寫字母。

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## 符合{#matches}

的 `matches` 函式用於確定字串是否與特定規則運算式匹配。 請參閱 [此文檔](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) 的子菜單。

**格式**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**範例**

以下查詢（不區分大小寫）確定人員姓名是否以「John」開頭。

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## 掩碼(#mask)

的 `Mask` 函式用於用「X」字元替換字串的一部分。

**格式**

```sql
{%= mask(string,integer,integer) %}
```

**範例**

以下查詢將「123456789」字串替換為「X」字元，但前兩個字元除外。

```sql
{%= mask("123456789",1,2) %}
```

查詢返回 `1XXXXXX89`。

## MD5 {#md5}

的 `md5` 函式用於計算和返回字串的md5哈希。

**格式**

```sql
{%= md5(string) %}: string
```

**範例**

```sql
{%= md5("hello world") %}
```

返回「5eb63bbbe01eed093cb2bb8f5acdc3」

## 不等於{#notEqualTo}

的 `notEqualTo` 函式用於確定字串是否不等於指定的字串。

**格式**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串進行比較的字串。 |

**範例**

以下查詢以區分大小寫的方式確定人員的姓名不是「John」。

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## 不等於忽略大小寫 {#not-equal-with-ignore-case}

的 `notEqualWithIgnoreCase` 函式用於比較兩個字串忽略事例。

**格式**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串進行比較的字串。 |

**範例**

以下查詢確定人員的姓名是否不是「john」，且不區分大小寫。

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## 規則運算式組{#regexGroup}

的 `Group` 函式用於根據所提供的規則運算式提取特定資訊。

**格式**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING}` | 要執行檢查的字串。 |
| `{EXPRESSION}` | 與第一個字串匹配的規則運算式。 |
| `{GROUP}` | 要匹配的表達式組。 |

**範例**

以下查詢用於從電子郵件地址中提取域名。

```sql
{%= regexGroup(emailAddress,"@(\w+)", 1) %}
```

## Replace {#replace}

的 `replace` 函式用於將字串中的給定子字串替換為另一個子字串。

**格式**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 必須替換子字串的字串。 |
| `{STRING_2}` | 要替換的子字串。 |
| `{STRING_3}` | 替換子字串。 |

**範例**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

返回「Hello Mark，這是您的月度通訊！」

## 全部替換{#replaceAll}

的 `replaceAll` 函式用於將與&quot;target&quot;匹配的文本的所有子字串替換為指定的文本&quot;replacement&quot;字串。 替換從字串的開頭到結尾，例如，在字串&quot;aaa&quot;中將&quot;aa&quot;替換為&quot;b&quot;將導致&quot;ba&quot;而不是&quot;ab&quot;。

**格式**

```sql
{%= replaceAll(string,string,string) %}
```

## 右修剪 {#rightTrim}

的 `rightTrim` 函式用於從字串的末尾刪除空格。

**格式**

```sql
{%= rightTrim(string) %}
```

## Split {#split}

的 `split` 函式用於按給定字元拆分字串。

**格式**

```sql
{%= split(string,string) %}
```

## 開始於{#startsWith}

的 `startsWith` 函式用於確定字串是否以指定的子字串開頭。

**格式**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜索的字串。 |
| `{CASE_SENSITIVE}` | 用於確定檢查是否區分大小寫的可選參數。 預設情況下，此值設定為true。 |

**範例**

以下查詢以「Joe」開頭，並區分大小寫確定人員的姓名。

```sql
{%= startsWith(person.name,"Joe") %}
```

## 字串到整數 {#string-to-integer}

的 `string_to_integer` 函式用於將字串值轉換為整數值。

**格式**

```sql
{= string_to_integer(string) %}: int
```

## 字串到數字 {#string-to-number}

的 `stringToNumber` 函式將字串轉換為數字。 它返回與無效輸入的輸出相同的字串。

**格式**

```sql
{%= stringToNumber(string) %}: double
```

## 子字串 {#sub-string}

的 `Count string` 函式用於返回begin索引和end索引之間字串表達式的子字串。
**格式**

```sql
{= substr(string, integer, integer) %}: string
```

## 標題案例{#titleCase}

的 **titleCase** 函式用於大寫字串中每個單詞的首字母。

**語法**

```sql
{%= titleCase(string) %}
```

**範例**

如果這個人住在華盛頓大街，這個功能就會讓華盛頓大街回歸。

```sql
{%= titleCase(profile.person.location.Street) %}
```

## 托布爾 {#to-bool}

的 `toBool` 函式用於根據參數值的類型將參數值轉換為布爾值。

**格式**

```sql
{= toBool(string) %}: boolean
```

## 結束日期時間 {#to-date-time}

的 `toDateTime` 函式用於將字串轉換為日期。 它將紀元日期返回為無效輸入的輸出。

**格式**

```sql
{%= toDateTime(string, string) %}: date-time
```

## 僅截止日期時間 {#to-date-time-only}

的 `toDateTimeOnly` 函式用於將參數值轉換為僅日期時間值。 它將紀元日期返回為無效輸入的輸出。

**格式**

```sql
{%= toDateTimeOnly(string) %}: date-time
```

## 修剪{#trim}

的 **修剪** 函式將刪除字串開頭和結尾的所有空格。

**語法**

```sql
{%= trim(string) %}
```

## 大寫{#upper}

的 **大寫** 函式將字串轉換為大寫字母。

**語法**

```sql
{%= upperCase(string) %}
```

**範例**

此函式將配置檔案姓氏轉換為大寫字母。

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## url解碼 {#url-decode}

的 `urlDecode` 函式用於解碼url編碼字串。

**格式**

```sql
{%= urlDecode(string) %}: string
```

## URL編碼 {#url-encode}

的 `Count only null` 函式用於url編碼字串。

**格式**

```sql
{%= urlEncode(string) %}: string
```
