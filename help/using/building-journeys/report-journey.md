---
solution: Journey Optimizer
product: journey optimizer
title: Publish歷程
description: 瞭解如何報告您的歷程
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 發佈，歷程，即時，有效性，檢查
source-git-commit: 59a597a563074fa4daa74c64e97f6bb5c0f6834d
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# 歷程畫布中的即時報告 {#report-journey}

>[!NOTE]
>
>如果您在歷程即時報告中看不到資料，則必須擴充存取許可權，以包含&#x200B;**[!UICONTROL 檢視歷程報告]**&#x200B;許可權。 [了解更多](../administration/permissions.md)

您的歷程發佈後，**即時報告**&#x200B;會直接在歷程畫布中提供過去24小時的量度。

顯示的事件發生在過去24小時內，事件與其顯示之間至少間隔二分鐘，通常在五分鐘內。

![](assets/journey_live_report.png)

對於您的即時歷程，您有權存取：

* **[!UICONTROL 已輸入設定檔]**：進入此活動的個人總數。
* **[!UICONTROL 已退出設定檔]**：由於退出條件而從該活動退出歷程的個人總數。
* **[!UICONTROL 發生錯誤的設定檔]**：歷程中發生錯誤的個人總數。
* **[!UICONTROL 捨棄的設定檔]**：由於下列其中一個原因而從歷程捨棄的個人總數：

   * 對於&#x200B;**對象資格**&#x200B;活動，如果對象資格的預期動詞與歷程已收到的動詞不符（例如，「已退出」而不是「已實現」），則可能會發生捨棄。
   * 對於&#x200B;**事件觸發的**&#x200B;歷程，如果個人太快嘗試重新進入歷程或不允許重新進入，則可能會發生捨棄。
   * 在&#x200B;**循環**&#x200B;歷程中，如果個人已在歷程中，且重新進入原則未設定為「強制重新進入」，則捨棄會計入每個循環。
   * 在&#x200B;**讀取對象**&#x200B;活動中，如果未設定匯出個人的身分，或是收到的身分名稱空間不符合歷程的預期身分名稱空間，則會發生捨棄。

對於每個即時歷程中的每一個活動，您都有權存取：

* **[!UICONTROL 已輸入設定檔]**：進入此活動的個人總數。
* **[!UICONTROL 已退出的設定檔]**：由於退出條件而從該活動退出的個人總數。
* **[!UICONTROL 錯誤]**：在該活動中發生錯誤的個人總數。