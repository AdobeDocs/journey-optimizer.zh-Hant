---
title: 關於行程事件的ExperienceEvent架構
description: 瞭解旅程事件的ExperienceEvent架構
feature: Schemas
topic: Administration
role: Admin
level: Intermediate
exl-id: f19749c4-d683-4db6-bede-9360b9610eef
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 4%

---

# 關於ExperienceEvent架構 [!DNL Journey Optimizer] 事件 {#about-experienceevent-schemas}

[!DNL Journey Optimizer] 事件是通過流式接收發送到Adobe Experience Platform的XDM體驗事件。

因此，為 [!DNL Journey Optimizer] 您熟悉Adobe Experience Platform的經驗資料模型（或XDM），以及如何構成XDM體驗事件模式，以及如何將XDM格式的資料流式傳輸到Adobe Experience Platform。

## 架構要求 [!DNL Journey Optimizer] 事件  {#schema-requirements}

設定事件的第一步 [!DNL Journey Optimizer] 是為了確保您定義了用於表示事件的XDM架構，並建立了用於記錄Adobe Experience Platform事件實例的資料集。 不一定需要為事件建立資料集，但將事件發送到特定資料集將允許您維護用戶的事件歷史記錄以供將來參考和分析，因此始終是個好主意。 如果您還沒有適合您事件的模式和資料集，則可以在Adobe Experience PlatformWeb介面中完成這兩項任務。

![](assets/schema1.png)

將用於 [!DNL Journey Optimizer] 事件應滿足以下要求：

* 架構必須是XDM ExperienceEvent類。

   ![](assets/schema2.png)

* 對於系統生成的事件，架構必須包括Orchestration eventID欄位組。 [!DNL Journey Optimizer] 使用此欄位標識在行程中使用的事件。

   ![](assets/schema3.png)

* 聲明標識欄位以標識事件的主題。 如果未指定標識，則可以使用標識映射。 不建議採用此做法。

   ![](assets/schema4.png)

* 如果希望此資料稍後在「旅程」中可供查找，請將架構和資料集標籤為配置檔案。

   ![](assets/schema5.png)

   ![](assets/schema6.png)

* 您可以自由地包括資料欄位，以捕獲您希望與事件一起包括的任何其他上下文資料，例如有關用戶、從中生成事件的設備、位置或與事件相關的任何其它有意義的情況的資訊。

   ![](assets/schema7.png)

   ![](assets/schema8.png)

## 利用綱要關係{#leverage_schema_relationships}

Adobe Experience Platform 可讓您定義綱要之間的關係，以便將一個資料集用作另一個資料集的查詢表。 

假設您的品牌資料模型具有模式捕獲購買。 您還具有產品目錄的架構。 您可以在採購方案中捕獲產品ID，並使用關係從產品目錄中查找更完整的產品詳細資訊。 這允許您為購買筆記型電腦的所有客戶建立一個細分市場，而不必明確列出所有筆記型電腦ID或捕獲事務系統中的每個產品詳細資訊。

要定義關係，需要在源架構中有一個專用欄位，在這種情況下，採購架構中的產品ID欄位。 此欄位需要引用目標架構中的產品ID欄位。 必須為配置檔案啟用源表和目標表，並且目標架構必須將該公共欄位定義為其主標識。

下面是為配置檔案啟用的產品目錄方案，其中產品ID定義為主標識。

![](assets/schema9.png)

下面是在產品ID欄位中定義的具有關係的採購方案。

![](assets/schema10.png)

>[!NOTE]
>
>瞭解有關中架構關係的詳細資訊 [Experience Platform文檔](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/configure-relationships-between-schemas.html?lang=en)。

在Journey Optimizer，然後可以利用連結表中的所有欄位：

* 配置業務或單一事件時， [閱讀更多內容](../event/experience-event-schema.md#unitary_event_configuration)
* 在旅途中使用條件時， [閱讀更多內容](../event/experience-event-schema.md#journey_conditions_using_event_context)
* 在消息個性化中， [閱讀更多內容](../event/experience-event-schema.md#message_personalization)
* 在自定義操作個性化中， [閱讀更多內容](../event/experience-event-schema.md#custom_action_personalization_with_journey_event_context)

### 事件設定{#unitary_event_configuration}

連結的架構欄位在統一和業務事件配置中可用：

* 瀏覽事件配置螢幕中的事件模式欄位時。
* 定義系統生成事件的條件時。

![](assets/schema11.png)

連結的欄位不可用：

* 在事件鍵公式中
* 事件id條件（基於規則的事件）

要瞭解如何配置統一事件，請參閱 [頁](../event/about-creating.md)。

### 使用事件上下文的行程條件{#journey_conditions_using_event_context}

您可以使用連結到行程中使用的事件的查找表中的資料進行條件生成（表達式編輯器）。

在旅程中添加條件，編輯表達式並在表達式編輯器中展開事件節點。

![](assets/schema12.png)

要瞭解如何定義行程條件，請參閱 [頁](../building-journeys/condition-activity.md)。

### 消息個性化{#message_personalization}

當個性化消息時，連結欄位可用。 相關欄位顯示在從行程傳遞到消息的上下文中。

![](assets/schema14.png)

要瞭解如何使用上下文行程資訊個性化郵件，請參閱 [頁](../personalization/personalization-use-case.md)。

### 具有行程事件上下文的自定義操作個性化{#custom_action_personalization_with_journey_event_context}

在配置行程自定義操作活動的操作參數時，連結欄位可用。

![](assets/schema13.png)

要瞭解如何使用自定義操作，請參閱 [頁](../building-journeys/using-custom-actions.md)。
