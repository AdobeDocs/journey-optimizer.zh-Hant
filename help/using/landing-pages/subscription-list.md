---
title: 建立訂閱清單
description: 了解如何在Journey Optimizer中設定訂閱清單
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 建立訂閱清單 {#create-subscription-list}

## 什麼是訂閱清單？

訂閱服務是指向選擇接收特定主旨/事件/興趣等通訊的客戶提供的行銷商品及服務。 持續不斷地。 在 [!DNL Journey Optimizer]，這些選擇加入的客戶會收集到訂閱清單中。

訂閱服務可以是：

* 電子報，例如「執行系列」
* 例如&quot;2021年首腦會議&quot;
* 網路研討會，例如「深入了解加密」
* 對特定產品/體育/服務等的興趣，例如「有興趣在未來12個月內購買房子」
* 通知方式的偏好設定，例如「透過電子郵件接收新歌曲通知」

可透過 [登陸頁面](create-lp.md). 範例如 [本節](get-started-lp.md#subscription-to-a-service).

## 定義訂閱清單 {#define-subscription-list}

若要建立訂閱清單，請遵循下列步驟。

1. 若要存取訂閱清單，請選取 **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](../assets/lp_subscription-lists.png)

1. 在訂閱清單中，按一下 **[!UICONTROL Create subscription]** 清單。

   ![](../assets/lp_create-subscription-list.png)

1. 新增名稱和說明。 這些欄位是必填欄位。

1. 您可以定義開始日期和結束日期。

   ![](../assets/lp_subscription-list-dates.png)

1. 按一下「**[!UICONTROL Save]**」。

清單會顯示已建立的所有訂閱清單。 您可以根據建立日期或修改日期來篩選。

![](../assets/lp_subscription-filters.png)

可能的狀態如下：

* **[!UICONTROL Not started]**:您定義的開始日期晚於當天。 訂閱此清單的設定檔將不會收到與此訂閱清單相關的通訊。
* **[!UICONTROL Live]**:當天由訂閱清單開始日期和結束日期組成，或您未定義結束/開始日期，這表示訂閱清單一律為上線狀態。
* **[!UICONTROL Expired]**:結束日期已過，訂閱清單已無效。 訂閱此清單的任何配置檔案將不會再接收與此訂閱清單相關的任何通信。

建立訂閱清單後，您就可以在登錄頁面中使用該清單，讓設定檔可以透過表單選擇加入並新增至清單。 [了解更多](design-lp.md)

建立歷程和個人化時，您也可以使用訂閱清單做為區段。

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* How do you handle the different statuses? Live, Not started, Expired? Is it only through start/end dates?

* What does it mean when a subscription list is expired or not started? You can't use it in a LP? And if a user is subscribed to this service, then he won't receive communications any more?

* What else can you currently do with subscription lists apart from attach them to a landing page?

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->