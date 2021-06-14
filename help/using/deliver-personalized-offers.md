---
title: 新增個人化優惠
description: 了解如何將個人化優惠方案新增至訊息
feature: Journeys
topic: 內容管理
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---

# 新增個人化優惠 {#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## 關於決定管理 {#about-offer-decisioning}

透過[!DNL Journey Optimizer]，您可以插入電子郵件訊息決策（先前稱為優惠方案活動）中，此決策將運用優惠方案決策引擎，以便挑選最合適的優惠方案並傳送給客戶。

例如，您可以新增決策，在電子郵件中顯示特別折扣優惠，該優惠會根據收件者的忠誠度而有所不同。

如需如何建立和管理選件的詳細資訊，請參閱[此區段](offers/get-started/starting-offer-decisioning.md)。

## 在電子郵件{#insert-offers}中插入決策

若要將決策插入電子郵件訊息，請遵循下列步驟：

1. 建立您的電子郵件，然後開啟電子郵件設計工具來設定其內容。

1. 新增&#x200B;**[!UICONTROL Offer decision]**&#x200B;內容元件（請參閱[使用內容元件](content-components.md)）。

   ![](assets/deliver-offer-component.png)

1. 元件中新增了&#x200B;**[!UICONTROL Offer decision]**&#x200B;索引標籤。 按一下&#x200B;**[!UICONTROL Add personalization - Offer decision]**&#x200B;以新增優惠方案活動。

   ![](assets/deliver-offer-tab.png)

1. 選取與您要顯示之選件相對應的位置。

   版位是用來展示優惠方案的容器。 在此範例中，我們將使用「電子郵件至上影像」位置。 此版位已建立在優惠方案庫中，以顯示位於訊息頂端的影像類型優惠方案。

1. 選取要在內容元件中使用的優惠方案活動，然後按一下&#x200B;**[!UICONTROL Add]**。

   >[!NOTE]
   >
   >請注意，清單中只會顯示與所選位置相容的決策。 在此範例中，只有一個優惠方案活動符合「電子郵件最上層影像」位置。

   ![](assets/deliver-offer-placement.png)

1. 優惠方案活動現在已新增至元件。 您可以使用&#x200B;**[!UICONTROL Offers]**&#x200B;區段或內容元件箭頭，預覽屬於決策一部分的不同選件。

   ![](assets/deliver-offer-preview.png)
