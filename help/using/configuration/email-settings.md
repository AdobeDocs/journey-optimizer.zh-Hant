---
title: 配置電子郵件設定
description: 瞭解如何在郵件預設級別配置電子郵件設定
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: 13fbe0583affb48269932134ea6bc214180903dd
workflow-type: tm+mt
source-wordcount: '2152'
ht-degree: 2%

---

# 配置電子郵件設定 {#email-settings}

在郵件預設配置的專用部分定義電子郵件設定。 瞭解如何在中建立消息預設 [此部分](message-presets.md)。

![](assets/preset-email.png)

## 電子郵件類型 {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="定義電子郵件類別"
>abstract="選擇使用此預設時將發送的消息類型：需要用戶同意的促銷消息的市場營銷，或非商業消息的事務性，這些消息也可以在特定上下文中發送到未訂閱的配置檔案。"

在 **電子郵件類型** 部分，選擇將使用預設發送的消息類型： **營銷** 或 **事務性**。

* 選擇 **營銷** 對於促銷消息：這些消息需要用戶同意。

* 選擇 **事務性** 非商業消息（例如，訂單確認、密碼重置通知或傳遞資訊）。

>[!CAUTION]
>
>**事務性** 消息可以發送到從營銷通信中取消訂閱的配置檔案。 這些消息只能在特定上下文中發送。

當 [建立消息](../messages/get-started-content.md#create-new-message)，必須選擇與您為消息選擇的類別匹配的有效消息預設。

## 子域和IP池 {#subdomains-and-ip-pools}

在 **子域和IP池詳細資訊** ，您必須：

1. 選擇要用於發送電子郵件的子域。 [了解更多](about-subdomain-delegation.md)

1. 選擇要與預設關聯的IP池。 [了解更多](ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

當所選IP池位於以下位置時，無法繼續建立預設 [版本](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** 狀態)，且從未與所選子域關聯。 否則，仍將使用IP池/子域關聯的最舊版本。 如果是這種情況，請將預設另存為草稿，並在IP池具有 **[!UICONTROL Success]** 狀態。

>[!NOTE]
>
>對於非生產環境，Adobe不建立現成的test子域，也不授予對共用發送IP池的訪問權限。 你需要 [委派自己的子域](delegate-subdomain.md) 並使用分配給您組織的池中的IP。

## 清單 — 取消訂閱 {#list-unsubscribe}

在 [選擇子域](#subdomains-and-ip-pools) 清單中， **[!UICONTROL Enable List-Unsubscribe]** 按鈕。

![](assets/preset-list-unsubscribe.png)

依預設，會啟用此選項。

如果保持啟用狀態，則取消訂閱連結將自動包含在電子郵件標題中，例如：

![](assets/preset-list-unsubscribe-header.png)

如果禁用此選項，則電子郵件標題中不會顯示取消訂閱連結。

取消訂閱連結包含兩個元素：

* 安 **取消訂閱電子郵件地址**，所有取消訂閱請求都發送到。

   在 [!DNL Journey Optimizer]，取消訂閱電子郵件地址是 **[!UICONTROL Mailto (unsubscribe)]** 在消息預設中顯示的地址，基於 [選定子域](#subdomains-and-ip-pools)。

   ![](assets/preset-list-unsubscribe-mailto.png)

* 的 **取消訂閱URL**，即登錄頁的URL，在取消訂閱後將重定向用戶。

   如果添加 [按一下選擇退出連結](../messages/consent.md#one-click-opt-out) 對於使用此預設建立的消息，取消訂閱URL將是為一次按一下選擇退出連結定義的URL。

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >如果您不在消息內容中添加一鍵退出選項連結，則不會向用戶顯示登錄頁。

瞭解有關將標題取消訂閱連結添加到郵件的詳細資訊 [此部分](../messages/consent.md#unsubscribe-header)。

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## 標題參數{#email-header}

在 **[!UICONTROL HEADER PARAMETERS]** 部分，輸入與使用該預設發送的郵件類型關聯的發件人姓名和電子郵件地址。

>[!CAUTION]
>
>電子郵件地址必須使用當前選定的 [委託子域](about-subdomain-delegation.md)。

* **[!UICONTROL Sender name]**:發件人的名稱，如您的品牌名稱。

* **[!UICONTROL Sender email]**:要用於通信的電子郵件地址。 例如，如果委派的子域是 *營銷.luma.com*，您可以使用 *contact@marketing.luma.com*。

* **[!UICONTROL Reply to (name)]**:收件人按一下 **答復** 按鈕。

* **[!UICONTROL Reply to (email)]**:收件人按一下 **答復** 按鈕。 必須使用在委派子域上定義的地址(例如， *reply@marketing.luma.com*)，否則將刪除電子郵件。

* **[!UICONTROL Error email]**:ISP在發送數天郵件（非同步綁定）後生成的所有錯誤都會在此地址上接收。

![](assets/preset-header.png)

>[!NOTE]
>
>地址必須以字母(A-Z)開頭，並且只能包含字母數字字元。 您還可以使用下划線 `_`，點`.` 連字元 `-` 字元。

### 轉發電子郵件 {#forward-email}

如果要轉發到特定電子郵件地址，則所有收到的電子郵件 [!DNL Journey Optimizer] 對於委派的子域，請與Adobe客戶服務部門聯繫。 您需要提供：

* 您選擇的轉發電子郵件地址。 請注意，轉發電子郵件地址域與委託給Adobe的任何子域不匹配。
* 沙盒名稱。
* 將使用轉發電子郵件（或「回復」）地址的預設名稱。
* 當前 **[!UICONTROL Reply to (email)]** 地址設定在預設級別。

>[!NOTE]
>
>每個子域只能有一個轉發電子郵件地址。 因此，如果多個預設使用相同的子域，則所有預設都必須使用相同的轉發電子郵件地址。

轉發電子郵件地址將通過Adobe設定。 這可能需要3到4天。

## 密件抄送電子郵件 {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="定義密件抄送電子郵件地址"
>abstract="您可以通過將已發送的電子郵件發送到密件抄送收件箱來保留其副本。 輸入您選擇的電子郵件地址，以便將發送的每封電子郵件盲目複製到此密件抄送地址。 此功能是選取性的。"

您可以發送由 [!DNL Journey Optimizer] 收件箱。 此可選功能允許您保留您發送給用戶的電子郵件通信副本，以便符合和/或存檔。 這對遞送收件人是不可見的。

### 啟用密件抄送電子郵件 {#enable-bcc}

啟用 **[!UICONTROL BCC email]** 選項，在「專用」欄位中輸入您選擇的電子郵件地址。 您可以以正確的格式指定任何外部地址，但委派子域上定義的電子郵件地址除外。 例如，如果委派的子域是 *營銷.luma.com*&#x200B;任何地址 *abc@marketing.luma.com* 禁止。

>[!NOTE]
>
>您只能定義一個密件抄送電子郵件地址。 確保BCC地址具有足夠的接收容量來儲存使用當前預設發送的所有電子郵件。

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

### Recommendations和限制 {#recommendations-limitations}

* 確保正確設定密件抄送電子郵件地址。 如果不是，您的客戶的個人身份資訊(PII)可能會發送到不需要的地址。

* 出於隱私原因，BCC電子郵件必須由能夠安全儲存個人身份資訊(PII)的存檔系統處理。

* 此功能可能在傳遞給收件人之前傳遞給BCC電子郵件地址，這可能導致發送BCC郵件，即使原始傳遞可能具有 [彈](../reports/suppression-list.md#delivery-failures)。

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* 如果開啟並按一下發送到密件抄送地址的電子郵件，則在開啟和按一下發送分析中的總次數中將考慮此問題，這可能會導致在 [報告](../reports/message-monitoring.md)。 同樣，將BCC電子郵件標籤為垃圾郵件會導致電子郵件落入收件箱的垃圾郵件資料夾中。

* 您用於密件抄送的收件箱應正確管理空間和傳遞。 如果收件箱返回回復，則可能無法接收某些電子郵件，因此無法存檔。

>[!CAUTION]
>
>避免在發送到密件抄送地址的電子郵件中按一下取消訂閱連結，因為您將立即取消訂閱相應收件人。

### GDPR合規性 {#gdpr-compliance}

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

### 密件抄送報告資料 {#bcc-reporting}

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

## 電子郵件重試參數 {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="調整重試時間段"
>abstract="當電子郵件由於臨時軟彈回錯誤而失敗時，將執行3.5天（84小時）的重試。 您可以調整此預設重試時間段，以更好地滿足您的需要。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/monitor-reputation/retries.html" text="關於重試"

您可以配置 **電子郵件重試參數**。

![](assets/preset-retry-parameters.png)

預設情況下， [重試時間](retries.md#retry-duration) 設定為84小時，但您可以調整此設定以更好地滿足您的需要。

必須在以下範圍內輸入整數值（以小時或分鐘為單位）:

* 對於市場營銷電子郵件，最短重試時間為6小時。
* 對於事務性電子郵件，最短重試時間為10分鐘。
* 對於這兩種電子郵件類型，最大重試時間為84小時（或5040分鐘）。

在中重試時瞭解更多資訊 [此部分](retries.md)。

## URL跟蹤 {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="URL跟蹤參數"
>abstract="使用此部分可自動將跟蹤參數附加到電子郵件內容中存在的市場活動URL。"

您可以使用 **[!UICONTROL URL Tracking Parameters]** 以衡量您跨渠道的營銷工作的成效。 此功能是選取性的。

本節中定義的參數將附加到電子郵件內容中包含的URL的末尾。 然後，您可以在Web分析工具(如Adobe Analytics或Google Analytics)中捕獲這些參數，並建立各種效能報告。

![](assets/preset-url-tracking.png)

建立消息預設時，會自動填充三個URL跟蹤參數。 您可以使用 **[!UICONTROL Add new parameter]** 按鈕

要配置URL跟蹤參數，可以直接在 **[!UICONTROL Name]** 和 **[!UICONTROL Value]** ，或導航到以下對象從預定義值清單中進行選擇：

* 行程屬性： **源ID**。 **源名稱**。 **源版本ID**
* 操作屬性： **操作ID**。 **操作名稱**
* Offer decisioning屬性： **服務ID**。 **優惠名稱**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>不選擇資料夾：確保瀏覽到必要的資料夾，並選擇一個配置檔案屬性作為跟蹤參數值。

以下是與Adobe Analytics和Google Analytics相容的URL的示例。

* Adobe Analytics相容URL: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* Google Analytics相容URL: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

>[!NOTE]
>
>可以將鍵入的文本值與選擇預定義的值合併。 每個 **[!UICONTROL Value]** 欄位總共最多可包含255個字元。
