---
title: 設定檔上限
description: 設定檔上限
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
hide: true
hidefromtoc: true
source-git-commit: b5ce2ea81d4091b4fa9c09e83573f9043c5e55a8
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---


# 建立寄件者的聲譽

如果您最近移至其他電子郵件服務提供者、IP位址、電子郵件網域或子網域，則需要建立寄件者的信譽。 否則，您的傳遞可能會遭到封鎖，或移至收件者信箱的垃圾郵件資料夾。

若要熱化IP，您可以逐步增加傳送的數量。 看這個 [使用案例](../building-journeys/ramp-up-deliveries-uc.md).

## 設定檔大寫條件類型 {#profile_cap}

其他條件類型在此中詳細說明 [節](../building-journeys/condition-activity.md).

使用此條件類型來設定歷程路徑的設定檔數目上限。 達到此限制時，輸入的設定檔會採取替代路徑。

您可以使用此條件類型來增加傳送量。 看這個 [使用案例](../building-journeys/ramp-up-deliveries-uc.md).

預設上限為1000。 您可以將整數值設為1到20,000。

計數器僅會套用至選取的歷程版本。 計數器會在一個月後重設為零。 重設後，進入的設定檔會再次取用公稱路徑，直到達到計數器限制為止。

即使您將替代路徑移至歷程畫布上標稱路徑上方，標稱路徑一律具有優先順序高於替代路徑。

![](../assets/profile-cap-condition.png)

## 使用案例：加速傳遞

如果您最近移至其他電子郵件服務提供者、IP位址、電子郵件網域或子網域，則需要建立寄件者的信譽。 否則，您的傳遞可能會遭到封鎖，或移至收件者信箱的垃圾郵件資料夾。 了解如何透過 [傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}。

若要熱化IP，您可以逐步增加傳送的數量。 深入了解 [最佳化Journey Optimizer的傳遞能力](../deliverability.md).

此使用案例的用途是建立歷程，以加速您的電子郵件傳送。 若要設定此歷程，請依照下列步驟操作：

1. 建立歷程. [閱讀全文](../building-journeys/journey-gs.md)。

1. 新增 **[!UICONTROL Condition]** 活動至歷程。 [閱讀全文](../building-journeys/condition-activity.md)。

1. 在 **[!UICONTROL Condition]** 活動設定，設定傳送的收件者人數上限：

   1. 在 **[!UICONTROL Condition]** 活動設定，請設定 **[!UICONTROL Type]** 欄位至 **[!UICONTROL Profile cap]**. [閱讀全文](profile-cap.md#profile_cap)。

   1. 設定 **[!UICONTROL Limit]** 欄位至此傳送的收件者人數上限。

   ![](../assets/profile-cap-condition.png)

   您可以逐步將此限制提高至訂閱者總數。

1. 新增 **[!UICONTROL Message]** 活動至 **[!UICONTROL Condition]** 活動。

   ![](../assets/ramp-up-deliveries-message.png)

   歷程執行時，會傳送輸入的設定檔，最多為您指定的設定檔數量上限。 達到此限制時，輸入的設定檔會採取替代路徑。

1. 使用您選擇的活動完成歷程。

您的IP升溫後，您可以移除此條件。

