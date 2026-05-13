---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Campaign v7/v8 動作
description: 瞭解Adobe Campaign v7/v8動作
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: 歷程，整合，行銷活動， v7， v8
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Saqu6Kkm1Rdym10IuwLF88Fj-hT2crAwENajyKBeY5w
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 28%

---

# [!DNL Adobe Campaign] v7/v8 動作 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="自訂動作"
>abstract="如果您有 [!DNL Adobe Campaign] v7 或 v8，則可整合。 這可讓您使用 [!DNL Adobe Campaign] 交易型訊息功能傳送電子郵件、推播通知及簡訊。"

如果您有 [!DNL Adobe Campaign] v7 或 v8，則可整合。 這可讓您使用 [!DNL Adobe Campaign] 交易型訊息功能傳送電子郵件、推播通知及簡訊。

Journey Optimizer 和 Campaign 執行個體之間的連線在佈建時由 Adobe 設定。 聯絡Adobe。

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
