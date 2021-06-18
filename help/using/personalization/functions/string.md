---
title: 字串函式庫
description: 字串函式庫
feature: 個性化
topic: 個性化
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 7%

---

# 字串函式 {#string}

了解如何在運算式編輯器中使用字串函式。

## 駝峰 {#camelCase}

`camelCase`函式會大寫字串每個字詞的第一個字母。

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

`concat`函式將兩個字串組合為一。

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

`contains`函式用於確定字串是否包含指定的子字串。

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

* 下列函式將檢查設定檔名是否包含字母A（在上或下）。 若是如此，則會傳回&#39;true&#39;，否則會傳回&#39;false&#39;。

   ```sql
   {%= contains(profile.person.name.firstName, "A", false) %}
   ```

* 下列查詢會區分大小寫，判斷人員的電子郵件地址是否包含字串「2010@gm」。

   ```sql
   {%= contains(profile.person.emailAddress,"2010@gm") %}
   ```

## 不包含{#doesNotContain}

`doesNotContain`函式用於確定字串是否不包含指定的子字串。

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

`doesNotEndWith`函式用於判斷字串是否未以指定的子字串結尾。

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

`doesNotStartWith`函式用於確定字串是否以指定的子字串開頭。

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

`encode64`函式用於編碼字串，以保留個人資訊(PI)，如果要包括在URL中。

**格式**

```sql
{%= encode64(string) %}
```

## 終止於{#endsWith}

`endsWith`函式用於確定字串是否以指定的子字串結尾。

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

`equals`函式用於確定字串是否等於指定字串，且區分大小寫。

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

`equalsIgnoreCase`函式用於確定字串是否等於指定字串，不區分大小寫。

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

`extractEmailDomain`函式用於提取電子郵件地址的域。

**格式**

```sql
{%= extractEmailDomain(string) %}
```

**範例**

以下查詢會擷取個人電子郵件地址的電子郵件網域。

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Is empty {#isEmpty}

`isEmpty`函式用於確定字串為空。

**格式**

```sql
{%= isEmpty(string) %}
```

**範例**

如果設定檔的行動電話號碼空白，下列函式會傳回&#39;true&#39;。 否則，會傳回&#39;false&#39;。

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## 左修剪 {#leftTrim}

`leftTrim`函式用於從字串的開頭移除空格。

**格式**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

`length`函式用於獲取字串或表達式中的字元數。

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

`like`函式用於確定字串是否與指定模式匹配。

**格式**

```sql
{%= like(STRING_1, STRING_2) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 比對第一個字串的運算式。 建立運算式時有兩個支援的特殊字元：`%`和`_`。 <ul><li>`%` 用於表示零個或多個字元。</li><li>`_` 僅代表一個字元。</li></ul> |

**範例**

下列查詢會擷取所有使用包含模式「es」之設定檔的城市。

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## 小寫{#lower}

`lowerCase`函式將字串轉換為小寫字母。

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

`matches`函式用於確定字串是否與特定規則運算式匹配。 有關規則運算式中的匹配模式的詳細資訊，請參閱[本文檔](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html)。

**格式**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**範例**

以下查詢將不區分大小寫地確定人員的名稱以「John」開頭。

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## 不等於{#notEqualTo}

`notEqualTo`函式用於確定字串是否不等於指定字串。

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

## 規則運算式群組{#regexGroup}

`Group`函式用於根據提供的規則運算式擷取特定資訊。

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
{%= regexGroup(emailAddress,"@(\w+)", 1) %}
```

## Replace {#replace}

`replace`函式用於將字串中的指定子字串替換為另一個子字串。

**格式**

```sql
{%= replace(string,string,string) %}
```

**範例**

下列函式。

```sql

```


## 全部替換{#replaceAll}

`replaceAll`函式用指定的常值「取代」字串取代與「target」相符之文字的所有子字串。 替換從字串的開頭到結尾，例如，將字串&quot;aaa&quot;中的&quot;aa&quot;取代為&quot;b&quot;將產生&quot;ba&quot;而非&quot;ab&quot;。

**格式**

```sql
{%= replaceAll(string,string,string) %}
```


## 右修剪 {#rightTrim}

使用`rightTrim`函式會移除字串結尾的空格。


**格式**

```sql
{%= rightTrim(string) %}
```

## Split {#split}

`split`函式用於按給定字元拆分字串。

**格式**

```sql
{%= split(string,string) %}
```

<!--
**Example**

The following function .

```sql

```

-->

## 開始於{#startsWith}

`startsWith`函式用於確定字串是否以指定的子字串開頭。

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

## 標題案例{#titleCase}

**titleCase**&#x200B;函式用於大寫字串中每個字詞的首字母。

**語法**

```sql
{%= titleCase(string) %}
```

**範例**

如果這個人住在華盛頓高街，這個功能將返回華盛頓高街。

```sql
{%= titleCase(profile.person.location.Street) %}
```

## 修剪{#trim}

**trim**&#x200B;函式會從字串的開頭和結尾移除所有空格。

**語法**

```sql
{%= trim(string) %}
```

## 大寫{#upper}

**upperCase**&#x200B;函式將字串轉換為大寫字母。

**語法**

```sql
{%= upperCase(string) %}
```

**範例**

此函式會將描述檔姓氏轉換為大寫字母。

```sql
{%= upperCase(profile.person.name.lastName) %}
```
