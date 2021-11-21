---
title: 反應事件
description: 了解反應事件
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 2%

---

# 反應事件 {#section_dhx_gss_dgb}

浮動視窗中可用的不同事件活動中，會有內建的 **[!UICONTROL Reactions]** 事件。 此活動可讓您對與相同歷程中傳送之訊息相關的追蹤資料做出反應。 我們會在與Adobe Experience Platform共用資訊的當下即時擷取這些資訊。 若是推播通知，您可以對點按、傳送或失敗的訊息做出反應。 對於SMS訊息，您可以對已傳送或失敗的訊息做出反應。 若是電子郵件，您可以對點按、傳送、開啟或失敗的訊息做出反應。

您也可以使用此機制，在訊息沒有反應時執行動作。 要執行此操作，請建立與反應活動平行的第二個路徑，並新增等待活動。 如果在等待活動中定義的期間內沒有反應，則會選擇第二個路徑。 例如，您可以選擇傳送後續訊息。

請注意，您只能在畫布中使用反應活動，前提是 **訊息** 之前的活動。

請參閱 [關於動作活動](../building-journeys/about-journey-activities.md#action-activities).

![](../assets/journey45.png)

以下是設定反應事件的不同步驟：

1. 新增 **[!UICONTROL Label]** 反應。 此步驟為選填。
1. 從下拉式清單中，選取您要回應的動作活動。 您可以選取位於路徑前幾個步驟中的任何動作活動。
1. 根據您選取的動作，選擇您要回應的項目。
1. 您可以定義事件逾時（40秒到30天之間）和逾時路徑。 這會為在定義期間內未反應的個人建立第二個路徑。 測試使用反應事件的歷程時，即測試模式 **[!UICONTROL Wait time]** 預設值和最小值為40秒。 請參閱[本節](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>
>反應事件無法追蹤在不同歷程中發生的訊息。
>
>反應事件會追蹤「追蹤」類型的連結上的點按。 未考慮取消訂閱和鏡像頁面連結。

>[!IMPORTANT]
>
>Gmail等電子郵件用戶端允許影像封鎖。 使用電子郵件中包含的0像素影像來追蹤開啟的電子郵件。 如果影像遭到封鎖，系統就不會考慮電子郵件開啟次數。
