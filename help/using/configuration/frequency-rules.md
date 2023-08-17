---
solution: Journey Optimizer
product: journey optimizer
title: 頻率規則
description: 瞭解如何定義頻率規則
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 訊息，頻率，規則，壓力
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 13%

---

# 訊息頻率規則 {#frequency-rules}

[!DNL Journey Optimizer] 可讓您設定跨頻道規則，控制使用者收到訊息或進入歷程的頻率，這些規則會自動從訊息和動作中排除過度請求的設定檔。

例如，針對品牌，規則每個月不得傳送超過3則行銷訊息給客戶。 為此，您可以使用頻率規則，該規則將限制每月日曆期間根據一個或多個頻道傳送的訊息數。

>[!NOTE]
>
>訊息頻率規則與選擇退出管理不同，後者允許使用者取消訂閱以停止接收來自品牌的通訊。 [了解更多](../privacy/opt-out.md#opt-out-management)

➡️ [在影片中探索此功能](#video)

## 存取權規則 {#access-rules}

規則可從以下網址取得： **[!UICONTROL 管理]** > **[!UICONTROL 規則]** 功能表。 所有規則都會列出，並依修改日期排序。

使用篩選器圖示來篩選類別、狀態和/或頻道。 您也可以搜尋訊息標籤。

![](assets/message-rules-filter.png)

### 權限{#permissions-frequency-rules}

若要存取、建立、編輯或刪除訊息頻率規則，您必須擁有 **[!UICONTROL 管理頻率規則]** 許可權。

使用者具有 **[!UICONTROL 檢影片率規則]** 許可權可以檢視規則，但不能修改或刪除規則。

![](assets/message-rules-access.png)

進一步瞭解中的許可權 [本節](../administration/high-low-permissions.md).

## 建立規則 {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rules_category"
>title="選取訊息規則類別"
>abstract="啟動並套用至訊息時，和所選類別相符的所有頻率規則會自動應用至該訊息。目前只有行銷類別可用。"

>[!CONTEXTUALHELP]
>id="ajo_rules_capping"
>title="設定規則的上限"
>abstract="指定每月傳送到客戶設定檔的最大訊息數。頻率上限將依據每月的行事曆期間設定，並會在每個月的月初重設。"

>[!CONTEXTUALHELP]
>id="ajo_rules_channel"
>title="定義套用規則的管道"
>abstract="選取至少一個管道。上限會以總計數套用在所有管道上。"

若要建立新規則，請遵循下列步驟。

1. 存取 **[!UICONTROL 訊息頻率規則]** 清單，然後按一下 **[!UICONTROL 建立規則]**.

   ![](assets/message-rules-create.png)

1. 定義規則名稱。

   ![](assets/message-rules-details.png)

1. 選取訊息規則類別.

   >[!NOTE]
   >
   >目前僅限 **[!UICONTROL 行銷]** 類別可供使用。

1. 設定規則的上限，即每月可傳送至個別使用者設定檔的最大訊息數量。

   ![](assets/message-rules-capping.png)

   >[!NOTE]
   >
   >頻率上限是以日曆的每月週期為基礎。 它會在每個月的月初重設。

1. 選取您要用於此規則的管道： **[!UICONTROL 電子郵件]** 或 **[!UICONTROL 推播通知]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >您必須至少選取一個管道才能建立規則。

1. 如果您要將上限套用至所有選取的色版總數，請選取數個色版。

   例如，將上限設為15，然後選取電子郵件和推播通道。 如果設定檔已收到10封行銷電子郵件和5個行銷推播通知，則此設定檔將從任何行銷電子郵件或推播通知的下一個傳送中排除。

1. 按一下 **[!UICONTROL 另存為草稿]** 以確認建立規則。 您的訊息將新增至規則清單，並包含 **[!UICONTROL 草稿]** 狀態。

   ![](assets/message-rules-created.png)

## 啟用規則 {#activate-rule}

建立時，訊息頻率規則具有 **[!UICONTROL 草稿]** 狀態，且尚未影響任何訊息。 若要啟用，請按一下規則旁的省略符號，然後選取「 」 **[!UICONTROL 啟動]**.

![](assets/message-rules-activate.png)

啟用規則會影響規則在下次執行時套用的任何訊息。 瞭解如何 [將頻率規則套用至訊息](#apply-frequency-rule).

>[!NOTE]
>
>規則完整啟用最多可能需要10分鐘。 您不需要修改訊息或重新發佈歷程，規則就能生效。

若要停用訊息頻率規則，請按一下規則旁的省略符號，然後選取 **[!UICONTROL 停用]**.

![](assets/message-rules-deactivate.png)

規則的狀態將變更為 **[!UICONTROL 非使用中]** 而且規則不會套用於未來的訊息執行。 目前執行中的任何訊息都不會受到影響。

>[!NOTE]
>
>停用規則不會影響或重設個別設定檔的任何計數。

## 將頻率規則套用至訊息 {#apply-frequency-rule}

若要將頻率規則套用至訊息，請遵循下列步驟。

1. 建立 [歷程](../building-journeys/journey-gs.md)，選取您為規則定義的其中一個管道，以新增訊息。

1. 選取您為定義的類別 [您已建立的規則](#create-new-rule).

   ![](assets/journey-message-category.png)

   >[!NOTE]
   >
   >目前僅限 **[!UICONTROL 行銷]** 類別適用於訊息頻率規則。

1. 您可以按一下 **[!UICONTROL 頻率規則]** 連結以在新的索引標籤中檢影片率規則畫面。 [了解更多](#access-rules)

   所有符合所選類別和頻道的頻率規則都會自動套用至此訊息。

   >[!NOTE]
   >
   >所選類別為的訊息 **[!UICONTROL 異動]** 將不會根據頻率規則進行評估。

1. 您可以在以下位置檢視從傳送中排除的設定檔數： [全域報告](../reports/global-report.md)，以及 [即時報告](../reports/live-report.md)，其中會列出頻率規則，作為使用者從傳送中排除的可能原因。

>[!NOTE]
>
>數個規則可套用至相同的管道，但一旦達到較低上限，設定檔將從下一次傳送中排除。

## 範例：合併數個規則 {#frequency-rule-example}

您可以結合數個訊息頻率規則，如下列範例所述。

1. [建立規則](#create-new-rule) 已呼叫 *整體行銷上限*：

   * 選取電子郵件和推播通道。
   * 將上限設為12。

   ![](assets/message-rules-ex-overall-cap.png)

1. 若要進一步限制傳送給使用者的行銷型推播通知數量，請建立第二個規則，稱為 *推播行銷上限*：

   * 選取推播頻道。
   * 將上限設為4。

   ![](assets/message-rules-ex-push-cap.png)

1. 儲存並 [啟用](#activate-rule) 規則。

1. 建立電子郵件並選取 **[!UICONTROL 行銷]** 該訊息的類別。 [了解更多](../email/create-email.md)

1. 建立推播通知並選取 **[!UICONTROL 行銷]** 該訊息的類別。 [了解更多](../push/create-push.md)

在此案例中，個別設定檔：
* 每月最多可接收12則行銷訊息；
* 但是在收到4個推播通知後，便會從行銷推播通知中排除。

>[!NOTE]
>
>測試頻率規則時，建議使用新建立的 [測試設定檔](../audience/creating-test-profiles.md)，因為一旦達到設定檔的頻率上限，就無法在下個月之前重設計數器。 停用規則將允許限定設定檔接收訊息，但不會移除或刪除任何計數器增量。

## 操作說明影片 {#video}

瞭解如何建立、啟動、測試並報告頻率規則。 

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
