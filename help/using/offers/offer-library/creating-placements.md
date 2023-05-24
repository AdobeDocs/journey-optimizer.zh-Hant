---
title: 建立版位
description: 瞭解如何為您的產品建立放置
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

放置有助於確保在郵件中的適當位置顯示適當的優惠內容。 將內容新增至優惠方案時，系統會要求您選取可顯示該內容的版位。

➡️ [瞭解如何在此視頻中建立放置](#video)

在下面的示例中，有三個放置位置，對應於不同類型的內容(影像、文本、HTML)。

![](../assets/offers_placement_schema.png)

可在 **[!UICONTROL 元件]** 的子菜單。 篩選器可幫助您根據特定渠道或內容檢索放置位置。

![](../assets/placements_filter.png)

要建立放置，請執行以下步驟：

1. 按一下 **[!UICONTROL 建立放置]**。

   ![](../assets/offers_placement_creation.png)

1. 定義放置的屬性：

   * **[!UICONTROL 名稱]**:放置的名稱。 確保定義有意義的名稱，以便更輕鬆地檢索它。
   * **[!UICONTROL 通道類型]**:將使用放置的通道。
   * **[!UICONTROL 內容類型]**:允許放置顯示的內容類型：文本、HTML、影像連結或JSON。
   * **[!UICONTROL 說明]**:位置的說明（可選）。

   ![](../assets/offers_placement_creation_properties.png)


1. 的 **[!UICONTROL 請求設定]** 和 **[!UICONTROL 響應格式]** 各節提供了其他參數：

   * **[!UICONTROL 允許跨放置重複項]**:控制是否可以在不同位置多次建議同一報價。 如果啟用，系統將考慮同一優惠進行多次放置。 預設情況下，參數設定為false。

      如果此選項對於決策請求中的任何放置設定為false，則請求中的所有放置都將繼承「false」設定。

   * **[!UICONTROL 請求聘用]**:預設情況下，每個配置檔案都返回一個決策範圍。 您可以使用此選項調整返回的優惠數量。 例如，如果選擇2，則最佳的2個優惠將顯示為所選決策範圍。

   * **[!UICONTROL 包括內容]** / **[!UICONTROL 包括元資料]**:指定是否應在API響應中返回提供的內容和元資料。 您只能包含所有元資料或特定欄位。 預設情況下，「包括」元資料值設定為true。
   如果使用 [決策API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html)。 但是，在用戶介面中配置它們可以幫助您節省時間，因為您不必在每個API請求中傳遞它們。 請注意，如果在用戶介面和API請求中都配置了參數，則API請求中的值將優先於介面中的參數。

   >[!NOTE]
   >
   >如果您使用 [邊緣判定API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?)，不能將這些參數設定到請求中。 您需要在此螢幕中定義它們。
   >
   >如果您使用 [批處理決策API](../api-reference/offer-delivery-api/batch-decisioning-api.md)，可以在此螢幕或API請求中設定這些參數。 如果螢幕和APi請求之間的參數值不匹配，將使用請求值。

1. 按一下 **[!UICONTROL 保存]** 確認。

1. 建立放置後，它將顯示在放置清單中。 可以選擇它以顯示其屬性並對其進行編輯。

   ![](../assets/placement_created.png)

## 操作說明影片{#video}

瞭解如何在決策管理中建立放置位置。

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

