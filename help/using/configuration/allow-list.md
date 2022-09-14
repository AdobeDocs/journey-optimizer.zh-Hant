---
title: 允許清單
description: 了解如何使用允許的清單。
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: e81e21f714a3c5450defa1129e1e2b9969dc1de7
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 2%

---

# 允許清單 {#allow-list}

您可以在 [沙箱](../administration/sandboxes.md) 層級。

此允許清單可讓您指定個別電子郵件地址或網域，這些地址或網域將是唯一獲授權接收您從特定沙箱傳送之電子郵件的收件者或網域。

>[!NOTE]
>
>生產沙箱和非生產沙箱均提供此功能。

例如，在可能發生錯誤的非生產實例上，允許的清單可確保您沒有將不需要的消息發送到真實客戶地址的風險，因此，為測試目的提供了安全的環境。

此外，當允許的清單處於活動狀態但為空時，不會傳出任何郵件。 因此，如果您遇到一些重大問題，可以使用此功能來停止 [!DNL Journey Optimizer] 直到你解決問題。 深入了解 [允許的清單邏輯](#logic).

>[!CAUTION]
>
>此功能僅適用於電子郵件通道。

## 訪問允許的清單 {#access-allowed-list}

若要存取允許的電子郵件地址和網域的詳細清單，請前往 **[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL 電子郵件設定]**，然後選取 **[!UICONTROL 允許的清單]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>檢視、匯出及管理允許清單的權限限制為 [歷程管理員](../administration/ootb-product-profiles.md#journey-administrator). 深入了解管理 [!DNL Journey Optimizer] 中的使用者存取權限 [本節](../administration/permissions-overview.md).

若要將允許的清單匯出為CSV檔案，請選取 **[!UICONTROL 下載CSV]** 按鈕。

使用 **[!UICONTROL 刪除]** 按鈕以永久刪除條目。

您可以搜尋電子郵件地址或網域，並篩選 **[!UICONTROL 地址類型]**. 選取後，您可以清除顯示在清單頂端的篩選器。

![](assets/allowed-list-filtering-example.png)

## 啟動允許的清單 {#enable-allow-list}

要激活允許的清單，請執行以下步驟。

1. 存取  **[!UICONTROL 管道]** > **[!UICONTROL 電子郵件設定]** > **[!UICONTROL 允許清單]** 功能表。

1. 按一下 **[!UICONTROL 已停用]**.

   ![](assets/allow-list-edit.png)

1. 選擇 **[!UICONTROL 激活允許清單]**. 允許的清單現在處於活動狀態。

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >啟用允許清單後，延遲5分鐘才會在歷程和行銷活動中生效。

當功能啟用時，會套用允許的清單邏輯。 請參閱[此章節](#logic)深入瞭解。

>[!NOTE]
>
>啟動後，執行歷程時，以及透過測試訊息時，都會採用允許的清單功能 [校樣](../design/preview.md#send-proofs) 和使用 [測試模式](../building-journeys/testing-the-journey.md).

## 停用允許的清單 {#deactivate-allow-list}

要停用允許的清單，請執行以下步驟。

1. 存取  **[!UICONTROL 管道]** > **[!UICONTROL 電子郵件設定]** > **[!UICONTROL 允許清單]** 功能表。

1. 按一下 **[!UICONTROL 作用中]**.

   ![](assets/allow-list-edit-active.png)

1. 選擇 **[!UICONTROL 停用允許清單]**. 允許的清單不再處於活動狀態。

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >停用允許清單後，延遲5分鐘才會在歷程和行銷活動中生效。

停用功能時，不會套用允許的清單邏輯。 請參閱[此章節](#logic)深入瞭解。

## 將實體新增至允許的清單 {#add-entities}

若要將新電子郵件地址或網域新增至特定沙箱的允許清單，您可以 [手動填入清單](#manually-populate-list)，或使用 [API呼叫](#api-call-allowed-list).

>[!NOTE]
>
>允許的清單最多可包含1,000個項目。

### 手動填入允許的清單 {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="將地址或域添加到允許的清單"
>abstract="您可以逐一選取新電子郵件地址或網域，手動將其新增至允許清單。"

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="將地址或域添加到允許的清單"
>abstract="您可以逐一選取新電子郵件地址或網域，手動將其新增至允許清單。"

您可以手動填入 [!DNL Journey Optimizer] 允許清單，方法是透過使用者介面新增電子郵件地址或網域。

>[!NOTE]
>
>一次只能添加一個電子郵件地址或域。

請依照下列步驟以執行此操作。

1. 選取 **[!UICONTROL 新增電子郵件或網域]** 按鈕。

   ![](assets/allowed-list-add-email.png)

1. 選擇地址類型： **[!UICONTROL 電子郵件地址]** 或 **[!UICONTROL 網域位址]**.

1. 輸入要向其發送電子郵件的電子郵件地址或域。

   >[!NOTE]
   >
   >請務必輸入有效的電子郵件地址(如abc@company.com)或網域（如abc.company.com）。

1. 視需要指定原因。

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >在 **[!UICONTROL 原因]** 欄位。 您可以在 [本頁](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters)例如{target=&quot;_blank&quot;}。

1. 按一下&#x200B;**[!UICONTROL 提交]**。

### 使用API呼叫新增實體 {#api-call-allowed-list}

若要填入允許的清單，您也可以使用 `ALLOWED` 值 `listType` 屬性。 例如：

![](assets/allow-list-api.png)

您可以執行 **新增**, **刪除** 和 **取得** 操作。

進一步了解在 [Adobe Experience Platform API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target=&quot;_blank&quot;}參考檔案。

## 允許的清單邏輯 {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="管理允許的清單"
>abstract="啟用允許清單時，只有包含在允許清單中的收件者才會收到來自此沙箱的電子郵件訊息。"

允許的清單為 [活動](#enable-allow-list)，則套用下列邏輯：

* 如果允許的清單為 **空白**，則不會傳送任何電子郵件。

* 如果實體為 **在允許的清單上**，而不是在取消清單中，則會將電子郵件傳送給對應的收件者。 不過，如果實體同時位於 [隱藏清單](../reports/suppression-list.md)，則對應的收件者將不會收到電子郵件，原因為 **[!UICONTROL 隱藏]**.

* 如果實體為 **不在允許的清單上** （且不在隱藏清單中），對應的收件者將不會收到電子郵件，原因是 **[!UICONTROL 不允許]**.

>[!NOTE]
>
>具有 **[!UICONTROL 不允許]** 在訊息傳送程式期間會排除狀態。 因此，若 **歷程報表** 會將這些設定檔顯示為已在歷程中移動([讀取區段](../building-journeys/read-segment.md) 和 [訊息活動](../building-journeys/journeys-message.md)), **電子郵件報表** 不會將其納入 **[!UICONTROL 已傳送]** 量度，因為在傳送電子郵件前會先將量度篩選掉。
>
>深入了解 [即時報表](../reports/live-report.md) 和 [全域報表](../reports/global-report.md).

允許的清單為 [停用](#deactivate-allow-list)，您從目前沙箱傳送的所有電子郵件都會傳送給所有收件者（前提是他們不在隱藏清單中），包括真實的客戶地址。

## 排除報表 {#reporting}

當允許的清單處於活動狀態時，您可以檢索因不在允許清單中而從發送中排除的電子郵件地址或域。 若要這麼做，您可以使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}以進行下方的API呼叫。

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
