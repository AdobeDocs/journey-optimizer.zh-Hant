---
title: 建立行銷活動
description: 瞭解如何在 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6177a33edeb3b8381c3eb5609762b4d974dc93e3
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 建立行銷活動 {#create-campaign}

>[!NOTE]
>
>在建立新市場活動之前，請確保您已預置了消息，並且已準備好使用Adobe Experience Platform段。 在以下各節中瞭解更多資訊：
>
>* [建立訊息預設集](../configuration/message-presets.md)
>* [開始使用區段](../segment/about-segments.md)


## 配置市場活動 {#configure}

建立市場活動的步驟如下：

1. 訪問 **[!UICONTROL Campaigns]** 菜單，然後按一下 **[!UICONTROL Create campaign]**。

   ![](assets/create-campaign.png)

1. 在 **[!UICONTROL Properties]** 部分，指定要執行市場活動的時間：

   * **[!UICONTROL Scheduled]**:立即或在指定日期執行市場活動。 計畫的市場活動旨在發送 **營銷** 鍵入消息。
   * **[!UICONTROL API-triggered]**:使用API調用執行市場活動。 API觸發的市場活動旨在發送 **事務** 消息，即在個人執行的操作後發送的消息：密碼重置、卡棄用等。 [瞭解如何使用API觸發市場活動](api-triggered-campaigns.md)

1. 在 **[!UICONTROL Actions]** 選擇用於發送消息的通道和消息面（即消息預設），然後按一下 **[!UICONTROL Create]**。

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >下拉清單中只列出與市場活動類型（市場營銷或事務性）相容的消息曲面。

1. 指定市場活動的標題和說明。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 在 **[!UICONTROL Actions]** 部分，配置要隨市場活動一起發送的消息：

   1. 按一下 **[!UICONTROL Edit content]** 按鈕，然後配置和設計消息。 [瞭解如何配置消息](../messages/get-started-content.md)。

      內容準備好後，按一下箭頭返回市場活動建立螢幕。

      ![](assets/create-campaign-design.png)

   1. 在 **[!UICONTROL Actions tracking]** 部分，指定是否要跟蹤收件人對交貨的反應。

      市場活動一旦執行，便可以從市場活動報告訪問跟蹤結果。 [瞭解有關市場活動報告的更多資訊](campaign-global-report.md)

1. 定義目標受眾。 要執行此操作，請按一下 **[!UICONTROL Select audience]** 按鈕來顯示可用的Adobe Experience Platform段清單。 [瞭解有關網段的更多資訊](../segment/about-segments.md)

   >[!NOTE]
   >
   >對於API觸發的市場活動，需要通過API調用來設定受眾。 [了解更多](api-triggered-campaigns.md)

   在 **[!UICONTROL Identity namespace]** 欄位中，選擇要用於標識選定段中的個體的命名空間。 [瞭解有關命名空間的詳細資訊](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >該活動不會針對屬於在其不同身份中沒有選定身份（命名空間）的段的個人。

1. 配置市場活動的開始和結束日期。 預設情況下，市場活動配置為在手動激活市場活動後啟動，並在消息已發送一次時以暫停結束。

1. 此外，您還可以指定執行市場活動中配置的操作的頻率。

   >[!NOTE]
   >
   >對於API觸發的市場活動，由於通過API觸發活動，因此在特定日期和時間進行具有重複的計畫不可用。 但是，開始和結束日期與確保在窗口之後進行API調用之前，這些調用將出錯。

   ![](assets/create-campaign-schedule.png)

1. 如果要建立API觸發的市場活動， **[!UICONTROL cURL request]** 部分允許您檢索 **[!UICONTROL Campaign ID]** 在API調用中使用。 [了解更多](api-triggered-campaigns.md)

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

1. 該活動現已啟動，並 **[!UICONTROL Live]** 狀態(或 **[!UICONTROL Scheduled]**  )的正平方根。 [瞭解有關市場活動狀態的詳細資訊](get-started-with-campaigns.md#statuses)

   市場活動中配置的消息將立即或在指定日期執行。

   >[!NOTE]
   >
   >一旦激活了市場活動，即使在消息執行後，它仍將保持「即時」狀態。 要更改其狀態，需要手動停止它。 [瞭解如何停止活動](modify-stop-campaign.md)

1. 激活市場活動後，您可以隨時通過開啟市場活動資訊來檢查其資訊。 該摘要允許您獲取有關目標配置檔案數量以及交付和失敗操作的統計資訊。

   您還可以通過按一下 **[!UICONTROL Reports]** 按鈕 [了解更多](campaign-global-report.md)

   ![](assets/create-campaign-summary.png)

   >[!IMPORTANT]
   >
   >在市場活動中建立的消息特定於 [!DNL Journey Optimizer] 市場活動能力。 建立後，將只能從市場活動訪問它們，並且不會顯示在 **[!UICONTROL Messages]** 的子菜單。

## 其他資源

* [開始使用行銷活動](get-started-with-campaigns.md)
* [建立API觸發的市場活動](api-triggered-campaigns.md)
* [修改或停止行銷活動](modify-stop-campaign.md)
* [行銷活動即時報告](campaign-live-report.md)
* [行銷活動全域報告](campaign-global-report.md)
