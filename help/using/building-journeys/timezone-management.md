---
solution: Journey Optimizer
product: journey optimizer
title: 時區管理
description: 了解時區管理
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 時區，屬性，歷程，條件，時間，日期，自訂
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 2%

---

# 時區管理 {#timezone_management}

您可以在 [屬性](../building-journeys/journey-gs.md#change-properties) 你的旅程。

若要存取「歷程屬性」，請按一下畫面右上方的鉛筆圖示。

此時區將用於歷程中包含時間元素的每個活動，例如：

* [時間條件](../building-journeys/condition-activity.md#time_condition)
* [日期條件](../building-journeys/condition-activity.md#date_condition)
* [自訂等待](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

您可以選取時區或選擇使用使用者設定檔中定義的時區。

>[!NOTE]
>
>設定檔時區可搭配 **timeZone** 欄位 **首選項詳細資訊** 欄位群組。

## 定義固定時區 {#fixed-timezone}

時區也可以固定。 清除預先定義的時區，然後從下拉式清單中選取時區。 如果您使用固定時區，則所有進入歷程的個人都會使用相同時區。

若要這麼做，請在 **[!UICONTROL 歷程屬性]** ，請選擇時區。

![](assets/journey72.png)

## 使用設定檔來定義歷程時區 {#timezone-from-profiles}

如果歷程的登入事件具有命名空間，表示歷程可存取Adobe Experience Platform的即時客戶個人檔案服務，您可能會想使用設定檔層級定義的時區。 若要這麼做，請輸入 **屬性**，檢查 **在等待和條件中使用設定檔時區**. 預設不會勾選此選項。

如果已為設定檔定義時區，則會由歷程擷取並使用。 如果尚未使用，則使用的時區將是時區欄位中定義的時區。

![](assets/journey73.png)

## 在運算式中使用時區 {#timezone-in-expressions}

歷程的開始和結束日期無法連結至特定時區。 它們會自動與執行個體的時區相關聯。
