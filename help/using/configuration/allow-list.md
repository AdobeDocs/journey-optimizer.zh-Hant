---
solution: Journey Optimizer
product: journey optimizer
title: 允許清單
description: 瞭解如何使用允許的清單
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
keywords: 允許的清單、清單、安全、配置
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 14%

---

# 允許清單 {#allow-list}

可以在 [沙坑](../administration/sandboxes.md) 級別。

通過此允許清單，您可以指定單個電子郵件地址或域，這些地址或域將是唯一有權接收您從特定沙箱發送的電子郵件的收件人或域。

>[!NOTE]
>
>此功能可用於生產和非生產砂箱。

例如，在非生產實例中，如果可能發生錯誤，則允許清單可確保您沒有風險將不需要的消息發送到真正的客戶地址，因此為測試目的提供了安全的環境。

此外，當允許的清單處於活動狀態但為空時，將不會傳出任何郵件。 因此，如果遇到某個主要問題，可使用此功能停止所有傳出通信 [!DNL Journey Optimizer] 直到你解決問題。 瞭解 [允許清單邏輯](#logic)。

>[!CAUTION]
>
>此功能僅適用於電子郵件通道。

## 訪問允許的清單 {#access-allowed-list}

要訪問允許的電子郵件地址和域的詳細清單，請轉到 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL 電子郵件配置]**，然後選擇 **[!UICONTROL 允許清單]**。

![](assets/allow-list-access.png)

>[!CAUTION]
>
>查看、導出和管理允許清單的權限限制為 [旅程管理員](../administration/ootb-product-profiles.md#journey-administrator)。 瞭解有關管理的更多資訊 [!DNL Journey Optimizer] 用戶在 [此部分](../administration/permissions-overview.md)。

要將允許的清單導出為CSV檔案，請選擇 **[!UICONTROL 下載CSV]** 按鈕

使用 **[!UICONTROL 刪除]** 按鈕，將選定控制項在Tab鍵次序中下移一個位置。

您可以搜索電子郵件地址或域，並在 **[!UICONTROL 地址類型]**。 選中後，可清除清單頂部顯示的過濾器。

![](assets/allowed-list-filtering-example.png)

## 激活允許的清單 {#enable-allow-list}

要激活允許的清單，請執行以下步驟。

1. 訪問  **[!UICONTROL 頻道]** > **[!UICONTROL 電子郵件配置]** > **[!UICONTROL 允許清單]** 的子菜單。

1. 選擇切換按鈕。

   ![](assets/allow-list-edit.png)

1. 選擇 **[!UICONTROL 激活允許清單]**。 允許的清單現在處於活動狀態。

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >激活允許清單後，該清單在您的行程和市場活動中有5分鐘的延遲。

當功能處於活動狀態時，將應用允許的清單邏輯。 請參閱[此章節](#logic)深入瞭解。

>[!NOTE]
>
>激活後，執行行程時，以及使用測試消息時，允許的清單功能會得到遵守 [證明](../email/preview.md#send-proofs) 並測試旅程 [test模式](../building-journeys/testing-the-journey.md)。

## 停用允許的清單 {#deactivate-allow-list}

要停用允許的清單，請執行以下步驟。

1. 訪問  **[!UICONTROL 頻道]** > **[!UICONTROL 電子郵件配置]** > **[!UICONTROL 允許清單]** 的子菜單。

1. 選擇切換按鈕。

   ![](assets/allow-list-edit-active.png)

1. 選擇 **[!UICONTROL 停用允許清單]**。 允許的清單不再處於活動狀態。

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >停用允許清單後，該清單在您的行程和市場活動中有5分鐘的延遲。

禁用功能時，允許的清單邏輯不適用。 請參閱[此章節](#logic)深入瞭解。

## 將實體添加到允許的清單 {#add-entities}

要將新電子郵件地址或域添加到特定沙盒的允許清單中，您可以 [手動填充清單](#manually-populate-list)，或使用 [API調用](#api-call-allowed-list)。

>[!NOTE]
>
>允許的清單最多可包含1,000個條目。

### 手動填充允許的清單 {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="將地址或網域新增到允許清單"
>abstract="您可以透過逐一選取來手動將新的電子郵件地址或網域新增到允許清單中。"

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="將地址或網域新增到允許清單"
>abstract="您可以透過逐一選取來手動將新的電子郵件地址或網域新增到允許清單中。"

您可以手動填充 [!DNL Journey Optimizer] 通過用戶介面添加電子郵件地址或域允許的清單。

>[!NOTE]
>
>一次只能添加一個電子郵件地址或域。

請依照下列步驟以執行此操作。

1. 選擇 **[!UICONTROL 添加電子郵件或域]** 按鈕

   ![](assets/allowed-list-add-email.png)

1. 選擇地址類型：**[!UICONTROL 電子郵件地址]**&#x200B;或&#x200B;**[!UICONTROL 網域地址]**。

1. 輸入要向其發送電子郵件的電子郵件地址或域。

   >[!NOTE]
   >
   >確定輸入有效的電子郵件地址 (例如 abc@company.com) 或網域 (例如 abc.company.com)。

1. 如果需要，請指定原因。

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >中允許包含32到126之間的所有ASCII字元 **[!UICONTROL 原因]** 的子菜單。 例如，完整清單可在[此頁面](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target="_blank"}中找到。

1. 按一下&#x200B;**[!UICONTROL 提交]**。

### 使用API調用添加實體 {#api-call-allowed-list}

要填充允許的清單，還可以使用 `ALLOWED` 值 `listType` 屬性。 例如：

![](assets/allow-list-api.png)

您可以執行 **添加**。 **刪除** 和 **獲取** 操作。

瞭解有關在中進行API調用的詳細資訊 [Adobe Experience PlatformAPI](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target="_blank"} 參考文檔。

## 下載允許的清單 {#download-allowed-list}

要將允許的清單導出為CSV檔案，請執行以下步驟：

1. 選擇 **[!UICONTROL 下載CSV]** 按鈕

   ![](assets/allowed-list-download-csv.png)

1. 等待檔案生成。

   ![](assets/allowed-list-download-generate.png)

   >[!NOTE]
   >
   >下載時間取決於檔案大小，即允許清單上的地址數。
   >
   >一次可以處理一個下載請求，用於給定沙盒。

1. 生成檔案後，您會收到通知。 按一下螢幕右上方的鈴表徵圖以顯示。

1. 按一下通知本身以下載檔案。

   ![](assets/allowed-list-download-notification.png)

   >[!NOTE]
   >
   >該連結的有效期為24小時。

## 允許的清單邏輯 {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="管理允許清單"
>abstract="啟動允許清單後，只有包含在允許清單中的收件者才能接收來自此沙箱的電子郵件訊息。停用時，所有收件者都會收到電子郵件。"

當允許清單為 [活動](#enable-allow-list)，應用以下邏輯：

* 如果允許的清單為 **空**，不會發送電子郵件。

* 如果實體為 **在允許的清單上**，而不是在禁止清單中，電子郵件將發送到相應的收件人。 但是，如果實體 [隱藏清單](../reports/suppression-list.md)，相應的收件人將不會收到電子郵件，原因是 **[!UICONTROL 隱藏]**。

* 如果實體為 **不在允許的清單中** （且不在禁止清單上），相應收件人將不會接收電子郵件，原因是 **[!UICONTROL 不允許]**。

>[!NOTE]
>
>配置檔案 **[!UICONTROL 不允許]** 在消息發送過程中，狀態被排除。 因此，當 **行程報告** 將顯示這些配置檔案在旅途中移動([讀取段](../building-journeys/read-segment.md) 和 [消息活動](../building-journeys/journeys-message.md)) **電子郵件報告** 不會把它們包括在 **[!UICONTROL 已發送]** 在發送電子郵件之前過濾掉度量。
>
>瞭解 [即時報告](../reports/live-report.md) 和 [全局報告](../reports/global-report.md)。

當允許清單為 [停用](#deactivate-allow-list)，您從當前沙箱發送的所有電子郵件都會發送到所有收件人（前提是這些郵件不在禁止清單中），包括真實的客戶地址。

## 排除報告 {#reporting}

當允許清單處於活動狀態時，可以檢索因不在允許清單中而從發送中排除的電子郵件地址或域。 要執行此操作，可使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"} 調用。

獲取 **電子郵件數** 由於收件人不在允許清單中而未發送的，請使用以下查詢：

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

獲取 **電子郵件地址清單** 由於收件人不在允許清單中而未發送的，請使用以下查詢：

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
