---
solution: Journey Optimizer
product: journey optimizer
title: 關於歷程事件的ExperienceEvent結構
description: 瞭解歷程事件的ExperienceEvent結構描述
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: 結構描述， XDM，平台，串流，擷取，歷程
exl-id: f19749c4-d683-4db6-bede-9360b9610eef
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '831'
ht-degree: 0%

---

# 關於[!DNL Journey Optimizer]事件的ExperienceEvent結構描述 {#about-experienceevent-schemas}

[!DNL Journey Optimizer]事件是指透過串流擷取傳送至Adobe Experience Platform的XDM體驗事件。

因此，為[!DNL Journey Optimizer]設定事件的重要先決條件是，您熟悉Adobe Experience Platform的體驗資料模型（或XDM）、如何組成XDM體驗事件結構，以及如何將XDM格式的資料串流到Adobe Experience Platform。

## [!DNL Journey Optimizer]個事件的結構描述需求  {#schema-requirements}

為[!DNL Journey Optimizer]設定事件的第一步是確保您已定義代表該事件的XDM結構描述，以及已建立資料集以在Adobe Experience Platform上記錄該事件的執行個體。 嚴格來說，沒有必要為事件建立資料集，但將事件傳送至特定資料集可讓您維護使用者的事件歷史記錄，以供日後參考和分析，因此總是不錯的做法。 如果您還沒有適合事件的結構描述和資料集，這兩項工作都可以在Adobe Experience Platform網頁介面中完成。

![](assets/schema1.png)

將用於[!DNL Journey Optimizer]事件的任何XDM結構描述都應符合下列要求：

* 結構描述必須是XDM ExperienceEvent類別。

  ![](assets/schema2.png)

* 對於系統產生的事件，結構描述必須包括Orchestration eventID欄位群組。 [!DNL Journey Optimizer]使用此欄位來識別歷程中使用的事件。

  ![](assets/schema3.png)

* 宣告身分欄位，以識別事件中的個別設定檔。 如果未指定身分，則可使用身分對應。 不建議採用此做法。

  ![](assets/schema4.png)

* 如果您希望這些資料稍後可在歷程中查詢，請標籤設定檔的結構描述和資料集。

  ![](assets/schema5.png)

  ![](assets/schema6.png)

* 您可以隨意加入資料欄位，以擷取您要與事件一併加入的任何其他內容資料，例如關於使用者的資訊、產生事件的裝置、位置或與事件相關的任何其他有意義的情況。

  ![](assets/schema7.png)

  ![](assets/schema8.png)

## 利用結構描述關係{#leverage_schema_relationships}

Adobe Experience Platform可讓您定義結構描述之間的關係，以便將一個資料集用作另一個資料集的查詢表。

假設您的品牌資料模型有一個結構描述擷取購買。 您也有產品目錄的結構描述。 您可以擷取購買結構描述中的產品ID，並使用關係從產品目錄中查詢更完整的產品詳細資訊。 舉例來說，這可讓您為所有購買筆記型電腦的客戶建立受眾，而不需明確列出所有筆記型電腦ID，或將每個單一產品的詳細資訊擷取到交易系統中。

若要定義關係，來源結構描述中需要有專用欄位，在此案例中是購買結構描述中的產品ID欄位。 此欄位需要參考目的地結構描述中的產品ID欄位。 必須為設定檔啟用來源和目的地表格，而且目的地結構描述必須將這個通用欄位定義為其主要身分。

以下是為設定檔啟用的產品目錄結構描述，其產品ID已定義為主要身分。

![](assets/schema9.png)

以下是購買結構描述，其關係定義在產品ID欄位上。

![](assets/schema10.png)

>[!NOTE]
>
>在[Experience Platform檔案](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/configure-relationships-between-schemas.html?lang=zh-Hant)中進一步瞭解結構描述關係。

在Journey Optimizer中，您可以善用連結表格中的所有欄位：

* 設定商務或單一事件時，[瞭解詳情](../event/experience-event-schema.md#unitary_event_configuration)
* 在歷程中使用條件時，[瞭解詳情](../event/experience-event-schema.md#journey_conditions_using_event_context)
* 在訊息個人化中，[瞭解詳情](../event/experience-event-schema.md#message_personalization)
* 在自訂動作個人化中，[瞭解詳情](../event/experience-event-schema.md#custom_action_personalization_with_journey_event_context)

### 陣列{#relationships_limitations}

您可以在字串陣列上定義結構描述關係，例如，產品ID清單。

![](assets/schema15.png)

您也可以與物件陣列內部的屬性定義結構描述關係，例如購買資訊清單（產品ID、產品名稱、價格、折扣）。 查閱值將在歷程（條件、自訂動作等）和個人化訊息中使用。

![](assets/schema16.png)

### 事件設定{#unitary_event_configuration}

連結的結構描述欄位可用於單一和業務事件設定：

* 瀏覽事件設定畫面中的事件結構欄位時。
* 定義系統產生事件的條件時。

![](assets/schema11.png)

連結的欄位無法使用：

* 在事件索引鍵公式中
* 在事件id條件中（規則型事件）

若要瞭解如何設定單一事件，請參閱此[頁面](../event/about-creating.md)。

### 使用事件內容的歷程條件{#journey_conditions_using_event_context}

您可以使用查詢表格中的資料，連結至用於條件建置之歷程中的事件（運算式編輯器）。

在歷程中新增條件、編輯運算式，並在運算式編輯器中展開事件節點。

![](assets/schema12.png)

若要瞭解如何定義歷程條件，請參閱此[頁面](../building-journeys/condition-activity.md)。

### 訊息個人化{#message_personalization}

個人化訊息時，可使用連結的欄位。 相關欄位會顯示在從歷程傳遞至訊息的內容中。

![](assets/schema14.png)

若要瞭解如何使用內容歷程資訊個人化訊息，請參閱此[頁面](../personalization/personalization-use-case.md)。

### 使用歷程事件內容進行自訂動作個人化{#custom_action_personalization_with_journey_event_context}

設定歷程自訂動作活動的動作引數時，可使用連結的欄位。

![](assets/schema13.png)

若要瞭解如何使用自訂動作，請參閱此[頁面](../building-journeys/using-custom-actions.md)。
