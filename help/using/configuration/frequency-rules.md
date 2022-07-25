---
title: 頻率規則
description: 瞭解如何定義頻率規則
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 3%

---

# 消息頻率規則 {#frequency-rules}

[!DNL Journey Optimizer] 允許您通過設定跨通道規則來控制用戶接收消息或進入行程的頻率，這些規則將自動從消息和操作中排除過度請求的配置檔案。

例如，您不希望您的品牌每月向其客戶發送3封以上的營銷資訊。

為此，可以使用頻率規則，該規則將限制在每月日曆期間基於一個或多個渠道發送的消息數。

>[!NOTE]
>
>消息頻率規則不同於選擇退出管理，它允許用戶取消訂閱從品牌接收通信。 [了解更多](../messages/consent.md#opt-out-management)

➡️ [在影片中探索此功能](#video)

## 訪問規則 {#access-rules}

規則可從 **[!UICONTROL Administration]** > **[!UICONTROL Rules]** 的子菜單。 將列出所有規則，並按修改日期排序。

使用篩選器表徵圖可以篩選類別、狀態和/或通道。 您也可以在消息標籤上搜索。

![](assets/message-rules-filter.png)

### 權限{#permissions-frequency-rules}

要訪問、建立、編輯或刪除消息頻率規則，必須 **[!UICONTROL Manage frequency rules]** 權限。

具有 **[!UICONTROL View frequency rules]** 權限可以查看規則，但不能修改或刪除規則。

![](assets/message-rules-access.png)

瞭解有關中權限的詳細資訊 [此部分](../administration/high-low-permissions.md)。

## 建立規則 {#create-new-rule}

要建立新規則，請執行以下步驟。

1. 訪問 **[!UICONTROL Message frequency rules]** 清單，然後按一下 **[!UICONTROL Create rule]**。

   ![](assets/message-rules-create.png)

1. 定義規則名稱。

   ![](assets/message-rules-details.png)

1. 選擇消息規則類別。

   >[!NOTE]
   >
   >當前僅 **[!UICONTROL Marketing]** 的下界。

1. 設定規則的上限設定，即每月可發送到單個用戶配置檔案的最大消息數。

   ![](assets/message-rules-capping.png)

   >[!NOTE]
   >
   >頻率上限基於月曆期間。 在每月初重置。

1. 選擇要用於此規則的通道： **[!UICONTROL Email]** 或 **[!UICONTROL Push notification]**。

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >必須至少選擇一個通道才能建立規則。

1. 如果要將覆蓋覆蓋覆蓋覆蓋覆蓋覆蓋覆蓋所有選定通道作為總計數，請選擇多個通道。

   例如，將上限設定為15，然後同時選擇電子郵件和推送通道。 如果某個配置檔案已收到10封營銷電子郵件和5封營銷推送通知，則此配置檔案將從任何營銷電子郵件或推送通知的下一次交付中排除。

1. 按一下 **[!UICONTROL Save as draft]** 確認規則建立。 您的消息將添加到規則清單， **[!UICONTROL Draft]** 狀態。

   ![](assets/message-rules-created.png)

## 激活規則 {#activate-rule}

建立時，消息頻率規則 **[!UICONTROL Draft]** 狀態，尚未影響任何消息。 要啟用它，請按一下規則旁邊的省略號並選擇 **[!UICONTROL Activate]**。

![](assets/message-rules-activate.png)

激活規則將影響其應用於其下次執行的任何消息。 瞭解如何 [將頻率規則應用於消息](#apply-frequency-rule)。

>[!NOTE]
>
>完全激活規則可能需要10分鐘。 您無需修改消息或重新發佈行程，規則即可生效。

要取消激活消息頻率規則，請按一下該規則旁邊的省略號，然後選擇 **[!UICONTROL Deactivate]**。

![](assets/message-rules-deactivate.png)

規則的狀態將更改為 **[!UICONTROL Inactive]** 並且該規則不適用於將來的消息執行。 當前正在執行的任何消息都將不受影響。

>[!NOTE]
>
>停用規則不會影響或重置單個配置檔案上的任何計數。

## 將頻率規則應用於消息 {#apply-frequency-rule}

要將頻率規則應用於消息，請執行以下步驟。

1. [建立消息](../messages/get-started-content.md#create-new-message) 通過選擇為規則定義的通道之一。

1. 選擇為 [已建立的規則](#create-new-rule)。

   ![](assets/inline-message-category.png)

   >[!NOTE]
   >
   >當前僅 **[!UICONTROL Marketing]** 類別可用於消息頻率規則。

   <!--
   1. You can click the **[!UICONTROL Frequency rule]** link to view the frequency rules that will apply for the selected category and channel(s). A new tab will open to display the matching message frequency rules.-->

1. 所有與所選類別和通道匹配的頻率規則將自動應用於此消息。

   >[!NOTE]
   >
   >選擇類別的消息 **[!UICONTROL Transactional]** 不會根據頻率規則進行評估。

1. 您可以在中查看從交貨中排除的配置檔案數 [全局報告](../reports/global-report.md)的 [即時報告](../reports/live-report.md)，其中頻率規則將作為用戶從傳遞中排除的可能原因列出。

>[!NOTE]
>
>幾個規則可以應用於同一渠道，但一旦達到下限，配置檔案將從下次交貨中排除。

## 示例：組合若干規則 {#frequency-rule-example}

您可以組合多種消息頻率規則，如下例中所述。

1. [建立規則](#create-new-rule) 調用 *總體營銷上限*:

   * 選擇「電子郵件」和「推送」通道。
   * 將上限設定為12。

   ![](assets/message-rules-ex-overall-cap.png)

1. 要進一步限制發送用戶的基於市場營銷的推送通知的數量，請建立稱為 *推式營銷上限*:

   * 選擇「推送通道」。
   * 將上限設定為4。

   ![](assets/message-rules-ex-push-cap.png)

1. 保存和 [激活](#activate-rule) 規則。

1. 建立電子郵件並選擇 **[!UICONTROL Marketing]** 的下界。 [了解更多](../messages/get-started-content.md#create-new-message)

1. 建立推送通知並選擇 **[!UICONTROL Marketing]** 的下界。 [了解更多](../messages/get-started-content.md#create-new-message)

在此方案中，單個配置檔案：
* 每月最多可收到12條營銷資訊；
* 但在收到4個推送通知後，將不再提供營銷推送通知。

>[!NOTE]
>
>測試頻率規則時，建議使用新建立的 [test配置檔案](../segment/creating-test-profiles.md)，因為一旦達到配置檔案的頻率上限，則直到下個月才能重置計數器。 停用規則將允許封閉配置檔案接收消息，但不會刪除或刪除任何計數器增量。

## How-to視頻 {#video}

瞭解如何建立、啟動、測試並報告頻率規則。 

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
