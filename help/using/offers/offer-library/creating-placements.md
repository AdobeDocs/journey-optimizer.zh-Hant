---
title: 建立版位
description: 了解如何建立優惠方案的版位
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: dfaf887e-d4b3-45b0-8297-bffdb0abff4d
source-git-commit: 51f93270c969875e94cc3e98919149d67d764ed1
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 11%

---

# 建立版位 {#create-placements}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement"
>title="版位"
>abstract="位置是用於展示優惠的容器。它有助於確保正確的優惠內容顯示在訊息中的正確位置。位置是從「元件」選單建立的。"

版位有助於確保正確的優惠方案內容顯示在訊息中的正確位置。 將內容新增至優惠方案時，系統會要求您選取可顯示該內容的版位。

➡️ [了解如何在此影片中建立版位](#video)

在下列範例中，有三個版位對應於不同的內容類型(影像、文字、HTML)。

![](../assets/offers_placement_schema.png)

位置清單可在 **[!UICONTROL 元件]** 功能表。 篩選器可協助您根據特定頻道或內容擷取版位。

![](../assets/placements_filter.png)

要建立版位，請執行以下步驟：

1. 按一下 **[!UICONTROL 建立版位]**.

   ![](../assets/offers_placement_creation.png)

1. 定義版位的屬性：

   * **[!UICONTROL 名稱]**:版位的名稱。 請務必定義有意義的名稱，以便更輕鬆擷取名稱。
   * **[!UICONTROL 通道類型]**:將使用版位的管道。
   * **[!UICONTROL 內容類型]**:允許版位顯示的內容類型：文字、HTML、影像連結或JSON。
   * **[!UICONTROL 說明]**:版位的說明（選用）。

   ![](../assets/offers_placement_creation_properties.png)


1. 此 **[!UICONTROL 請求設定]** 和 **[!UICONTROL 回應格式]** 各節提供其他參數：

   * **[!UICONTROL 允許跨版位重複項目]**:控制是否可以在不同版位間多次建議相同優惠方案。 如果已啟用，系統會針對多個版位考慮相同的優惠方案。 依預設，參數會設為false。

      如果對決策請求中的任何版位將此選項設為false，則請求中的所有版位都會繼承「false」設定。

   * **[!UICONTROL 要求選件]**:依預設，會為每個設定檔傳回一個決策範圍選件。 您可以使用此選項調整傳回選件的數量。 例如，若您選取2，則會針對所選決策範圍顯示最佳2個選件。

   * **[!UICONTROL 包含內容]** / **[!UICONTROL 包含中繼資料]**:在API回應中指定是否應傳回選件的內容和中繼資料。 您只能包含所有中繼資料或特定欄位。 依預設，「包含中繼資料」值會設為true。
   如果您使用的是 [決策API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html). 不過，在使用者介面中設定這些參數可協助您節省時間，因為您不必在每個API請求中傳遞這些參數。 請注意，如果您同時在使用者介面和API請求中設定參數，則來自API請求的值將優於來自介面的值。

   >[!NOTE]
   >
   >如果您使用 [Edge Decisioning API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?)，您無法將這些參數設定到您的請求中。 您需要在此畫面中定義它們。
   >
   >如果您使用 [批次決策API](../api-reference/offer-delivery-api/batch-decisioning-api.md)，您可以在此畫面或API請求中設定這些參數。 如果畫面與APi要求之間的參數值不符，則會使用要求值。

1. 按一下 **[!UICONTROL 儲存]** 確認。

1. 版位建立後，會顯示在版位清單中。 您可以選取它以顯示其屬性並加以編輯。

   ![](../assets/placement_created.png)

## 作法影片{#video}

了解如何在決策管理中建立版位。

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

