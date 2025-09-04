---
solution: Journey Optimizer
product: journey optimizer
title: 發佈此歷程
description: 瞭解如何報告您的歷程
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 發佈，歷程，即時，有效性，檢查
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 2%

---

# 歷程畫布中的即時報告 {#report-journey}

發佈您的歷程後，[試執行模式](journey-dry-run.md)啟動後，**即時報告**&#x200B;會直接在歷程畫布中提供過去24小時的量度。


>[!AVAILABILITY]
>
>如果您在歷程即時報告中看不到資料，則必須擴充存取許可權，以包含&#x200B;**[!UICONTROL 檢視歷程報告]**&#x200B;許可權。 [了解更多](../administration/permissions.md)


顯示的事件發生在過去24小時內，事件與其顯示之間至少間隔二分鐘，通常在五分鐘內。

![](assets/journey_live_report.png)

對於您處於即時或[試執行模式](journey-dry-run.md)的歷程，您可以檢查：

* **[!UICONTROL 已進入設定檔]**：進入歷程的個人總數。
* **[!UICONTROL 已退出設定檔]**：已退出歷程的個人總數（包括錯誤）。
* **[!UICONTROL 發生錯誤的設定檔]**：歷程中發生錯誤的個人總數。
* **[!UICONTROL 捨棄的設定檔]**：由於下列其中一個原因而從歷程捨棄的個人總數：

   * 對於&#x200B;**對象資格**&#x200B;活動，如果對象資格的預期動詞與歷程已收到的動詞不符（例如，「已退出」而不是「已實現」），則可能會發生捨棄。
   * 對於&#x200B;**事件觸發的**&#x200B;歷程，如果個人太快嘗試重新進入歷程或不允許重新進入，則可能會發生捨棄。
   * 在&#x200B;**循環**&#x200B;歷程中，如果個人已在歷程中，且重新進入原則未設定為「強制重新進入」，則捨棄會計入每個循環。
   * 在&#x200B;**讀取對象**&#x200B;活動中，如果未設定匯出個人的身分，或是收到的身分名稱空間不符合歷程的預期身分名稱空間，則會發生捨棄。

對於處於即時或[試執行模式](journey-dry-run.md)的每個歷程中的每個活動，您都可以存取：

* **[!UICONTROL 已進入]**：進入此活動的個人總數。 對於&#x200B;**動作**&#x200B;活動，由於它們不是在練習模式中執行，因此此量度會指出通過的個人檔案。
* **[!UICONTROL 已退出（符合退出條件）]**：由於退出條件（包括錯誤），從該活動退出歷程的個人總數。
* **[!UICONTROL 已退出（強制退出）]**：由於歷程從業人員設定而暫停歷程時，已退出歷程的個人總數。 對於處於練習模式的歷程，此量度一律等於零。
* **[!UICONTROL 錯誤]**：在該活動中發生錯誤的個人總數。


>[!MORELIKETHIS]
>
>* [開始使用報告功能](../reports/gs-reports.md)
>* [發佈您的歷程](publishing-the-journey.md)
>* [歷程練習](journey-dry-run.md)
>* [設定並追蹤您的歷程量度](success-metrics.md)
>* [自訂歷程報告](../reports/sharing-overview.md)