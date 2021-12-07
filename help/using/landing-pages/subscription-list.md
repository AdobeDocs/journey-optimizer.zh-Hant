---
title: 建立訂閱清單
description: 了解如何在Journey Optimizer中設定訂閱清單
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 88b037e079a46e10f7ee4715e78e5edc5a34a6ce
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 2%

---

# 訂閱清單 {#create-subscription-list}

## 什麼是訂閱清單？

訂閱服務是指向選擇接收特定主旨/事件/興趣等通訊的客戶提供的行銷商品及服務。 持續不斷地。 在 [!DNL Journey Optimizer]，這些選擇加入的客戶會收集到訂閱清單中。

訂閱服務可以是：

* 例如，電子報：&quot;運行系列&quot;
* 例如，事件：《2021年峰會》
* 例如，網路研討會：「了解有關加密的更多資訊」
* 對特定產品/運動/服務等的興趣，例如：「未來12個月有興趣買房」
* 通知方式的偏好設定，例如：&quot;接收電子郵件上的新歌曲通知&quot;

可透過 [登陸頁面](create-lp.md). 範例如 [本節](lp-use-cases.md#subscription-to-a-service).

## 定義訂閱清單 {#define-subscription-list}

若要建立訂閱清單，請遵循下列步驟。

1. 若要存取訂閱清單，請選取 **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](../assets/lp_subscription-lists.png)

1. 選取 **[!UICONTROL Create subscription list]** 按鈕。

   ![](../assets/lp_create-subscription-list.png)

1. 新增名稱和說明。 這些欄位是必填欄位。

1. 您可以定義開始日期和結束日期。

   ![](../assets/lp_subscription-list-dates.png)

1. 按一下「**[!UICONTROL Save]**」。

清單會顯示已建立的所有訂閱清單。 您可以根據建立日期或修改日期及其狀態來篩選。

![](../assets/lp_subscription-filters.png)

可能的狀態如下：

* **[!UICONTROL Not started]**:您定義的開始日期晚於當天。 暫停的設定檔將不會收到與此訂閱清單相關的通訊。
* **[!UICONTROL Live]**:當天由訂閱清單開始日期和結束日期組成，或您未定義結束/開始日期，這表示訂閱清單一律為上線狀態。
* **[!UICONTROL Expired]**:結束日期已過，因此訂閱清單已無效。 任何訂閱的配置檔案將不會再接收與此訂閱清單相關的任何通信。

建立訂閱清單後，您就可以在登錄頁面中使用它。 會將透過登錄頁面表單選擇加入的設定檔新增至清單。 [了解更多](design-lp.md)

您也可以在 [建立歷程](../building-journeys/journey-gs.md#jo-build) 和新增個人化。

>[!NOTE]
>
>您可以透過特定報告來監控訂閱清單的影響。 [了解更多](subscription-report.md)

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->
