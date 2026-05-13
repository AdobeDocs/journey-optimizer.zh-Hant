---
title: Personalization訣竅
description: Adobe Journey Optimizer的常見個人化模式和真實世界範例
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
source-git-commit: 04fca756923d53595639e221fb59d3f6a458ac4a
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---

# Personalization訣竅 {#personalization-recipes}

本頁針對Adobe Journey Optimizer中最常見的使用案例提供現成的個人化模式。 所有範例都使用個人化編輯器語法，並可直接複製到電子郵件、簡訊或推播內容中。

如需可用函式的完整參考，請參閱[協助程式函式](functions/helpers.md)、[日期/時間函式](functions/dates.md)、[字串函式](functions/string.md)和[陣列函式](functions/arrays-list.md)。

>[!TIP]
>
>在複製範例之前，請檢閱[Personalization最佳實務](personalization-syntax.md#best-practices)以避免最常見的語法錯誤。

## 日期與時間配方 {#date-time-recipes}

### 方式1 — 以可讀格式顯示目前日期 {#recipe-current-date}

使用`formatDate`搭配`getCurrentZonedDateTime()`以任何格式呈現今天的日期：

```sql
{%= formatDate(getCurrentZonedDateTime(), "MMMM dd, yyyy") %}
```

輸出（範例）： `April 11, 2026`

**通用格式模式：**

| 模式 | 輸出範例 |
|---------|---------------|
| `"dd/MM/yyyy"` | `11/04/2026` |
| `"MM/dd/yyyy"` | `04/11/2026` |
| `"EEEE, MMMM dd"` | `Saturday, April 11` |
| `"yyyy-MM-dd"` | `2026-04-11` |

>[!NOTE]
>
>請使用小寫`y` （行事曆年份）而非`Y` （以周為單位的年份），以避免在年份邊界出現非預期的結果。 如需完整參考，請參閱[圖樣字元](functions/dates.md#pattern-characters)。

### 方式2 — 到期或事件日期的倒數 {#recipe-countdown}

使用`dateDiff`計算設定檔日期屬性之前的剩餘天數，然後以動態方式呈現：

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
{%#if daysLeft > 0%}
Your reward points expire in {{daysLeft}} day{%#if daysLeft > 1%}s{%/if%}. Use them before they're gone!
{%else%}
Your reward points have expired.
{%/if%}
```

輸出（範例）： `Your reward points expire in 7 days. Use them before they're gone!`

### 配方3 — 動態結束日期前的X天 {#recipe-days-before}

若要計算設定檔屬性之前X天的日期（例如在內容或主旨行中參照），請使用負位移的`addDays`：

```sql
{%= formatDate(addDays(stringToDate(profile.subscription.endDate), -7), "MMMM dd, yyyy") %}
```

輸出（範例）： `April 04, 2026` *（4月11日前7天）*

若要同時設定一天中的固定時間（例如，上午9點），請結合`setHours`：

```sql
{%= formatDate(setHours(addDays(stringToDate(profile.subscription.endDate), -7), 9), "dd/MM/yyyy HH:mm") %}
```

### 配方4 — 將目前時間顯示為HH:MM {#recipe-time-only}

使用`extractHours`和`extractMinutes`只顯示時間部分，並在前導為零時保留分鐘：

```handlebars
{% let h = extractHours(getCurrentZonedDateTime()) %}
{% let m = extractMinutes(getCurrentZonedDateTime()) %}
Your appointment is at {{h}}:{%#if m < 10%}0{%/if%}{{m}}.
```

輸出（範例）： `Your appointment is at 14:05.`

### 食譜5 — 偵測週末與平日 {#recipe-weekend}

使用`dayOfWeek`根據日期調整內容。 此函式傳回1 （星期一）到7 （星期日）。 使用單一`=`運運算元（PQL語法，而非`==`）：

```handlebars
{%#if dayOfWeek(getCurrentZonedDateTime()) = 6 or dayOfWeek(getCurrentZonedDateTime()) = 7%}
We're closed on weekends — our team will follow up on the next business day.
{%else%}
Our team will get back to you within 24 hours.
{%/if%}
```

>[!NOTE]
>
>`dayOfWeek()`是根據日期調整&#x200B;**內容**。 若要根據一週中的某天在歷程中以不同方式路由設定檔，請在歷程條件活動中使用內建的&#x200B;**時間條件→一週中的某天**&#x200B;選項。 [了解更多](../building-journeys/condition-activity.md#date_condition)

## 陣列與回圈配方 {#array-recipes}

### 指導方針6 — 列出設定檔陣列中的所有專案 {#recipe-list-items}

使用`{{#each}}`來反複處理設定檔陣列並演算每個專案。 這僅在個人化編輯器（電子郵件、簡訊、推播）中可用：

```handlebars
{{#each profile.purchases.recentItems}}
  - {{this.name}}: {{this.price}}&euro;
{{/each}}
```

輸出（範例）：

```
- Running shoes: 89&euro;
- Water bottle: 15&euro;
- Gym bag: 45&euro;
```

>[!NOTE]
>
>歷程條件活動不支援`{{#each}}`。 若要在條件中篩選陣列，請使用[集合管理函式](../building-journeys/expression/collection-management-functions.md)。

### 配方7 — 依價格顯示陣列中的前N個專案 {#recipe-first-n}

使用`topN`依數值欄位排序及擷取前N個專案。 由於`topN`是PQL函式，請先將其指派給具有`{% let %}`的變數，然後以`{{#each}}`進行回圈：

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

>[!NOTE]
>
>`topN(profile.orders, price, 3)`會依遞減順序排序`price`並傳回前3個專案 — 它不會簡單地傳回原始陣列順序中的前3個專案。

或使用`head`只取得單一最上層專案：

```sql
{%= head(profile.purchases.recentItems).name %}
```

### 方式8 — 根據陣列專案有條件地呈現內容 {#recipe-conditional-loop}

在`{{#each}}`內使用`{%#if%}`僅針對相符的專案轉譯輸出。 定義具有`as |order|`的回圈別名，讓PQL評估器能夠解析條件中的屬性參考：

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending — we'll notify you when it ships.
  {%/if%}
{{/each}}
```

>[!NOTE]
>
>`this.status`在Handlebars運算式中運作，但未由`{%#if%}`內的PQL評估程式解析。 使用具名回圈別名（例如`order`）可讓屬性同時用於Handlebars和PQL內容。

## 字串與格式設定配方 {#string-recipes}

### 方式9 — 使用replaceAll清除字串並重複使用 {#recipe-replaceall-reuse}

`replaceAll`傳回新值 — 它不會修改原始值。 使用`{% let %}`儲存結果並多次參考它，而不重複函式呼叫：

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}},
Your exclusive code is: WELCOME-{%= upperCase(cleanName) %}
```

輸出（範例）：

```
Hi John,
Your exclusive code is: WELCOME-JOHN
```

### 指導方針10 — JSON輸出中的雙引號值 {#recipe-json-quotes}

若要在字串中包含常值雙引號（例如為自訂裝載產生JSON），請使用反斜線(`\"`)將其逸出：

```handlebars
{ "greeting": "Hello \"{{profile.person.name.firstName}}\"" }
```

輸出： `{ "greeting": "Hello \"John\"" }`

### 方式11 — 將日期元件格式化為大寫 {#recipe-uppercase-date}

將`formatDate`與`upperCase`結合，以大寫方式呈現月份或日期名稱：

```sql
{%= upperCase(formatDate(getCurrentZonedDateTime(), "MMMM")) %}
```

輸出（範例）： `APRIL`

若為完整的大寫日期字串：

```sql
{%= upperCase(formatDate(profile.person.birthDateTime, "EEEE MMMM dd yyyy")) %}
```

輸出（範例）： `WEDNESDAY JANUARY 01 2020`

## 條件邏輯配方 {#conditional-recipes}

### 指導方針12 — 個人化內容中的IF/ELSEIF/ELSE {#recipe-if-elseif}

針對多分支條件式邏輯使用`{%#if%}`、`{%else if%}`和`{%else%}`。 此模式適用於電子郵件內容和片段：

```handlebars
{%#if profile.loyalty.tier = "gold"%}
As a Gold member, enjoy free shipping on all orders.
{%else if profile.loyalty.tier = "silver"%}
As a Silver member, enjoy free shipping on orders over &euro;50.
{%else%}
Join our loyalty program to unlock exclusive benefits.
{%/if%}
```

### 配方13 — 空值安全屬性顯示 {#recipe-null-safe}

使用條件式遞補，以避免在設定檔屬性可能為Null或遺失時呈現空白值：

```handlebars
{%#if profile.person.name.firstName%}
Hi {{profile.person.name.firstName}},
{%else%}
Hi there,
{%/if%}
```

或使用`isEmpty`以三元樣式模式內嵌：

```handlebars
Hi {%#if isEmpty(profile.person.name.firstName)%}valued customer{%else%}{{profile.person.name.firstName}}{%/if%},
```

## PQL邊緣案例訣竅 {#pql-edge-cases}

### 指導方針14 — 參照連字屬性索引鍵 {#recipe-hyphenated-key}

如果您的XDM結構描述欄位名稱包含連字型大小（例如`order-total`、`event-type`），請在PQL運算式中以反引號將其包裝，以防止將連字型大小解譯為減法運運算元：

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>只有PQL運算式(`{%= ... %}`)內支援反引號。 在純的Handlebars內插(`{{...}}`)中不接受它們。 如果您需要直接轉譯斷字欄位值，請先透過PQL運算式評估該值，或使用`{% let %}`將其儲存在變數中。

### 方式15 — 參考內容屬性中的數值事件ID {#recipe-numeric-event-id}

使用歷程內容事件時，若其ID為數值字串（例如`1697323153`），請以反引號括住該ID，並使用`{% let %}`搭配`toDateTime()`和`formatDate()`：

```handlebars
{% let appointmentDate = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy HH:mm") %}
Your appointment: {{appointmentDate}}
```

輸出（範例）： `Your appointment: 18/03/2026 14:30`

### 方式16 — 輸入強制：比較字串欄位與數字 {#recipe-type-coercion}

PQL是強型別。 當設定檔欄位儲存為字串，但您需要以數值加以比較時，請先將其轉換為`stringToNumber()`：

```sql
{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}
```

對於儲存為字串的布林值欄位：

```sql
{%= toBool(profile.consents.email.val) = true %}
```

