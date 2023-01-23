---
solution: Journey Optimizer
product: journey optimizer
title: 新增個人化優惠方案
description: 了解如何將個人化優惠方案新增至訊息
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 選件，決策，電子郵件，個人化，決策
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 1%

---

# 新增個人化優惠方案 {#deliver-personalized-offers}

在 [!DNL Journey Optimizer] 電子郵件中，您可以插入將利用決策管理引擎的決策，以便選擇最合適的優惠方案來提供給客戶。

例如，您可以新增決策，在電子郵件中顯示特別折扣優惠，該優惠會根據收件者的忠誠度而有所不同。

如需如何建立和管理優惠方案的詳細資訊，請參閱 [本節](../offers/get-started/starting-offer-decisioning.md).

若 **完整端對端範例** 顯示如何設定優惠方案、在決策中使用優惠方案，以及在電子郵件中運用此決策、結帳 [本節](../offers/offers-e2e.md#insert-decision-in-email).

➡️ [了解如何在此影片中將選件新增為個人化](#video-offers)

## 在電子郵件中插入決策 {#insert-offers}

>[!CAUTION]
>
>開始之前，您必須 [定義優惠方案決策](../offers/offer-activities/create-offer-activities.md).

若要將決策插入電子郵件訊息，請遵循下列步驟：

1. 建立您的電子郵件，然後開啟電子郵件設計工具來設定其內容。

1. 新增 **[!UICONTROL 優惠方案決策]** 內容元件。

   ![](assets/deliver-offer-component.png)

   了解如何在 [本節](content-components.md).

1. 此 **[!UICONTROL 優惠方案決策]** 標籤。 按一下 **[!UICONTROL 選擇優惠方案決策]**.

   ![](assets/deliver-offer-tab.png)

1. 在顯示的視窗中，選取與您要顯示之選件相對應的位置。

   [版位](../offers/offer-library/creating-placements.md) 是用來展示優惠方案的容器。 在此範例中，我們將使用「電子郵件至上影像」位置。 此版位已建立在優惠方案庫中，以顯示位於訊息頂端的影像類型優惠方案。

1. 與所選版位相符的決策會顯示。 選取要在內容元件中使用的決策，然後按一下 **[!UICONTROL 新增]**.

   >[!NOTE]
   >
   >只有與所選位置相容的決策才會顯示在清單中。 在此範例中，只有一個優惠方案活動符合「電子郵件最上層影像」位置。

   ![](assets/deliver-offer-placement.png)

決定現在已新增至元件。

儲存變更後，您的選件即可在歷程中傳送訊息時顯示給相關設定檔。

>[!NOTE]
>
>當您更新直接或間接參考訊息的優惠方案、備援優惠方案、優惠方案收集或優惠方案決策時，更新會自動反映在對應的訊息中。

## 在電子郵件中預覽優惠方案 {#preview-offers-in-email}

您可以使用 **[!UICONTROL 選件]** 或內容元件箭頭。

![](assets/deliver-offer-preview.png)

若要使用客戶設定檔顯示屬於決策一部分的不同選件，請遵循下列步驟。

1. 按一下 **[!UICONTROL 預覽]**.

   ![](assets/deliver-offer-preview-button.png)

   >[!NOTE]
   >
   >您必須有測試設定檔可供預覽訊息。 了解如何 [建立測試設定檔](../segment/creating-test-profiles.md).

1. 若要選擇用來識別測試設定檔的命名空間，請選取 **[!UICONTROL 電子郵件]** 從 **[!UICONTROL 身分命名空間]** 欄位。

   >[!NOTE]
   >
   >在此範例中，我們將使用 **電子郵件** 命名空間。 深入了解Adobe Experience Platform身分識別命名空間 [在本節](../segment/get-started-identity.md).

1. 在身分識別命名空間清單中，選取 **[!UICONTROL 電子郵件]** 按一下 **[!UICONTROL 選擇]**.

1. 在 **[!UICONTROL 身分值]** 欄位中，輸入要識別測試設定檔的值。 在此範例中，輸入測試設定檔的電子郵件地址。

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

1. 新增其他設定檔，以便根據設定檔資料測試不同的訊息變體。

   ![](assets/deliver-offer-test-profiles.png)

1. 按一下 **[!UICONTROL 預覽]** 標籤來測試訊息。

1. 選取測試設定檔。 會顯示與所選設定檔（女性）對應的選件。

   ![](assets/deliver-offer-test-profile-female-preview.png)

1. 選取其他測試設定檔，以預覽訊息每個變體的電子郵件內容。 在訊息內容中，現在會顯示與所選測試設定檔（現在為男性）對應的選件。

   ![](assets/deliver-offer-test-profile-male-preview.png)

進一步了解檢查訊息預覽的詳細步驟，位於 [本節](#preview-your-messages).

## 作法影片{#video-offers}

了解如何將決策管理元件新增至 [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)

