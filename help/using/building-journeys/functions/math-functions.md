---
product: journey optimizer
title: 數學函式
description: 瞭解數學函式
feature: Journeys
role: Developer
level: Experienced
keywords: 數學，函式，運算式，歷程，計算，數字
version: Journey Orchestration
exl-id: da710b22-3112-41fe-8b91-2b6563b79f27
TQID: https://experienceleague.adobe.com/POIbPCZrqtqGjHqn3ehGonxwv9KhKWlgg2igdN8Y4yw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 475
ht-degree: 2%

---

# 數學函式 {#math-functions}

數學函式為歷程運算式中的數值計算提供基本的數學運算。 這些函式可讓您對資料執行精確數值計算和轉換。

當您需要以下作業時使用數學函式：

* 產生測試、抽樣或隨機化的隨機值([random](#random))
* 將十進位數字四捨五入為最接近的整數，以便呈現較乾淨的資料（[四捨五入](#round)）
* 對數值欄位執行數學計算
* 轉換商業邏輯和決策的數值

數學函式會處理十進位和整數型別，並自動管理型別轉換，以確保歷程運算式中的結果準確。

## random {#random}

產生介於0和1之間的隨機數字。

+++語法

`random()`

+++

+++簽章與傳回的型別

`random()`

傳回小數。

+++

## round {#round}

傳回引數最接近的整數值，並會將四捨五入連結至正無限。

+++語法

`round(<parameters>)`

+++

+++參數

* 小數
* 整數

+++

+++簽章與傳回型別

`round(<decimal>)`

`round(<integer>)`

傳回整數。

+++

+++範例

`round(3.14)`

傳回3。

`round(3.54)`

傳回4。

`round(-3.14)`

傳回–3。

`round(3)`

傳回3。

+++

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;本頁記錄了AJO歷程運算式中可用的兩個數學函式 — `random`用於產生介於0和1之間的隨機小數，而`round`用於將小數或整數四捨五入到最接近的整數。

**意圖：**
* 使用`random`產生介於0和1之間的隨機十進位值，用於取樣或隨機化邏輯
* 使用`round`將十進位數字四捨五入到最接近的整數
* 在商業邏輯中套用舍入，其中小數點計算需要整數

**字彙表：**
* **random**：傳回0 （含）到1 （含） *（產品特定）*&#x200B;的偽隨機十進位值的函式
* **round**：傳回與輸入最接近的整數的函式，半值會舍入為正無窮大

**護欄：**
* `random()`不使用引數
* `round`接受十進位或整數輸入並一律傳回整數
* `round`中的繫結可透過舍入至正無窮大來解析（例如，3.5舍入至4，-3.5舍入至–3）

**術語：**
* 正式名稱：數學函式 — 首字母縮寫：none — 變體：數學函式，數值函式
* 同義字： &quot;round&quot; = &quot;round to nearest integer&quot;
* 請勿混淆： 「四捨五入」（四捨五入到最接近的整數）≠轉換函式，如`toInteger` （會截斷小數部分而不進行四捨五入）

**常見問題集：**
* **問：`random()`傳回什麼？**  — 它會傳回0到1之間的隨機十進位數字。
* **問：`round`如何處理負數？**  — 它會舍入至正無窮大，因此`round(-3.14)`會傳回–3，`round(-3.54)`也會傳回–3 （最接近正無窮大的整數）。
* **問：`round`與`toInteger`之間有何差異？** — `round`會舍入至最接近的整數（3.7會變成4），而`toInteger`會截斷小數部分而不捨入（3.7會變成3）。
* **問： `random`是否接受任何引數？**  — 否，`random()`不需要引數，且一律會傳回0到1之間的小數。

+++
