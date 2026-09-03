---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用動作
description: 瞭解如何使用動作
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Experienced
keywords: 動作，歷程，訊息，傳送，連線
exl-id: 7f0cda1d-daf0-4d4c-9978-ddef81473813
TQID: https://experienceleague.adobe.com/u-fLClLKK9cC7D2BwO5vxdW11tywPDRWzOMBtYUj5Ts
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 62bc5f833b5612570ba50c98519a2f9c07d0bd5e
workflow-type: tm+mt
source-wordcount: 397
ht-degree: 35%

---

# 開始使用自訂動作 {#about_actions}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解動作和自訂動作如何讓您透過REST API呼叫提供個人化體驗並連線協力廠商系統，讓您可以延伸歷程至內建訊息以外的範圍。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_list"
>title="自訂動作"
>abstract="動作是指您向客戶提供個人化即時體驗時使用的連結，例如推播通知、電子郵件、簡訊或您在業務中使用的任何其他數位參與方式。"

動作是指您向客戶提供個人化即時體驗時使用的連結，例如推播通知、電子郵件、簡訊或您在業務中使用的任何其他數位參與方式。

➡️ [在影片中探索此功能](#video)

[!DNL Journey Optimizer]隨附內建訊息功能。 自訂動作可讓您設定第三方系統的連線，以傳送訊息或 API 呼叫。 您可以使用任何提供者提供的任何服務來設定動作，這些服務可經由 REST API，搭配 JSON 格式的承載進行呼叫。

* 如果您使用Adobe Campaign v7或v8，整合可應要求提供。 請參見[此頁面](../action/acc-action.md)。

* 如果您使用協力廠商系統來傳送訊息，例如Epsilon、Facebook、Adobe Developer、Firebase等，則需要建立和設定自訂動作。 請參見[此頁面](../action/about-custom-action-configuration.md)。

>[!CAUTION]
>
>自訂動作的設定必須由&#x200B;**技術使用者**&#x200B;執行。

自訂動作是技術使用者定義的其他動作，可供行銷人員使用：設定後，自訂動作會顯示在您歷程的左側浮動視窗，位於&#x200B;**[!UICONTROL 動作]**&#x200B;類別中。 請在[此頁面](../building-journeys/about-journey-activities.md#action-activities)了解更多。

若要檢視動作清單或設定新動作，請在[管理]功能表區段中選取&#x200B;**[!UICONTROL 組態]**。 在&#x200B;**[!UICONTROL 動作]**&#x200B;區段中，按一下&#x200B;**[!UICONTROL 管理]**。 畫面隨即顯示動作清單。 如需介面的詳細資訊，請參閱[此頁面](../start/user-interface.md)。

![](assets/custom1.png)

瞭解如何在此專屬頁面[&#128279;](../action/troubleshoot-custom-action.md)上疑難排解自訂動作。

## 作法影片 {#video}

瞭解如何設定自訂動作。

>[!VIDEO](https://video.tv.adobe.com/v/3428396?quality=12)

## 其他資源

瀏覽以下章節，進一步瞭解設定及使用自訂動作：

* [設定您的自訂動作](../action/about-custom-action-configuration.md) — 瞭解如何建立和設定自訂動作
* [使用自訂動作](../building-journeys/using-custom-actions.md) — 瞭解如何在歷程中使用自訂動作
* [將集合傳遞至自訂動作引數](../building-journeys/collections.md) — 瞭解如何在執行階段動態填入的自訂動作引數中傳遞集合
* [自訂動作疑難排解](../action/troubleshoot-custom-action.md) — 瞭解如何疑難排解自訂動作

