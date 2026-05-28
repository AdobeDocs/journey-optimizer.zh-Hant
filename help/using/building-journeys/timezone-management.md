---
solution: Journey Optimizer
product: journey optimizer
title: 時區管理
description: 瞭解時區管理
feature: Journeys, Profiles
topic: Content Management
role: User
level: Intermediate
keywords: 時區，屬性，歷程，條件，時間，日期，自訂
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/PdwGEuWqJcncbkokE0eOhMaEk9L0AmCJ--VZBxxtDDU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 378
ht-degree: 23%

---

# 時區管理 {#timezone_management}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="歷程時區"
>abstract="選取歷程的時區。 當使用固定時區時，對於所有進入歷程的個人來說都是相同的。"


您可以在歷程的[屬性](../building-journeys/journey-properties.md#timezone)中定義時區。

若要存取歷程屬性，請選取畫面右上角的鉛筆圖示。

此時區將用於包含時間元素的歷程的每個活動，例如：

* [時間條件](../building-journeys/conditions.md#time_condition)
* [日期條件](../building-journeys/conditions.md#date_condition)
* [自訂等待](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

您可以選取[固定時區](#fixed-timezone)，或選擇使用使用者設定檔](#timezone-from-profiles)中定義的時區[。

## 定義固定時區 {#fixed-timezone}

時區可以固定。 清除預先定義的時區，並從下拉式清單中選取一個時區。 如果您使用固定時區，則所有進入歷程的個人都將使用相同的時區。

若要這麼做，請在&#x200B;**[!UICONTROL 歷程屬性]**&#x200B;窗格中選取時區。

![歷程屬性中的時區選取下拉式清單](assets/journey72.png)

## 使用輪廓時區 {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="使用輪廓時區"
>abstract="勾選此選項，即可在&#x200B;**「等待」**&#x200B;及&#x200B;**「條件」**&#x200B;活動中使用即時輪廓時區。 如果已經定義輪廓的時區，系統便會取得該時區並在歷程中使用。 若未設定，將使用上面時區欄位中定義的時區。"

如果歷程的進入事件具有名稱空間，這表示歷程可以存取[!DNL Adobe Experience Platform]的即時客戶設定檔服務，您可能會想要使用設定檔層級定義的時區。 若要這麼做，請在&#x200B;**屬性**&#x200B;中勾選&#x200B;**在等待和條件中使用設定檔時區**。 預設不會勾選此選項。

如果為設定檔定義了時區，則會擷取該時區並由歷程使用。 如果沒有，則使用的時區是時區欄位中定義的時區。

![資料來源中的個人化計時設定檔時區設定](assets/journey73.png)

>[!NOTE]
>
>設定檔時區與&#x200B;**偏好設定詳細資料**&#x200B;欄位群組中現有的&#x200B;**時區**&#x200B;欄位搭配使用。

## 在運算式中使用時區 {#timezone-in-expressions}

歷程的開始和結束日期無法連結至特定時區。 它們會自動關聯至執行個體的時區。
