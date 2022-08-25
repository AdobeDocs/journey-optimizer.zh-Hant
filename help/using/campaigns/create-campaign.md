---
title: 建立行銷活動
description: 瞭解如何在 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 4%

---

# 建立行銷活動 {#create-campaign}

>[!NOTE]
>
>在建立新市場活動之前，請確保您有一個表面通道（即消息預設）和一個Adobe Experience Platform段可供使用。 在以下各節中瞭解更多資訊：
>
>* [建立頻道介面](../configuration/channel-surfaces.md)
>* [開始使用區段](../segment/about-segments.md)


## 配置市場活動 {#configure}

建立市場活動的步驟如下：

1. 訪問 **[!UICONTROL Campaigns]** 菜單，然後按一下 **[!UICONTROL Create campaign]**。

   ![](assets/create-campaign.png)

   >[!NOTE]
   >
   >您還可以複製現有的即時市場活動，以建立新市場活動。[了解更多](modify-stop-campaign.md#duplicate) <!-- check if only live campaigns-->

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date. Scheduled campaigns are aimed at sending **marketing** type messages.
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. API-triggered campaigns are aimed at sending **transactional** messages, i.e. messages sent out following an action performed by an individual: password reset, card abandonment etc. [Learn how to trigger a campaign using APIs](api-triggered-campaigns.md)-->

1. 在 **[!UICONTROL Actions]** ，選擇用於發送消息的通道和通道曲面，然後按一下 **[!UICONTROL Create]**。

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >下拉清單中只列出與市場活動類型（市場營銷或事務性）相容的渠道曲面。

1. 指定市場活動的標題和說明。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 在 **[!UICONTROL Actions]** 部分，配置要隨市場活動一起發送的消息：

   1. 按一下 **[!UICONTROL Edit content]** 按鈕，然後配置和設計消息內容。 [瞭解有關郵件的更多資訊](../messages/get-started-content.md)

      >[!NOTE]
      >
      >的 **[!UICONTROL Simulate content]** 按鈕，您可以使用test配置式預覽和test內容。 [了解更多](../design/preview.md)

   1. 內容準備好後，按一下箭頭返回市場活動建立螢幕。

      ![](assets/create-campaign-design.png)

   1. 在 **[!UICONTROL Actions tracking]** 部分，指定是否要跟蹤收件人對交貨的反應。

      市場活動一旦執行，便可以從市場活動報告訪問跟蹤結果。 [瞭解有關市場活動報告的更多資訊](../reports/campaign-global-report.md)

1. 定義目標受眾。 要執行此操作，請按一下 **[!UICONTROL Select audience]** 按鈕來顯示可用的Adobe Experience Platform段清單。 [瞭解有關網段的更多資訊](../segment/about-segments.md)

   <!-- NOTE For API-triggered campaigns, the audience needs to be set via API call. [Learn more](api-triggered-campaigns.md)-->

   在 **[!UICONTROL Identity namespace]** 欄位中，選擇要用於標識選定段中的個體的命名空間。 [瞭解有關命名空間的詳細資訊](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >該活動不會針對屬於在其不同身份中沒有選定身份（命名空間）的段的個人。

1. 配置市場活動的開始和結束日期。 預設情況下，市場活動配置為在手動激活市場活動後啟動，並在消息已發送一次時以暫停結束。

1. 此外，您還可以指定執行市場活動中配置的操作的頻率。

   <!-- NOTE For API-triggered campaigns, scheduling at a specific date and time with recurrence is not available as action is triggered via API. However, start and end date are relevant to ensure that, if an API call is made prior of after the window, then those get errored.-->

   ![](assets/create-campaign-schedule.png)

<!--1. If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

市場活動準備好後，您可以查看並發佈它(請參閱 [複查並激活市場活動](#review-activate))。

## 複查並激活市場活動 {#review-activate}

配置市場活動後，您需要先查看其參數和內容，然後再激活它。 要執行此操作，請依照下列步驟執行：

1. 在市場活動配置螢幕中，按一下 **[!UICONTROL Review to activate]** 顯示市場活動的摘要。

   匯總允許您在必要時修改市場活動，並檢查是否有任何參數不正確或缺失。

   >[!IMPORTANT]
   >
   >如果出現錯誤，您將無法激活市場活動。 在繼續之前解決錯誤。

   ![](assets/create-campaign-alerts.png)

1. 檢查市場活動配置是否正確，然後按一下 **[!UICONTROL Activate]**。

   ![](assets/create-campaign-review.png)

1. 該活動現已啟動，並 **[!UICONTROL Live]** 狀態(或 **[!UICONTROL Scheduled]**  )的正平方根。 [瞭解有關市場活動狀態的詳細資訊](get-started-with-campaigns.md#statuses)。 市場活動中配置的消息將立即或在指定日期執行。

   >[!NOTE]
   >
   >的 **[!UICONTROL Completed]** 狀態在市場活動激活3天後自動分配給市場活動，如果市場活動有定期執行，則在市場活動的結束日期自動分配。
   >
   >如果未指定結束日期，市場活動將保持「即時」狀態。 要更改市場活動，您需要手動停止市場活動。 [瞭解如何停止活動](modify-stop-campaign.md)

1. 激活市場活動後，您可以隨時通過開啟市場活動資訊來檢查其資訊。 該摘要允許您獲取有關目標配置檔案數量以及交付和失敗操作的統計資訊。

   您還可以通過按一下 **[!UICONTROL Reports]** 按鈕 [了解更多](../reports/campaign-global-report.md)

   ![](assets/create-campaign-summary.png)
