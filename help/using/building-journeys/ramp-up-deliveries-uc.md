---
title: 加快交貨速度
description: 瞭解如何提高交貨量
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 3%

---

# 用例：加快交貨量{#use-case-ramp-up-your-deliveries}

如果您最近轉到了其他電子郵件服務提供商、 IP地址、電子郵件域或子域，則需要建立您作為發件人的信譽。 否則，您的遞送可能會被阻止或移動到收件人郵箱的垃圾郵件資料夾。 瞭解如何通過IP升溫提高您的電子郵件聲譽 [交付能力最佳實踐指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}。

要預熱您的IP，您可以逐步增加交貨數量。 閱讀有關 [優化Journey Optimizer的可交付性](../messages/deliverability.md)。

此使用案例的目的是建立加快電子郵件遞送的行程。 要配置此行程，請執行以下步驟：

1. 建立歷程. [閱讀全文](journey-gs.md)。

1. 添加 **[!UICONTROL Condition]** 活動到旅程。 [閱讀全文](condition-activity.md)。

1. 在 **[!UICONTROL Condition]** 活動設定，設定交貨的最大收件人數：

   1. 在 **[!UICONTROL Condition]** 活動設定，設定 **[!UICONTROL Type]** 欄位 **[!UICONTROL Profile cap]**。 [閱讀全文](condition-activity.md#profile_cap)。

   1. 設定 **[!UICONTROL Limit]** 到此傳遞的最大收件人數。

   ![](../assets/profile-cap-condition.png)

   您可以逐步將此限制增加到訂閱者總數。

1. 添加 **[!UICONTROL Message]** 活動到 **[!UICONTROL Condition]** 的子菜單。

   ![](../assets/ramp-up-deliveries-message.png)

   行程運行時，系統會向輸入的配置檔案發送消息，最多為您指定的配置檔案的最大數量。 當達到此限制時，輸入的配置檔案將採用備用路徑。

1. 完成您選擇的活動。

IP升溫後，可以刪除此條件。
