---
title: 使用密件抄送電子郵件
description: 瞭解如何在郵件預設級別配置電子郵件設定
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 169ad138ea27b9049698d8d3bfa8a0817ed39fee
workflow-type: tm+mt
source-wordcount: '1069'
ht-degree: 3%

---

# 使用密件抄送電子郵件 {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="定義密件抄送電子郵件地址"
>abstract="您可以通過將已發送的電子郵件發送到密件抄送收件箱來保留其副本。 輸入您選擇的電子郵件地址，以便將發送的每封電子郵件盲目複製到此密件抄送地址。 此功能是選取性的。"

您可以發送由 [!DNL Journey Optimizer] 收件箱。 此可選功能允許您保留您發送給用戶的電子郵件通信副本，以便符合和/或存檔。 這對遞送收件人是不可見的。

## 啟用密件抄送電子郵件 {#enable-bcc}

啟用 **[!UICONTROL BCC email]** 選項，在「專用」欄位中輸入您選擇的電子郵件地址。 您可以以正確的格式指定任何外部地址，但委派子域上定義的電子郵件地址除外。 例如，如果委派的子域是 *營銷.luma.com*&#x200B;任何地址 *abc@marketing.luma.com* 禁止。

>[!NOTE]
>
>您只能定義一個密件抄送電子郵件地址。 確保BCC地址具有足夠的接收容量來儲存使用當前預設發送的所有電子郵件。
>
>中列出了更多建議 [此部分](#bcc-recommendations-limitations)。

![](assets/preset-bcc.png)

使用此預設的所有電子郵件將被盲目複製到您輸入的密件抄送電子郵件地址。 從那裡，可以使用外部系統處理和存檔這些檔案。

>[!CAUTION]
>
>您的密件抄送功能使用情況將根據您獲得許可的郵件數計算。 因此，僅在用於要存檔的關鍵通信的預設中啟用它。 檢查您的合同中是否有許可的卷。

BCC電子郵件地址設定將立即保存並處理在預設級別。 當你 [建立新消息](../messages/get-started-content.md#create-new-message) 使用此預設，系統會自動顯示密件抄送電子郵件地址。

![](assets/preset-bcc-in-msg.png)

但是，BCC地址會按照以下邏輯被拾取以發送通信：

* 對於批處理和拆分行程，它不適用於在進行BCC設定之前已啟動的批處理或拆分執行。 更改將在下次重複或新執行時進行。

* 對於事務性消息，立即為下一次通信（最多1分鐘延遲）接收更改。

>[!NOTE]
>
>您不需要重新發佈消息或行程以接收BCC設定。

## Recommendations和限制 {#bcc-recommendations-limitations}

* 為確保您的隱私合規性，BCC電子郵件必須由能夠安全儲存個人身份資訊(PII)的存檔系統處理。

* 由於郵件可以包含敏感或私有資料，因此請確保BCC地址正確，並確保對郵件的訪問安全。

* 您用於密件抄送的收件箱應正確管理空間和傳遞。 如果收件箱返回回復，則可能無法接收某些電子郵件，因此無法存檔。

* 郵件可以在目標收件人之前傳送到密件抄送電子郵件地址。 即使原始消息可能具有 [彈](../reports/suppression-list.md#delivery-failures)。

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* 不要開啟或按一下發送到密件抄送地址的電子郵件，因為在發送分析的總開啟和按一下時會考慮電子郵件，這可能會導致在 [報告](../reports/message-monitoring.md)。

* 不要在密件抄送收件箱中將郵件標籤為垃圾郵件，因為它會影響發送到此地址的所有其他電子郵件。


>[!CAUTION]
>
>不要在發送到密件抄送地址的電子郵件中按一下取消訂閱連結，因為您將立即取消訂閱相應收件人。

## GDPR合規性 {#gdpr-compliance}

GDPR等法規規定資料主體應能夠隨時修改其同意。 由於您與Journey Optimizer一起發送的BCC電子郵件包含安全的個人身份資訊(PII)，因此您必須編輯 **[!UICONTROL CJM Email BCC Feedback Event Schema]** 能夠按照GDPR和類似的法規管理這些PII。

請依照下列步驟以執行此操作。

1. 轉到 **[!UICONTROL Data management]** > **[!UICONTROL Schemas]** > **[!UICONTROL Browse]** 選擇 **[!UICONTROL CJM Email BCC Feedback Event Schema]**。

   ![](assets/preset-bcc-schema.png)

1. 按一下展開 **[!UICONTROL _experience]**。 **[!UICONTROL customerJourneyManagment]** 然後 **[!UICONTROL secondaryRecipientDetail]**。

1. 選擇「**[!UICONTROL originalRecipientAddress]**」。

1. 在 **[!UICONTROL Field properties]** 在右側，向下滾動到 **[!UICONTROL Identity]** 複選框。

1. 選擇它，然後 **[!UICONTROL Primary identity]**。

1. 從下拉清單中選擇一個命名空間。

   ![](assets/preset-bcc-schema-identity.png)

1. 按一下「**[!UICONTROL Apply]**」。

>[!NOTE]
>
>在 [Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hant){target=&quot;_blank&quot;} 中進一步瞭解隱私權管理和相關法規。

## 密件抄送報告資料 {#bcc-reporting}

行程和消息報告中不提供BCC的報告。 但是，資訊儲存在名為 **[!UICONTROL AJO BCC Feedback Event Dataset]**。 您可以對此資料集運行查詢，以查找用於調試的有用資訊。

您可以通過用戶介面訪問此資料集。 選擇 **[!UICONTROL Data management]** > **[!UICONTROL Datasets]** > **[!UICONTROL Browse]** 並啟用 **[!UICONTROL Show system datasets]** 從篩選器切換以顯示系統生成的資料集。 瞭解有關如何訪問資料集的詳細資訊 [此部分](../start/get-started-datasets.md#access-datasets)。

![](assets/preset-bcc-dataset.png)

要針對此資料集運行查詢，可以使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。 要訪問它，請選擇 **[!UICONTROL Data management]** > **[!UICONTROL Queries]** 按一下 **[!UICONTROL Create query]**。 [了解更多](../start/get-started-queries.md)

![](assets/preset-bcc-queries.png)

根據您要查找的資訊，您可以運行以下查詢。

1. 對於下面的所有其它查詢，您需要行程操作ID。 運行此查詢，以獲取在過去2天內與特定行程版本ID關聯的所有操作ID:

       「」
       選擇
       獨特
       CAST(TIMESTAMP AS DATE)AS EventTime,
       _experience.journeyOrchestration.stepEvents.journeyVersionID,
       _experie.journeyOrchestration.stepEvents.actionName,
       _experie.journeyOrchestration.stepEvents.actionID
       FROM journey_step_events
       位置
       _experie.journeyOrchepration.stepEvents.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&#39;和
       _experience.journeyOrchestration.stepEvents.actionID不為NULL AND
       TIMESTAMP > NOW()- INTERVAL &#39;2&#39; DAY
       按事件時間排序；
       「」
   
   >[!NOTE]
   >
   >獲取 `<journey version id>`參數，選擇相應的 [旅程版本](../building-journeys/journey-versions.md) 從 **[!UICONTROL Journey management]** > **[!UICONTROL Journeys]** 的子菜單。 行程版本ID顯示在Web瀏覽器中顯示的URL的末尾。
   >
   >![](assets/preset-bcc-action-id.png)

1. 運行此查詢以獲取過去2天內為特定用戶目標的特定消息生成的所有消息反饋事件（尤其是反饋狀態）:

       「」
       選擇
       _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID,
       _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID,
       時間戳AS EventTime,
       _experience.customerJourneyManagement.emailChannelContext.address AS收件人地址，
       _experience.customerjournemanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
       CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
       WHEN &#39;sent&#39; THEN &#39;Sent&#39;
       當「delay」時，然後「Retry」
       WHEN &#39;out_of_band&#39; THEN &#39;Bounce&#39;
       「bounce」時，「bounce」
       END AS FeedbackStatusCategory
       FROM cjm_message_feedback_event_dataset
       位置
       timestamp > now()- INTERVAL &#39;2&#39; day AND
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&#39;和
       _experience.customerJourneyManagement.messageExecution.journeyActionID = &#39;&lt;journey action=&quot;&quot; id=&quot;&quot;>&#39;和
       _experience.customerJourneyManagement.emailChannelContext.address = &#39;&lt;recipient email=&quot;&quot; address=&quot;&quot;>&quot;
       按事件時間排序；
       「」
   
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
