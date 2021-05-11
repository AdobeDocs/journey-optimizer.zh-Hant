---
title: 建立個人化優惠方案
description: 瞭解如何在Adobe Experience Platform建立個人化優惠。
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 6%

---

# 建立個人化優惠方案 {#creating-personalized-offers}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="關於選件限制"
>abstract="有了限制，您可以指定與其他選件相比，選件的優先順序和呈現方式。"
>additional-url="https://video.tv.adobe.com/v/329375?captions=chi_hant" text="觀看示範影片"

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="關於優惠資格"
>abstract="在本節中，您可以使用決策規則來判斷哪些使用者符合選件的資格。"
>additional-url="https://experienceleague.adobe.com/docs/offer-decisioning/using/managing-offers-in-the-offer-library/creating-decision-rules.html" text="建立決定規則"
>additional-url="https://video.tv.adobe.com/v/329373?captions=chi_hant" text="觀看示範影片"

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="關於選件優先順序"
>abstract="在此欄位中，您可以指定選件的優先順序設定。 優先順序是用於排名符合資格、日期和上限等所有限制的選件的數字。"
>additional-url="https://video.tv.adobe.com/v/329375" text="觀看示範影片"

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="關於選件封閉"
>abstract="在此欄位中，您可以指定選件在所有使用者中可顯示的次數。"
>additional-url="https://video.tv.adobe.com/v/329375" text="觀看示範影片"

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="關於選件屬性"
>abstract="使用選件屬性，您可以將關鍵值配對與選件建立關聯，以便用於報告和分析。"
>additional-url="https://video.tv.adobe.com/v/329375" text="觀看示範影片"

建立選件之前，請確定您已建立：

* 顯示選件的&#x200B;**位置**。 請參閱[建立位置](../offer-library/creating-placements.md)
* **決定規則**，將定義提供選件的條件。 請參閱[建立決策規則](../offer-library/creating-decision-rules.md)。
* 您要與選件建立關聯的一或數個&#x200B;**標籤**。 請參閱[建立標籤](../offer-library/creating-tags.md)。

![](../assets/do-not-localize/how-to-video.png) [在影片中探索此功能](#video)

您可從&#x200B;**[!UICONTROL Offers]**&#x200B;功能表存取個人化優惠清單。

![](../assets/offers_list.png)

## 建立選件{#create-offer}

若要建立&#x200B;**offer**，請依照下列步驟進行：

1. 按一下&#x200B;**[!UICONTROL Create offer]** ，然後選擇&#x200B;**[!UICONTROL Personalized offer]**。

   ![](../assets/create_offer.png)

1. 指定選件的名稱，以及其開始和結束日期與時間。 您也可以將一或多個現有標籤與選件建立關聯，讓您更輕鬆地搜尋和組織選件程式庫。

   ![](../assets/offer_details.png)

   >[!NOTE]
   >
   >**[!UICONTROL Offer attributes]**&#x200B;區段可讓您將索引鍵值配對與選件建立關聯，以便用於報告和分析。

## 設定選件的表示法{#representations}

1. 使用&#x200B;**[!UICONTROL Add representation]**&#x200B;按鈕為選件新增一或多個表示法。

   >[!NOTE]
   >
   >選件可以顯示在訊息的不同位置：在具有影像的頂端橫幅中，以段落中的文字、以html區塊等形式顯示。 選件的表示方式越多，在不同位置上下文中使用選件的機會就越多。

1. 對於每個表示法，請指定&#x200B;**[!UICONTROL Channel]**&#x200B;和&#x200B;**[!UICONTROL Placement]**，其中將顯示選件。

   ![](../assets/channel-placement.png)

   **[!UICONTROL Browse]**&#x200B;按鈕可讓您篩選可用位置，並依其頻道和／或內容類型加以篩選。

   ![](../assets/browse-placements.png)

1. 將內容新增至來自Adobe Experience Cloud資產庫或外部公共位置的每個代表。

   * 若要從「Adobe Experience Cloud資產」資料庫新增內容，請從左窗格拖放內容至表示區域，然後在&#x200B;**[!UICONTROL Destination link]**&#x200B;欄位中指定要與內容關聯的URL。

      >[!NOTE]
      >
      >內容只能從左側面板的「資產選擇器」拖放。 只有與位置的內容類型對應的內容可供使用。

      ![](../assets/offer_drag_content.png)

   * 若要從外部公用位置新增內容，請按一下&#x200B;**[!UICONTROL Add content]**&#x200B;按鈕，然後指定要新增內容的名稱、URL和目標連結。

      請確定您要新增的內容與所選位置的內容類型相對應。

      ![](../assets/offer_add_content.png)

   * 您也可以插入文字內容。 要執行此操作，請按一下&#x200B;**[!UICONTROL Add content]**&#x200B;按鈕，然後選擇&#x200B;**[!UICONTROL Custom text]**&#x200B;選項。 在&#x200B;**[!UICONTROL Text]**&#x200B;欄位中，輸入將顯示在選件中的文字。

      >[!NOTE]
      >
      >此選項不適用於影像類型位置。

      ![](../assets/offer_text_content.png)

## 新增資格規則和限制{#eligibility}

資格規則和限制可讓您定義要顯示選件的條件。

1. 配置&#x200B;**[!UICONTROL Offer eligibility]**。 依預設，會選取&#x200B;**[!UICONTROL All visitors]**&#x200B;決策規則選項，這表示任何設定檔都符合提供選件的資格。

   您可以限制一或多個Adobe Experience Platform區段的成員呈現選件。 若要這麼做，請啟動&#x200B;**[!UICONTROL Visitors who fall into one or multiple segments]**&#x200B;選項，然後從左窗格新增一或多個區段，然後使用&#x200B;**[!UICONTROL And]** / **[!UICONTROL Or]**&#x200B;邏輯運算子加以結合。

   有關如何使用區段的詳細資訊，請參閱[區段服務檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)。

   ![](../assets/offer-eligibility-segment.png)

   如果您想要將特定決策規則與選件建立關聯，請選取&#x200B;**[!UICONTROL By defined decision rule]**，然後從左窗格拖曳所要的規則至&#x200B;**[!UICONTROL Decision rule]**&#x200B;區域。 有關如何建立決策規則的詳細資訊，請參閱[本節](../offer-library/creating-decision-rules.md)。

   ![](../assets/offer_rule.png)

1. 如果使用者符合多個選件的資格，請定義選件的&#x200B;**[!UICONTROL Priority]**&#x200B;與其他選件的比較。 優惠的優先順序最高，其優先順序最高，與其他優惠相比

1. 指定選件的&#x200B;**[!UICONTROL Capping]**，表示選件在所有使用者中總共顯示的次數。 如果選件已傳送給所有使用者，且您在此欄位中指定的次數，則其傳送將停止。

   >[!NOTE]
   >
   >建議選件的次數是在電子郵件準備時計算。 例如，如果您準備包含多個優惠方案的電子郵件，無論是否有傳送電子郵件，這些數量都會計入您的次數上限中。
   >
   >如果刪除電子郵件傳送，或是在傳送之前再次進行準備，則會自動更新選件的上限值。

   ![](../assets/offer_capping.png)

   在上述範例中：

   * 優惠的優先順序設為&quot;50&quot;，表示優惠會先於優惠1至49，再於優先順序至少為51的優惠後顯示。
   * 只有符合「黃金忠誠度客戶」決策規則的使用者才會考慮此優惠。
   * 每位使用者只會顯示一次選件。

## 檢閱選件{#review}

一旦定義資格規則和限制，就會顯示選件屬性的摘要。 如果所有項目皆已正確設定，而您的選件已準備好要呈現給使用者，請按一下&#x200B;**[!UICONTROL Finish]**，然後選取&#x200B;**[!UICONTROL Save and approve]**。

您也可以將選件儲存為草稿，以便稍後編輯及核准。

![](../assets/offer_review.png)

選件會顯示在具有&#x200B;**[!UICONTROL Live]**&#x200B;或&#x200B;**[!UICONTROL Draft]**&#x200B;狀態的清單中，這取決於您在上一步驟中是否核准了選件。

現在，它已可以傳送給使用者。 可以選取它以顯示其屬性，並編輯或隱藏它。

![](../assets/offer_created.png)

建立選件後，您可以按一下清單中的選件名稱以存取詳細資訊，並使用&#x200B;**[!UICONTROL Change log]**&#x200B;標籤來監控對選件所做的所有變更（請參閱[監控選件和決策的變更](../get-started/user-interface.md#monitoring-changes)）。

## 教學課程影片{#video}

>[!NOTE]
>
>此視訊適用於以Adobe Experience Platform為基礎的Offer decisioning應用程式服務。 然而，它提供了在Journey Optimizer背景下使用選件的一般指導。

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
