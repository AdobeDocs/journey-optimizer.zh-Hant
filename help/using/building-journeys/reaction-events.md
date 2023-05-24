---
solution: Journey Optimizer
product: journey optimizer
title: 反應事件
description: 瞭解反應事件
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 旅程，事件，反應，跟蹤，平台
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 21%

---

# 反應事件 {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="反應事件"
>abstract="本活動可讓您回應和同一歷程中傳送的訊息相關的追蹤資料。我們會在和 Adobe Experience Platform 共用時即時擷取此資訊。"

在元件面板中提供的不同事件活動中，您將發現 **[!UICONTROL 反應]** 的子菜單。 本活動可讓您回應和同一歷程中傳送的訊息相關的追蹤資料。我們會在和 Adobe Experience Platform 共用時即時擷取此資訊。

您可以對按一下或開啟的消息做出反應。

您還可以使用此機制在消息沒有反應時執行操作。 為此，請建立與反應活動平行的第二條路徑，並添加等待活動。 如果在等待活動中定義的期間內沒有反應，則將選擇第二條路徑。 您可以選擇發送後續消息。

請注意，只有在前面有渠道操作活動（電子郵件和推送）時，您才能在畫布中使用反應活動。

請參閱 [關於操作活動](../building-journeys/about-journey-activities.md#action-activities)。

![](assets/journey45.png)

以下是配置反應事件的不同步驟：

1. 添加 **[!UICONTROL 標籤]** 反應。 此步驟為選填。
1. 從下拉清單中，選擇要對其做出反應的操作活動。 您可以選擇在路徑的前幾個步驟中定位的任何活動。
1. 根據您選擇的操作，選擇您要對其做出的反應。
1. 您可以定義事件超時（40秒到30天之間）和超時路徑。 這將為未在定義的持續時間內做出反應的個人建立第二條路徑。 測試使用反應事件的行程時，test模式 **[!UICONTROL 等待時間]** 預設值和最小值為40秒。 請參閱[本節](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>
>反應事件無法跟蹤在不同行程中發生的消息。
>
>反應事件跟蹤「跟蹤」類型連結的點擊量。 未考慮取消訂閱和鏡像頁面連結。

>[!IMPORTANT]
>
>電子郵件客戶端（如Gmail）允許阻止影像。 使用電子郵件中包含的0像素影像跟蹤開啟的電子郵件。 如果影像被阻止，則開啟的電子郵件將不被考慮在內。
