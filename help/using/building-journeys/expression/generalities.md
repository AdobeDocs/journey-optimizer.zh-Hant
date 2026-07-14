---
solution: Journey Optimizer
product: journey optimizer
title: 進階運算式編輯器語法
description: 瞭解進階運算式編輯器中使用的語法
feature: Journeys
role: Developer
level: Experienced
keywords: 語法，編輯器，歷程
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-PTYUf-njT3-LsI-A5IKEMDGOl4JecZ-ayM0rU4f2HI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 621
ht-degree: 2%

---

# 進階運算式編輯器語法 {#syntax}

以下列出使用[進階運算式編輯器](expressionadvanced.md)時的語法基本知識。<!-- Samples of use of the advanced expression editor are available on [this page](advanced-editor-use-cases.md).-->

## 括弧和運算式優先順序 {#parentheses-and-expression-priority}

括弧可用來讓複雜的運算式更容易閱讀。 _（&lt;運算式>）_&#x200B;相當於&#x200B;_&lt;運算式>_。 括弧也可用來定義評估順序和關聯性。

運算式將由左至右評估。 必須套用算術運運算元的關聯性：乘法和除法優先於加法和減法。 為了強制特定順序，必須加入括弧以分隔操作。 例如:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| 運算式 | 評估 |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39;優先順序高於&#39;+&#39;：2 \* 10→20計算</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>括弧會變更優先順序： (4 + 2)的評估方式→6</li><li> 6 * 10 → 60</li></ul> |

## 區分大小寫 {#case-sensitivity}

以下是不同的區分大小寫規則：

* 所有運運算元（和、或等） 應該寫成小寫。 例如，_`<expression1>`和`<expression2>`_&#x200B;是有效的運算式，而運算式&#x200B;_`<expression1>`AND`<expression2>`_&#x200B;則否。
* 所有函式名稱都區分大小寫。 例如，_inAudience()_&#x200B;有效，而函式&#x200B;_INAUDIENCE()_&#x200B;無效。
* 欄位參照和常數值區分大小寫：它們不是語言的內建元素（與運運算元和函式相反），而是由一般使用者撰寫。

## 傳回的運算式型別 {#returned-expression-type}

根據使用內容，運算式編輯器可傳回不同的值。

| 進階運算式編輯器使用 | 預期傳回的運算式型別 |
|--- |--- |
| 條件（資料來源條件、日期條件） | 布林值 |
| 自訂計時器 | dateTimeOnly |
| 動作引數對應 | 任何 |

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面涵蓋Journey進階運算式編輯器的核心語法規則 — 運運算元優先順序加上括弧、運運算元和函式區分大小寫，以及每個編輯器內容的預期傳回型別。

**意圖：**

* 將子運算式包在括弧中來控制運算式評估順序
* 以小寫寫入運運算元(`and`， `or`， `not`)以避免語法錯誤
* 使用大小寫正確的函式名稱（例如`inAudience()`而非`INAUDIENCE()`）
* 瞭解條件必須傳回布林值，自訂計時器必須傳回`dateTimeOnly`，而且動作引數對應可以傳回任何型別

**字彙表：**

* **運算式優先順序**：運運算元的評估順序；乘法和除法優先於加法和減法&#x200B;*（產品特定）*
* **區分大小寫**：在進階編輯器中，運運算元必須為小寫、函式名稱區分大小寫，且欄位參考如使用者&#x200B;*（產品特有）*&#x200B;所撰寫則區分大小寫
* **dateTimeOnly**：自訂計時器（等待活動）運算式所需的傳回型別；代表沒有時區&#x200B;*（產品特定）*&#x200B;的日期時間

**護欄：**

* 運運算元（`and`、`or`、`not`等） 必須以小寫字母撰寫 — 大寫變體無效
* 所有函式名稱都區分大小寫 — `inAudience()`有效，但`INAUDIENCE()`無效
* 算術遵循標準優先順序： `*`和`/`在`+`和`-`之前評估；使用括弧來覆寫
* 條件一律傳回布林值；自訂計時器一律傳回`dateTimeOnly`

**術語：**

* 正式名稱：進階運算式編輯器語法 — 首字母縮寫：none — 變體：運算式語法，編輯器語法
* 同義字： &quot;expression priority&quot; = &quot;operator precedence&quot;； &quot;parentheses&quot; = &quot;brackets&quot; （在運算式內容中）
* 請勿混淆：運運算元區分大小寫（運運算元必須為小寫）≠欄位參考區分大小寫（欄位名稱由使用者編寫且區分大小寫）

**常見問題集：**

* **問：`4 + 2 * 10`是評估為60還是24？**  — 其評估為24，因為`*`優先於`+`；使用`(4 + 2) * 10`以取得60。
* **問：我可以在運算式中以大寫字母撰寫`AND`嗎？**  — 否；所有運運算元都必須是小寫(`and`， `or`， `not`)。
* **問：函式名稱是否區分大小寫？**  — 是；`inAudience()`有效，但`INAUDIENCE()`無效。
* **問：條件運算式必須傳回哪種型別？**  — 布林值。
* **問：自訂「等待」活動計時器運算式需要哪種傳回型別？** — `dateTimeOnly`。

+++
