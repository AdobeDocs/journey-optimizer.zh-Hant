---
title: 新增表示法至優惠方案
description: 了解如何將表示法新增至優惠方案
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 1%

---

# 新增表示法至優惠方案 {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="表示"
>abstract="新增表示法以定義您的選件在訊息中的顯示位置。 優惠方案表示得越多，在不同版位內容中使用優惠方案的機會就越多。"

選件可顯示在訊息中的不同位置：在頂端橫幅中，以影像、段落中的文字、HTML區塊等形式顯示。 優惠方案表示得越多，在不同版位內容中使用優惠方案的機會就越多。

## 設定優惠方案的陳述 {#representations}

若要新增一或多個表示法並加以設定，請遵循下列步驟。

1. 對於第一個表示，請從選取 **[!UICONTROL 管道]** 會使用。

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >只有所選管道的可用位置會顯示在 **[!UICONTROL 版位]** 下拉式清單。

1. 從清單中選取位置。

   您也可以使用 **[!UICONTROL 版位]** 下拉式清單來瀏覽所有版位。

   ![](../assets/browse-button-placements.png)

   您仍可在此根據版位的頻道和/或內容類型篩選版位。 選擇位置並按一下 **[!UICONTROL 選擇]**.

   ![](../assets/browse-placements.png)

1. 將內容新增至您的表示法。 了解 [本節](#content).

1. 新增內容（例如影像或URL）時，您可以指定 **[!UICONTROL 目的地連結]**:點按選件的使用者會導向至對應的頁面。

   ![](../assets/offer-destination-link.png)

1. 最後，選取您選擇的語言，以協助識別及管理要向使用者顯示的內容。

1. 要添加其他表示，請使用 **[!UICONTROL 添加表示]** 按鈕，並視需要新增表示法。

   ![](../assets/offer-add-representation.png)

1. 添加所有表示形式後，請選擇 **[!UICONTROL 下一個]**.

## 定義表示的內容 {#content}

您可以將不同類型的內容添加到表示中。

>[!NOTE]
>
>只有與版位內容類型對應的內容可供使用。

### 新增影像 {#images}

如果選取的版位是影像類型，您可以新增來自 **Adobe Experience Cloud Asset** 程式庫，由 [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> 使用 [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}, you need to deploy [!DNL Assets Essentials] for your organization and make sure that users are a part of the **Assets Essentials Consumer Users** or/and **Assets Essentials Users** Product profiles. Learn more on [this page](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target="_blank"}.

1. 選擇 **[!UICONTROL 資產庫]** 選項。

1. 選擇 **[!UICONTROL 瀏覽]**.

   ![](../assets/offer-browse-asset-library.png)

1. 瀏覽資產以選取您所選的影像

1. 按一下&#x200B;**[!UICONTROL 「選取」]**。

   ![](../assets/offer-select-asset.png)

### 新增HTML或JSON檔案 {#html-json}

如果選取的版位是HTML類型，您也可以新增來自的HTML或JSON內容 [Adobe Experience Cloud Asset Library](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"})。

例如，您在 [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"} 而且您想要將該檔案用於優惠方案內容。 您只需將範本上傳至 **資產庫** 以便在優惠方案的陳述式中重複使用。

要重複使用表示中的內容，請瀏覽 **資產庫** 如 [本節](#images) 並選取您所選擇的HTML或JSON檔案。

![](../assets/offer-browse-asset-library-json.png)

### 新增URL {#urls}

若要從外部公用位置新增內容，請選取 **[!UICONTROL URL]**，然後輸入要新增的內容的URL位址。

您可以使用運算式編輯器個人化URL。 深入了解 [個人化](../../personalization/personalize.md#use-expression-editor).

![](../assets/offer-content-url.png)

例如，您想要個人化顯示為選件的影像。 你希望那些喜歡城市度假的用戶看到紐約的天際線，以及喜歡海灘度假的用戶看到夏威夷的北岸。

使用運算式編輯器，使用聯合結構擷取儲存在Adobe Experience Platform中的設定檔屬性。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

如果您指定 **[!UICONTROL 目的地連結]**，您也可以個人化URL，將點按選件的使用者導向至該URL。

### 新增自訂文字 {#custom-text}

選取相容的版位時，您也可以插入文字類型內容。

1. 選取 **[!UICONTROL 自訂]** 選項，然後按一下 **[!UICONTROL 新增內容]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >此選項不適用於影像類型版位。

1. 輸入要在選件中顯示的文字。

   ![](../assets/offer-text-content.png)

   您可以使用運算式編輯器個人化您的內容。 深入了解 [個人化](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >僅 **[!UICONTROL 設定檔屬性]**, **[!UICONTROL 區段成員資格]** 和 **[!UICONTROL 輔助函式]** 來源可用於決策管理。

