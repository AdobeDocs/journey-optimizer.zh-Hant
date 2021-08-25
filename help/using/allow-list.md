---
title: 允許清單
description: 了解如何使用允許的清單。
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 0%

---

# 允許的清單 {#allow-list}

您現在可以在[sandbox](administration/sandboxes.md)層級定義特定的傳送安全清單，以便擁有用於測試的安全環境。 在可能發生錯誤的非生產執行個體上，允許的清單可確保您沒有將不需要的訊息傳送給客戶的風險。

允許的清單可讓您指定個別電子郵件地址或網域，這些地址或網域將是唯一獲授權接收您從特定沙箱傳送之電子郵件的收件者或網域。 這可防止您在測試環境中意外傳送電子郵件至真實的客戶地址。

>[!CAUTION]
>
>此功能&#x200B;**不**&#x200B;適用於生產沙箱。 它僅適用於電子郵件通道。

## 啟用允許的清單 {#enable-allow-list}

若要在非生產沙箱上啟用允許的清單，您必須使用訊息預設集服務中的對應API端點來更新一般設定。

* 使用此API，您也可以隨時停用功能。

* 您可以在啟用功能之前或之後更新允許的清單。

* 如果允許的清單為&#x200B;**not**&#x200B;空白，則允許的清單邏輯會在功能啟用&#x200B;**和**&#x200B;時套用。 進一步了解[本節](#logic)。

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>啟用後，執行歷程時，以及使用[校樣](preview.md#send-proofs)測試訊息，以及使用[測試模式](building-journeys/testing-the-journey.md)測試歷程時，都會採用允許的清單功能。

## 將實體新增至允許的清單 {#add-entities}

若要將新電子郵件地址或網域新增至特定沙箱的允許清單，您必須使用`listType`屬性的`ALLOWED`值呼叫抑制API。 例如：

![](assets/allow-list-api.png)

您可以執行&#x200B;**Add**、**Delete**&#x200B;和&#x200B;**Get**&#x200B;操作。

>[!NOTE]
>
>允許的清單最多可包含1,000個項目。

<!--
Learn more on making these API calls in the API reference documentation.
Found this link in Experience Platform documentation, but may not be the final one: (https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## 允許的清單邏輯 {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

當允許的清單為&#x200B;**empty**&#x200B;時，不會應用允許的清單邏輯。 這表示您可以傳送電子郵件給任何設定檔，但前提是它們不在[隱藏清單](suppression-list.md)中。

當允許的清單為&#x200B;**非空**&#x200B;時，將應用允許的清單邏輯：

* 如果允許的清單&#x200B;**上沒有實體，且隱藏清單上沒有實體，則相應的收件人將不會收到電子郵件，原因為&#x200B;**[!UICONTROL Not allowed]**。**

* 如果允許的清單&#x200B;**上的實體為**，而非隱藏清單上的實體，則可以將電子郵件發送到相應的收件人。 但是，如果實體也在[隱藏清單](suppression-list.md)中，則相應的收件人將不會收到電子郵件，原因為&#x200B;**[!UICONTROL Suppressed]**。

>[!NOTE]
>
>狀態為&#x200B;**[!UICONTROL Not allowed]**&#x200B;的設定檔會在訊息傳送程式期間排除。 因此，雖然&#x200B;**歷程報表**&#x200B;會將這些設定檔顯示為已在歷程（[讀取區段](building-journeys/read-segment.md)和[訊息](building-journeys/journeys-message.md)活動）中移動，但&#x200B;**電子郵件報表**&#x200B;不會在電子郵件傳送前篩選掉的&#x200B;**[!UICONTROL Sent]**&#x200B;量度中納入這些設定檔。
>
>進一步了解[即時報表](reports/live-report.md)和[全域報表](reports/global-report.md)。

## 排除報表 {#reporting}

在非生產沙箱上啟用此功能時，您可以擷取因不在允許清單中而從傳送中排除的電子郵件地址或網域。 若要這麼做，您可以使用[Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}進行下列API呼叫。

若要取得因收件者不在允許清單中而未傳送的&#x200B;**電子郵件數**，請使用下列查詢：

```
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

若要取得因收件者不在允許清單中而未傳送的&#x200B;**電子郵件地址清單**，請使用下列查詢：

```
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

