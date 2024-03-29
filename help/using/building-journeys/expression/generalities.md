---
solution: Journey Optimizer
product: journey optimizer
title: 語法
description: 瞭解進階運算式編輯器
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 語法，編輯器，歷程
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---

# 進階運算式編輯器語法 {#syntax}

## 括弧和運算式優先順序{#parentheses-and-expression-priority}

括弧可用來讓複雜的運算式更容易閱讀。 _(&lt;expression>)_ 相當於 _&lt;expression>_. 括弧也可用來定義評估順序和關聯性。

運算式將由左至右評估。 必須套用算術運運算元的關聯性：乘法和除法優先於加法和減法。 為了強制特定順序，必須加入括弧以分隔操作。 例如：

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| 運算式 | 評估 |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39;優先順序高於&#39;+&#39;：2 * 10→20計算</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>括弧會變更優先順序： (4 + 2)的評估方式→6</li><li> 6 * 10 → 60</li></ul> |

## 區分大小寫{#case-sensitivity}

以下是不同的區分大小寫規則：

* 所有運運算元（和、或等） 應該寫成小寫。 例如， _`<expression1>`和`<expression2>`_ 是有效的運算式，但運算式 _`<expression1>`和`<expression2>`_ 不是。
* 所有函式名稱都區分大小寫。 例如， _inAudience()_ 有效，但函式 _INAUDIENCE()_ 不是。
* 欄位參照和常數值區分大小寫：它們不是語言的內建元素（與運運算元和函式相反），而是由一般使用者撰寫。

## 傳回的運算式型別{#returned-expression-type}

根據使用內容，運算式編輯器可傳回不同的值。

| 進階運算式編輯器使用 | 預期傳回的運算式型別 |
|--- |--- |
| 條件（資料來源條件、日期條件） | 布林值 |
| 自訂計時器 | dateTimeOnly |
| 動作引數對應 | 任何 |
