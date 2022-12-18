---
solution: Journey Optimizer
product: journey optimizer
title: 頻率規則
description: 了解如何定義頻率規則
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 3%

---

# 訊息頻率規則 {#frequency-rules}

[!DNL Journey Optimizer] 可讓您設定跨管道規則，自動從訊息和動作中排除過度請求的設定檔，以控制使用者接收訊息或進入歷程的頻率。

例如，您不希望您的品牌每月向其客戶傳送超過3則行銷訊息。

若要這麼做，您可以使用頻率規則來限制每月日曆期間根據一或多個通道傳送的訊息數量。

>[!NOTE]
>
>訊息頻率規則與選擇退出管理不同，選擇退出管理可讓使用者取消訂閱，而無法接收來自品牌的通訊。 [了解更多](../privacy/opt-out.md#opt-out-management)

➡️ [在影片中探索此功能](#video)

## 存取規則 {#access-rules}

規則可從 **[!UICONTROL 管理]** > **[!UICONTROL 規則]** 功能表。 會列出所有規則，依修改日期排序。

使用篩選圖示來篩選類別、狀態和/或通道。 您也可以在訊息標籤上搜尋。

![](assets/message-rules-filter.png)

### 權限{#permissions-frequency-rules}

若要存取、建立、編輯或刪除訊息頻率規則，您必須具備 **[!UICONTROL 管理頻率規則]** 權限。

具有 **[!UICONTROL 檢視頻率規則]** 權限可以檢視規則，但無法修改或刪除規則。

![](assets/message-rules-access.png)

進一步了解權限，請參閱 [本節](../administration/high-low-permissions.md).

## 建立規則 {#create-new-rule}

若要建立新規則，請遵循下列步驟。

1. 存取 **[!UICONTROL 訊息頻率規則]** 清單，然後按一下 **[!UICONTROL 建立規則]**.

   ![](assets/message-rules-create.png)

1. 定義規則名稱。

   ![](assets/message-rules-details.png)

1. 選取訊息規則類別。

   >[!NOTE]
   >
   >目前僅 **[!UICONTROL 行銷]** 類別。

1. 為規則設定上限，即每月可傳送至個別使用者設定檔的訊息數上限。

   ![](assets/message-rules-capping.png)

   >[!NOTE]
   >
   >頻率上限是根據每月日曆期間而定。 會在每月初重設。

1. 選取要用於此規則的管道： **[!UICONTROL 電子郵件]** 或 **[!UICONTROL 推播通知]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >您必須至少選取一個管道才能建立規則。

1. 如果要對所有選取的管道套用上限作為總計數，請選取數個管道。

   例如，將上限設定為15，然後選取電子郵件和推播通道。 如果設定檔已收到10封行銷電子郵件和5封行銷推播通知，則此設定檔將從任何行銷電子郵件或推播通知的下一次傳送中排除。

1. 按一下 **[!UICONTROL 另存為草稿]** 確認規則建立。 您的訊息會新增至規則清單，並搭配 **[!UICONTROL 草稿]** 狀態。

   ![](assets/message-rules-created.png)

## 啟動規則 {#activate-rule}

建立後，訊息頻率規則會將 **[!UICONTROL 草稿]** 狀態且尚未影響任何訊息。 若要啟用，請按一下規則旁的刪節號，然後選取 **[!UICONTROL 啟動]**.

![](assets/message-rules-activate.png)

啟用規則會影響規則套用至下次執行時的任何訊息。 了解如何 [將頻率規則應用於消息](#apply-frequency-rule).

>[!NOTE]
>
>完全啟動規則最多可能需要10分鐘。 您不需要修改訊息或重新發佈歷程，規則才會生效。

若要停用訊息頻率規則，請按一下規則旁的省略號，然後選取 **[!UICONTROL 停用]**.

![](assets/message-rules-deactivate.png)

規則的狀態會變更為 **[!UICONTROL 非作用中]** 並且該規則將不適用於將來的消息執行。 目前執行中的任何訊息將不受影響。

>[!NOTE]
>
>停用規則不會影響或重設個別設定檔上的任何計數。

## 將頻率規則套用至訊息 {#apply-frequency-rule}

若要將頻率規則套用至訊息，請遵循下列步驟。

1. 選取您為規則定義的其中一個管道，以建立訊息。

1. 選取您為 [已建立的規則](#create-new-rule).

   ![](assets/inline-message-category.png)

   >[!NOTE]
   >
   >目前僅 **[!UICONTROL 行銷]** 類別適用於訊息頻率規則。

   <!--
   1. You can click the **[!UICONTROL Frequency rule]** link to view the frequency rules that will apply for the selected category and channel(s). A new tab will open to display the matching message frequency rules.-->

1. 符合所選類別和通道的所有頻率規則將自動應用於此消息。

   >[!NOTE]
   >
   >訊息 <!--that do not have any selected category or messages -->其中選取的類別為 **[!UICONTROL 交易]** 不會根據頻率規則來評估。

   <!--Clicking the link out button next to the category selector will jump you over to the rules inventory screen to see which rules will be applied to the message.-->

1. 您可以在 [全域報表](../reports/global-report.md)，和 [即時報表](../reports/live-report.md)，其中頻率規則會列為將使用者排除在傳送之外的可能原因。

>[!NOTE]
>
>數個規則可套用至相同的管道，但一旦達到下限，設定檔就會從下次傳送中排除。

## 範例：組合多個規則 {#frequency-rule-example}

您可以結合數個訊息頻率規則，如下列範例所述。

1. [建立規則](#create-new-rule) 呼叫 *整體行銷限定*:

   * 選取「電子郵件」和「推播」通道。
   * 將上限設定為12。

   ![](assets/message-rules-ex-overall-cap.png)

1. 若要進一步限制使用者所傳送的行銷型推播通知數量，請建立第二個規則，稱為 *推播行銷上限*:

   * 選取「推播」通道。
   * 將上限設定為4。

   ![](assets/message-rules-ex-push-cap.png)

1. 儲存和 [啟用](#activate-rule) 規則。

1. 建立電子郵件並選取 **[!UICONTROL 行銷]** 類別。 [了解更多](../email/create-email.md)

1. 建立推播通知並選取 **[!UICONTROL 行銷]** 類別。 [了解更多](../push/create-push.md)

在此案例中，個別設定檔：
* 每月最多可接收12則行銷訊息；
* 但在收到4個推播通知後，就會從行銷推播通知中排除。

>[!NOTE]
>
>測試頻率規則時，建議使用新建立的 [測試設定檔](../segment/creating-test-profiles.md)，因為一旦達到設定檔的頻率上限，就要等到下個月才能重設計數器。 停用規則將允許有上限的設定檔接收訊息，但不會移除或刪除任何計數器增量。

## 作法影片 {#video}

瞭解如何建立、啟動、測試並報告頻率規則。 

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
