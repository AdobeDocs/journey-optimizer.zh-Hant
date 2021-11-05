---
title: 建立決定
description: 了解如何建立決策
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: 7f8871fdaf5bb543ce8dc894f3a7dc7304eccf36
workflow-type: tm+mt
source-wordcount: '1234'
ht-degree: 1%

---

# 建立決定 {#create-offer-activities}

決策（先前稱為優惠方案活動）是您優惠方案的容器，會運用優惠方案決策引擎，以根據傳送目標挑選最佳優惠方案以供傳送。

➡️ [在影片中探索此功能](#video)

您可以在 **[!UICONTROL Offers]** 菜單> **[!UICONTROL Decisions]** 標籤。 篩選器可協助您根據狀態或開始和結束日期擷取決策。

![](../../assets/activities-list.png)

建立決策之前，請確定下列元件已在選件資料庫中建立：

* [版位](../offer-library/creating-placements.md)
* [集合](../offer-library/creating-collections.md)
* [個人化優惠](../offer-library/creating-personalized-offers.md)
* [遞補優惠](../offer-library/creating-fallback-offers.md)

## 建立決策 {#create-activity}

1. 存取決策清單，然後按一下 **[!UICONTROL Create decision]**.

1. 指定決策的名稱。

1. 視需要定義開始和結束日期和時間，然後按一下 **[!UICONTROL Next]**.

   ![](../../assets/activities-name.png)

## 定義決策範圍 {#add-decision-scopes}

1. 從下拉式清單中選取位置。 它會新增至您決定中的第一個決策範圍。

   ![](../../assets/activities-placement.png)

1. 按一下 **[!UICONTROL Add]** 來選擇此位置的評估標準。

   ![](../../assets/activities-evaluation-criteria.png)

   每個條件都包含與資格限制相關聯的優惠方案集合，以及用以決定要在版位中顯示的優惠方案的排名方法。

   >[!NOTE]
   >
   >至少需要一個評估標準。

1. 選取包含要考慮之選件的選件集合，然後按一下 **[!UICONTROL Add]**.

   ![](../../assets/activities-collection.png)

   >[!NOTE]
   >
   >您可以按一下 **[!UICONTROL Open offer collections]** 連結可在新索引標籤中顯示集合清單，讓您可以瀏覽集合及其包含的選件。

   選取的集合會新增至條件。

   ![](../../assets/activities-collection-added.png)

1. 使用 **[!UICONTROL Eligibility]** 欄位來限制此版位選擇優惠方案。

   此限制可透過使用 **決策規則**，或一或多個 **Adobe Experience Platform區段**. 這兩者在 [本節](#segments-vs-decision-rules).

   * 若要將選件的選取限制在Experience Platform區段的成員，請選取 **[!UICONTROL Segments]**，然後按一下 **[!UICONTROL Add segments]**.

      ![](../../assets/activity_constraint_segment.png)

      從左窗格新增一或多個區段，然後使用 **[!UICONTROL And]** / **[!UICONTROL Or]** 邏輯運算子。

      ![](../../assets/activity_constraint_segment2.png)

      了解如何在 [本節](../../segment/about-segments.md).

   * 如果要使用決策規則添加選擇約束，請使用 **[!UICONTROL Decision rule]** 選項，然後選取您選取的規則。

      ![](../../assets/activity_constraint_rule.png)

      了解如何在 [本節](../offer-library/creating-decision-rules.md).

1. 定義您要用來為每個設定檔選取最佳選件的排名方法。

   ![](../../assets/activity_ranking-method.png)

   * 依預設，如果多個優惠方案符合此版位的資格，則會將優先順序分數最高的優惠方案傳送給客戶。

   * 如果您想使用特定公式來選擇要交付的合格優惠方案，請選擇 **[!UICONTROL Ranking formula]**. 了解如何在 [本節](../offer-activities/configure-offer-selection.md).

1. 按一下 **[!UICONTROL Add]** 為相同版位定義更多條件。

   ![](../../assets/activity_add-collection.png)

1. 新增多個條件時，會以特定順序評估這些條件。 系統會先評估新增至序列的第一個集合，以此類推。

   若要變更預設序列，您可以拖放集合以視需要重新排序。

   ![](../../assets/activity_reorder-collections.png)

1. 您也可以同時評估多個條件。 若要這麼做，請將系列拖放至其他系列上方。

   ![](../../assets/activity_move-collection.png)

   他們現在擁有相同的排名，因此將同時評估。

   ![](../../assets/activity_same-rank-collections.png)

1. 若要在此決策中為優惠方案新增其他版位，請使用 **[!UICONTROL New scope]** 按鈕。 對每個決策範圍重複上述步驟。

   ![](../../assets/activity_new-scope.png)

### 使用區段與決策規則 {#segments-vs-decision-rules}

<!--to move to create-offers?-->

要應用約束，可以將選件的選擇限制在一個或多個成員 **Adobe Experience Platform區段**，或者您可以使用 **決策規則**，兩個解決方案會對應不同的使用方式。

基本上，區段的輸出是設定檔清單，而決策規則則是決策過程中針對單一設定檔依需求執行的函式。 以下詳細說明這兩種用法之間的差異。

* **區段**

   一方面，區段是一組Adobe Experience Platform設定檔，會根據設定檔屬性和體驗事件來比對特定邏輯。 不過，Offer Management不會重新計算區段，這在呈現優惠方案時可能不會是最新的。

   進一步了解 [本節](../../segment/about-segments.md).

* **決定規則**

   另一方面，決策規則是以Adobe Experience Platform中可用的資料為基礎，並決定可向誰顯示優惠方案。 在優惠方案中選取或針對指定版位的決策後，每次做出決策時，都會執行規則，以確保每個設定檔都能取得最新和最佳的優惠方案。

   進一步了解中的決策規則 [本節](../offer-library/creating-decision-rules.md).

## 新增回退優惠方案 {#add-fallback}

定義決策範圍後，請定義後援優惠方案，以針對不符合優惠方案適用性規則和限制的客戶，將其顯示為最後的選擇。

若要這麼做，請從決策中定義的版位的可用備援優惠方案清單中選取該優惠方案，然後按一下 **[!UICONTROL Next]**.

![](../../assets/add-fallback-offer.png)

>[!NOTE]
>
>您可以按一下 **[!UICONTROL Open offer library]** 連結以在新索引標籤中顯示選件清單。

## 檢閱並儲存決策 {#review}

如果所有項目皆已正確設定，決策屬性的摘要便會顯示。

1. 請確定已準備好使用此決策來向客戶呈現優惠方案。 系統會顯示所有決策範圍及其包含的備援優惠方案。

   ![](../../assets/review-decision.png)

   您可以展開或折疊每個版位。 您也可以預覽每個版位的可用優惠方案、資格和排名詳細資訊。

   ![](../../assets/review-decision-details.png)

1. 按一下「**[!UICONTROL Finish]**」。
1. 選擇「**[!UICONTROL Save and activate]**」。

   ![](../../assets/save-activities.png)

   您也可以將決定儲存為草稿，以便稍後編輯並啟動決定。

決策會顯示在清單中，且 **[!UICONTROL Live]** 或 **[!UICONTROL Draft]** 狀態，具體取決於您在上一步驟中是否啟動了狀態。

現在，它已準備好用於提供優惠方案給客戶。

## 決定清單 {#decision-list}

從決策清單中，您可以選取要顯示其屬性的決策。 您也可以從該處編輯，變更其狀態(**草稿**, **即時**, **完成**, **已封存**)、複製或刪除決策。

![](../../assets/decision_created.png)

選取 **[!UICONTROL Edit]** 按鈕，返回決策版本模式，在此可以修改決策 [詳細資訊](#create-activity), [決策範圍](#add-decision-scopes) 和 [回退優惠方案](#add-fallback).

選取即時決策，然後按一下 **[!UICONTROL Deactivate]** 將決策狀態設回 **[!UICONTROL Draft]**.

將狀態再次設定為 **[!UICONTROL Live]**，請選取 **[!UICONTROL Activate]** 按鈕。

![](../../assets/decision_activate.png)

此 **[!UICONTROL More actions]** 按鈕可啟用以下說明的動作。

![](../../assets/decision_more-actions.png)

* **[!UICONTROL Complete]**:將決策的狀態設定為 **[!UICONTROL Complete]**，表示無法再呼叫決定。 此動作僅適用於已啟動的決策。 此決定仍可從清單中取得，但您無法將其狀態設回 **[!UICONTROL Draft]** 或 **[!UICONTROL Approved]**. 您只能複製、刪除或封存它。

* **[!UICONTROL Duplicate]**:使用相同的屬性、決策範圍和備援優惠方案建立決策。 依預設，新決策會 **[!UICONTROL Draft]** 狀態。

* **[!UICONTROL Delete]**:從清單中移除決策。

   >[!CAUTION]
   >
   >決策及其內容將無法再存取。 此動作無法復原。
   >
   >如果該決策用於另一個對象，則無法刪除該決策。

* **[!UICONTROL Archive]**:將決策狀態設定為 **[!UICONTROL Archived]**. 此決定仍可從清單中取得，但您無法將其狀態設回 **[!UICONTROL Draft]** 或 **[!UICONTROL Approved]**. 您只能複製或刪除它。

您也可以選取對應的核取方塊，以同時刪除或變更多個決策的狀態。

![](../../assets/decision_multiple-selection.png)

如果您想要變更狀態不同的數個決策的狀態，則只會變更相關的狀態。

![](../../assets/decision_change-status.png)

建立決策後，您就可以從清單按一下其名稱。

![](../../assets/decision_click-name.png)

這可讓您存取該決策的詳細資訊。 選取 **[!UICONTROL Change log]** 標籤 [監視所有更改](../get-started/user-interface.md#changes-log) 已經做出了決定。

![](../../assets/decision_information.png)

## 教學課程影片 {#video}

>[!NOTE]
>
>此影片適用於以Adobe Experience Platform為基礎的Offer decisioning應用程式服務。 不過，它提供在Journey Optimizer內容中使用Offer的一般指引。

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
