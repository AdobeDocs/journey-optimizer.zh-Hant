---
title: 允許清單
description: 了解如何使用允許的清單。
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: e1d0afb70af4ab31db56f90c189c085ba8d1eb7c
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 0%

---

# 允許的清單 {#allow-list}

現在可以在 [沙箱](administration/sandboxes.md) 級別，以擁有安全的環境以用於測試。 在可能發生錯誤的非生產執行個體上，允許的清單可確保您沒有將不需要的訊息傳送給客戶的風險。

允許的清單可讓您指定個別電子郵件地址或網域，這些地址或網域將是唯一獲授權接收您從特定沙箱傳送之電子郵件的收件者或網域。 這可防止您在測試環境中意外傳送電子郵件至真實的客戶地址。

>[!CAUTION]
>
>此功能為 **not** 適用於生產沙箱。 它僅適用於電子郵件通道。

## 啟用允許的清單 {#enable-allow-list}

若要在非生產沙箱上啟用允許的清單，您必須使用訊息預設集服務中的對應API端點來更新一般設定。

* 使用此API，您也可以隨時停用功能。

* 您可以在啟用功能之前或之後更新允許的清單。

* 啟用功能時，會套用允許的清單邏輯 **和** 如果允許的清單為 **not** 空白。 深入了解 [本節](#logic).

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>啟用後，執行歷程時，以及透過測試訊息時，都會採用允許的清單功能 [校樣](preview.md#send-proofs) 和使用 [測試模式](building-journeys/testing-the-journey.md).

## 將實體新增至允許的清單 {#add-entities}

若要將新電子郵件地址或網域新增至特定沙箱的允許清單，您必須使用 `ALLOWED` 值 `listType` 屬性。 例如：

![](assets/allow-list-api.png)

您可以執行 **新增**, **刪除** 和 **取得** 操作。

>[!NOTE]
>
>允許的清單最多可包含1,000個項目。

<!--
Learn more on making these API calls in the API reference documentation.
Found this link in Experience Platform documentation, but may not be the final one: (https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## 允許的清單邏輯 {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

允許的清單為 **空白**，則不會套用允許的清單邏輯。 這表示您可以傳送電子郵件給任何設定檔，但前提是這些設定檔不在 [隱藏清單](suppression-list.md).

允許的清單為 **非空白**，則會套用允許的清單邏輯：

* 如果實體為 **不在允許的清單上**，而不在取消清單上，則對應的收件者將不會收到電子郵件，原因是 **[!UICONTROL Not allowed]**.

* 如果實體為 **在允許的清單上**，而不是顯示在隱藏清單上，則可以將電子郵件傳送給對應的收件者。 不過，如果實體同時位於 [隱藏清單](suppression-list.md)，則對應的收件者將不會收到電子郵件，原因為 **[!UICONTROL Suppressed]**.

>[!NOTE]
>
>具有 **[!UICONTROL Not allowed]** 在訊息傳送程式期間會排除狀態。 因此，若 **歷程報表** 會將這些設定檔顯示為已在歷程中移動([讀取區段](building-journeys/read-segment.md) 和 [訊息](building-journeys/journeys-message.md) 活動), **電子郵件報表** 不會將其納入 **[!UICONTROL Sent]** 量度，因為在傳送電子郵件前會先將量度篩選掉。
>
>深入了解 [即時報表](reports/live-report.md) 和 [全域報表](reports/global-report.md).

## 排除報表 {#reporting}

在非生產沙箱上啟用此功能時，您可以擷取因不在允許清單中而從傳送中排除的電子郵件地址或網域。 若要這麼做，您可以使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}以進行下方的API呼叫。

若要取得 **電子郵件數** 由於收件者未列在允許清單上，因此未傳送，請使用下列查詢：

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

若要取得 **電子郵件地址清單** 由於收件者未列在允許清單上，因此未傳送，請使用下列查詢：

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
