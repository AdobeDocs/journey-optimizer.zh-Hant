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
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 761
ht-degree: 11%

---

# [!DNL Adobe Campaign] v7/v8 動作 {#using_campaign_v7-v8}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何使用Adobe Campaign v7和v8整合，透過Campaign交易訊息從您的歷程傳送電子郵件、推播通知和SMS。

>[!ENDSHADEBOX]

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

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;本頁說明如何在Journey Optimizer歷程中使用Adobe Campaign v7/v8作為動作，透過Campaign異動訊息傳送電子郵件、推播通知和簡訊。

**意圖：**

* 將Campaign v7/v8動作新增至傳送異動訊息的歷程
* 將歷程事件或資料來源欄位對應至行銷活動訊息裝載引數
* 將Campaign v7/v8動作與原生Journey Optimizer頻道動作結合在同一歷程中
* 設定Campaign v7/v8整合所需的專用動作

**字彙表：**

* **促銷活動異動訊息**： Adobe Campaign v7/v8功能可透過與Journey Optimizer *（產品專屬）*&#x200B;整合的專用動作，傳送觸發訊息（電子郵件、簡訊、推播）
* **動作引數**：歷程活動窗格中將歷程資料對應至預期行銷活動訊息承載&#x200B;*（產品專屬）*&#x200B;的欄位

**護欄：**

* Journey Optimizer與Campaign執行個體之間的連線在布建時由Adobe設定；請聯絡Adobe以啟用連線。
* 必須先設定專用動作，歷程浮動視窗中才能使用Campaign v7/v8動作。
* Campaign v7/v8動作無法用於「讀取對象」或「對象資格」活動。
* 存取Campaign交易訊息和Campaign的必要許可權是先決條件。

**術語：**

* 正式名稱：Adobe Campaign v7/v8 — 縮寫：ACC — 變體：Campaign v7、Campaign v8、Campaign Classic
* 請勿混淆：「Campaign v7/v8動作」（可與原生動作搭配使用）≠「Campaign Standard動作」（無法與相同歷程中的原生動作結合）

**常見問題集：**

* **問：誰會設定Journey Optimizer與Campaign v7/v8之間的連線？** — Adobe會在布建時設定連線；您必須聯絡Adobe才能進行設定。
* **問：Campaign v7/v8動作可以和同一歷程中的原生Journey Optimizer頻道動作結合嗎？**  — 是，Campaign v7/v8動作可搭配原生頻道動作使用；Campaign Standard動作則非如此。
* **問：Campaign v7/v8動作是否可搭配「讀取對象」或「對象資格」活動使用？**  — 否，Campaign v7/v8動作無法與讀取對象或對象資格活動搭配使用。
* **問：如何將歷程資料對應至行銷活動訊息承載？**  — 在「動作引數」窗格中，將每個預期的裝載欄位對應至歷程事件或資料來源的對應欄位，其方式與自訂動作相同。

+++
