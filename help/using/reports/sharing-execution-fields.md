---
solution: Journey Optimizer
product: journey optimizer
title: journeyStep 事件動作執行欄位
description: journeyStep 事件動作執行欄位
feature: Journeys, Reporting
topic: Content Management
role: Engineer, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 3%

---

# journeyStep 事件動作執行欄位 {#sharing-execution-fields}

此欄位群組將由journeyStepEvent和journeyStepProfileEvent共用。

如果步驟有要處理的動作，這些欄位將會新增至事件裝載。

## actionID {#actionid-field}

正在執行的動作ID。

型別：字串

## actionName {#actionname-field}

動作的名稱。 如果尚未設定名稱，則會採用stepName。

型別：字串

## actionType {#actionType-field}

動作的型別。

型別：字串

## actionParameterized {#actionparameterized-field}

指出動作是否已引數化。

型別：布林值

## actionExecutionTime {#actionexecutiontime-field}

執行目前動作所需的時間（毫秒）。

型別： long

`actionExecutionTime`欄位代表執行動作所花費的總時間（以毫秒為單位），包括請求在佇列中等待的時間（如果已設定節流且達到速率限制）以及實際執行時間（包括連線至外部端點的網路延遲）。

`Timestamp`欄位指出動作執行的結束時間。 若要判斷設定檔何時進入自訂動作節點，請從`actionExecutionTime`中減去`Timestamp`。

例如，如果`Timestamp`是&quot;2025-02-04 09:39:03 UTC&quot;，而`actionExecutionTime`是1,813,227毫秒（~31分鐘），則設定檔在大約&quot;2025-02-04 09:08:32 UTC&quot;進入節點。




## actionExecutionError {#actionexecutionerror-field}

呼叫動作時發生的錯誤型別。

型別：字串

值：

* http
* 上限
* 逾時
* 錯誤

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

動作執行錯誤的程式碼。 如果錯誤有程式碼（例如HTTP程式碼）則會出現。

型別：字串

## actionExecutionOriginError {#actionexecutionoriginerror-field}

在兩種情況下，可能會發生逾時：

* 在第一次嘗試時會執行動作。 在此情況下，執行未完成，因此沒有基礎錯誤
* 重試：在此情況下，actionExecOrigError/actionExecOrigErrorCode會說明在重試之前嘗試遇到的錯誤。

例如，會傳送電子郵件，而第一次嘗試時會傳回HTTP 500錯誤。 會重試擷取，但嘗試2次的持續時間超過逾時。 之後，該動作執行會被標籤為逾時。 動作部分看起來會像這樣：

```
    ...
    "actionId": "myActionId",
    "actionName": "My mail sending",
    "actionType": "acsRestAction",
    "actionParameterized": true,
    "actionExecError": "timedout",
    "actionExecOrigError": "http",
    "actionExecOrigErrorCode": "500"
```

型別：字串

## actionExecutionOriginCode {#actionexecutionorigincode-field}

actionExecOrigError的錯誤碼。

型別：字串

## actionBusinessType {#actionbusinesstype-field}

指示動作的型別。

值：

* 內建
   * ACS電子郵件
   * ACS簡訊
   * ACS推播
* 客戶
   * Epsilon
   * ...

型別：字串

## deliveryJobId {#deliveryjobid-field}

此屬性說明批次歷程的傳送工作ID。

型別：字串

## batchdeliveryid {#batchdeliveryid-field}

此屬性說明批次歷程的傳遞ID。

型別：字串

## fromSegmentTrigger {#fromsegmenttrigger-field}

這描述了批次歷程是否從受眾區段觸發。

型別：布林值

## actionSchedulerCount {#actionschedulercount-field}

在步驟處理期間傳送給排程器服務的排程器通知要求計數。

型別： long
