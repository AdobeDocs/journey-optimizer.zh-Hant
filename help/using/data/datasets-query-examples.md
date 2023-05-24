---
solution: Journey Optimizer
product: journey optimizer
title: 資料集查詢示例
description: 資料集查詢示例
feature: Reporting
topic: Content Management
role: User
level: Intermediate
keywords: 資料集，優化程式，使用案例
exl-id: 26ba8093-8b6d-4ba7-becf-b41c9a06e1e8
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 3%

---

# 資料集使用案例 {#tracking-datasets}

在此頁中，您將找到Adobe Journey Optimizer資料集清單和相關使用案例：

[電子郵件跟蹤體驗事件資料集](#email-tracking-experience-event-dataset)
[消息反饋事件資料集](#message-feedback-event-dataset)
[推送跟蹤體驗事件資料集](#push-tracking-experience-event-dataset)
[行程步驟事件](#journey-step-event)
[決定事件資料集](#ode-decisionevents)
[BCC反饋事件資料集](#bcc-feedback-event-dataset)
[實體資料集](#entity-dataset)

若要檢視每個結構描述的欄位與屬性完整清單，請參閱 [Journey Optimizer 結構描述字典](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=zh-Hant){target="_blank"}。

## 電子郵件跟蹤體驗事件資料集{#email-tracking-experience-event-dataset}

_介面中的名稱：CJM電子郵件跟蹤體驗事件資料集_

用於從Journey Optimizer接收電子郵件跟蹤體驗事件的系統資料集。

相關架構是CJM電子郵件跟蹤體驗事件架構。

此查詢顯示給定郵件的不同電子郵件交互（開啟、按一下）計數：

```sql
select
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageInteraction.interactionType
```

此查詢按給定行程的消息顯示不同電子郵件交互（開啟、按一下）的計數細目：

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
limit 100;
```

## 消息反饋事件資料集{#message-feedback-event-dataset}

_介面中的名稱：CJM消息反饋事件資料集_

用於從Journey Optimizer接收電子郵件和推送應用程式反饋事件的資料集。

相關架構為CJM消息反饋事件架構。

此查詢顯示給定消息的不同電子郵件反饋狀態（發送、彈出等）的計數：

```sql
select
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus;
```

此查詢按給定行程的消息顯示不同電子郵件反饋狀態（發送、彈出等）的計數細分：

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
limit 100;
```

在聚合級別，域級別報告（按頂級域排序）:域名、消息已發送、回放

```sql
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

每天發送電子郵件：

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

查找特定電子郵件ID是否收到電子郵件，如果沒有，則錯誤、彈出類別、代碼：

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

查找過去x小時/天內出現特定錯誤、彈出類別或代碼或與特定郵件傳遞關聯的所有單個電子郵件ID的清單：

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

匯總層硬彈跳率：

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

按彈出代碼分組的永久錯誤：

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

### 在ISP中斷後確定隔離地址{#isp-outage-query}

在Internet服務提供商(ISP)中斷時，您需要在一定時間內將錯誤標籤為特定域的回報（隔離）的電子郵件地址標識為。 要獲取這些地址，請使用以下查詢：

```sql
SELECT
    _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
    timestamp AS EventTime,
    _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.reason AS "Invalid Recipient"
FROM cjm_message_feedback_event_dataset
WHERE
    eventtype = 'message.feedback' AND
    DATE(timestamp) BETWEEN '<start-date-time>' AND '<end-date-time>' AND
    _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND
    _experience.customerJourneyManagement.emailChannelContext.address ILIKE '%domain.com%'
ORDER BY timestamp DESC;
```

其中日期格式為：YYYY-MM-DD HH:MM:SS

一旦確定，就從Journey Optimizer禁止清單中刪除這些地址。 [了解更多](../configuration/manage-suppression-list.md#remove-from-suppression-list)。

## 推送跟蹤體驗事件資料集 {#push-tracking-experience-event-dataset}

_介面中的名稱：CJM推送跟蹤體驗事件資料集_

用於接收移動跟蹤體驗事件以從Journey Optimizer推送的資料集。

相關架構是CJM推送跟蹤體驗事件架構。

查詢示例：

```sql
select _experience.customerJourneyManagement.pushChannelContext.platform, sum(pushNotificationTracking.customAction.value)  from cjm_push_tracking_experience_event_dataset
group by _experience.customerJourneyManagement.pushChannelContext.platform

select  _experience.customerJourneyManagement.pushChannelContext.platform, SUM (_experience.customerJourneyManagement.messageInteraction.offers.offerCount) from cjm_email_tracking_experience_event_dataset
  group by _experience.customerJourneyManagement.pushChannelContext.platform
```

## 行程步驟事件{#journey-step-event}

_內部名稱：行程步驟事件（系統資料集）_

用於在行程中接收步驟事件的資料集。

相關架構是用於Journey Orchestration的行程步驟事件架構。

此查詢按給定行程的活動標籤顯示活動成功計數的細分：

```sql
select
    _experience.journeyOrchestration.stepEvents.actionName AS actionLabel,
    count(1) actionSuccessCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.actionID IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionType IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode IS NULL
group by
    _experience.journeyOrchestration.stepEvents.actionName;   
```

此查詢顯示給定行程按nodeId和nodeLabel輸入的步驟計數的細分。 節點ID包含在此處，因為節點標籤對於不同的行程節點可以是相同的。

```sql
select
    _experience.journeyOrchestration.stepEvents.nodeID AS nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName AS nodeLabel,
    count(1) stepEnteredCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = TRUE
     AND _experience.journeyOrchestration.stepEvents.eventID IS DISTINCT FROM 'createInstance'
group by
    _experience.journeyOrchestration.stepEvents.nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName; 
```

## 決定事件資料集{#ode-decisionevents}

_介面中的名稱：ODE DecisionEvents（系統資料集）_

用於接收的資料集向用戶提供命題。

相關架構為ODE DecisionEvents。

此查詢顯示前一天返回的所有優惠：

```sql
SELECT date_format(Decision.Timestamp, 'MM/dd/yyyy') as Date
,HOUR(Decision.timestamp) as Hour
,COUNT(*)  as Count
FROM ode_decisionevents_b699fa78_efec_41b1_99fa_78efecc1b1ef_decision AS Decision
WHERE date_format(Decision.timestamp, 'MM/dd/yyyy') = date_format(CURRENT_DATE, 'MM/dd/yyyy') and Decision._experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:13ab41890a335ad6'
GROUP BY date_format(Decision.Timestamp, 'MM/dd/yyyy')
,HOUR(Decision.timestamp)
ORDER BY 1, 2 DESC;
```

此查詢顯示在特定活動/決定及其關聯的優惠優先順序的過去30天內建議的優惠次數。

```sql
select proposedOffers.id,proposedOffers.name, po._experience.decisioning.ranking.priority, count(proposedOffers.id) as ProposedCount from (
select explode(propositionexplode.selections) AS proposedOffers from
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20200925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

<!--
## Consent Service Dataset{#consent-service-dataset}

_Name in the interface: CJM Consent Service Dataset (system dataset)_

Dataset for Journey Optimizer Consent service.

The related schema is CJM Consent Service Schema.

Query to list email IDs that have consented to receive email:

```sql
select key as email FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
)
where value.marketing.email.val == 'y'
```

Query to return consent value for an email ID where email ID would be the input:

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```
-->

## BCC反饋事件資料集{#bcc-feedback-event-dataset}

_介面中的名稱：AJO BCC反饋事件資料集（系統資料集）_

用於儲存BCC消息資訊的資料集。

在2天內查詢所有密件抄送消息（對於特定市場活動）:

```sql
SELECT bcc.*
FROM ajo_bcc_feedback_event_dataset AS bcc
WHERE 
    bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID = '<message-execution-id>' AND 
    bcc.timestamp >= now() - INTERVAL '2' day; 
```

使用反饋資料集進行查詢，以顯示未接收（所有回饋和禁止顯示）以及具有特定消息的BCC條目的用戶：

```sql
SELECT 
    distinct bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS OriginalRecipientAddress 
FROM ajo_bcc_feedback_event_dataset  AS bcc 
WHERE 
    bcc.timestamp > now() - INTERVAL '2' DAY AND     bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND      bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress != '' AND
    ( 
            bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress NOT IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
            mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent'
        )  
    OR     bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
        mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND 
            mfe._experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.category = 'async' AND 
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus
```

## 實體資料集{#entity-dataset}

_介面中的名稱：ajo_entity_dataset（系統資料集）_

用於儲存發送到最終用戶的消息的實體元資料的資料集。

相關架構為AJO實體架構。

此資料集使您能夠訪問商家定義的元資料，這使您能夠在導出Journey Optimizer資料集以在外部工具中報告可視化時獲得更好的報告洞察力。 這是使用消息ID屬性實現的，該屬性幫助縫合諸如消息反饋資料集和體驗事件跟蹤資料集之類的各種資料集，以在配置檔案級別獲得從發送到跟蹤的消息傳遞的詳細資訊。

**重要備註**

* 只有在發佈行程或市場活動後，才會建立消息條目。

* 在市場活動/旅程發佈後30分鐘，您可能會看到該條目。

>[!NOTE]
>
>目前，由於未來相容性原因，實體資料集中每個消息發佈有兩個條目。 這不會影響您根據需要跨資料集使用聯接查詢來獲取所需資訊的能力。

如果您想在報告中根據發送的操作對特定行程發送的電子郵件進行排序。 可以將消息反饋資料集與實體資料集連接。 要使用的欄位包括： `_experience.decisioning.propositions.scopeDetails.correlationID` 和 `_id field in entity dataset`。

以下查詢可幫助您獲取給定市場活動的關聯消息模板：

```sql
SELECT
  AE._experience.customerJourneyManagement.entities.channelDetails.template
from
  ajo_entity_dataset AE
    WHERE AE._experience.customerJourneyManagement.entities.campaign.campaignVersionID = 'd7a01136-b113-4ef2-8f59-b6001f7eef6e'
```

以下查詢有助於獲取與所有反饋事件關聯的旅程詳細資訊和電子郵件主題：

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject 
from 
  ajo_entity_dataset AE 
  INNER JOIN cjm_message_feedback_event_dataset MF ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```

您可以縫合行程步驟事件、消息反饋和跟蹤資料集，以獲取特定配置檔案的統計資訊：

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.PROFILEID,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.NODENAME
from 
  ajo_entity_dataset AE 
  INNER JOIN cjm_message_feedback_event_dataset MF 
    ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
    INNER JOIN journey_step_events JE
    ON AE._experience.customerJourneyManagement.entities.journey.journeyActionID = JE._experience.journeyOrchestration.stepEvents.actionID
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```
