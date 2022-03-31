---
title: 建立訂閱清單
description: 瞭解如何在Journey Optimizer設定訂閱清單
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 3%

---

# 訂閱清單 {#create-subscription-list}

## 什麼是訂閱清單？ {#subscription-list-definition}

訂閱服務是指向選擇接收特定主題/事件/興趣等通信的客戶提供的營銷商品和服務。 持續進行。 在 [!DNL Journey Optimizer]，這些已選擇的客戶被收集到訂閱清單中。

訂閱服務可以是：

* 例如，新聞簡報：&quot;運行系列&quot;
* 例如，事件：《2021年首腦會議》
* 例如：&quot;瞭解有關加密的詳細資訊&quot;
* 對特定產品/運動/服務/等的興趣，例如：「有興趣在未來12個月內買房」
* 例如：&quot;通過電子郵件接收新歌曲通知&quot;

配置檔案可通過 [登錄頁](create-lp.md)。 在 [此部分](lp-use-cases.md#subscription-to-a-service)。

## 定義訂閱清單 {#define-subscription-list}

要建立訂閱清單，請執行以下步驟。

1. 要訪問訂閱清單，請選擇 **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**。

   ![](assets/lp_subscription-lists.png)

1. 選取 **[!UICONTROL Create subscription list]** 按鈕。

   ![](assets/lp_create-subscription-list.png)

1. 添加名稱和說明。 這些欄位是必填的。

1. 您可以定義起始日期和終止日期。

   ![](assets/lp_subscription-list-dates.png)

1. 按一下「**[!UICONTROL Save]**」。

該清單顯示所有建立的訂閱清單。 您可以根據建立日期或修改日期及其狀態來篩選它們。

![](assets/lp_subscription-filters.png)

可能的狀態如下：

* **[!UICONTROL Not started]**:您定義的開始日期晚於當前日期。 訂閱的配置檔案尚未接收與此訂閱清單相關的通信。
* **[!UICONTROL Live]**:當前日期包括在訂閱清單開始日期和結束日期之間，或者您未定義結束/開始日期，這意味著訂閱清單始終處於活動狀態。
* **[!UICONTROL Expired]**:結束日期已過，因此訂閱清單不再有效。 任何已訂閱配置檔案將不會再接收與此訂閱清單相關的通信。

一旦建立了訂閱清單，您就可以在登錄頁中使用它。 選擇通過登錄頁表單加入的配置檔案將添加到清單中。 [了解更多](design-lp.md)

您還可以將訂閱清單用作段 [乘機](../building-journeys/journey-gs.md#jo-build) 添加個性化。

>[!NOTE]
>
>您可以通過特定報告監視訂閱清單的影響。 [了解更多](../reports/subscription-report-live.md)
