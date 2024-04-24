---
solution: Journey Optimizer
product: journey optimizer
title: 業務規則
description: 瞭解如何建立和套用商業規則
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: 訊息，頻率，規則，壓力
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: c1eef06b0edc4e1bcd1b145f8f822295924b205c
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 10%

---

# 業務規則 {#business-rules}

>[!AVAILABILITY]
>
>商業規則目前僅供特定使用者使用，作為測試版提供。

[!DNL Journey Optimizer] 可讓您設定跨頻道規則，控制使用者接收訊息的頻率，這些規則會自動從訊息和動作中排除過度請求的設定檔。

例如，對於品牌，規則可以是：每月向其客戶傳送的行銷訊息不能超過4則。 為此，您可以使用頻率規則，該規則將限制每月日曆期間根據一個或多個頻道傳送的訊息數。

透過建立不同的規則集以提升精細度， [!DNL Journey Optimizer] 可讓您將頻率上限套用至不同型別的行銷通訊。 例如，您可以建立規則集以限制 **促銷通訊** 傳送給您的客戶，並建立另一個規則集以限制 **電子報** 已傳送給他們。

>[!NOTE]
>
>商業規則與選擇退出管理不同，後者允許使用者取消訂閱以停止接收來自品牌的通訊。 [了解更多](../privacy/opt-out.md#opt-out-management)

## 存取規則集 {#access-rule-sets}

規則集可從 **[!UICONTROL 管理]** > **[!UICONTROL 商業規則（測試版）]** 功能表。 所有規則都會列出，並按建立日期排序。

![](assets/rule-sets-list.png)

按一下規則集名稱，即可檢視及編輯其內容。 該規則集中包含的所有規則都會列出。

右上方的內容功能表可讓您：

* 編輯規則集的名稱和說明
* 啟動規則集 —  [瞭解更多](#activate-rule)
* 刪除規則集

![](assets/rule-set-example.png)

對於規則集中的每個規則， **[!UICONTROL 更多動作]** 按鈕可讓您：

* 編輯規則
* 啟用規則 [瞭解更多](#activate-rule)
* 刪除規則

![](assets/rule-set-example-rules.png)

<!--### Permissions{#permissions-frequency-rules}

To access, create, edit or delete message frequency rules, you must have the **[!UICONTROL Manage frequency rules]** permission. 

Users with the **[!UICONTROL View frequency rules]** permission are able to view rules, but not to modify or delete them.

![](assets/message-rules-access.png)

Learn more about permissions in [this section](../administration/high-low-permissions.md).-->

## 建立規則集 {#create-rule-set}

若要建立規則集，請遵循下列步驟。

1. 存取 **[!UICONTROL 規則集]** 清單，然後按一下 **[!UICONTROL 建立規則集]**.

   ![](assets/rule-sets-create-button.png)

1. 定義規則集名稱，視需要新增說明，然後按一下 **[!UICONTROL 儲存]**.

   ![](assets/rule-sets-create.png)

   >[!NOTE]
   >
   >規則集名稱必須是唯一的。

1. 現在您可以 [定義規則](#create-new-rule) 您想要新增至此規則集，以及 [啟用](#activate-rule) it.

   >[!NOTE]
   >
   >請確定您要套用至訊息的所有規則也在規則集中啟動。

## 建立規則 {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_category"
>title="選取訊息規則類別"
>abstract="啟動並套用至訊息時，和所選類別相符的所有頻率規則會自動應用至該訊息。目前只有行銷類別可用。"

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_capping"
>title="設定規則的上限"
>abstract="指定在所選時間範圍內傳送至客戶設定檔的最大訊息數量。頻率上限會以所選的行事曆期間為基礎，並會在對應的時間段開始時重設。 "

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_channel"
>title="定義套用規則的管道"
>abstract="選取至少一個管道。上限會以總計數套用在所有管道上。"

若要將規則新增至規則集，請遵循下列步驟。

1. 從您剛建立的規則集中，按一下 **[!UICONTROL 新增規則]**.

   ![](assets/rule-sets-create-rule-button.png)

1. 定義規則名稱。

   >[!NOTE]
   >
   >規則集名稱必須是唯一的。

1. 選取訊息規則類別。

   >[!NOTE]
   >
   >目前僅限 **[!UICONTROL 行銷]** 類別可供使用。

1. 從 **[!UICONTROL 持續時間]** 下拉式清單，選取要套用之上限的時間範圍。 [了解更多](#frequency-cap)

1. 設定規則的上限，代表根據您上述選擇，每個月、每週或每天可傳送至個別使用者設定檔的最大訊息數量。

1. 選取您要用於此規則的管道： **[!UICONTROL 電子郵件]**， **[!UICONTROL 簡訊]**， **[!UICONTROL 推播通知]** 或 **[!UICONTROL 直接郵件]**.

   ![](assets/rule-set-channels.png)

   >[!NOTE]
   >
   >您必須至少選取一個管道才能建立規則。

1. 如果您要將上限套用至所有選取的色版總數，請選取數個色版。

   例如，將上限設為5，然後選取電子郵件和簡訊頻道。 如果設定檔在選定期間內已收到3封行銷電子郵件和2封行銷簡訊，則會在下次傳送行銷電子郵件或簡訊時排除此設定檔。

1. 按一下 **[!UICONTROL 儲存]** 以確認建立規則。 您的訊息將新增至規則集，並使用 **[!UICONTROL 草稿]** 狀態。

   ![](assets/rule-set-rule-created.png)

1. 重複上述步驟，視需求將任意數量的規則新增至規則集。

現在，您必須先啟用每個規則，才能將其套用至任何訊息。 [了解更多](#activate-rule)

>[!NOTE]
>
>確定規則集也已啟動，以便能夠在您的訊息中選取它。

### 頻率上限 {#frequency-cap}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_duration"
>title="選取訊息規則類別"
>abstract="啟動並套用至訊息時，和所選類別相符的所有頻率規則會自動應用至該訊息。目前只有行銷類別可用。"

從 **[!UICONTROL 持續時間]** 下拉式清單，選取是否要每月、每週或每日套用上限。

頻率上限是根據所選的日曆期間。 它會在對應的時間範圍開始時重設。

![](assets/rule-set-capping-duration.png)

每個期間的計數器到期日如下：

* **[!UICONTROL 每月]**：頻率上限有效期至當月最後一天23:59:59 UTC. 例如，1月的每月到期日為01-31 23:59:59 UTC.

* **[!UICONTROL 每週]**：頻率上限有效期到星期六23日:59:當週的59 UTC作為行事曆周從星期日開始。 無論規則建立與否，有效期都相同。 例如，如果規則是在星期四建立，則此規則有效期至星期六的23日:59:59.

* **[!UICONTROL 每日]**：每日頻率上限對該日有效，直到23:59:59 UTC並在第二天開始時重設為0。

### 每日頻率上限 {#daily-frequency-cap}

>[!CAUTION]
>
>為確保每日頻率限定規則的準確性，請使用 [串流細分](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"} 為必填欄位。 進一步瞭解中的對象評估方法 [本節](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

任何區段大小，每小時最多6,000萬則訊息<!--not clear-->，請確定您的行銷活動至少相隔2小時。


<!-- Journey example:

* If customer sets a Daily rule under the Global Ruleset for email <= 2/day:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for noon)
   * Journey 789 (scheduled for 1 pm)

   In this example, the Daily Frequency cap will not guarantee <= 2/day. The rule will only be guaranteed when Journeys are at least 2 hours apart:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for 2 pm)
   * Journey 789 (scheduled for 4 pm)-->

例如，如果您在電子郵件頻道的規則集下設定每日規則，且規則集小於或等於2天，以及如果您建立下列行銷活動：
* 行銷活動A （排程在中午）
* 行銷活動A （排程在下午3點）
* 行銷活動B （排程在中午1點）

此設定無法運作，原因有二：
* 由於行銷活動不會相隔2小時，因此無法保證每日頻率上限。
* 為了利用每日上限，我們不建議一天內多次排程相同的行銷活動。

每日頻率上限應遵循以下範例：
* 行銷活動A （排程在中午）
* 行銷活動B （排程在中午2點）

<!--* To use the Daily Cap with a Journey, customers can use either an Event Triggered Journey or an Audience Qualified Journey. If customers wish to use the Daily Cap with a Read Audience Journey, they should use a Campaign instead and associate a Local Ruleset with the campaign, following the example given above.-->

## 啟用規則和規則集 {#activate-rule}

建立時，規則具有 **[!UICONTROL 草稿]** 狀態，且尚未影響任何訊息。 若要啟用此功能，請按一下 **[!UICONTROL 更多動作]** 按鈕並選取 **[!UICONTROL 啟動]**.

![](assets/rule-set-activate-rule.png)

您也必須啟用規則集，才能在行銷活動/歷程中存取它，並將其套用至您的訊息。

![](assets/rule-set-activate-set.png)

啟用規則集將會影響在下次執行時套用到的任何訊息。 瞭解如何 [套用規則集至訊息](#apply-rule-set).

>[!NOTE]
>
>完全啟用規則或規則集最多可能需要10分鐘。 您不需要修改訊息或重新發佈歷程，規則就能生效。

<!--Currently, once a rule set is activated, no more rules can be added to that rule set.-->

## 停用規則和規則集 {#deactivate-rule}

若要停用規則或規則集，請按一下 **[!UICONTROL 更多動作]** 按鈕並選取 **[!UICONTROL 停用]**.

![](assets/rule-set-inactive-rule.png)

其狀態將變更為 **[!UICONTROL 非使用中]** 而且規則不會套用於未來的訊息執行。 目前執行中的任何訊息都不會受到影響。

>[!NOTE]
>
>停用規則或規則集不會影響或重設個別設定檔的任何計數。

## 將頻率規則套用至訊息 {#apply-frequency-rule}

若要將頻率規則套用至訊息，請遵循下列步驟。

1. 建立 [行銷活動](../campaigns/create-campaign.md)，選取您為規則集定義的其中一個管道，並編輯訊息內容。

1. 在內容版本畫面中，按一下 **[!UICONTROL 新增商業規則]** 按鈕。

1. 選取 [您已建立的規則集](#create-rule-set).

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >僅限 [已啟用](#activate-rule) 規則集會顯示在清單中。

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. 您可以在以下位置檢視從傳送中排除的設定檔數： [全域報告](../reports/global-report.md)，以及 [即時報告](../reports/live-report.md)，其中會列出頻率規則，作為使用者從傳送中排除的可能原因。

>[!NOTE]
>
>數個規則可套用至相同的管道，但一旦達到較低上限，設定檔將從下一次傳送中排除。

<!--
## Example: combine several rules {#frequency-rule-example}

You can combine several message frequency rules, such as described in the example below.

1. [Create a rule](#create-new-rule) called *Overall Marketing Capping*:

   * Select all channels.
   * Set capping to 12 monthly.

   ![](assets/message-rules-ex-overall-cap.png)

1. To further restrict the number of marketing-based push notifications that a user is sent, create a second rule called *Push Marketing Cap*:

   * Select Push channel.
   * Set capping to 4 monthly.

   ![](assets/message-rules-ex-push-cap.png)

1. Save and [activate](#activate-rule) the rule.

1. [Create a message](../building-journeys/journeys-message.md) for every channel you want to communicate through and select the **[!UICONTROL Marketing]** category for each message. [Learn how to apply a frequency rule](#apply-frequency-rule)

   ![](assets/journey-message-category.png)

In this scenario, an individual profile:
* can receive up to 12 marketing messages per month;
* but will be excluded from marketing push notifications after they have received 4 push notifications.-->

測試頻率規則時，建議使用新建立的 [測試設定檔](../audience/creating-test-profiles.md)，因為一旦達到設定檔的頻率上限，就無法在下一個週期前重設計數器。 停用規則將允許限定設定檔接收訊息，但不會移除或刪除任何計數器增量。

