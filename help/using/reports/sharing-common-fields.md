---
solution: Journey Optimizer
product: journey optimizer
title: journeysteps事件常見欄位
description: journeysteps事件常見欄位
feature: Journeys, Reporting
topic: Content Management
role: Engineer, Admin
level: Experienced
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# journeysteps事件常見欄位 {#sharing-common-fields}

此欄位群組將由以下事件共用： **journeyStepEvent**&#x200B;和&#x200B;**journeyStepProfileEvent**。

這些是[!DNL Journey Optimizer]傳送至Adobe Experience Platform的常見XDM欄位。 歷程中處理的每個步驟都會傳送通用欄位。 自訂動作和增強功能會使用更具體的欄位。

其中一些欄位僅適用於特定處理模式（動作執行、資料擷取等），以限制事件大小。


>[!NOTE]
>
>在本節[中進一步瞭解歷程屬性](../building-journeys/expression/journey-properties.md#journey-propertoes-fields)。


## 入口 {#entrance-field}

指出使用者是否已進入歷程。 如果不存在，我們會假設值為false。

型別：布林值

值： true/false

## 重新進入 {#reentrance-field}

指出使用者是否已使用相同執行個體重新進入歷程。 如果不存在，我們會假設值為false。

型別：布林值

值： true/false

## instanceEnded {#instance-ended-field}

表示執行個體是否已結束（成功或失敗）。

型別：布林值

## eventID {#eventid-field}

處理中的事件ID，用於步驟處理。 如果事件是外部事件，則值為其eventId。 如果事件是內部事件，則值為內部eventId （例如scheduledNotificationReceived、executedAction等）。

型別：字串

## nodeID {#nodeid-field}

使用者端節點id （來自畫布）。

型別：字串

## stepID {#stepdid-field}

目前正在處理之步驟的唯一ID。

型別：字串

## stepName {#stepname-field}

目前正在處理的步驟名稱。

型別：字串

## stepType {#steptype-field}

步驟型別。

型別：字串

可能的值：

* 條件
* 動作
* 排程器
* 計時器

## 步驟狀態 {#stepstatus-field}

步驟的狀態，代表步驟在處理完成（且引發步驟事件）時的狀態。

型別：字串

狀態可以是：

* 已結束：步驟沒有轉變，其處理已成功結束。
* 錯誤：步驟處理發生錯誤。
* 轉變：步驟正在等待事件轉變到另一個步驟。
* 上限：步驟因上限錯誤而失敗，在動作或擴充期間發生。
* 逾時：步驟因逾時錯誤而失敗，在動作或擴充期間發生。
* instanceTimedout：步驟已停止處理，因為執行個體已達到其逾時。

## journeyID {#journeyid-field}

歷程的ID。

型別：字串

## journeyVersionID {#journeyversionid-field}

歷程版本的ID。 在journeyStepEvent的情況下，此id代表歷程的身分參考。

型別：字串

>[!NOTE]
>
>基於疑難排解目的，我們建議在查詢歷程時使用journeyVersionID，而不是journeyVersionName。

## journeyVersionName {#journeyversionname-field}

歷程版本的名稱。

型別：字串

>[!NOTE]
>
>基於疑難排解目的，我們建議在查詢歷程時使用journeyVersionID，而不是journeyVersionName。

## journeyVersion {#journeyversion-field}

歷程版本的版本。

型別：字串

## instanceID {#instanceid-field}

歷程執行個體的內部ID。

型別：字串

## externalKey {#externalkey-field}

從事件擷取的外部索引鍵加以處理。

型別：字串

## parentstepid {#parenstepid-field}

執行個體中目前已處理步驟的父級步驟ID。

型別：字串

## parentStepName {#parentstepname-field}

目前步驟之父項的步驟名稱。

型別：字串

## parentTransitionID {#parenttransitionid-field}

將執行個體帶到已處理步驟的轉變ID。

型別：字串

## parentTransitionName {#parenttransitionname-field}

將執行個體帶到已處理步驟的轉變名稱。

型別：字串

## inTest {#intest-field}

表示此歷程是否處於測試模式。

型別：布林值

## processingtime {#processingtime-field}

從執行個體步驟進入到處理結束的總時間量（以毫秒為單位）。

型別： long

## instanceType {#instancetype-field}

指示執行個體型別（若為批次或單一）。

型別：字串

值：批次/單一

## recurrenceIndex {#recurrenceindex-field}

如果歷程是批次和週期性（第一次執行有recurrenceIndex = 1），則為週期性的索引。

型別： long

## isBatchToUniary {#isbatchtounitary-field}

表示此單一執行個體是否已從批次執行個體觸發。

型別：布林值

## batchExternalKey {#batchexternalkey-field}

批次事件的外部索引鍵。

型別：字串

## batchinstanceid {#batchinstanceid-field}

這是批次例項ID。

型別：字串

## batchUnitaryBranchID {#batchunitarybranchid-field}

如果執行個體是從批次執行個體觸發的，則為單一分支ID。

型別：字串

## exitCriteriaID

exitCriteria的ID

型別：字串

## exitCriteriaName

exitCriteria的名稱

型別：字串