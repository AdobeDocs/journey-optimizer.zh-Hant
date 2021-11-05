---
title: 建立個人化優惠方案
description: 了解如何在Adobe Experience Platform中建立個人化優惠方案。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: b08eb138bbdf9c8a594735824eeac3496a58daba
workflow-type: tm+mt
source-wordcount: '1348'
ht-degree: 3%

---

# 建立個人化優惠方案 {#creating-personalized-offers}

建立優惠方案之前，請確定您已建立：

* A **刊登** 顯示選件的。 請參閱 [建立版位](../offer-library/creating-placements.md)
* 如果要新增資格條件：a **決策規則** 以定義將呈現選件的條件。 請參閱 [建立決策規則](../offer-library/creating-decision-rules.md).
* 一或多個 **標籤** 您可能想要與選件建立關聯。 請參閱 [建立標籤](../offer-library/creating-tags.md).

➡️ [在影片中探索此功能](#video)

個人化優惠方案清單可在 **[!UICONTROL Offers]** 功能表。

![](../../assets/offers_list.png)

## 建立優惠方案 {#create-offer}

若要建立 **優惠方案**，請遵循下列步驟：

1. 按一下 **[!UICONTROL Create offer]**，然後選取 **[!UICONTROL Personalized offer]**.

   ![](../../assets/create_offer.png)

1. 指定選件的名稱，以及其開始和結束日期與時間。 您也可以將一或多個現有標籤與選件建立關聯，讓您更輕鬆搜尋及組織選件資料庫。

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL Offer attributes]** 區段可讓您為報表和分析目的，將索引鍵值配對與選件建立關聯。

## 設定優惠方案的陳述 {#representations}

選件可顯示在訊息中的不同位置：在頂端橫幅中，以影像、段落中的文字、HTML區塊等形式顯示。 優惠方案表示得越多，在不同版位內容中使用優惠方案的機會就越多。

若要新增一或多個表示法並加以設定，請遵循下列步驟。

1. 對於第一個表示，請從選取 **[!UICONTROL Channel]** 會使用。

   ![](../../assets/channel-placement.png)

   >[!NOTE]
   >
   >只有所選管道的可用位置會顯示在 **[!UICONTROL Placement]** 下拉式清單。


1. 從清單中選取位置。

   您也可以使用 **[!UICONTROL Placement]** 下拉式清單來瀏覽所有版位。

   ![](../../assets/browse-button-placements.png)

   您仍可在此根據版位的頻道和/或內容類型篩選版位。 選擇位置並按一下 **[!UICONTROL Select]**.

   ![](../../assets/browse-placements.png)

1. 將內容新增至您的表示法。 了解 [本節](#content).

1. 新增內容（例如影像或URL）時，您可以指定 **[!UICONTROL Destination link]**:點按選件的使用者會導向至對應的頁面。

   ![](../../assets/offer-destination-link.png)

1. 最後，選取您選擇的語言，以協助識別及管理要向使用者顯示的內容。

1. 要添加其他表示，請使用 **[!UICONTROL Add representation]** 按鈕，並視需要新增表示法。

   ![](../../assets/offer-add-representation.png)

1. 添加所有表示形式後，請選擇 **[!UICONTROL Next]**.

## 定義表示的內容 {#content}

您可以將不同類型的內容添加到表示中。

>[!NOTE]
>
>只有與版位內容類型對應的內容可供使用。

### 新增影像

如果選取的版位是影像類型，您可以新增來自 **Adobe Experience Cloud Asset** 程式庫，由 [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> 使用 [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=en){target=&quot;_blank&quot;}，您需要部署 [!DNL Assets Essentials] 確認使用者是 **Assets Essentials消費者使用者** 或/和 **Assets Essentials使用者** 產品設定檔。 深入了解 [本頁](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}。

1. 選取 **[!UICONTROL Asset library]** 選項。

1. 選擇「**[!UICONTROL Browse]**」。

   ![](../../assets/offer-browse-asset-library.png)

1. 瀏覽資產以選取您所選的影像

1. 按一下「**[!UICONTROL Select]**」。

   ![](../../assets/offer-select-asset.png)

### 新增URL

若要從外部公用位置新增內容，請選取 **[!UICONTROL URL]**，然後輸入要新增的內容的URL位址。

![](../../assets/offer-content-url.png)

### 新增自訂文字 {#custom-text}

選取相容的版位時，您也可以插入文字類型內容。

1. 選取 **[!UICONTROL Custom]** 選項，然後按一下 **[!UICONTROL Add content]**.

   ![](../../assets/offer-add-content.png)

   >[!NOTE]
   >
   >此選項不適用於影像類型版位。

1. 輸入要在選件中顯示的文字。

   ![](../../assets/offer-text-content.png)

   您可以使用運算式編輯器個人化您的內容。 深入了解 [個人化](../../personalization/personalize.md#use-expression-editor).

   ![](../../assets/offer-personalization.png)

   >[!NOTE]
   >
   >僅 **[!UICONTROL Profile attributes]**, **[!UICONTROL Segment memberships]** 和 **[!UICONTROL Helper functions]** 來源可用於決策管理。

## 新增適用性規則和限制 {#eligibility}

適用性規則和限制可讓您定義顯示優惠方案的條件。

1. 設定 **[!UICONTROL Offer eligibility]**.

   * 依預設， **[!UICONTROL All visitors]** 已選取決策規則選項，這表示任何設定檔都有資格呈現選件。

   * 您可以將優惠方案的呈現方式限制為一或多個Adobe Experience Platform區段的成員。 若要這麼做，請啟用 **[!UICONTROL Visitors who fall into one or multiple segments]** 選項，然後從左側窗格新增一或多個區段，並使用 **[!UICONTROL And]** / **[!UICONTROL Or]** 邏輯運算子。

      如需如何使用區段的詳細資訊，請參閱 [本頁](../../segment/about-segments.md).

      ![](../../assets/offer-eligibility-segment.png)

   * 如果您想要將特定決策規則與選件建立關聯，請選取 **[!UICONTROL By defined decision rule]**，然後將所需規則從左窗格拖曳至 **[!UICONTROL Decision rule]** 的上界。 如需如何建立決策規則的詳細資訊，請參閱 [本節](../offer-library/creating-decision-rules.md).

      ![](../../assets/offer_rule.png)

      >[!CAUTION]
      >
      >目前不支援以事件為基礎的選件 [!DNL Journey Optimizer]. 如果您根據 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}，您將無法在選件中運用它。
   進一步了解如何在中使用區段與決策規則 [本節](../offer-activities/create-offer-activities.md#segments-vs-decision-rules).

1. 定義 **[!UICONTROL Priority]** 選件的數量，而非其他選件（如果使用者符合多個選件的資格）。 優惠方案的優先順序越高，優先順序與其他優惠方案相比就越高。

1. 指定選件的 **[!UICONTROL Capping]**，表示所有使用者中總共會顯示選件的次數。 如果已將選件傳送給所有使用者的次數超過您在此欄位中指定的次數，則其傳送將停止。

   >[!NOTE]
   >
   >系統會在準備電子郵件時計算建議某個優惠方案的次數。 例如，如果您準備包含多個優惠方案的電子郵件，無論是否有傳送電子郵件，這些數量都會計入您的次數上限中。
   >
   >如果刪除電子郵件傳送，或在傳送前再次進行準備，則會自動更新選件的上限值。

   ![](../../assets/offer_capping.png)

   在上述範例中：

   * 優先順序設為「50」，這表示優惠方案會在優先順序介於1到49之間的優惠方案之前，以及優先順序至少為51的優惠方案之後呈現。
   * 只有符合「金級忠誠客戶」決策規則的使用者才會考慮此優惠方案。
   * 每位使用者只會呈現一次選件。

## 檢閱優惠方案 {#review}

定義資格規則和限制後，即會顯示優惠方案屬性的摘要。

1. 請確定所有項目皆已正確設定。

1. 當您的優惠方案準備好呈現給使用者時，請按一下 **[!UICONTROL Finish]**.

1. 選擇「**[!UICONTROL Save and approve]**」。

   ![](../../assets/offer_review.png)

   您也可以將優惠方案儲存為草稿，以便稍後編輯並核准。

選件會顯示在清單中，且 **[!UICONTROL Approved]** 或 **[!UICONTROL Draft]** 狀態，取決於您在上一步驟中是否核准。

現在已可供使用者使用。

![](../../assets/offer_created.png)

## 優惠清單 {#offer-list}

您可以從選件清單中選取要顯示其屬性的選件。 您也可以編輯、變更其狀態(**草稿**, **已核准**, **已封存**)、複製選件或將其刪除。

![](../../assets/offer_created.png)

選取 **[!UICONTROL Edit]** 按鈕，返回優惠方案版本模式，您可在其中修改優惠方案的 [詳細資訊](#create-offer), [表示](#representations)，以及編輯 [適用性規則與限制](#eligibility).

選取已核准的優惠方案，然後按一下 **[!UICONTROL Undo approve]** 將優惠方案狀態設回 **[!UICONTROL Draft]**.

將狀態再次設定為 **[!UICONTROL Approved]**，請選取現在顯示的對應按鈕。

![](../../assets/offer_approve.png)

此 **[!UICONTROL More actions]** 按鈕可啟用以下說明的動作。

![](../../assets/offer_more-actions.png)

* **[!UICONTROL Duplicate]**:建立具有相同屬性、表示、適用性規則和限制的優惠方案。 依預設，新選件具有 **[!UICONTROL Draft]** 狀態。
* **[!UICONTROL Delete]**:從清單中移除選件。

   >[!CAUTION]
   >
   >優惠方案及其內容將無法再存取。 此動作無法復原。
   >
   >如果在集合或決策中使用選件，則無法刪除選件。 您必須先從任何物件中移除選件。

* **[!UICONTROL Archive]**:將優惠方案狀態設為 **[!UICONTROL Archived]**. 選件仍可從清單中取得，但您無法將其狀態設回 **[!UICONTROL Draft]** 或 **[!UICONTROL Approved]**. 您只能複製或刪除它。

您也可以選取對應的核取方塊，以同時刪除或變更多個選件的狀態。

![](../../assets/offer_multiple-selection.png)

如果您想要變更多個狀態不同之優惠方案的狀態，則只會變更相關狀態。

![](../../assets/offer_change-status.png)

建立選件後，您就可以從清單按一下其名稱。

![](../../assets/offer_click-name.png)

這可讓您存取該選件的詳細資訊。 選取 **[!UICONTROL Change log]** 標籤 [監視所有更改](../get-started/user-interface.md#monitoring-changes) 已經向你提出了。

![](../../assets/offer_information.png)

## 教學課程影片 {#video}

>[!NOTE]
>
>此影片適用於以Adobe Experience Platform為基礎的Offer decisioning應用程式服務。 不過，它提供在Journey Optimizer內容中使用Offer的一般指引。

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
