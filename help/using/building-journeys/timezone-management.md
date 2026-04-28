---
solution: Journey Optimizer
product: journey optimizer
title: 時區管理
description: Learn about time zone management
feature: Journeys, Profiles
topic: Content Management
role: User
level: Intermediate
keywords: time zone, properties, journey, condition, time, date, custom
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
version: Journey Orchestration
source-git-commit: 8521e59022c221c0ca4e5b69b5b3aefe6304b417
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 23%

---

# 時區管理 {#timezone_management}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="歷程時區"
>abstract="選取歷程的時區。 當使用固定時區時，對於所有進入歷程的個人來說都是相同的。"


You can define a time zone in the [properties](../building-journeys/journey-properties.md#timezone) of your journey.

To access journey properties, select the pencil icon in the top-right of the screen.

This time zone will be used for every activity of the journey containing a time element such as:

* [Time condition](../building-journeys/conditions.md#time_condition)
* [Date condition](../building-journeys/conditions.md#date_condition)
* [Custom wait](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

You can select a [fixed time zone](#fixed-timezone) or choose to use the time zone [defined in the user profile](#timezone-from-profiles).

## Define a fixed time zone {#fixed-timezone}

The time zone can be fixed. Clear the pre-defined time zone and pick one from the drop-down list. If you use a fixed time zone, it will be the same for all individuals entering the journey.

To do so, in the **[!UICONTROL Journey Properties]** pane, select a time zone.

![Timezone selection dropdown in journey properties](assets/journey72.png)

## 使用輪廓時區 {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="使用輪廓時區"
>abstract="勾選此選項，即可在&#x200B;**「等待」**&#x200B;及&#x200B;**「條件」**&#x200B;活動中使用即時輪廓時區。 如果已經定義輪廓的時區，系統便會取得該時區並在歷程中使用。 若未設定，將使用上面時區欄位中定義的時區。"

If the entry event of the journey has a namespace, meaning that the journey can reach the Real-time Customer Profile service of [!DNL Adobe Experience Platform], you may want to use the time zone defined at the profile level. To do so, in **Properties**, check **Use Profile time zone in waits and conditions**. This option is not checked by default.

If a time zone has been defined for a profile, it is retrieved and used by the journey. If it hasn&#39;t, the time zone used is the one defined in the time zone field.

![Profile time zone configuration in data sources for personalized timing](assets/journey73.png)

>[!NOTE]
>
>The profile time zone works with the **timeZone** field existing in the **Preference Details** field group.

## Use time zones in expressions {#timezone-in-expressions}

The start and end dates of a journey cannot be linked to a specific time zone. They are automatically associated to the instance&#39;s time zone.
