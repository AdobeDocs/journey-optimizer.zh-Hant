---
title: 建立決定
description: 了解如何建立決策
feature: 優惠
topic: 整合
role: User
level: Intermediate
source-git-commit: 80451fcd012257c8648e751076ed668aa05c44c7
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 3%

---

# 建立決定 {#create-offer-activities}

決策（先前稱為優惠方案活動）是您優惠方案的容器，會運用優惠方案決策引擎，以根據傳送目標挑選最佳優惠方案以供傳送。

➡️ [在影片中探索此功能](#video)

可在&#x200B;**[!UICONTROL Offers]**&#x200B;功能表/ **[!UICONTROL Decisions]**&#x200B;標籤中存取決策清單。 篩選器可協助您根據狀態或開始和結束日期擷取決策。

![](../../assets/activities-list.png)

建立決策之前，請確定下列元件已在選件資料庫中建立：

* [版位](../offer-library/creating-placements.md)
* [集合](../offer-library/creating-collections.md)
* [個人化優惠](../offer-library/creating-personalized-offers.md)
* [遞補優惠](../offer-library/creating-fallback-offers.md)

## 建立決策 {#create-activity}

1. 訪問決策清單，然後按一下&#x200B;**[!UICONTROL Create decision]**。

1. 指定決策的名稱及其開始和結束日期和時間，然後按一下&#x200B;**[!UICONTROL Next]**。

   ![](../../assets/activities-name.png)

## 添加決策範圍 {#add-decision-scopes}

1. 從清單中拖放版位以將其新增至決策，然後按一下&#x200B;**[!UICONTROL Add collection]**。

   ![](../../assets/activities-placement.png)

   >[!NOTE]
   >
   >可在決策中選取相同版位多次。

1. 選取包含要考慮之選件的集合，然後按一下&#x200B;**[!UICONTROL Add]**。

   ![](../../assets/activities-collection.png)

1. 選取的優惠方案會新增至版位。 在此範例中，我們選取了兩個優惠方案，這些優惠方案將顯示在JSON類型的版位中，以將優惠方案呈現在客服中心解決方案中。

   ![](../../assets/offers-added.png)

1. 依預設，如果多個優惠方案符合此版位的資格，則優先順序分數最高的優惠方案會傳送給客戶。

   如果您想使用特定公式來選擇要傳送的合格優惠方案，請從&#x200B;**[!UICONTROL Rank offers by]**&#x200B;下拉式清單中選取排名公式。 如需詳細資訊，請參閱[本章節](../offer-activities/configure-offer-selection.md)。

1. **[!UICONTROL Constraint]**&#x200B;欄位會限制為此版位選取優惠方案。 您可以使用決策規則或一或多個Adobe Experience Platform區段來套用此限制。

   若要將選件的選取限制在Adobe Experience Platform區段的成員，請選取&#x200B;**[!UICONTROL Segments]**，然後按一下&#x200B;**[!UICONTROL Add segments]**。

   ![](../../assets/activity_constraint_segment.png)

   從左窗格新增一或多個區段，使用&#x200B;**[!UICONTROL And]** / **[!UICONTROL Or]**&#x200B;邏輯運算子加以結合，然後按一下&#x200B;**[!UICONTROL Select]**&#x200B;以確認。

   如需如何使用區段的詳細資訊，請參閱[本頁面](../../segment/about-segments.md)。

   ![](../../assets/activity_constraint_segment2.png)

   如果要使用決策規則為此位置添加選擇約束，請選擇&#x200B;**[!UICONTROL Decision rule]**&#x200B;選項，然後從左窗格將所需規則拖到&#x200B;**[!UICONTROL Decision rule]**&#x200B;區域。 有關如何建立決策規則的詳細資訊，請參閱[此區段](../offer-library/creating-decision-rules.md)。

   ![](../../assets/activity_constraint_rule.png)

## 新增回退優惠方案 {#add-fallback}

選擇將作為最後手段呈現給不符合優惠方案適用性規則和限制的客戶的回退優惠方案，然後按一下&#x200B;**[!UICONTROL Next]**。

![](../../assets/add-fallback-offer.png)

## 檢閱並儲存決策 {#review}

如果所有項目皆已正確設定，決策屬性的摘要便會顯示。

1. 請確定已準備好使用決策來向客戶呈現優惠方案。
1. 按一下「**[!UICONTROL Finish]**」。
1. 然後選擇&#x200B;**[!UICONTROL Save and activate]**。

   ![](../../assets/save-activities.png)

   您也可以將決定儲存為草稿，以便稍後編輯並啟動決定。

決策會顯示在清單中，且狀態為&#x200B;**[!UICONTROL Live]**&#x200B;或&#x200B;**[!UICONTROL Draft]**，具體取決於您是否在上一個步驟中啟動了它。

現在，它已準備好用於提供優惠方案給客戶。

## 決策清單 {#decision-list}

從決策清單中，您可以選取要顯示其屬性的決策。 您也可以從該處編輯它，變更其狀態(**Draft**、**Live**、**Complete**、**Archived**)、複製決定或刪除它。

![](../../assets/decision_created.png)

選擇&#x200B;**[!UICONTROL Edit]**&#x200B;按鈕以返回決策版本模式，在該模式中，您可以修改決策的[details](#create-activity)、[決策範圍](#add-decision-scopes)和[回退優惠方案](#add-fallback)。

選取即時決策，然後按一下&#x200B;**[!UICONTROL Deactivate]**&#x200B;將決策狀態設回&#x200B;**[!UICONTROL Draft]**。

若要將狀態再次設為&#x200B;**[!UICONTROL Live]**，請選取現在顯示的&#x200B;**[!UICONTROL Activate]**&#x200B;按鈕。

![](../../assets/decision_activate.png)

**[!UICONTROL More actions]**&#x200B;按鈕可啟用下面所述的操作。

![](../../assets/decision_more-actions.png)

* **[!UICONTROL Complete]**:將決策的狀態設 **[!UICONTROL Complete]**&#x200B;為，表示無法再呼叫決策。此動作僅適用於已啟動的決策。 此決策仍可從清單中取得，但您無法將其狀態設回&#x200B;**[!UICONTROL Draft]**&#x200B;或&#x200B;**[!UICONTROL Approved]**。 您只能複製、刪除或封存它。

* **[!UICONTROL Duplicate]**:使用相同的屬性、決策範圍和備援優惠方案建立決策。依預設，新決策的狀態為&#x200B;**[!UICONTROL Draft]**。

* **[!UICONTROL Delete]**:從清單中移除決策。

   >[!CAUTION]
   >
   >決策及其內容將無法再存取。 此動作無法復原。
   >
   >如果該決策用於另一個對象，則無法刪除該決策。

* **[!UICONTROL Archive]**:將決策狀態設定為 **[!UICONTROL Archived]**。此決策仍可從清單中取得，但您無法將其狀態設回&#x200B;**[!UICONTROL Draft]**&#x200B;或&#x200B;**[!UICONTROL Approved]**。 您只能複製或刪除它。

您也可以選取對應的核取方塊，以同時刪除或變更多個決策的狀態。

![](../../assets/decision_multiple-selection.png)

如果您想要變更狀態不同的數個決策的狀態，則只會變更相關的狀態。

![](../../assets/decision_change-status.png)

建立決策後，您就可以從清單按一下其名稱。

![](../../assets/decision_click-name.png)

這可讓您存取該決策的詳細資訊。 選擇&#x200B;**[!UICONTROL Change log]**&#x200B;頁簽以[監視已對決策進行的所有更改](../get-started/user-interface.md#changes-log)。

![](../../assets/decision_information.png)

## 教學課程影片 {#video}

>[!NOTE]
>
>此影片適用於以Adobe Experience Platform為基礎的Offer decisioning應用程式服務。 不過，它提供在Journey Optimizer內容中使用Offer的一般指引。

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
