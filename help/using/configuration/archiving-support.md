---
solution: Journey Optimizer
product: journey optimizer
title: 在Journey Optimizer的存檔支援
description: 瞭解如何存檔郵件
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 存檔，郵件， HIPAA，密件抄送，電子郵件
exl-id: 186a5044-80d5-4633-a7a7-133e155c5e9f
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 7%

---

# 支援封存 {#archiving-support}

## 如何存檔郵件 {#about-archiving}

HIPAA等法規要求 [!DNL Journey Optimizer] 應提供一種存檔發送給個人的郵件的方法。 實際上，如果您的客戶提出索賠，他們應該能夠獲得已發送郵件的副本，以便進行驗證。

* 對於電子郵件通道， [!DNL Journey Optimizer] 提供內置的密件抄送電子郵件功能。 [了解更多](#bcc-email)

* 另外，對於所有通道，您可以使用 **實體資料集**，其中包含非個性化消息模板的詳細資訊。 使用此欄位導出資料集以保存元資料，例如：誰發了資訊，誰和什麼時候。 請注意，個性化資料不會導出 — 只考慮模板（消息的格式和結構）。 [了解更多](../data/datasets-query-examples.md#entity-dataset)

>[!NOTE]
>
>[!DNL Journey Optimizer] 不支援SMS存檔要求。 要獲得專門的存檔支援，請與您的SMS供應商（Synch或Twilio）合作。

## 如何對電子郵件使用密件抄送 {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="定義密件副本電子郵件地址"
>abstract="您可以透過將電子郵件傳送到密件副本收件匣來保留已傳送之電子郵件的副本。輸入您選擇的電子郵件地址，以便每封電子郵件都會以密件方式傳送至此密件副本地址。請注意，密件副本地址網域不應和委派給 Adobe 的任何子網域相同。此功能為選用。"

您可以發送由 [!DNL Journey Optimizer] 收件箱。 此可選功能允許您保留您發送給用戶的電子郵件通信副本，以便符合和/或存檔。 這對遞送收件人是不可見的。

### 啟用密件抄送電子郵件 {#enable-bcc}

啟用 **[!UICONTROL 密件抄送電子郵件]** 選項，在 [通道表面](channel-surfaces.md) （即消息預設）。 您可以以正確的格式指定任何外部地址，但子域上已定義的電子郵件地址除外，該子域已委派給Adobe。 例如，如果您委託 *營銷.luma.com* 子域到Adobe，任何類似 *abc@marketing.luma.com* 禁止。

>[!CAUTION]
>
>您只能定義一個密件抄送電子郵件地址。 確保BCC地址具有足夠的接收容量來儲存使用當前通道表面發送的所有電子郵件。
>
>中列出了更多建議 [此部分](#bcc-recommendations-limitations)。

>[!NOTE]
>
>如果您已購買了Healthcare Shield附加產品，則必須確保BCC地址的ISP支援TLS 1.2協定。

![](assets/preset-bcc.png)

使用此表面的所有電子郵件將盲目複製到您輸入的BCC電子郵件地址。 從那裡，可以使用外部系統處理和存檔這些檔案。

>[!CAUTION]
>
>您的密件抄送功能使用情況將根據您獲得許可的郵件數計算。 因此，僅在用於要存檔的關鍵通信的曲面中啟用它。 檢查您的合同中是否有許可的卷。

BCC電子郵件地址設定將立即在表面級保存和處理。 使用此表面建立新郵件時，系統會自動顯示密件抄送電子郵件地址。

![](assets/preset-bcc-in-msg.png)

但是，BCC地址會按照描述的邏輯被拾取以發送通信 [這裡](../email/email-settings.md)。

### Recommendations和限制 {#bcc-recommendations-limitations}

* 為確保您的隱私合規性，BCC電子郵件必須由能夠安全儲存個人身份資訊(PII)的存檔系統處理。

* 由於郵件可以包含敏感或私有資料，因此請確保BCC地址正確，並確保對郵件的訪問安全。

* 您用於密件抄送的收件箱應正確管理空間和傳遞。 如果收件箱返回回復，則可能無法接收某些電子郵件，因此無法存檔。

* 郵件可以在目標收件人之前傳送到密件抄送電子郵件地址。 即使原始消息可能具有 [彈](../reports/suppression-list.md#delivery-failures)。

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* 不要開啟或按一下發送到密件抄送地址的電子郵件，因為在發送分析的總開啟和按一下時會考慮電子郵件，這可能會導致在 [報告](../reports/global-report.md)。

* 不要在密件抄送收件箱中將郵件標籤為垃圾郵件，因為它會影響發送到此地址的所有其他電子郵件。

>[!CAUTION]
>
>不要在發送到密件抄送地址的電子郵件中按一下取消訂閱連結，因為您將立即取消訂閱相應收件人。

### GDPR合規性 {#gdpr-compliance}

GDPR等法規規定資料主體應能夠隨時修改其同意。 由於您與Journey Optimizer一起發送的BCC電子郵件包含安全的個人身份資訊(PII)，因此您必須編輯 **[!UICONTROL CJM電子郵件BCC反饋事件架構]** 能夠按照GDPR和類似的法規管理這些PII。

請依照下列步驟以執行此操作。

1. 轉到 **[!UICONTROL 資料管理]** > **[!UICONTROL 架構]** > **[!UICONTROL 瀏覽]** 選擇 **[!UICONTROL CJM電子郵件BCC反饋事件架構]**。

   ![](assets/preset-bcc-schema.png)

1. 按一下展開 **[!UICONTROL 體驗]**。 **[!UICONTROL 客戶旅程管理]** 然後 **[!UICONTROL secondaryRecipientDetail]**。

1. 選擇 **[!UICONTROL 原始收件人地址]**。

1. 在 **[!UICONTROL 欄位屬性]** 在右側，向下滾動到 **[!UICONTROL 身份]** 複選框。

1. 選擇它，然後 **[!UICONTROL 主標識]**。

1. 從下拉清單中選擇一個命名空間。

   ![](assets/preset-bcc-schema-identity.png)

1. 按一下&#x200B;**[!UICONTROL 套用]**。

>[!NOTE]
>
>瞭解有關管理隱私和中適用法規的更多資訊 [Experience Platform文檔](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hant){target="_blank"}。

### 密件抄送報告資料 {#bcc-reporting}

行程和消息報告中不提供BCC的報告。 但是，資訊儲存在名為 **[!UICONTROL AJO BCC反饋事件資料集]**。 您可以對此資料集運行查詢，以查找用於調試的有用資訊。

您可以通過用戶介面訪問此資料集。 選擇 **[!UICONTROL 資料管理]** > **[!UICONTROL 資料集]** > **[!UICONTROL 瀏覽]** 並啟用 **[!UICONTROL 顯示系統資料集]** 從篩選器切換以顯示系統生成的資料集。 瞭解有關如何訪問資料集的詳細資訊 [此部分](../data/get-started-datasets.md#access-datasets)。

![](assets/preset-bcc-dataset.png)

要針對此資料集運行查詢，可以使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}。 要訪問它，請選擇 **[!UICONTROL 資料管理]** > **[!UICONTROL 查詢]** 按一下 **[!UICONTROL 建立查詢]**。 [了解更多](../data/get-started-queries.md)

![](assets/preset-bcc-queries.png)

根據您要查找的資訊，您可以運行以下查詢。

1. 對於下面的所有其它查詢，您需要行程操作ID。 運行此查詢，以獲取在過去2天內與特定行程版本ID關聯的所有操作ID:

   ```
   SELECT
   DISTINCT
   CAST(TIMESTAMP AS DATE) AS EventTime,
   _experience.journeyOrchestration.stepEvents.journeyVersionID,
   _experience.journeyOrchestration.stepEvents.actionName, 
   _experience.journeyOrchestration.stepEvents.actionID 
   FROM journey_step_events 
   WHERE 
   _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND 
   _experience.journeyOrchestration.stepEvents.actionID is not NULL AND 
   TIMESTAMP > NOW() - INTERVAL '2' DAY 
   ORDER BY EventTime DESC;
   ```

   >[!NOTE]
   >
   >獲取 `<journey version id>`參數，選擇相應的 [旅程版本](../building-journeys/journey.md#journey-versions) 從 **[!UICONTROL 行程管理]** > **[!UICONTROL 旅程]** 的子菜單。 行程版本ID顯示在Web瀏覽器中顯示的URL的末尾。
   >
   >![](assets/preset-bcc-action-id.png)

1. 運行此查詢以獲取過去2天內為特定用戶目標的特定消息生成的所有消息反饋事件（尤其是反饋狀態）:

   ```
   SELECT  
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
       WHEN 'sent' THEN 'Sent'
       WHEN 'delay' THEN 'Retry'
       WHEN 'out_of_band' THEN 'Bounce' 
       WHEN 'bounce' THEN 'Bounce'
   END AS FeedbackStatusCategory
   FROM cjm_message_feedback_event_dataset 
   WHERE  
       timestamp > now() - INTERVAL '2' day  AND
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
       _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND  
       _experience.customerJourneyManagement.emailChannelContext.address = '<recipient email address>'
       ORDER BY EventTime DESC;
   ```

   >[!NOTE]
   >
   >獲取 `<journey action id>` 參數，使用行程版本id運行上述第一個查詢。 的 `<recipient email address>` 參數是目標或實際收件人的電子郵件地址。

1. 運行此查詢，以獲取過去2天內為特定用戶目標的特定消息生成的所有密件抄送消息反饋事件：

   ```
   SELECT   
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   _experience.customerJourneyManagement.emailChannelContext.address AS BccEmailAddress,
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
               WHEN 'sent' THEN 'Sent'
               WHEN 'delay' THEN 'Retry'
               WHEN 'out_of_band' THEN 'Bounce' 
               WHEN 'bounce' THEN 'Bounce'
           END AS FeedbackStatusCategory 
   FROM ajo_bcc_feedback_event_dataset  
   WHERE  
   timestamp > now() - INTERVAL '2' day  AND
   _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journeyaction id>' AND 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = '<recipient email address>'
   ORDER BY EventTime DESC;
   ```

1. 運行此查詢以獲取所有未收到郵件的收件人地址，而其BCC條目在過去30天記憶體在：

   ```
    SELECT
        DISTINCT 
    bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddressesNotRecievedMessage
    FROM ajo_bcc_feedback_event_dataset bcc
    LEFT JOIN cjm_message_feedback_event_dataset mfe
    ON 
   bcc._experience.customerJourneyManagement.messageExecution.journeyVersionID =
            mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID AND    bcc._experience.customerJourneyManagement.messageExecution.journeyActionID = mfe._experience.customerJourneyManagement.messageExecution.journeyActionID AND 
   bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = mfe._experience.customerJourneyManagement.emailChannelContext.address AND
   mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   mfe._experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND
   mfe.timestamp > now() - INTERVAL '30' DAY AND
   mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus IN ('bounce', 'out_of_band') 
    WHERE bcc.timestamp > now() - INTERVAL '30' DAY;
   ```
