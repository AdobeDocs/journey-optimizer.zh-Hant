---
title: 函式館
description: 函式館
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 7%

---

# 字串函式{#string}

![](../../assets/do-not-localize/badge.png)


TBC CJM字串函式

## 贊

`like`函式用於確定字串是否與指定的模式匹配。

**格式**

```sql
like ({STRING_1},{STRING_2})
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 與第一個字串相符的運算式。 建立表達式時有兩個支援的特殊字元：`%`和`_`。 <ul><li>`%` 用於表示零或多個字元。</li><li>`_` 僅代表一個字元。</li></ul> |

**範例**

以下查詢檢索包含模式&quot;es&quot;的所有城市。

```sql
like (city ,"%es%")
```

## 開始於

`startsWith`函式用於確定字串是否以指定的子字串開頭。

**格式**

```sql
startsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜索的字串。 |
| `{BOOLEAN}` | 可選參數，用於確定檢查是否區分大小寫。 依預設，此值會設為true。 |

**範例**

以下查詢以區分大小寫的方式確定人員的姓名是否以&quot;Joe&quot;開頭。

```sql
startsWith(person.name,"Joe")
```

## 不以

`doesNotStartWith`函式用於確定字串是否不以指定的子字串開頭。

**格式**

```sql
doesNotStartWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜索的字串。 |
| `{BOOLEAN}` | 可選參數，用於確定檢查是否區分大小寫。 依預設，此值會設為true。 |

**範例**

以下查詢以區分大小寫的方式確定人員姓名不是以&quot;Joe&quot;開頭。

```sql
doesNotStartWith(person.name,"Joe")
```

## 終止於

`endsWith`函式用於確定字串是否以指定的子字串結尾。

**格式**

```sql
endsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜索的字串。 |
| `{BOOLEAN}` | 可選參數，用於確定檢查是否區分大小寫。 依預設，此值會設為true。 |

**範例**

下列查詢會區分大小寫，判斷人員的電子郵件地址是否以&quot;。com&quot;結尾。

```sql
endsWith(person.emailAddress,".com")
```

## 不以

`doesNotEndWith`函式用於確定字串是否不以指定的子字串結尾。

**格式**

```sql
doesNotEndWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜索的字串。 |
| `{BOOLEAN}` | 可選參數，用於確定檢查是否區分大小寫。 依預設，此值會設為true。 |

**範例**

下列查詢會區分大小寫，判斷人員的電子郵件地址是否以&quot;。com&quot;結尾。

```sql
doesNotEndWith(person.emailAddress,".com")
```

## 包含

`contains`函式用於確定字串是否包含指定的子字串。

**格式**

```sql
contains({STRING_1},{STRING_2}, {BOOLEAN})
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜索的字串。 |
| `{BOOLEAN}` | 可選參數，用於確定檢查是否區分大小寫。 依預設，此值會設為true。 |

**範例**

下列查詢會區分大小寫，判斷人員的電子郵件地址是否包含字串「2010@gm」。

```sql
contains(person.emailAddress,"2010@gm")
```

## 不包含

`doesNotContain`函式用於確定字串是否不包含指定的子字串。

**格式**

```sql
doesNotContain({STRING_1},{STRING_2}, {BOOLEAN})
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串內搜索的字串。 |
| `{BOOLEAN}` | 可選參數，用於確定檢查是否區分大小寫。 依預設，此值會設為true。 |

**範例**

下列查詢會區分大小寫，判斷人員的電子郵件地址是否不包含字串「2010@gm」。

```sql
doesNotContain(person.emailAddress,"2010@gm")
```

## 等於

`equals`函式用於確定字串是否等於指定字串。

**格式**

```sql
equals({STRING_1},{STRING_2})
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串比較的字串。 |

**範例**

以下查詢以區分大小寫的方式確定人員的名稱是否為&quot;John&quot;。

```sql
equals(person.name,"John")
```

## 不等於

`notEqualTo`函式用於確定字串是否不等於指定字串。

**格式**

```sql
notEqualTo({STRING_1},{STRING_2})
```

| 引數 | 說明 |
| --------- | ----------- |
| `{STRING_1}` | 要執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串比較的字串。 |

**範例**

以下查詢以區分大小寫的方式確定人員的名稱不是&quot;John&quot;。

```sql
notEqualTo(person.name,"John")
```

## 符合

`matches`函式用於確定字串是否與特定規則運算式匹配。 有關規則運算式中的匹配模式的詳細資訊，請參閱[本檔案](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html)。

**格式**

```sql
matches({STRING_1},STRING_2})
```

**範例**

以下查詢會在不區分大小寫的情況下確定人員名稱是否以&quot;John&quot;開頭。

```sql
matches(person.name.,"(?i)^John")
```

## 規則運算式群組

`regexGroup`函式用於根據提供的規則運算式提取特定資訊。

**格式**

```sql
regexGroup({STRING},{EXPRESSION})
```

**範例**

以下查詢用於從電子郵件地址中提取域名。

```sql
regexGroup(emailAddress,"@(\w+)", 1)
```
