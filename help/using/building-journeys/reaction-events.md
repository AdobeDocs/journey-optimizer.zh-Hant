---
solution: Journey Optimizer
product: journey optimizer
title: 回應事件
description: 瞭解反應事件
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，事件，反應，追蹤，平台
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 110fd5f1055455ec040ab8de0b599a343e8de298
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 20%

---

# 反應事件 {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="反應事件"
>abstract="本活動可讓您回應和同一歷程中傳送的訊息相關的追蹤資料。我們會在和 Adobe Experience Platform 共用時即時擷取此資訊。"

在浮動視窗中可用的不同事件活動中，您會找到內建的&#x200B;**[!UICONTROL 回應]**&#x200B;事件。 本活動可讓您回應和同一歷程中傳送的訊息相關的追蹤資料。我們會在和 Adobe Experience Platform 共用時即時擷取此資訊。

您可以對點按或開啟的訊息做出反應。

您也可以使用此機制，在訊息沒有反應時執行動作。 若要這麼做，請建立與反應活動平行的第二個路徑，並新增等待活動。 如果等待活動中定義的期間內沒有反應，則會選擇第二個路徑。 舉例來說，您可以選擇傳送後續追蹤訊息。

請注意，如果之前有管道動作活動（電子郵件和推播），您只能在畫布中使用回應活動。

請參閱[關於動作活動](../building-journeys/about-journey-activities.md#action-activities)。

![](assets/journey45.png)

以下是設定反應事件的不同步驟：

1. 新增&#x200B;**[!UICONTROL 標籤]**&#x200B;至回應。 此步驟為選填。
1. 從下拉式清單中，選取您要回應的動作活動。 您可以選取位於路徑前幾個步驟中的任何動作活動。
1. 根據您選取的動作，選擇您要回應的專案。
1. 您可以定義事件逾時（40秒至29天之間）和逾時路徑。 這會為未在定義期間內回應的個人建立第二個路徑。 測試歷程的反應事件時，測試模式&#x200B;**[!UICONTROL 等待時間]**&#x200B;預設值及最小值為40秒。 請參閱[本節](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>
>反應事件無法追蹤發生在不同歷程中的訊息。
>
>反應事件會追蹤「已追蹤」型別連結的點按。 未考慮取消訂閱和映象頁面連結。

>[!IMPORTANT]
>
>電子郵件使用者端（例如Gmail）允許影像封鎖。 系統會使用電子郵件中包含的0畫素影像來追蹤電子郵件開啟次數。 如果封鎖影像，則不會將電子郵件開啟次數納入考量。
