---
title: 建立模擬
description: 了解如何建立模擬
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: null
source-git-commit: bad206b6c9b48241dbbd7758a331d602fac466b4
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# 建立模擬

## 關於模擬

若要驗證決策邏輯，您可以模擬哪些選件將傳遞至指定位置的測試設定檔。

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

這可讓您測試和調整各種優惠方案版本，而不會影響目標收件者。

>[!NOTE]
>
>此功能可模擬 [!DNL Decisions] API。 深入了解 [使用決策API傳送優惠方案](../api-reference/decisions-api/deliver-offers.md).

若要存取此功能，請選取 **[!UICONTROL Simulation]** 標籤 **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** 功能表。

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## 選取測試設定檔

首先，您需要選取要用於模擬的測試設定檔。

1. 按一下「**[!UICONTROL Manage profile]**」。

   ![](../../assets/offers_simulation-manage-profile.png)

1. 選取您要用來識別測試設定檔的身分命名空間。 在此範例中，我們將使用 **電子郵件** 命名空間。

   >[!NOTE]
   >
   >身分命名空間會定義識別碼的內容，例如電子郵件地址或CRM ID。 深入了解Adobe Experience Platform身分識別命名空間 [在本節](../../get-started-identity.md){target=&quot;_blank&quot;}。

1. 輸入身分值，然後按一下 **[!UICONTROL View]** 以列出可用的設定檔。

   ![](../../assets/offers_simulation-add-profile.png)

1. 如果您想要測試不同的設定檔資料，請新增其他設定檔，並儲存您的選取項目。

   ![](../../assets/offers_simulation-save-profiles.png)

1. 新增後，所有設定檔都會列在下方的下拉式清單中 **[!UICONTROL Test profile]**. 您可以在儲存的測試設定檔之間切換，以顯示每個選取設定檔的結果。

   ![](../../assets/offers_simulation-saved-profiles.png)

1. 您可以按一下 **[!UICONTROL Profile details]** 連結以顯示選取的設定檔資料。

<!--Learn more on [selecting test profiles](preview.md#select-test-profiles)-->

## 添加決策範圍

現在，選取您要在測試設定檔上模擬的選件決策。

1. 選擇「**[!UICONTROL Add decision scope]**」。

   ![](../../assets/offers_simulation-add-decision.png)

1. 從清單中選取位置。

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. 將顯示可用的決策。

   * 您可以使用搜尋欄位來調整選取範圍。
   * 您可以按一下 **[!UICONTROL Open offer decisions]** 連結以開啟您建立的所有決策的清單。 深入了解 [決策](create-offer-activities.md).

   選取您所選的決策，然後按一下 **[!UICONTROL Add]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. 您剛定義的決策範圍會顯示在主要工作區中。

   您可以調整要求的優惠方案數量。 例如，若您選取2，則此決策範圍會顯示最佳2個選件。

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >您最多可以要求30個選件。

1. 重複上述步驟，以新增您需要的決策數。

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >即使您定義多個決策範圍，系統也只會模擬一個API請求。
   >
   >所有重複資料消除標誌都預設為模擬啟用，這意味著決策引擎允許重複資料，因此可以在多個決策中做出相同的主張。 深入了解 [!DNL Decisions] 中的API要求屬性 [本節](../api-reference/decisions-api/deliver-offers.md).

## 查看模擬結果

新增決策範圍並選取測試設定檔後，您就可以檢視結果。

1. 按一下「**[!UICONTROL View results]**」。

   ![](../../assets/offers_simulation-view-results.png)

1. 系統會根據每個決策所選取的設定檔來顯示最佳可用選件。

   選取要顯示其詳細資訊的選件。

   ![](../../assets/offers_simulation-offer-details.png)

1. 從清單中選取其他設定檔，以顯示不同測試設定檔的選件決策結果。

1. 您可以根據需要多次添加、刪除或更新決策範圍。

>[!NOTE]
>
>每次變更設定檔或更新決策範圍時，您都需要使用 **[!UICONTROL View results]** 按鈕。

<!--Questions

* Is it recommended to first select profiles or first add decision scopes?
* What does Request offer changes?
* Nothing displays when I click View results? Can't see any score...
* What's the typical example? i.e. how many decisions do you select, and how do you compare scores?
* What do you learn from simulation? i.e. if I selected 2 decisions and I compare the scores, which one is better or should I use for my customers?
* Is there a way to create relevant test profiles?
* Error on Profile details link.
* Is there a tutorial planned to be released?
* Why still a big red frame when no profile is found?

## Tutorial video {#video}

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
-->