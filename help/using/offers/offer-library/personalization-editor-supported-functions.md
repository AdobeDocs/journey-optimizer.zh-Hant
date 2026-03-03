---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 個人化編輯器中支援的功能
description: 瞭解在決定管理(Offer Decisioning)中個人化優惠內容時，哪些個人化編輯器功能受到支援。
badge: label="舊版" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
exl-id: c4df41a2-d740-437c-acc3-957508c4a1c0
source-git-commit: c15bae97ea52243d65aa59fdd4e924dc4e1852d8
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 15%

---

# 個人化編輯器中支援的功能 {#personalization-editor-supported-functions}

在決定管理中，當您&#x200B;**新增代表**&#x200B;並個人化[優惠內容](add-representations.md) （優惠中的影像、文字、連結）時，請使用&#x200B;**個人化編輯器**。

當個人化該內容時，Offer Decisioning後端僅支援個人化編輯器中可用的&#x200B;**子集**&#x200B;功能。 此頁面列出可在選件內容編輯器中安全使用的每個功能。 展開每個區段以檢視支援的運運算元、協助程式和函式。

>[!NOTE]
>
>此函式清單只將&#x200B;**套用至個人化優惠內容** （表示方式）。 決定規則和排名公式使用不同的編輯器，而且不限於此子集。

## 支援的函式清單 {#supported-functions-list}

+++ 操作者

* 算術： `+` `-` `*` `/` `%`
* 邏輯： `and` `or` `!`
* 比較： `=` `!=` `>` `>=` `<` `<=`

+++

+++ 輔助程式

* 每個
* 替換為
* 若
* Unless
* Let
* 預設遞補值
* 片段
* datasetLookup
* externalDataLookup (Alpha)
* 內嵌
* Url
* 執行中繼資料
* valueAt路徑

+++

+++ 字串函式

| 顯示名稱 | 內部名稱 |
|--------------|---------------|
| 小寫 | 小寫 |
| 大寫 | 大寫 |
| 駝峰式大小寫 | 駝峰式大小寫 |
| 字首大寫 | titleCase |
| 修剪 | trim |
| 左側修剪 | leftTrim |
| 右側修剪 | rightTrim |
| 為空 | IsEmpty |
| 等於（忽略大小寫） | equalsIgnoreCase |
| 不等於，忽略大小寫 | notEqualWithIgnoreCase |
| 取代 | replace |
| 全部取代 | replaceAll |
| Concat | concat |
| 分割 | split |
| Encode64 | encode64 |
| 長度 | 長度 |
| MD5 | md5 |
| SHA256 | sha256 |
| 類似 | 類似 |
| 開始於 | startsWith |
| 開頭不是 | doesNotStartWith |
| 結束於 | endsWith |
| 結尾不是 | doesNotEndWith |
| 包含 | 包含 |
| 不包含 | doesNotContain |
| 等於 | 等於 |
| 不等於 | notEqualto |
| 符合 | matches |
| 規則運算式群組 | regexgroup |
| 字串至數字 | stringToNumber |
| 字串至日期 | stringToDate |
| 至日期時間 | toDateTime |
| To Date Time Only | toDateTimeOnly |
| 擷取電子郵件網域 | extractEmailDomain |
| 擷取電子郵件使用者名稱 | Extractemailusername |
| 不是空的 | isNotEmpty |
| 索引： | indexOf |
| 最後索引： | lastIndexOf |
| 子字串 | substr |
| 至Bool | toBool |
| 字串至整數 | string_to_integer |
| 遮色片 | 遮色片 |
| 取得格式貨幣 | formatCurrency |
| 取得字元的Unicode值 | charCodeAt |
| 取得任何文字的Qr碼 | qrCode |

+++

+++ 陣列、清單和設定函式

| 顯示名稱 | 內部名稱 |
|--------------|---------------|
| Distinct | distinct |
| 在 | 在  |
| 不在 | notIn |
| 相交 | 相交 |
| 子集： | subsetOf |
| 超集 | 超集Of |
| 包含 | 包含 |
| 排序並取得陣列中的前N個 | topN |
| 排序並取得陣列中的最後N個 | bottomN |
| 第一個專案 | head |
| Count | 計數 |
| Sum | sum |
| 平均 | 平均 |
| 最小值 | min |
| 最大值 | max |

+++

+++ 地圖函式

| 顯示名稱 | 內部名稱 |
|--------------|---------------|
| Get | get |
| 索引鍵 | 金鑰 |
| 值 | 值 |

+++

+++ 物件函式

| 顯示名稱 | 內部名稱 |
|--------------|---------------|
| 為空 | isNull |
| 不是Null | isNotNull |

+++

+++ 數學函式

| 顯示名稱 | 內部名稱 |
|--------------|---------------|
| 至百分比 | toPercentage |
| 向上四捨五入 | 綜述 |
| 向下四捨五入 | roundDown |
| 至精確度 | toPrecision |
| 絕對 | 絕對 |
| 隨機 | random |
| 至十六進位 | toHexString |
| 取得地區設定的號碼 | formatnumber |
| 至字串 | toString |
| 到Int | toInt |
| 至長 | toLong |

+++

+++ 日期時間函式

| 顯示名稱 | 內部名稱 |
|--------------|---------------|
| 現在 | now |
| 取得CurrentZonedDateTime | getCurrentZonedDateTime |
| 結束日期 | toDate |
| 結束時間 | toTime |
| 至日期時間 | toDateTime |
| To Date Time Only | toDateTimeOnly |
| 僅截止日期 | toDateOnly |
| To Time Only | toTimeOnly |
| 至時區 | toTimeZone |
| 格式化日期 | formatDate |
| 格式化日期時間 | formatDateTime |
| 格式化時間 | formatTime |
| 剖析日期 | parseDate |
| 剖析日期時間 | parseDateTime |
| 剖析時間 | parseTime |
| 新增天數 | addDays |
| 新增月份 | addMonths |
| 新增年份 | addYears |
| 新增小時 | addHours |
| 新增分鐘 | addMinutes |
| 新增秒數 | addSeconds |
| 減去天數 | subtractDays |
| 減去月份 | subtractMonths |
| 減去年數 | subtractYears |
| 減去小時 | subtractHours |
| 減去分鐘 | subtractminutes |
| 減去秒數 | subtractSeconds |
| 天數差異 | diffDays |
| 月份差異 | diffMonths |
| 年差異 | diffyears |
| 時數差異 | diffhours |
| 差異分鐘數 | diffMinutes |
| 秒數差異 | diffSeconds |
| 一天開始 | startOfDay |
| 一天結束時 | endOfDay |
| 早於 | isBefore |
| 晚於 | isAfter |

+++

+++ URL函式

| 顯示名稱 | 內部名稱 |
|--------------|---------------|
| 編碼URL | encodeUrl |
| 解碼URL | decodeUrl |
| 取得URL查詢引數 | getUrlQueryParam |
| 取得URL通訊協定 | getUrlProtocol |
| 取得URL主機 | getUrlHost |

+++

>[!NOTE]
>
>如果您在個人化選件內容時使用不在上述清單中的函式，運算式在執行階段可能會失敗或產生非預期的結果。 如需[!DNL Journey Optimizer]個人化中可用的完整功能集，請參閱[協助程式功能清單](../../personalization/functions/functions.md)。 Offer Decisioning中個人化內容僅支援此頁面上記錄的子集。
