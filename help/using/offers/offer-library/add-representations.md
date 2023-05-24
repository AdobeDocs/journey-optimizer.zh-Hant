---
title: 向優惠添加表示
description: 瞭解如何向您的產品添加表示法
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 9%

---

# 向優惠添加表示 {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="表示方式"
>abstract="新增表示方式以定義您的優惠在訊息中顯示的位置。優惠具有的表示方式越多，在不同位置內容中使用優惠的機會就越多。"

可以在消息中的不同位置顯示優惠：在帶有影像、段落中的文本、HTML塊等的頂部標題中。 優惠具有的表示方式越多，在不同位置內容中使用優惠的機會就越多。

## 配置優惠的表示法 {#representations}

要將一個或多個表示形式添加到您的產品中並配置它們，請執行以下步驟。

1. 對於第一個表示，首先選擇 **[!UICONTROL 頻道]** 會被使用。

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >僅在中顯示所選通道的可用位置 **[!UICONTROL 放置]** 的子菜單。

1. 從清單中選取一個放置。

   您還可以使用 **[!UICONTROL 放置]** 下拉清單，瀏覽所有放置。

   ![](../assets/browse-button-placements.png)

   您仍然可以根據其頻道和/或內容類型篩選放置。 選擇放置，然後按一下 **[!UICONTROL 選擇]**。

   ![](../assets/browse-placements.png)

1. 將內容添加到您的表示法。 瞭解 [此部分](#content)。

1. 添加影像或URL等內容時，可以指定 **[!UICONTROL 目標連結]**:按一下優惠的用戶將被定向到相應頁面。

   ![](../assets/offer-destination-link.png)

1. 最後，選擇您選擇的語言以幫助確定和管理要顯示給用戶的內容。

1. 要添加其他表示法，請使用 **[!UICONTROL 添加表示法]** 按鈕並根據需要添加多個表示法。

   ![](../assets/offer-add-representation.png)

1. 添加所有表示法後，選擇 **[!UICONTROL 下一個]**。

## 定義表示法的內容 {#content}

可以向表示法中添加不同類型的內容。

>[!NOTE]
>
>只有與放置的內容類型對應的內容可供使用。

### 新增影像 {#images}

如果所選位置是影像類型，則可添加來自 **Adobe Experience Cloud資產** 庫，由 [!DNL Adobe Experience Manager Assets Essentials]。

>[!NOTE]
>
> 使用 [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}, you need to deploy [!DNL Assets Essentials] for your organization and make sure that users are a part of the **Assets Essentials Consumer Users** or/and **Assets Essentials Users** Product profiles. Learn more on [this page](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target="_blank"}。

1. 選擇 **[!UICONTROL 資產庫]** 的雙曲餘切值。

1. 選擇 **[!UICONTROL 瀏覽]**。

   ![](../assets/offer-browse-asset-library.png)

1. 瀏覽資產以選擇您選擇的影像

1. 按一下&#x200B;**[!UICONTROL 「選取」]**。

   ![](../assets/offer-select-asset.png)

### 添加HTML或JSON檔案 {#html-json}

如果所選位置是HTML類型，則還可以添加HTML或來自 [Adobe Experience Cloud資產庫](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"})。

例如，您在中建立了HTML電子郵件模板 [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"} 而且您希望將該檔案用於您的優惠內容。 您只需將模板上載到 **資產庫** 能夠在報價表中重新使用它。

要在表示形式中重用內容，請瀏覽 **資產庫** 如所述 [此部分](#images) 並選擇您選擇的HTML或JSON檔案。

![](../assets/offer-browse-asset-library-json.png)

### 添加URL {#urls}

要從外部公共位置添加內容，請選擇 **[!UICONTROL URL]**，然後輸入要添加的內容的URL地址。

可以使用表達式編輯器對URL進行個性化。 瞭解更多 [個性化](../../personalization/personalize.md#use-expression-editor)。

![](../assets/offer-content-url.png)

例如，您希望個性化顯示為優惠的影像。 你希望那些喜歡城市度假的用戶能看到紐約的天際線，而那些喜歡海灘度假的用戶能看到夏威夷的北岸。

使用表達式編輯器可使用聯合架構檢索儲存在Adobe Experience Platform中的配置檔案屬性。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

如果指定 **[!UICONTROL 目標連結]**，您還可以個性化URL，按一下此優惠的用戶將定向到該URL。

### 添加自定義文本 {#custom-text}

在選擇相容的放置時，也可插入文本類型內容。

1. 選擇 **[!UICONTROL 自定義]** 選項 **[!UICONTROL 添加內容]**。

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
   >僅 **[!UICONTROL 配置檔案屬性]**。 **[!UICONTROL 段成員資格]** 和 **[!UICONTROL 幫助程式函式]** 源可用於決策管理。

