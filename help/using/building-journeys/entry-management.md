---
solution: Journey Optimizer
product: journey optimizer
title: 設定檔專案管理
description: 瞭解如何管理設定檔輸入
feature: Journeys
role: User
level: Intermediate
keywords: 重新進入、歷程、設定檔、週期性
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 1cf62f949c1309b864ccd352059a444fd7bd07f0
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 22%

---


# 設定檔專案管理 {#entry-management}

依預設，新歷程允許重新進入。 您可以取消勾選「一次性」歷程的選項，例如，如果您想要在某人進入商店時提供一次性禮物。 在這種情況下，您不希望客戶能夠重新進入歷程並再次收到選件。

![](assets/journey-re-entrance.png)

歷程結束時，其狀態為 **[!UICONTROL 已關閉]**. 新的個人無法再進入歷程。 已在歷程中的人員會正常完成歷程。

預設全域逾時30天後，歷程會切換至 **已完成** 狀態。  [了解更多](journey-gs.md#global_timeout)。


## 單一歷程{#entry-unitary}

單一歷程 (從事件或區段資格開始) 包含可防止為同一事件多次錯誤觸發歷程的護欄。 在預設情況下，設定檔重新進入時會暫時封鎖 5 分鐘。 例如，如果某個事件在 12:01 觸發特定設定檔的歷程，而另一個事件在 12:03 達到時間限制 (無論是相同事件或是不同事件觸發相同歷程)，則此設定檔的歷程將不會再次開始。

除此之外：

* 如果啟用重新進入，設定檔可以進入歷程多次，但必須完全退出歷程的上一個執行個體，才能進入歷程。

* 如果停用重新進入，則設定檔無法多次進入同一歷程

## 讀取區段歷程{#entry-read-segment}

在讀取區段歷程中：

* 對於非循環歷程：設定檔進入歷程一次，且只進入歷程一次。

* 對於週期性歷程：如果設定檔處於區段/預期狀態，設定檔會在每次週期性進入歷程。 如果他們仍然在上一個循環的歷程中，他們將從頭重新開始。

在商業事件歷程中，從 **讀取區段** 活動：瞭解此歷程是根據接收業務事件，如果設定檔符合預期區段中的資格，他們會針對收到的每個業務事件進入歷程，這表示此設定檔可能同時於相同歷程中多次，但位於不同業務事件的內容中。

<!--
# Profile entry management {#entry-management}

There are two main types of journeys:

* event-based journeys: starting with an event, these journeys are unitary, they are associated to one individual. When the event is received, the individual enters the journey. [Read more](#entry-unitary)
* read segment journeys: starting with a read segment, these are batch journeys. Individuals belonging to the segment all enter the same journey. These journeys can be recurring or one-shot. [Read more](#entry-read-segment)

In both journey types, a profile cannot be present multiple times in the same journey, at the same time.


## Unitary journeys{#entry-unitary}

In unitary journeys, you can enable or disable re-entrance:

* If re-entrance is enabled, a profile can enter a journey several times, but cannot do it until he fully exited that previous instance of the journey.

* If re-entrance is disabled, a profile cannot enter multiple times the same journey

By default, new journeys allow re-entrance. You can uncheck the option for “one shot” journeys, for example if you want to offer a one-time gift when a person enters a shop. In that case, you don't want the customer to be able to re-enter the journey and receive the offer again. When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey finish the journey normally. [Learn more](journey-gs.md#entrance)

![](assets/journey-re-entrance.png)

After the default global timeout of 30 days, the journey switches to the **Finished** status. New individuals can no longer enter the journey. Persons already in the journey finish the journey normally.Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 30 days. Indeed, as we remove all information about persons who entered the journey 30 days after they enter, we cannot know the person entered previously, more than 30 days ago. [Learn more](journey-gs.md#global_timeout).

Unitary journeys (starting with an event or a segment qualification) include a guardrail that prevents journeys from being erroneously triggered multiple times for the same event. Profile re-entrance is temporally blocked by default for 5 minutes. For instance, if an event triggers a journey at 12:01 for a specific profile and another one arrives at 12:03 (whether it is the same event or a different one triggering the same journey) that journey will not start again for this profile.

The key is also used to check that a person is in a journey. Indeed, a person cannot be at two different places in the same journey. As a result, the system does not allow the same key, for example the key CRMID=3224, to be at different places in the same journey.

## Read segment journeys{#entry-read-segment}

In a read segment journey:

* For non-recurring journeys: the profile enters once and only once the journey.

* For recurring journeys: by default, all the profiles belonging to the segment enters the journey on each recurrence. They must finish the journey before they can reenter in another occurrence. 

>[!NOTE]
>
>Two options are available for recurring read segment journeys. The **Force reentrance on recurrence** option makes all the profiles still present in the journey automatically exit it on the next execution. The **Incremental read** option only targets the individuals who entered the segment since the last execution of the journey. Refer to this [section](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

In business event journeys starting with a **Read segment** activity: knowing that this journey is based on the reception of a business event, if the profile is qualified in the expected segment, they will enter the journey for each business event received, meaning that this profile can be multiple times in the same journey, at the same time, but in the context of different business events.
-->