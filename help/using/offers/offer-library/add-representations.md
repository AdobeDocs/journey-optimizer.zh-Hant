---
title: 將代表新增至優惠方案
description: 瞭解如何將代表新增至您的優惠
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# 將代表新增至優惠方案 {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="表示方式"
>abstract="新增代表以定義訊息中顯示優惠的位置。 優惠方案的代表性愈多，在不同的版位內容中使用優惠方案的機會就愈多。"

選件可顯示在訊息中的不同位置：在含有影像的頂端橫幅中、作為段落中的文字、作為HTML區塊等。 優惠方案的代表性愈多，在不同的版位內容中使用優惠方案的機會就愈多。

## 設定優惠的宣告 {#representations}

若要新增一或多個代表至您的優惠方案並加以設定，請遵循下列步驟。

1. 對於第一個表示，從選取 **[!UICONTROL 頻道]** 將會使用的區段。

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >只有所選頻道的可用版位會顯示在 **[!UICONTROL 刊登]** 下拉式清單。

1. 從清單中選取位置。

   您也可以使用「 」旁的按鈕 **[!UICONTROL 刊登]** 下拉式清單來瀏覽所有版位。

   ![](../assets/browse-button-placements.png)

   您仍然可以在這裡根據版位頻道和/或內容型別來篩選版位。 選擇位置並按一下 **[!UICONTROL 選取]**.

   ![](../assets/browse-placements.png)

1. 將內容新增至您的代表。 瞭解如何 [本節](#content).

1. 新增影像或URL等內容時，您可以指定 **[!UICONTROL 目的地連結]**：按一下選件的使用者將被導向至對應的頁面。

   ![](../assets/offer-destination-link.png)

1. 最後，選取您選擇的語言，以協助識別並管理要向使用者顯示的內容。

1. 若要新增其他表示法，請使用 **[!UICONTROL 新增表示方式]** 按鈕並視需要新增任意數量的表示。

   ![](../assets/offer-add-representation.png)

1. 新增所有表示後，請選取 **[!UICONTROL 下一個]**.

## 定義表示的內容 {#content}

您可以將不同型別的內容新增到表現中。

>[!NOTE]
>
>只有與版位內容型別對應的內容才可供使用。

### 新增影像 {#images}

如果所選版位為影像型別，您可以新增來自 **Adobe Experience Cloud資產** 資料庫，資產集中存放庫，由 [!DNL Adobe Experience Manager Assets].

>[!NOTE]
>
> 使用方式 [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}，您必須部署 [!DNL Assets Essentials] ，並確保使用者屬於 **Assets Essentials消費者使用者** 或/和 **Assets Essentials使用者** 產品設定檔。 進一步瞭解 [此頁面](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target="_blank"}.

1. 選擇 **[!UICONTROL 資產庫]** 選項。

1. 選取 **[!UICONTROL 瀏覽]**.

   ![](../assets/offer-browse-asset-library.png)

1. 瀏覽資產以選取您選擇的影像

1. 按一下 **[!UICONTROL 選取]**.

   ![](../assets/offer-select-asset.png)

### 新增HTML或JSON檔案 {#html-json}

如果所選版位為HTML型別，您也可以新增來自的HTML或JSON內容 [Adobe Experience Cloud資產庫](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"})。

例如，您已在下列位置建立HTML電子郵件範本： [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"} 而且您想要將該檔案用於選件內容。 您可以直接將範本上傳到 **資產庫** 以便在優惠的表示中重複使用它。

若要在表現中重複使用您的內容，請瀏覽 **資產庫** 如所述 [本節](#images) 並選取您選擇的HTML或JSON檔案。

![](../assets/offer-browse-asset-library-json.png)

### 新增URL {#urls}

若要從外部公共位置新增內容，請選取「 」 **[!UICONTROL URL]**，然後輸入要新增內容的URL位址。

您可以使用個人化編輯器個人化URL。 進一步瞭解 [個人化](../../personalization/personalize.md#use-expression-editor).

![](../assets/offer-content-url.png)

例如，您想要個人化顯示為選件的影像。 你想讓喜歡城市度假的使用者看紐約的天際線，也想讓喜歡海灘度假的使用者看夏威夷的北岸。

使用個人化編輯器，使用聯合結構描述擷取儲存在Adobe Experience Platform中的設定檔屬性。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

如果您指定 **[!UICONTROL 目的地連結]**，您也可以個人化URL，將按一下選件的使用者導向至該URL。

### 新增自訂文字 {#custom-text}

您也可以在選取相容版位時插入文字型內容。

1. 選取 **[!UICONTROL 自訂]** 選項並按一下 **[!UICONTROL 新增內容]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >此選項不適用於影像型別的位置。

1. 輸入要在優惠方案顯示的文字。

   ![](../assets/offer-text-content.png)

   您可以使用個人化編輯器個人化您的內容。 進一步瞭解 [個人化](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >僅限 **[!UICONTROL 設定檔屬性]**， **[!UICONTROL 受眾]** 和 **[!UICONTROL 輔助函式]** 來源可用於「決定管理」。

## 根據內容資料個人化表示{#context-data}

當內容資料傳入時 [邊緣決策](../api-reference/offer-delivery-api/edge-decisioning-api.md) 呼叫，您可以利用這些資料以動態方式個人化表現。 例如，您可以根據即時因素（例如在做出決定時的目前天氣條件）來定製優惠方案的表示方式。

若要這麼做，請使用將上下文資料變數直接併入表示內容 `profile.timeSeriesEvents.` 名稱空間。

以下是根據使用者的作業系統來個人化優惠方案表現的語法範例：

```
 {%#if profile.timeSeriesEvents.device.model = "Apple"%}ios{%else%}android{%/if%} 
```

包含內容資料的對應Edge decisioning請求如下：

```
{
    "body": {
        "xdm": {
            "identityMap": {
                "Email": [
                    {
                        "id": "xyz@abc.com"
                    }
                ]
            },
            "device": {
                "model": "Apple"
            }
        },
        "extra": {
            "query": {
                "decisionScopes": [
                    "eyJ4ZG06..."
                ]
            }
        }
    }
}
```
