---
title: 建立個人化優惠
description: 了解如何在Adobe Experience Platform中建立個人化優惠方案。
feature: 優惠
topic: 整合
role: User
level: Intermediate
source-git-commit: 80451fcd012257c8648e751076ed668aa05c44c7
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 3%

---

# 建立個人化優惠 {#creating-personalized-offers}

建立優惠方案之前，請確定您已建立：

* 將顯示優惠方案的&#x200B;**placement**。 請參閱[建立版位](../offer-library/creating-placements.md)
* **決策規則**&#x200B;將定義要呈現選件的條件。 請參閱[建立決策規則](../offer-library/creating-decision-rules.md)。
* 您要與選件建立關聯的一或多個&#x200B;**標籤**。 請參閱[建立標籤](../offer-library/creating-tags.md)。

➡️ [在影片中探索此功能](#video)

可在&#x200B;**[!UICONTROL Offers]**&#x200B;功能表存取個人化優惠方案清單。

![](../../assets/offers_list.png)

## 建立優惠方案 {#create-offer}

若要建立&#x200B;**選件**，請執行下列步驟：

1. 按一下&#x200B;**[!UICONTROL Create offer]**，然後選擇&#x200B;**[!UICONTROL Personalized offer]**。

   ![](../../assets/create_offer.png)

1. 指定選件的名稱，以及其開始和結束日期與時間。 您也可以將一或多個現有標籤與選件建立關聯，讓您更輕鬆搜尋及組織選件資料庫。

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >**[!UICONTROL Offer attributes]**&#x200B;區段可讓您將索引鍵值配對與選件建立關聯，以用於報表和分析用途。

## 設定優惠方案的陳述 {#representations}

1. 使用&#x200B;**[!UICONTROL Add representation]**&#x200B;按鈕，為您的選件新增一或多個表示法。

   >[!NOTE]
   >
   >選件可顯示在訊息中的不同位置：在頂端橫幅中，以影像、段落中的文字、html區塊等形式顯示。 優惠方案表示得越多，在不同版位內容中使用優惠方案的機會就越多。

1. 對於每個表示，指定將顯示選件的&#x200B;**[!UICONTROL Channel]**&#x200B;和&#x200B;**[!UICONTROL Placement]**。

   ![](../../assets/channel-placement.png)

   **[!UICONTROL Browse]**&#x200B;按鈕可讓您篩選可用版位，並根據版位的頻道和/或內容類型加以篩選。

   ![](../../assets/browse-placements.png)

1. 將內容新增至來自Adobe Experience Cloud Assets資料庫或外部公用位置的每個呈現。

   * 若要從Adobe Experience Cloud Assets資料庫新增內容，請從左窗格將其拖曳至表示區域，然後指定要與&#x200B;**[!UICONTROL Destination link]**&#x200B;欄位中的內容建立關聯的URL。

      >[!NOTE]
      >
      >只能從左側面板的「資產選擇器」拖放內容。 只有與版位內容類型對應的內容可供使用。

      ![](../../assets/offer_drag_content.png)

   * 若要從外部公用位置新增內容，請按一下&#x200B;**[!UICONTROL Add content]**&#x200B;按鈕，然後指定要新增內容的名稱、URL和目的地連結。

      請確定新增的內容與選取版位的內容類型相對應。

      ![](../../assets/offer_add_content.png)

   * 您也可以插入文字類型內容。 要執行此操作，請按一下&#x200B;**[!UICONTROL Add content]**&#x200B;按鈕，然後選取&#x200B;**[!UICONTROL Custom text]**&#x200B;選項。 在&#x200B;**[!UICONTROL Text]**&#x200B;欄位中，輸入要顯示在選件中的文字。

      >[!NOTE]
      >
      >此選項不適用於影像類型版位。

      ![](../../assets/offer_text_content.png)

## 新增適用性規則和限制 {#eligibility}

適用性規則和限制可讓您定義要顯示優惠方案的條件。

1. 配置&#x200B;**[!UICONTROL Offer eligibility]**。 依預設，會選取&#x200B;**[!UICONTROL All visitors]**&#x200B;決策規則選項，這表示任何設定檔都有資格呈現選件。

   您可以將優惠方案的呈現方式限制為一或多個Adobe Experience Platform區段的成員。 要執行此操作，請啟動&#x200B;**[!UICONTROL Visitors who fall into one or multiple segments]**&#x200B;選項，然後從左窗格中添加一個或多個段，並使用&#x200B;**[!UICONTROL And]** / **[!UICONTROL Or]**&#x200B;邏輯運算子將它們組合起來。

   如需如何使用區段的詳細資訊，請參閱[本頁面](../../segment/about-segments.md)。

   ![](../../assets/offer-eligibility-segment.png)

   如果您想要將特定決策規則與選件建立關聯，請選取&#x200B;**[!UICONTROL By defined decision rule]**，然後從左窗格將所需規則拖曳至&#x200B;**[!UICONTROL Decision rule]**&#x200B;區域。 有關如何建立決策規則的詳細資訊，請參閱[此區段](../offer-library/creating-decision-rules.md)。

   ![](../../assets/offer_rule.png)

   >[!CAUTION]
   >
   >[!DNL Journey Optimizer]中目前不支援以事件為基礎的選件。 如果您根據[event](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}建立決策規則，將無法在選件中運用該規則。

1. 如果使用者符合多個選件的資格，請定義選件的&#x200B;**[!UICONTROL Priority]**，而非其他選件。 優惠方案的優先順序越高，優先順序與其他優惠方案相比就越高。

1. 指定選件的&#x200B;**[!UICONTROL Capping]**，表示所有使用者總共會顯示該選件的次數。 如果已將選件傳送給所有使用者的次數超過您在此欄位中指定的次數，則其傳送將停止。

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

1. 當您的選件準備好呈現給使用者時，按一下&#x200B;**[!UICONTROL Finish]**。

1. 選擇「**[!UICONTROL Save and approve]**」。

   ![](../../assets/offer_review.png)

   您也可以將優惠方案儲存為草稿，以便稍後編輯並核准。

選件會顯示在清單中，且狀態為&#x200B;**[!UICONTROL Approved]**&#x200B;或&#x200B;**[!UICONTROL Draft]**，視您在上一個步驟中是否核准而定。

現在已可供使用者使用。

![](../../assets/offer_created.png)

## 選件清單 {#offer-list}

您可以從選件清單中選取要顯示其屬性的選件。 您也可以編輯選件、變更其狀態(**Draft**、**Approved**、**Archived**)、複製選件或刪除選件。

![](../../assets/offer_created.png)

選取&#x200B;**[!UICONTROL Edit]**&#x200B;按鈕，返回優惠方案版本模式，您可在此修改優惠方案的[details](#create-offer)、[representations](#representations)，以及編輯[適用性規則和限制](#eligibility)。

選取已核准的優惠方案，然後按一下&#x200B;**[!UICONTROL Undo approve]**&#x200B;將優惠方案狀態設回&#x200B;**[!UICONTROL Draft]**。

若要將狀態再次設為&#x200B;**[!UICONTROL Approved]**，請選取現在顯示的對應按鈕。

![](../../assets/offer_approve.png)

**[!UICONTROL More actions]**&#x200B;按鈕可啟用下面所述的操作。

![](../../assets/offer_more-actions.png)

* **[!UICONTROL Duplicate]**:建立具有相同屬性、表示、適用性規則和限制的優惠方案。依預設，新選件的狀態為&#x200B;**[!UICONTROL Draft]**。
* **[!UICONTROL Delete]**:從清單中移除選件。

   >[!CAUTION]
   >
   >優惠方案及其內容將無法再存取。 此動作無法復原。
   >
   >如果在集合或決策中使用選件，則無法刪除選件。 您必須先從任何物件中移除選件。

* **[!UICONTROL Archive]**:將選件狀態設為 **[!UICONTROL Archived]**。選件仍可從清單中取得，但您無法將其狀態設回&#x200B;**[!UICONTROL Draft]**&#x200B;或&#x200B;**[!UICONTROL Approved]**。 您只能複製或刪除它。

您也可以選取對應的核取方塊，以同時刪除或變更多個選件的狀態。

![](../../assets/offer_multiple-selection.png)

如果您想要變更多個狀態不同之優惠方案的狀態，則只會變更相關狀態。

![](../../assets/offer_change-status.png)

建立選件後，您就可以從清單按一下其名稱。

![](../../assets/offer_click-name.png)

這可讓您存取該選件的詳細資訊。 選取&#x200B;**[!UICONTROL Change log]**&#x200B;標籤，以[監視對選件進行的所有變更](../get-started/user-interface.md#monitoring-changes)。

![](../../assets/offer_information.png)

## 教學課程影片 {#video}

>[!NOTE]
>
>此影片適用於以Adobe Experience Platform為基礎的Offer decisioning應用程式服務。 不過，它提供在Journey Optimizer內容中使用Offer的一般指引。

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
