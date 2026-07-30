---
solution: Journey Optimizer
product: journey optimizer
title: 使用 Campaign v7/v8 傳送訊息
description: 瞭解如何使用Campaign v7/v8傳送訊息
feature: Journeys, Integrations, Custom Actions, Use Cases
topic: Administration
role: Admin, Developer, User
level: Intermediate, Experienced
keywords: 歷程，訊息，行銷活動，整合
exl-id: b07feb98-b2ae-476c-8fcb-873b308176f0
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/btOUMO8tgvwLD7kjVdgpj6I6QXRrj1iTD3P8AUrqJFM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1025
ht-degree: 0%

---

# 使用Campaign v7/v8傳送訊息 {#campaign-v7-v8-use-case}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何使用與Adobe Campaign v7和v8的整合，從歷程傳送電子郵件，包括建立異動範本、事件和動作。

>[!ENDSHADEBOX]

此使用案例說明使用與[!DNL Adobe Campaign] v7和[!DNL Adobe Campaign] v8的整合來傳送電子郵件所需的所有步驟。

>[!NOTE]
>
>若要使用此整合，您必須有Campaign v7/v8版本編號9125或更高版本。

首先，在Campaign中建立交易式電子郵件範本。 然後，在Journey Optimizer中建立事件、動作並設計歷程。

若要進一步瞭解Campaign整合，請參閱以下頁面：

* [建立行銷活動動作](../action/acc-action.md)
* [在歷程中使用動作](../building-journeys/using-adobe-campaign-v7-v8.md)。

**[!DNL Adobe Campaign]**

必須布建您的Campaign執行個體才能進行此整合。 必須設定異動訊息傳送功能。

1. 登入您的Campaign控制例項。

1. 在&#x200B;**管理** > **平台** > **列舉**&#x200B;下，選取&#x200B;**事件型別** (eventType)列舉。 建立新的事件型別（範例中為「journey-event」）。 稍後寫入JSON檔案時，請使用事件型別的內部名稱。

   ![使用結構描述和欄位選取來設定[!DNL Adobe Journey Optimizer]中的事件](assets/accintegration-uc-1.png)

1. 中斷連線並重新連線至執行個體，建立作業才會生效。

1. 在&#x200B;**訊息中心** > **異動訊息範本**&#x200B;下，根據先前建立的事件型別建立新的電子郵件範本。

   ![事件組態顯示名稱空間和設定檔識別碼設定](assets/accintegration-uc-2.png)

1. 設計您的範本。 在此範例中，個人化會套用至設定檔的名字和訂單編號。 名字在[!DNL Adobe Experience Platform]資料來源中，而訂單編號是來自Journey Optimizer事件的欄位。 請確定您在Campaign中使用正確的欄位名稱。

   ![事件裝載預覽顯示具有設定檔和事件資料的JSON結構](assets/accintegration-uc-3.png)

1. 發佈您的交易式範本。

   ![複製API整合之裝載識別碼的事件複製按鈕](assets/accintegration-uc-4.png)

1. 撰寫與範本相對應的JSON裝載。

```
{
     "channel": "email",
     "eventType": "journey-event",
     "email": "Email address",
     "ctx": {
          "firstName": "First name", "purchaseOrderNumber": "Purchase order number"
     }
}
```

* 對於頻道，您需要輸入「電子郵件」。
* 對於eventType，請使用先前建立之事件型別的內部名稱。
* 電子郵件地址將是變數，因此您可以鍵入任何標籤。
* 在ctx底下，個人化欄位也是變數。

**Journey Optimizer**

1. 建立事件。 包含「purchaseOrderNumber」欄位。

   [!DNL Adobe Campaign]傳統整合的![自訂動作設定畫面](assets/accintegration-uc-5.png)

1. 在Journey Optimizer中建立與行銷活動範本對應的動作。 在&#x200B;**動作型別**&#x200B;下拉式清單中，選取&#x200B;**[!DNL Adobe Campaign]Classic**。

   ![動作型別選取專案顯示[!DNL Adobe Campaign]傳統選項](assets/accintegration-uc-6.png)

1. 按一下&#x200B;**裝載欄位**&#x200B;並貼上先前建立的JSON。

   ![動作整合的Campaign帳戶選擇下拉式清單](assets/accintegration-uc-7.png)

1. 針對電子郵件地址和兩個個人化欄位，將&#x200B;**常數**&#x200B;變更為&#x200B;**變數**。

   ![具有Campaign整合之欄位對應的動作裝載組態](assets/accintegration-uc-8.png)

1. 現在建立新歷程，並從先前建立的事件開始。

   ![已設定事件和行銷活動動作的歷程畫布](assets/accintegration-uc-9.png)

1. 新增動作，並將每個欄位對應至Journey Optimizer中的正確欄位。

   ![動態值的運算式編輯器對映動作引數](assets/accintegration-uc-10.png)

1. 測試您的歷程。

   ![使用事件觸發程式和行銷活動動作執行完成歷程流程](assets/accintegration-uc-11.png)

1. 您現在可以發佈您的歷程。

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面提供使用Adobe Campaign v7/v8整合從Adobe Journey Optimizer傳送異動電子郵件的逐步使用案例，涵蓋行銷活動範本建立、事件和動作設定，以及歷程設計。

**意圖：**
* 在Adobe Campaign v7/v8中設定交易式電子郵件範本以與Journey Optimizer搭配使用
* 在Journey Optimizer中建立事件，其中包含自訂欄位，例如採購單編號
* 使用JSON裝載在Journey Optimizer中建立和設定Campaign Classic動作
* 將歷程事件欄位對應至動作設定中的Campaign個人化變數
* 建立並發佈觸發Campaign交易電子郵件的歷程

**字彙表：**
* **異動訊息**：根據事件傳送即時觸發電子郵件的Campaign功能；必須先設定此整合，才可使用&#x200B;*（產品特定）*
* **事件型別(eventType)**：在Campaign中定義的列舉值，可識別交易式事件的型別；其內部名稱已在JSON裝載&#x200B;*（產品專屬）*&#x200B;中參照
* **Campaign Classic動作**：連線至Adobe Campaign v7/v8以傳送交易式訊息的Journey Optimizer動作型別&#x200B;*（產品專用）*
* **裝載欄位**： JSON結構已貼入Journey Optimizer動作，該動作定義傳送至行銷活動&#x200B;*（產品專屬）*&#x200B;的資料欄位

**護欄：**
* 此整合需要Campaign v7/v8版本編號9125或更高版本
* 必須先在Campaign執行個體中設定異動訊息傳送功能，才能使用
* 在Campaign中建立新事件型別後，您必須中斷連線並重新連線至執行個體，事件型別才會生效
* 在動作中設為「常數」的Personalization欄位值必須變更為「變數」，才能在執行階段允許動態填入

**術語：**
* 正式名稱：Adobe Campaign v7/v8 — 首字母縮寫：ACC — 變體：Campaign Classic、Campaign v7、Campaign v8
* 同義字： &quot;eventType&quot; = &quot;event type internal name&quot;
* 請勿混淆：「Campaign Classic動作」≠「自訂動作」（Campaign Classic動作是ACC整合的特定內建動作型別）

**常見問題集：**
* **問：這項整合需要哪個Campaign版本？**  — 需要Campaign v7/v8版本編號9125或更高版本。
* **問：在開始之前，必須在Campaign中設定哪些專案？**  — 必須設定異動訊息功能，而且必須根據事件型別建立異動電子郵件範本。
* **問：如何在Journey Optimizer動作中讓個人化欄位成為動態欄位？**  — 在動作裝載設定中，針對將在執行階段填入的欄位，將欄位設定從「常數」變更為「變數」。
* **問：在這個使用案例中，名字個人化資料來自何處？**  — 名字來自Adobe Experience Platform資料來源，而訂單編號來自Journey Optimizer事件裝載。
* **問：如何將Journey Optimizer動作連結至Campaign範本？**  — 選取「Adobe Campaign Classic」作為動作型別，然後貼上符合交易式訊息範本結構的JSON裝載。

+++
