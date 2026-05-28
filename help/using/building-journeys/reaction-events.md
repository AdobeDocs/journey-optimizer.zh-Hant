---
solution: Journey Optimizer
product: journey optimizer
title: 回應事件
description: 瞭解如何使用回應事件來回應訊息追蹤資料（例如歷程中的開啟和點按），以及為未回應者設定逾時路徑。
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，事件，反應，追蹤，平台
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/6myO49j2-TgkX0-diC8JDePxvMBPjZGnMYdxO466cP4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: e57d1da4-32c2-4cc6-945c-9feb219156ff
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 506
ht-degree: 15%

---

# 反應事件 {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="反應事件"
>abstract="本活動可讓您回應和同一歷程中傳送的訊息相關的追蹤資料。 我們會在和 [!DNL Adobe Experience Platform] 共用時即時擷取此資訊。"

## 概觀 {#overview}

在浮動視窗中可用的不同事件活動中，您會找到內建的&#x200B;**[!UICONTROL 回應]**&#x200B;事件。 本活動可讓您回應和同一歷程中傳送的訊息相關的追蹤資料。 我們會在和 [!DNL Adobe Experience Platform] 共用時即時擷取此資訊。

您可以對點按或開啟的訊息做出反應。 例如，如果某人開啟了先前的電子郵件或按一下了電子郵件內部，您就可以傳送另一封郵件；如果未與您的通訊互動，則可以傳送不同的後續郵件。

檢視[動作活動](../building-journeys/about-journey-activities.md#action-activities)。

當您的訊息沒有回應時，您可以使用&#x200B;**[!UICONTROL 回應]**&#x200B;活動來執行動作。 若要這麼做，請建立與&#x200B;**[!UICONTROL 回應]**&#x200B;活動平行的第二個路徑，並新增&#x200B;**[!UICONTROL 等待]**&#x200B;活動。 如果在&#x200B;**[!UICONTROL 等待]**&#x200B;活動中定義的期間內沒有反應，將會選擇第二個路徑。 舉例來說，您可以選擇傳送後續追蹤訊息。

## 如何設定反應事件 {#configure}

![反應事件設定，包含管道選取和事件型別選項](assets/journey45.png)

請依照下列步驟設定反應事件：

1. 在歷程畫布上的[頻道動作活動](journey-action.md)後立即放置&#x200B;**[!UICONTROL 回應]**&#x200B;活動&#x200B;**&#x200B;**。
1. 新增&#x200B;**[!UICONTROL 標籤]**&#x200B;至回應。 此步驟為選填。
1. 從下拉式清單中，選取您要回應的動作活動。 您可以選取位於路徑前幾個步驟中的任何動作活動。
1. 根據您選取的動作，選擇您要回應的專案。
1. 您可以定義事件逾時（40秒至90天之間）和逾時路徑。 這會為未在定義期間內回應的個人建立第二個路徑。 測試歷程的反應事件時，測試模式&#x200B;**[!UICONTROL 等待時間]**&#x200B;預設值及最小值為40秒。 請參閱[本節](../building-journeys/testing-the-journey.md)。

## 護欄與限制 {#guardrails-limitations}

* 在歷程畫布中的[頻道動作活動](journey-action.md)之後，**[!UICONTROL 回應]**&#x200B;活動必須置於&#x200B;**立即**。
* 如果之前沒有管道動作活動，則無法使用&#x200B;**[!UICONTROL 回應]**&#x200B;活動。
* 不支援在頻道動作和&#x200B;**[!UICONTROL 回應]**&#x200B;活動之間放置&#x200B;**[!UICONTROL 等待]**&#x200B;活動或任何其他活動，並可能導致回應無法如預期運作。
* 反應事件只能追蹤相同歷程中傳送的訊息。 他們無法追蹤發生在不同歷程中的訊息。
* 反應事件會追蹤「已追蹤」型別連結的點按。 未考慮取消訂閱和映象頁面連結。
* 系統會使用電子郵件中包含的0畫素影像來追蹤電子郵件開啟次數。 如果電子郵件使用者端（例如Gmail）封鎖影像，系統不會將電子郵件開啟列入考量。
