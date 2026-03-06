---
solution: Journey Optimizer
product: journey optimizer
title: 動態媒體
description: 搭配Journey Optimizer使用Dynamic Media
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4c1d39c4-3154-4bec-ac3c-c2ead7164d69
source-git-commit: f212a2178e83283d4755da5483d7c11ba4df183f
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# 插入倒數計時器 {#countdown}

利用Dynamic Media倒數計時器建立急迫性並最大化轉換次數，以在收件者開啟您的電子郵件時即時更新。 此功能適用於快閃銷售、限時優惠方案及對時間敏感的促銷活動。

例如，作為零售品牌的行銷人員，您執行48小時閃購。 在促銷電子郵件中使用倒數計時器：

* 立即開啟的收件者會看到「剩餘47小時」
* 24小時後開啟的收件者會看到「剩餘23小時」
* 在銷售結束後開啟的收件者會看到「時間已到！」

如需如何在Adobe Experience Manager中新增倒數計時器至Dynamic Media範本的詳細資訊，請參閱[此檔案](assets/do-not-localize/countdown.pdf)。


1. 在&#x200B;**[!DNL Adobe Experience Manager]**&#x200B;中建立Dynamic Media範本，並新增倒數計時器元件。

   ![](assets/timer-1.png)

1. 在&#x200B;**[!DNL Journey Optimizer]**&#x200B;中，建立新行銷活動或開啟現有行銷活動，然後存取電子郵件Designer。

1. 將&#x200B;**HTML**&#x200B;或&#x200B;**Asset**&#x200B;元件拖放到您的電子郵件內容中。

1. 將游標暫留在元件上，然後按一下&#x200B;**[!UICONTROL 顯示原始程式碼]** (適用於HTML元件)或&#x200B;**[!UICONTROL 瀏覽]** （適用於Asset元件）。

   ![](assets/timer-2.png)

1. 從&#x200B;**[!UICONTROL 編輯HTML]**&#x200B;功能表，導覽至&#x200B;**[!UICONTROL Assets]**，然後按一下&#x200B;**[!UICONTROL 開啟資產選擇器]**&#x200B;以瀏覽並選取您發佈的Dynamic Media範本。

   ![](assets/timer-3.png)

1. 透過切換藥丸到開啟來啟用藥丸體驗。 隱藏較長的屬性路徑可改善可讀性。

   ![](assets/timer-6.png)

1. 在&#x200B;**[!UICONTROL 自訂屬性]**&#x200B;功能表中，視需要設定範本的任何可自訂URL引數。

   完成時，按一下&#x200B;**[!UICONTROL 儲存]**。

   ![](assets/timer-4.png)

1. 或者，您也可以存取Dynamic Media範本的引數，方法是在Email Designer中選取資產，然後存取&#x200B;**[!UICONTROL 設定]**&#x200B;功能表。

   設定下列專案：

   * **橫幅文字**：計時器顯示的文字
   * **結束時間**：倒數計時到期的日期和時間。 僅以GMT （格林威治標準時間）輸入時間。 系統不接受其他時區。
   * **遞補文字**：計時器結束之後顯示的訊息

   ![](assets/timer-5.png)

1. 按一下&#x200B;**[!UICONTROL 預覽]**&#x200B;以檢視具有即時倒數計時器更新的計時器，並驗證您的設定。

當收件者開啟電子郵件時，他們會看到您快閃銷售的確切剩餘時間。 如果他們稍後重新開啟電子郵件，倒數計時會自動更新以反映目前的剩餘時間。 結束日期後，預設訊息會自動顯示。
