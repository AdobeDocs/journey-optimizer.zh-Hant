---
title: 新增個人化優惠
description: 瞭解如何在訊息中加入個人化優惠
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# 新增個人化優惠{#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## 關於決策管理{#about-offer-decisioning}

有了[!DNL Journey Optimizer]，您可以在電子郵件訊息中插入決策（先前稱為選件活動），以利用選件決策引擎來挑選最佳選件，以便傳遞給客戶。

例如，您可以新增決定，在電子郵件中顯示特別折扣優惠，折扣優惠會依收件者的忠誠度等級而有所不同。

如需如何建立和管理選件的詳細資訊，請參閱[本節](offers/get-started/starting-offer-decisioning.md)。

## 在電子郵件{#insert-offers}中插入決策

若要將決策插入電子郵件訊息，請遵循下列步驟：

1. 建立您的電子郵件，然後開啟「電子郵件設計器」以設定其內容。

1. 新增&#x200B;**[!UICONTROL Offer decision]**&#x200B;內容元件（請參閱[使用內容元件](content-components.md)）。

   ![](assets/deliver-offer-component.png)

1. 元件中添加了&#x200B;**[!UICONTROL Offer decision]**&#x200B;頁籤。 按一下&#x200B;**[!UICONTROL Add personalization - Offer decision]**&#x200B;以新增選件活動。

   ![](assets/deliver-offer-tab.png)

1. 選取與您要顯示之選件對應的位置。

   位置是用來展示選件的容器。 在此範例中，我們將使用「電子郵件最上層影像」位置。 此位置已建立在選件程式庫中，以顯示位於訊息頂端的影像類型選件。

1. 選取要在內容元件中使用的選件活動，然後按一下&#x200B;**[!UICONTROL Add]**。

   >[!NOTE]
   >
   >請注意，只有與所選位置相容的決策才會顯示在清單中。 在此範例中，只有一個選件活動符合「電子郵件最上層影像」位置。

   ![](assets/deliver-offer-placement.png)

1. 選件活動現在會新增至元件。 您可以使用&#x200B;**[!UICONTROL Offers]**&#x200B;區段或內容元件箭頭，預覽屬於決策的不同選件。

   ![](assets/deliver-offer-preview.png)
