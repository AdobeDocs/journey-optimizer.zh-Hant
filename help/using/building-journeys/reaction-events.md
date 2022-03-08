---
title: 反應事件
description: 瞭解反應事件
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 2%

---

# 反應事件 {#reaction-events}

在元件面板中提供的不同事件活動中，您將發現 **[!UICONTROL Reactions]** 的子菜單。 本練習允許您對與同一行程中發送的郵件相關的跟蹤資料做出響應。 我們在與Adobe Experience Platform分享資訊時即時捕獲這些資訊。 對於推送通知，您可以對按一下的、發送的或失敗的消息做出響應。 對於SMS消息，您可以對已發送或失敗的消息做出響應。 對於電子郵件，您可以對按一下的、發送的、開啟的或失敗的郵件做出反應。

您還可以使用此機制在消息沒有反應時執行操作。 為此，請建立與反應活動平行的第二條路徑，並添加等待活動。 如果在等待活動中定義的期間內沒有反應，則將選擇第二條路徑。 您可以選擇發送後續消息。

請注意，只有在存在 **消息** 活動。

請參閱 [關於操作活動](../building-journeys/about-journey-activities.md#action-activities)。

![](assets/journey45.png)

以下是配置反應事件的不同步驟：

1. 添加 **[!UICONTROL Label]** 反應。 此步驟為選填。
1. 從下拉清單中，選擇要對其做出反應的操作活動。 您可以選擇在路徑的前幾個步驟中定位的任何活動。
1. 根據您選擇的操作，選擇您要對其做出的反應。
1. 您可以定義事件超時（40秒到30天之間）和超時路徑。 這將為未在定義的持續時間內做出反應的個人建立第二條路徑。 測試使用反應事件的行程時，test模式 **[!UICONTROL Wait time]** 預設值和最小值為40秒。 請參閱[本節](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>
>反應事件無法跟蹤在不同行程中發生的消息。
>
>反應事件跟蹤「跟蹤」類型連結的點擊量。 未考慮取消訂閱和鏡像頁面連結。

>[!IMPORTANT]
>
>電子郵件客戶端（如Gmail）允許阻止影像。 使用電子郵件中包含的0像素影像跟蹤開啟的電子郵件。 如果影像被阻止，則開啟的電子郵件將不被考慮在內。
