---
title: 制定決策
description: 瞭解如何制定決策
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 2%

---

# 建立決策{#create-offer-activities}

決策（先前稱為選件活動）是選件的容器，可運用選件決策引擎，以根據遞送的目標來挑選最佳選件。

![](../../assets/do-not-localize/how-to-video.png) [在影片中探索此功能](#video)

可在&#x200B;**[!UICONTROL Offers]**&#x200B;菜單/ **[!UICONTROL Decisions]**&#x200B;頁籤中訪問決策清單。 您可使用篩選器來協助您根據決策的狀態或開始和結束日期來擷取決策。

![](../../assets/activities-list.png)

在建立決策之前，請確定下列元件已建立在選件程式庫中：

* [版位](../offer-library/creating-placements.md),
* [集合](../offer-library/creating-collections.md),
* [個人化優惠](../offer-library/creating-personalized-offers.md),
* [備援選件](../offer-library/creating-fallback-offers.md)。

## 建立決策{#create-activity}

1. 訪問決策清單，然後按一下&#x200B;**[!UICONTROL Create activity]**。

1. 指定決策的名稱及其開始和結束日期和時間，然後按一下&#x200B;**[!UICONTROL Next]**。

   ![](../../assets/activities-name.png)

## 添加決策{#add-decisions}

1. 從清單拖放位置以將其新增至決策，然後按一下&#x200B;**[!UICONTROL Add collection]**。

   ![](../../assets/activities-placement.png)

1. 選取包含要考慮之選件的系列，然後按一下&#x200B;**[!UICONTROL Add]**。

   ![](../../assets/activities-collection.png)

1. 選取的選件會新增至位置。 在此範例中，我們選取了兩個選件，這些選件會顯示在JSON類型的位置，以便在客服中心解決方案中呈現選件。

   ![](../../assets/offers-added.png)

1. 依預設，如果多個選件符合此位置的資格，則優先順序分數最高的選件將會傳送給客戶。

   如果您想要使用特定公式來選擇要傳送的合格選件，請從&#x200B;**[!UICONTROL Rank offers by]**&#x200B;下拉式清單中選取排名公式。 如需詳細資訊，請參閱[本章節](../offer-activities/configure-offer-selection.md)。

1. **[!UICONTROL Constraint]**&#x200B;欄位會限制此位置的選件選擇。 此限制可使用決策規則或一或多個Adobe Experience Platform區段來套用。

   若要將選件選擇限制在Adobe Experience Platform區段的成員，請選取&#x200B;**[!UICONTROL Segments]**，然後按一下&#x200B;**[!UICONTROL Add segments]**。

   ![](../../assets/activity_constraint_segment.png)

   從左窗格新增一或多個區段，使用&#x200B;**[!UICONTROL And]** / **[!UICONTROL Or]**&#x200B;邏輯運算子加以組合，然後按一下&#x200B;**[!UICONTROL Select]**&#x200B;以確認。

   有關如何使用區段的詳細資訊，請參閱[區段服務檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)。

   ![](../../assets/activity_constraint_segment2.png)

   如果要使用決策規則為此位置添加選擇約束，請選擇&#x200B;**[!UICONTROL Decision rule]**&#x200B;選項，然後從左窗格將所需規則拖動到&#x200B;**[!UICONTROL Decision rule]**&#x200B;區域。 有關如何建立決策規則的詳細資訊，請參閱[本節](../offer-library/creating-decision-rules.md)。

   ![](../../assets/activity_constraint_rule.png)

## 新增備援選件{#add-fallback}

選擇將作為最後選項呈現給不符合選件資格規則與限制的客戶的備用選件，然後按一下&#x200B;**[!UICONTROL Next]**。

![](../../assets/add-fallback-offer.png)

## 審查並保存決定{#review}

如果所有項目皆已正確設定，且您的決定已準備好用於向客戶展示優惠，請按一下&#x200B;**[!UICONTROL Finish]**，然後選取&#x200B;**[!UICONTROL Save and activate]**。

您也可以將決定儲存為草稿，以便稍後編輯並啟動決定。

![](../../assets/save-activities.png)

根據您在上一步驟中是否啟動該決策，該決策會以&#x200B;**[!UICONTROL Live]**&#x200B;或&#x200B;**[!UICONTROL Draft]**&#x200B;狀態顯示在清單中。

現在，它已可用來向客戶傳遞優惠。 可以選取它以顯示其屬性，並編輯或隱藏它。

有關提供選件的詳細資訊，請參閱以下章節：

* [在訊息中新增個人化優惠](../../deliver-personalized-offers.md)
* [使用API提供優惠](../api-reference/decisions-api/deliver-offers.md)

![](../../assets/activities-created.png)

>[!NOTE]
>
>建立決策後，您可以按一下清單中的其名稱以存取詳細資訊，並使用&#x200B;**[!UICONTROL Change log]**&#x200B;標籤檢視對其所做的所有變更（請參閱[選件與決策變更記錄](../get-started/user-interface.md#changes-log)）。

## 教學課程影片{#video}

>[!NOTE]
>
>此視訊適用於以Adobe Experience Platform為基礎的Offer decisioning應用程式服務。 然而，它提供了在Journey Optimizer背景下使用選件的一般指導。

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
