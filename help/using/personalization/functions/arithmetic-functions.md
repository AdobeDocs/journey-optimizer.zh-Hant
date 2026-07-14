---
title: 算術函式庫
description: 算術函式庫
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
TQID: https://experienceleague.adobe.com/vQcfLG40Xhz4-ebm--J875oU4o-6BXC0SvNq24OOyTk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 180
ht-degree: 7%

---

# 算術函式 {#maths}

算術函式用於對值執行基本計算。

## 新增{#add}

`+` （加法）函式是用來尋找兩個引數運算式的加總。

**語法**

```sql
{%= double + double %}
```

**範例**

下列作業會加總兩個不同產品的價格。

```sql
{%= product1.price + product2.price %}
```

## 乘{#multiply}

`*` （乘法）函式用於尋找兩個引數運算式的乘積。

**語法**

```sql
{%= double * double %}
```

**範例**

下列作業會尋找存貨的產品與產品價格，以尋找產品的總值。

```sql
{%= product.inventory * product.price %}
```

## 減{#substract}

`-` （減法）函式是用來找出兩個引數運算式的差異。

**語法**

```sql
{%= double - double %}
```

**範例**

下列作業會找出兩個不同產品之間的價格差異。

```sql
{%= product1.price - product2.price %}
```

## 除{#divide}

`/` （除法）函式用於尋找兩個引數運算式的商。

**語法**

```sql
{%= double / double %}
```

**範例**

下列作業會找出已售出產品總數與已賺取金額總數之間的商數，以檢視每個專案的平均成本。

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## 餘數{#remainder}

`%` （模數/餘數）函式用來找出兩個引數運算式相除後的餘數。

**語法**

```sql
{%= double % double %}
```

**範例**

下列作業會檢查個人的年齡是否可被5整除。

```sql
{%= person.age % 5 = 0 %}
```
