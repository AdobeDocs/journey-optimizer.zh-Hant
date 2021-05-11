---
title: 時區管理
description: 瞭解時區管理
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 2%

---

# 時區管理 {#timezone_management}

![](../assets/do-not-localize/badge.png)

您可以在歷程的[properties](../building-journeys/journey-gs.md#change-properties)中定義時區。

若要存取「屬性」，請按一下螢幕右上角的鉛筆圖示。

此時區將用於歷程中包含時間元素(例如：

* [時間條件](../building-journeys/condition-activity.md#time_condition)
* [日期條件](../building-journeys/condition-activity.md#date_condition)
* [自訂等待](../building-journeys/wait-activity.md#custom)
* [固定日期等待](../building-journeys/wait-activity.md#fixed_date)

您可以選擇時區，或選擇使用用戶配置檔案中定義的時區。

## 定義固定時區{#fixed-timezone}

時區也可以固定。 清除預先定義的時區，並從下拉式清單中選擇一個時區。 如果您使用固定的時區，則所有進入旅程的個人都會使用相同的時區。

若要這麼做，請在&#x200B;**[!UICONTROL Properties]**&#x200B;中選取時區。

![](../assets/journey73.png)

## 使用描述檔來定義旅程時區{#timezone-from-profiles}

如果旅程的登入事件具有命名空間，表示旅程可以到達Adobe Experience Platform的即時客戶個人檔案服務，則時區會預先定義為旅程中個人個人檔案中指定的時區。

如果在Adobe Experience Platform描述檔中定義時區，則可在歷程中擷取時區。

如果個人的描述檔不包含時區，則擷取的時區將是時區欄位中定義的時區。

若要這麼做，請在&#x200B;**[!UICONTROL Properties]**&#x200B;中，勾選&#x200B;**[!UICONTROL Use Profile timezone in timers and conditions]**。

![](../assets/journey72.png)

## 在運算式{#timezone-in-expressions}中使用時區

旅程的開始和結束日期無法連結至特定時區。 它們會自動關聯至例項的時區。
