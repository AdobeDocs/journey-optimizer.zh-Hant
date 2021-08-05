---
title: 新增個人化優惠
description: 了解如何將個人化優惠方案新增至訊息
feature: 歷程
topic: 內容管理
role: User
level: Intermediate
source-git-commit: a2aed1dbfa53aee6f5fe0aeec52773d22bc4ed29
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 2%

---

# 新增個人化優惠 {#deliver-personalized-offers}

在[!DNL Journey Optimizer]電子郵件訊息中，您可以插入將運用優惠方案決策引擎的決策（先前稱為「優惠方案活動」），以便挑選最合適的優惠方案並傳送給客戶。

例如，您可以新增決策，在電子郵件中顯示特別折扣優惠，該優惠會根據收件者的忠誠度而有所不同。

如需如何建立和管理選件的詳細資訊，請參閱[此區段](offers/get-started/starting-offer-decisioning.md)。

若要取得&#x200B;**完整的端對端範例**，說明如何設定選件，請在決策中使用這些選件，並在電子郵件中運用此決策，請查看[此區段](offers/offers-e2e.md#insert-decision-in-email)。

➡️ [了解如何在此影片中新增選件作為個人化內容](#video-offers)

## 在電子郵件中插入決策 {#insert-offers}

>[!CAUTION]
>
>開始之前，您必須[定義優惠方案決策](offers/offer-activities/create-offer-activities.md)。

若要將決策插入電子郵件訊息，請遵循下列步驟：

1. 建立您的電子郵件，然後開啟電子郵件設計工具來設定其內容。

1. 新增&#x200B;**[!UICONTROL Offer decision]**&#x200B;內容元件。

   ![](assets/deliver-offer-component.png)

   了解如何在[本小節](content-components.md)中使用內容元件。

1. **[!UICONTROL Offer decision]**&#x200B;標籤會顯示在右側浮動視窗中。 按一下「**[!UICONTROL Select Offer decision]**」。

   ![](assets/deliver-offer-tab.png)

1. 在顯示的視窗中，選取與您要顯示之選件相對應的位置。

   [](offers/offer-library/creating-placements.md) 佈置是用來展示優惠方案的容器。在此範例中，我們將使用「電子郵件至上影像」位置。 此版位已建立在優惠方案庫中，以顯示位於訊息頂端的影像類型優惠方案。

1. 選取要在內容元件中使用的優惠方案活動，然後按一下&#x200B;**[!UICONTROL Add]**。

   >[!NOTE]
   >
   >只有與所選位置相容的決策才會顯示在清單中。 在此範例中，只有一個優惠方案活動符合「電子郵件最上層影像」位置。

   ![](assets/deliver-offer-placement.png)

優惠方案活動現在已新增至元件。


## 在電子郵件中預覽優惠方案 {#preview-offers-in-email}

您可以使用&#x200B;**[!UICONTROL Offers]**&#x200B;區段或內容元件箭頭，預覽屬於新增至電子郵件之決策的不同選件。

![](assets/deliver-offer-preview.png)

若要使用客戶設定檔顯示屬於決策一部分的不同選件，請遵循下列步驟。

1. 按一下「**[!UICONTROL Preview]**」。

   ![](assets/deliver-offer-preview-button.png)

   >[!NOTE]
   >
   >您必須有測試設定檔可供預覽訊息。 了解如何[建立測試設定檔](building-journeys/creating-test-profiles.md)。

1. 若要選擇要用於識別測試設定檔的命名空間，請從&#x200B;**[!UICONTROL Identity namespace]**&#x200B;欄位中選取&#x200B;**[!UICONTROL Email]** 。

   >[!NOTE]
   >
   >在此範例中，我們將使用&#x200B;**Email**&#x200B;命名空間。 了解更多Adobe Experience Platform身分識別命名空間[，請參閱本節](get-started-identity.md)。

1. 在身分識別命名空間清單中，選擇&#x200B;**[!UICONTROL Email]**&#x200B;並按一下&#x200B;**[!UICONTROL Select]**。

1. 在&#x200B;**[!UICONTROL Identity value]**&#x200B;欄位中，輸入值以識別測試設定檔。 在此範例中，輸入測試設定檔的電子郵件地址。

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

1. 新增其他設定檔，以便根據設定檔資料測試不同的訊息變體。

   ![](assets/deliver-offer-test-profiles.png)

1. 按一下&#x200B;**[!UICONTROL Preview]**&#x200B;標籤以測試您的訊息。

1. 選取測試設定檔。 會顯示與所選設定檔（女性）對應的選件。

   ![](assets/deliver-offer-test-profile-female-preview.png)

1. 選取其他測試設定檔，以預覽訊息每個變體的電子郵件內容。 在訊息內容中，現在會顯示與所選測試設定檔（現在為男性）對應的選件。

   ![](assets/deliver-offer-test-profile-male-preview.png)

進一步了解在[此區段](#preview-your-messages)中檢查訊息預覽的詳細步驟。

## 作法影片{#video-offers}

了解如何將offer decisioning元件新增至[!DNL Journey Optimizer]中的訊息。

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
