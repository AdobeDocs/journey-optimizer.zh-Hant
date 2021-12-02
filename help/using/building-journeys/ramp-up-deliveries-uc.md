---
title: 加快傳遞速度
description: 了解如何加速傳遞
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 980aedcd0fb4dba161dc0041a77e0f8d06d6fe68
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 3%

---


# 使用案例：加速傳遞

如果您最近移至其他電子郵件服務提供者、IP位址、電子郵件網域或子網域，則需要建立寄件者的信譽。 否則，您的傳遞可能會遭到封鎖，或移至收件者信箱的垃圾郵件資料夾。 了解如何透過 [傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}。

若要熱化IP，您可以逐步增加傳送的數量。 深入了解 [最佳化Journey Optimizer的傳遞能力](../deliverability.md).

此使用案例的用途是建立歷程，以加速您的電子郵件傳送。 若要設定此歷程，請依照下列步驟操作：

1. 建立歷程. [閱讀全文](journey-gs.md)。

1. 新增 **[!UICONTROL Condition]** 活動至歷程。 [閱讀全文](condition-activity.md)。

1. 在 **[!UICONTROL Condition]** 活動設定，設定傳送的收件者人數上限：

   1. 在 **[!UICONTROL Condition]** 活動設定，請設定 **[!UICONTROL Type]** 欄位至 **[!UICONTROL Profile cap]**. [閱讀全文](condition-activity.md#profile_cap)。

   1. 設定 **[!UICONTROL Limit]** 欄位至此傳送的收件者人數上限。

   ![](../assets/profile-cap-condition.png)

   您可以逐步將此限制提高至訂閱者總數。

1. 新增 **[!UICONTROL Message]** 活動至 **[!UICONTROL Condition]** 活動。

   ![](../assets/ramp-up-deliveries-message.png)

   歷程執行時，會傳送輸入的設定檔，最多為您指定的設定檔數量上限。 達到此限制時，輸入的設定檔會採取替代路徑。

1. 使用您選擇的活動完成歷程。

您的IP升溫後，您可以移除此條件。





