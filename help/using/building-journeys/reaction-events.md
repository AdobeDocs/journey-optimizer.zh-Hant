---
title: 反應事件
description: 瞭解反應事件
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 2%

---

# 反應事件 {#section_dhx_gss_dgb}

![](../assets/do-not-localize/badge.png)

在浮動視窗中提供的不同事件活動中，您會找到內建的&#x200B;**[!UICONTROL Reactions]**&#x200B;事件。 此活動可讓您對追蹤資料做出回應，這些資料與在同一歷程中傳送的訊息有關。 我們在與Adobe Experience Platform分享資訊的那一刻即時擷取這些資訊。 對於推播通知，您可以回應已點按、已傳送或失敗的訊息。 對於SMS訊息，您可以回應已傳送或失敗的訊息。 對於電子郵件，您可以對被點按、傳送、開啟或失敗的訊息做出回應。

您也可以使用此機制，在您的訊息沒有反應時執行動作。 若要這麼做，請建立與反應活動平行的第二條路徑，並新增等待活動。 如果在等待活動中定義的時段內沒有反應，則將選擇第二個路徑。 您可以選擇傳送，例如後續訊息。

請注意，只有在畫布中有&#x200B;**Message**&#x200B;活動之前，您才能使用反應活動。

請參閱[關於操作活動](../building-journeys/about-journey-activities.md#action-activities)。

![](../assets/journey45.png)

以下是設定反應事件的不同步驟：

1. 將&#x200B;**[!UICONTROL Label]**&#x200B;加入反應。 此步驟為選填。
1. 從下拉式清單中，選取您要回應的動作活動。 您可以選取路徑上前幾個步驟中定位的任何動作活動。
1. 根據您選取的動作，選擇您要回應的動作。
1. 您可以定義事件逾時（40秒到30天之間）和逾時路徑。 這將為未在定義的持續時間內做出反應的個人建立第二個路徑。 測試使用反應事件的歷程時，測試模式&#x200B;**[!UICONTROL Wait time]**&#x200B;預設值和最小值為40秒。 請參閱[本節](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>
>反應事件無法追蹤在不同歷程中發生的訊息。
>
>反應事件會追蹤「追蹤」類型連結的點按次數。 未考慮取消訂閱和鏡像頁面連結。

>[!IMPORTANT]
>
>Gmail等電子郵件用戶端允許封鎖影像。 開啟的電子郵件會使用電子郵件中包含的0像素影像來追蹤。 如果影像遭到封鎖，則不會考慮開啟的電子郵件。
