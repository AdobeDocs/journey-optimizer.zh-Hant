---
solution: Journey Optimizer
product: journey optimizer
title: journeyStep事件資料擷取欄位
description: journeyStep事件資料擷取欄位
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# journeyStep事件資料擷取欄位 {#sharing-fetch-fields}

此欄位群組將由journeyStepEvent和journeyStepProfileEvent共用。

在步驟處理期間，我們可以在欄位群組上擷取N個資料。

## fetchTotalTime {#fetchtotaltime-field}

步驟處理期間以毫秒為單位的資料擷取總逗留時間。

類型：long

## fetchTypeInError {#fetchtypeinerror-field}

定義錯誤擷取是在Adobe Experience Platform上還是在自訂資料來源上。

類型：字串

值：
* aep
* 自訂

## fetchError {#fetcherror-field}

處理資料擷取時發生的錯誤類型。

類型：字串

值：
* http
* 上限
* timedout
* 錯誤

## fetchErrorCode {#fetcherrorcode-field}

擷取錯誤的程式碼。 如果錯誤有程式碼（例如HTTP程式碼），則顯示。 例如，如果actionExecError為http，則代碼404代表HTTP 404錯誤。

類型：字串

## fetchOriginError {#fetchoriginerror-field}

逾時可能發生，有兩種情況：

* 第一次嘗試時，會執行動作。 在此情況下，執行尚未完成，因此沒有基本錯誤
* 重試時：在這種情況下，actionExecOrigError/actionExecOrigErrorCode描述重試前在嘗試時遇到的錯誤。

例如，從統一設定檔服務擷取資料，並在第一次嘗試時傳回HTTP 500錯誤。 會重試擷取，但兩次嘗試的持續時間超過逾時。 然後，動作執行會標籤為逾時。 動作部分看起來會像這樣：

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

類型：字串

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

系統提供的錯誤代碼 [!DNL Journey Optimizer] 正在查詢。 例如，可以是404、500等。

類型：字串

## fetchCount {#fetchcount-field}

擷取資料的次數，無論來源類型為何。

類型：long

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

從Adobe Experience Platform擷取資料所花的總時間（以毫秒為單位）。 備注：從引擎將擴充事件發送到擴充服務並接收響應的時間開始計算該時間量。

類型：long

## fetchPlatformCount {#fetchplatformcount-field}

從Adobe Experience Platform擷取資料的次數。

類型：long

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

以毫秒為單位擷取自訂資料的時間量。 備注：從引擎將擴充事件發送到擴充服務並接收響應的時間開始計算該時間量

類型：long

## fetchCustomCount {#fetchcustomcount-field}

從外部系統擷取自訂資料的次數。

類型：long
