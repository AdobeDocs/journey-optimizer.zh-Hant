---
solution: Journey Optimizer
product: journey optimizer
title: '[!DNL Adobe Campaign] v7/v8動作'
description: 瞭解 [!DNL Adobe Campaign] v7/v8動作
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: 歷程，整合，行銷活動， v7， v8
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
version: Journey Orchestration
source-git-commit: 692b539f2c7623a14192558c3eba55d90c54f22d
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 4%

---

# [!DNL Adobe Campaign] v7/v8動作 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="自訂動作"
>abstract="如果您有[!DNL Adobe Campaign] v7或v8，則可整合。 它可讓您使用[!DNL Adobe Campaign]異動訊息功能來傳送電子郵件、推播通知及簡訊。"

如果您有[!DNL Adobe Campaign] v7或v8，則可整合。 它可讓您使用[!DNL Adobe Campaign]異動訊息功能來傳送電子郵件、推播通知及簡訊。

Journey Optimizer與Campaign執行個體之間的連線在布建時由Adobe設定。 聯絡Adobe。

**何時使用**：當您的傳訊依賴Campaign交易範本、Campaign特定資料模型或現有的Campaign傳遞工作流程時，請使用Campaign v7/v8動作。

**先決條件**

* 已布建您的[!DNL Adobe Campaign] v7/v8執行個體，並透過Adobe連線至Journey Optimizer。
* 您有權存取Campaign異動訊息及必要的許可權。

為了讓此功能發揮作用，您需要設定專用動作。 請參閱本[章節](../action/acc-action.md)。

此[區段](../building-journeys/ajo-ac.md)中呈現端對端使用案例。

1. 設計您的歷程，從事件開始。 請參閱[本章節](../building-journeys/journey.md)。
1. 在浮動視窗的&#x200B;**動作**&#x200B;區段中，選取行銷活動動作並將其新增至您的歷程。
1. 在&#x200B;**動作引數**&#x200B;中，會顯示訊息裝載中預期的所有欄位。 您需要將每個欄位與您要使用的欄位相對應，無論是從事件還是從資料來源進行。 這類似於自訂動作。 請參閱本[章節](../building-journeys/using-custom-actions.md)。

>[!NOTE]
>
>* Campaign v7/v8動作可與相同歷程中的原生頻道動作搭配使用。 這不適用於Campaign Standard動作。 請參閱[促銷活動護欄](../start/guardrails.md#ac-g)。
>* Campaign v7/v8動作無法用於「讀取對象」或「對象資格」活動。 請參閱護欄頁面中的讀取對象和對象資格護欄。

![[!DNL Adobe Campaign] v7/v8動作組態與整合設定](assets/accintegration2.png)
