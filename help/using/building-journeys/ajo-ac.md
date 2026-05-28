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
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 472
ht-degree: 1%

---

# 使用Campaign v7/v8傳送訊息 {#campaign-v7-v8-use-case}

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
