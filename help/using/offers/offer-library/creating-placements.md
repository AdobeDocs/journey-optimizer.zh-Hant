---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 建立版位
description: 瞭解如何建立優惠方案的版位
badge: label="舊版" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: dfaf887e-d4b3-45b0-8297-bffdb0abff4d
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 31%

---

# 建立版位 {#create-placements}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement"
>title="刊登"
>abstract="位置是用於展示產品建議的容器。它有助於確保正確的產品建議內容顯示在訊息中的正確位置。產品建議放置環境是從「元件」選單建立的。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement_request"
>title="請求設定"
>abstract="啟用「**[!UICONTROL 允許多個產品建議放置環境之間有重複產品]**」選項，讓系統能夠考量在多個放置環境提供相同的產品建議。使用「**[!UICONTROL 請求產品建議]**」欄位來調整傳回的產品建議數量。例如，您若選取「2」，則會針對所選取的決策範圍顯示最佳的 2 項產品建議。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement_response"
>title="回應格式"
>abstract="您可以使用「**[!UICONTROL 包含內容]**」和「**[!UICONTROL 包含中繼資料]**」選項來指定在 API 回應中是否回傳產品建議的內容和中繼資料。您可以選擇包含所有中繼資料或僅包含特定欄位。「包含後設資料」的值預設為「真」。"

版位有助於確保正確的選件內容顯示在訊息的正確位置。 將內容新增至產品建議時，系統會要求您選取可顯示該內容的版位。

➡️ [在此影片中瞭解如何建立刊登版位](#video)

在下列範例中，有三個版位，分別對應至不同型別的內容(影像、文字、HTML)。

![](../assets/offers_placement_schema.png)

可在&#x200B;**[!UICONTROL 元件]**&#x200B;功能表中存取位置清單。 篩選器可協助您根據特定頻道或內容擷取版位。

![](../assets/placements_filter.png)

若要建立版位，請依照下列步驟進行：

1. 按一下&#x200B;**[!UICONTROL 建立位置]**。

   ![](../assets/offers_placement_creation.png)

1. 定義位置的屬性：

   * **[!UICONTROL 名稱]**：位置名稱。 請務必定義有意義的名稱，以更輕鬆擷取該名稱。
   * **[!UICONTROL 頻道型別]**：將使用位置的頻道。
   * **[!UICONTROL 內容型別]**：允許刊登版位顯示的內容型別：文字、HTML、影像連結或JSON。
   * **[!UICONTROL 描述]**：位置的描述（選擇性）。

   ![](../assets/offers_placement_creation_properties.png)

1. **[!UICONTROL 要求設定]**&#x200B;和&#x200B;**[!UICONTROL 回應格式]**&#x200B;區段提供其他引數：

   * **[!UICONTROL 允許跨版位重複專案]**：控制是否可以在不同的版位中多次建議相同的選件。 如果啟用，系統會針對多個位置考慮相同的選件。 依預設，引數會設為false。

     如果決策請求中任何位置的此選項設為false，則請求中的所有位置都將繼承「false」設定。

   * **[!UICONTROL 要求優惠]**：依預設，會為每個設定檔傳回一個決定範圍的優惠。 您可以使用此選項調整傳回的優惠方案數量。 例如，您若選取「2」，則會針對所選取的決策範圍顯示最佳的 2 項產品建議。

   * **[!UICONTROL 包含內容]** / **[!UICONTROL 包含中繼資料]**：指定是否應該在API回應中傳回選件的內容和中繼資料。 您可以選擇包含所有中繼資料或僅包含特定欄位。「包含後設資料」的值預設為「真」。

   如果您使用[決策API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html?lang=zh-Hant)，也可以將這些引數直接設定到您的API要求中。 不過，在使用者介面中設定這些變數有助於節省時間，因為您不需要在每個API要求中傳遞這些變數。 請注意，如果您同時在使用者介面和API要求中設定引數，來自API要求的值將會優先於來自介面的值。

   >[!NOTE]
   >
   >如果您使用[Edge Decisioning API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?lang=zh-Hant&)，則無法在您的請求中設定這些引數。 您必須在此畫面中定義這些變數。
   >
   >如果您使用[批次決策API](../api-reference/offer-delivery-api/batch-decisioning-api.md)，您可以在此畫面或您的API要求中設定這些引數。 如果畫面和APi請求之間的引數值不相符，則會使用請求值。

1. 按一下&#x200B;**[!UICONTROL 儲存]**&#x200B;以確認。

1. 位置建立後，會顯示在「位置」清單中。 您可以選取它以顯示其屬性並加以編輯。

   ![](../assets/placement_created.png)

## 作法影片{#video}

瞭解如何在決定管理中建立刊登版位。

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

