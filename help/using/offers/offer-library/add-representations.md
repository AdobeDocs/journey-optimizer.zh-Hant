---
title: 向優惠添加表示
description: 瞭解如何向您的產品添加表示法
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: 0fa8ba1dc16062ea1553f9978752f3c018cec4c6
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 1%

---

# 向優惠添加表示 {#add-representations}

可以在消息中的不同位置顯示優惠：在帶有影像、段落中的文本、HTML塊等的頂部標題中。 一個要約擁有的表述越多，在不同的放置環境中使用該要約的機會就越多。

## 配置優惠的表示法 {#representations}

要將一個或多個表示形式添加到您的產品中並配置它們，請執行以下步驟。

1. 對於第一個表示，首先選擇 **[!UICONTROL Channel]** 會被使用。

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >僅在中顯示所選通道的可用位置 **[!UICONTROL Placement]** 的子菜單。

1. 從清單中選取一個放置。

   您還可以使用 **[!UICONTROL Placement]** 下拉清單，瀏覽所有放置。

   ![](../assets/browse-button-placements.png)

   您仍然可以根據其頻道和/或內容類型篩選放置。 選擇放置，然後按一下 **[!UICONTROL Select]**。

   ![](../assets/browse-placements.png)

1. 將內容添加到您的表示法。 瞭解 [此部分](#content)。

1. 添加影像或URL等內容時，可以指定 **[!UICONTROL Destination link]**:按一下優惠的用戶將被定向到相應頁面。

   ![](../assets/offer-destination-link.png)

1. 最後，選擇您選擇的語言以幫助確定和管理要顯示給用戶的內容。

1. 要添加其他表示法，請使用 **[!UICONTROL Add representation]** 按鈕並根據需要添加多個表示法。

   ![](../assets/offer-add-representation.png)

1. 添加所有表示法後，選擇 **[!UICONTROL Next]**。

## 定義表示法的內容 {#content}

可以向表示法中添加不同類型的內容。

>[!NOTE]
>
>只有與放置的內容類型對應的內容可供使用。

### 新增影像 {#images}

如果所選位置是影像類型，則可添加來自 **Adobe Experience Cloud資產** 庫，由 [!DNL Adobe Experience Manager Assets Essentials]。

>[!NOTE]
>
> 使用 [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=en){target=&quot;_blank&quot;}，需要部署 [!DNL Assets Essentials] 確保用戶是組織的一部分 **Assets Essentials消費者用戶** 或 **Assets Essentials用戶** 產品配置檔案。 瞭解更多 [此頁](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}。

1. 選取 **[!UICONTROL Asset library]** 選項。

1. 選擇「**[!UICONTROL Browse]**」。

   ![](../assets/offer-browse-asset-library.png)

1. 瀏覽資產以選擇您選擇的影像

1. 按一下「**[!UICONTROL Select]**」。

   ![](../assets/offer-select-asset.png)

### 添加URL {#urls}

要從外部公共位置添加內容，請選擇 **[!UICONTROL URL]**，然後輸入要添加的內容的URL地址。

![](../assets/offer-content-url.png)

### 添加自定義文本 {#custom-text}

在選擇相容的放置時，也可插入文本類型內容。

1. 選擇 **[!UICONTROL Custom]** 選項 **[!UICONTROL Add content]**。

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >此選項不可用於影像類型放置。

1. 鍵入將在優惠中顯示的文本。

   ![](../assets/offer-text-content.png)

   可以使用表達式編輯器個性化您的內容。 瞭解更多 [個性化](../../personalization/personalize.md#use-expression-editor)。

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >僅 **[!UICONTROL Profile attributes]**。 **[!UICONTROL Segment memberships]** 和 **[!UICONTROL Helper functions]** 源可用於決策管理。
