---
title: 建立後備產品建議
description: 瞭解如何建立遞補優惠，以顯示給不符合任何優惠方案資格的客戶
badge: label="舊版" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 9ba16ad9-a5e7-4ce7-8ed6-7707d37178c6
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 4%

---

# 建立後備產品建議 {#create-fallback-offers}

如果客戶不符合其他優惠方案的資格，系統會將遞補優惠方案傳送給客戶。 建立遞補優惠的步驟包含建立一或多個表示，例如建立優惠時。

➡️ [在影片中探索此功能](#video)

可在&#x200B;**[!UICONTROL 優惠]**&#x200B;功能表中存取遞補優惠清單。

![](../assets/offers_list.png)

若要建立遞補優惠，請依照下列步驟進行：

>[!NOTE]
>
>請注意，與個人化優惠不同，遞補優惠沒有適用規則和限制引數，因為它們是作為無條件的最後度假村提供給客戶的。

1. 按一下&#x200B;**[!UICONTROL 建立選件]**，然後選取&#x200B;**[!UICONTROL 遞補選件]**。

   ![](../assets/create_fallback.png)

1. 指定遞補優惠的名稱。 您也可以將一或多個現有的集合限定詞（先前稱為「標籤」）與其建立關聯，讓您更輕鬆地搜尋及組織「優惠資料庫」。

   ![](../assets/fallback_details.png)

1. 若要指派自訂或核心資料使用標籤給優惠方案，請選取&#x200B;**[!UICONTROL 管理存取權]**。 [進一步瞭解物件層級存取控制(OLAC)](../../administration/object-based-access.md)

1. 為遞補優惠建立一或多個代表。 若要這麼做，請從左側窗格拖放版位，就像建立個人化優惠方案一樣。 請參閱[建立個人化優惠](../offer-library/creating-personalized-offers.md)。

   ![](../assets/fallback_content.png)

   >[!CAUTION]
   >
   >遞補優惠應包含[決定](../offer-activities/create-offer-activities.md)內使用的所有代表。 例如，如果您在決定中有5個優惠方案，而且每個優惠方案都有不同的代表方式，則備援優惠方案應包含5個代表方式。

1. 新增遞補優惠的宣告後，會顯示摘要。 如果所有專案皆已正確設定，且您的遞補優惠已準備好呈現給客戶，請按一下[完成]&#x200B;**&#x200B;**，然後選取[儲存]並核准&#x200B;**[!UICONTROL 。]**

   您也可以將遞補優惠儲存為草稿，以便稍後編輯及核准。

   ![](../assets/fallback_review.png)

1. 遞補優惠會顯示在具有&#x200B;**[!UICONTROL 即時]**&#x200B;或&#x200B;**[!UICONTROL 草稿]**&#x200B;狀態的清單中，端視您在上一步驟中是否核准而定。

   現在已準備好傳送給客戶。 您可以選取它以顯示其屬性並加以編輯。<!-- no suppression? -->

   ![](../assets/fallback_created.png)

## 作法影片 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329383?quality=12)

