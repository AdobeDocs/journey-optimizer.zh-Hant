---
title: 建立集合
description: 瞭解如何使用集合來組織優惠方案
feature: Decision Management, Collections
topic: Integrations
role: User
level: Intermediate
exl-id: 0c8808e3-9148-4a33-9fd5-9218e02c2dfd
source-git-commit: 88e7140183700da0283fa00d89f6fff2c71c138f
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 7%

---

# 建立集合 {#create-collections}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_collection"
>title="關於優惠集合"
>abstract="有了優惠集合，您可以將優惠重新群組到您選擇的類別中以組織優惠。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic"
>title="動態集合"
>abstract="使用集合限定詞來動態限定集合的優惠。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static"
>title="靜態集合"
>abstract="使用狀態、集合限定詞、日期和管道等條件，手動選取優惠並將其群組在一起。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static_select"
>title="靜態集合預覽"
>abstract="靜態集合是透過手動選取要包含在集合中的個別優惠方案所建置。 集合只能透過手動新增更多優惠方案進行更新。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic_select"
>title="動態集合預覽"
>abstract="動態集合會根據集合限定詞來收集優惠。 這些集合會自動更新。 例如，如果使用「sports」集合限定詞建立新選件，系統就會自動將其新增至對應的集合。"

集合可讓您將優惠重新分組為您選擇的類別，以組織優惠。 例如，您可以建立只包含運動相關優惠方案的「運動」集合。

➡️ [在影片中探索此功能](#video)

可在&#x200B;**[!UICONTROL 優惠方案]**&#x200B;功能表中存取優惠方案集合清單。

![](../assets/collections_list.png)

您可以建立兩種型別的集合：

* **動態集合**&#x200B;是根據集合限定詞（先前稱為「標籤」）的優惠集合。 這些集合會自動更新。 例如，如果使用選取的集合限定詞建立新選件，則會自動將其新增至集合。

* **靜態集合**&#x200B;是透過手動選取要包含在集合中的個別優惠方案所建置的集合。 集合只能透過手動新增更多優惠方案進行更新。

若要建立集合，請依照下列步驟進行：

1. 移至&#x200B;**[!UICONTROL 集合]**&#x200B;標籤，然後按一下&#x200B;**[!UICONTROL 建立集合]**。

1. 指定要建立的集合名稱和型別。

   ![](../assets/collection_create.png)

1. 若要建立動態集合，請使用左窗格選取要新增至集合之優惠方案的集合限定詞，然後按一下[儲存]。**** 所有具有所選集合限定詞的優惠方案都會儲存在集合中。

   如需集合限定詞建立的詳細資訊，請參閱[建立集合限定詞](../offer-library/creating-tags.md)。

   ![](../assets/dynamic_collection.png)

1. 若要建立靜態集合，請使用左窗格來篩選優惠方案清單（狀態、集合限定詞、日期、管道、內容型別），然後選取要新增至集合的優惠方案。

   ![](../assets/static_collection.png)

   >[!NOTE]
   >
   >靜態集合不會自動更新。 若要將優惠方案新增至靜態集合，您需要編輯並手動新增。

1. 若要指派自訂或核心資料使用標籤給靜態集合，請選取&#x200B;**[!UICONTROL 管理存取權]**。 [進一步瞭解物件層級存取控制(OLAC)](../../administration/object-based-access.md)

   >[!NOTE]
   >
   >動態集合無法使用OLAC。 它必須在選件層級進行管理。 因此，如果您沒有這些優惠方案的存取權，您可能會在動態集合中看不到任何優惠方案。

1. 集合建立後，會顯示在清單中。 您可以選取它來進行編輯或刪除。

   ![](../assets/collection_created.png)

## 操作說明影片 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329376?quality=12)


