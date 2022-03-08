---
title: 建立個人化優惠方案
description: 瞭解如何建立、配置和管理您的產品
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '1491'
ht-degree: 5%

---

# 建立個人化優惠方案 {#create-personalized-offers}

在建立聘用前，請確保已建立：

* A **放置** 顯示要約。 請參閱 [建立放置](../offer-library/creating-placements.md)
* 如果要添加資格條件：a **決策規則** 將定義提出要約的條件。 請參閱 [建立決策規則](../offer-library/creating-decision-rules.md)。
* 一個或多個 **標籤** 你可能想和報價關聯。 請參閱 [建立標籤](../offer-library/creating-tags.md)。

➡️ [在影片中探索此功能](#video)

您可以在 **[!UICONTROL Offers]** 的子菜單。

![](../../assets/offers_list.png)

## 建立優惠 {#create-offer}

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="關於聘用屬性"
>abstract="使用聘用屬性，您可以將關鍵值對與聘用關聯，以便進行報告和分析。"
>additional-url="https://video.tv.adobe.com/v/329375" text="觀看示範影片"

建立 **提供**，請執行以下步驟：

1. 按一下 **[!UICONTROL Create offer]**，然後選擇 **[!UICONTROL Personalized offer]**。

   ![](../../assets/create_offer.png)

1. 指定聘用的名稱及其開始和結束日期和時間。 您還可以將一個或多個現有標籤與聘用相關聯，從而更輕鬆地搜索和組織聘用庫。

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL Offer attributes]** 部分允許您將鍵值對與報價關聯，以便用於報告和分析。

## 配置優惠的表示法 {#representations}

可以在消息中的不同位置顯示優惠：在帶有影像、段落中的文本、HTML塊等的頂部標題中。 一個要約擁有的表述越多，在不同的放置環境中使用該要約的機會就越多。

要將一個或多個表示形式添加到您的產品中並配置它們，請執行以下步驟。

1. 對於第一個表示，首先選擇 **[!UICONTROL Channel]** 會被使用。

   ![](../../assets/channel-placement.png)

   >[!NOTE]
   >
   >僅在中顯示所選通道的可用位置 **[!UICONTROL Placement]** 的子菜單。


1. 從清單中選取一個放置。

   您還可以使用 **[!UICONTROL Placement]** 下拉清單，瀏覽所有放置。

   ![](../../assets/browse-button-placements.png)

   您仍然可以根據其頻道和/或內容類型篩選放置。 選擇放置，然後按一下 **[!UICONTROL Select]**。

   ![](../../assets/browse-placements.png)

1. 將內容添加到您的表示法。 瞭解 [此部分](#content)。

1. 添加影像或URL等內容時，可以指定 **[!UICONTROL Destination link]**:按一下優惠的用戶將被定向到相應頁面。

   ![](../../assets/offer-destination-link.png)

1. 最後，選擇您選擇的語言以幫助確定和管理要顯示給用戶的內容。

1. 要添加其他表示法，請使用 **[!UICONTROL Add representation]** 按鈕並根據需要添加多個表示法。

   ![](../../assets/offer-add-representation.png)

1. 添加所有表示法後，選擇 **[!UICONTROL Next]**。

## 定義表示法的內容 {#content}

可以向表示法中添加不同類型的內容。

>[!NOTE]
>
>只有與放置的內容類型對應的內容可供使用。

### 新增影像 {#images}

如果所選位置是影像類型，則可添加來自 **Adobe Experience Cloud資產** 庫，由 [!DNL Adobe Experience Manager Assets Essentials]。

>[!NOTE]
>
> 使用 [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=en){target=&quot;_blank&quot;}，需要部署 [!DNL Assets Essentials] 確保用戶是組織的一部分 **Assets Essentials消費者用戶** 或 **Assets Essentials用戶** 產品配置檔案。 瞭解更多 [此頁](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}。

1. 選取 **[!UICONTROL Asset library]** 選項。

1. 選擇「**[!UICONTROL Browse]**」。

   ![](../../assets/offer-browse-asset-library.png)

1. 瀏覽資產以選擇您選擇的影像

1. 按一下「**[!UICONTROL Select]**」。

   ![](../../assets/offer-select-asset.png)

### 添加URL {#urls}

要從外部公共位置添加內容，請選擇 **[!UICONTROL URL]**，然後輸入要添加的內容的URL地址。

![](../../assets/offer-content-url.png)

### 添加自定義文本 {#custom-text}

在選擇相容的放置時，也可插入文本類型內容。

1. 選擇 **[!UICONTROL Custom]** 選項 **[!UICONTROL Add content]**。

   ![](../../assets/offer-add-content.png)

   >[!NOTE]
   >
   >此選項不可用於影像類型放置。

1. 鍵入將在優惠中顯示的文本。

   ![](../../assets/offer-text-content.png)

   可以使用表達式編輯器個性化您的內容。 瞭解更多 [個性化](../../personalization/personalize.md#use-expression-editor)。

   ![](../../assets/offer-personalization.png)

   >[!NOTE]
   >
   >僅 **[!UICONTROL Profile attributes]**。 **[!UICONTROL Segment memberships]** 和 **[!UICONTROL Helper functions]** 源可用於決策管理。

## 添加資格規則和約束 {#eligibility}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="關於提供約束"
>abstract="有了約束，您可以指定與其他優惠相比如何優先化並呈現給用戶。"
>additional-url="https://video.tv.adobe.com/v/329375" text="觀看示範影片"

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="關於提供資格"
>abstract="在本節中，您可以使用決策規則來確定哪些用戶有資格獲得此優惠。"
>additional-url="https://video.tv.adobe.com/v/329373" text="觀看示範影片"

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="關於優惠優先順序"
>abstract="在此欄位中，可以指定優惠的優先順序設定。 優先順序是用於對滿足所有約束（如資格、日期和上限設定）的優惠進行評級的數字。"
>additional-url="https://video.tv.adobe.com/v/329375" text="觀看示範影片"

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="關於服務封頂"
>abstract="在此欄位中，您可以指定在所有用戶之間提供優惠的次數。"
>additional-url="https://video.tv.adobe.com/v/329375" text="觀看示範影片"

資格規則和約束允許您定義顯示聘用的條件。

1. 配置 **[!UICONTROL Offer eligibility]**。

   * 預設情況下， **[!UICONTROL All visitors]** 選擇了「決策規則」選項，這意味著任何配置檔案都有資格提供此優惠。

   * 您可以將要約的呈現限制在一個或多個Adobe Experience Platform段的成員。 為此，請激活 **[!UICONTROL Visitors who fall into one or multiple segments]** 選項，然後從左窗格中添加一個或多個段，並使用 **[!UICONTROL And]** / **[!UICONTROL Or]** 邏輯運算子。

      有關如何使用段的詳細資訊，請參閱 [此頁](../../segment/about-segments.md)。

      ![](../../assets/offer-eligibility-segment.png)

   * 如果要將特定決策規則與聘用關聯，請選擇 **[!UICONTROL By defined decision rule]**，然後將所需規則從左窗格拖動到 **[!UICONTROL Decision rule]** 的子菜單。 有關如何建立決策規則的詳細資訊，請參閱 [此部分](../offer-library/creating-decision-rules.md)。

      ![](../../assets/offer_rule.png)

      >[!CAUTION]
      >
      >當前不支援基於事件的服務 [!DNL Journey Optimizer]。 如果根據 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}，您將無法在優惠中利用它。
   瞭解有關使用段與決策規則的詳細資訊 [此部分](../offer-activities/create-offer-activities.md#segments-vs-decision-rules)。

1. 定義 **[!UICONTROL Priority]** 如果用戶有資格獲得多個優惠，則與其他優惠相比。 優先順序越高，優先順序就越高。

1. 指定優惠 **[!UICONTROL Capping]**，表示將在所有用戶中全部顯示此優惠的次數。 如果已在所有用戶中傳遞了您在此欄位中指定的次數，則其傳遞將停止。

   >[!NOTE]
   >
   >在電子郵件準備時間計算建議的次數。 例如，如果您準備包含多個優惠方案的電子郵件，無論是否有傳送電子郵件，這些數量都會計入您的次數上限中。
   >
   >如果刪除了電子郵件傳遞，或在發送前再次完成了準備，則自動更新優惠的上限值。

   ![](../../assets/offer_capping.png)

   在上例中：

   * 優先順序設為&quot;50&quot;，這意味著在優先順序介於1和49之間的要約之前，以及在優先順序至少為51的要約之後，將提出要約。
   * 僅對符合「金會員客戶」決策規則的用戶考慮此優惠。
   * 每個用戶將僅提供一次優惠。

## 查看優惠 {#review}

一旦定義了資格規則和約束，將顯示聘用屬性的摘要。

1. 確保所有內容都配置正確。

1. 當您的產品可供向用戶展示時，按一下 **[!UICONTROL Finish]**。

1. 選擇「**[!UICONTROL Save and approve]**」。

   ![](../../assets/offer_review.png)

   您還可以將聘用保存為草稿，以便稍後編輯和批准。

在清單中顯示聘用， **[!UICONTROL Approved]** 或 **[!UICONTROL Draft]** 狀態，具體取決於您在上一步中是否批准了它。

現在，它已準備好交付給用戶。

![](../../assets/offer_created.png)

## 優惠清單 {#offer-list}

從聘用清單中，您可以選擇聘用以顯示其屬性。 您還可以編輯它，更改它的狀態(**草稿**。 **已批准**。 **存檔**)、複製或刪除此選項。

![](../../assets/offer_created.png)

選擇 **[!UICONTROL Edit]** 按鈕，返回至「聘用版」模式，在該模式中您可以修改聘用 [詳細資訊](#create-offer)。 [表示](#representations)，以及編輯 [資格規則和約束](#eligibility)。

選擇批准的優惠，然後按一下 **[!UICONTROL Undo approve]** 將聘用狀態設定回 **[!UICONTROL Draft]**。

將狀態再次設定為 **[!UICONTROL Approved]**，選擇現在顯示的相應按鈕。

![](../../assets/offer_approve.png)

的 **[!UICONTROL More actions]** 按鈕啟用下面描述的操作。

![](../../assets/offer_more-actions.png)

* **[!UICONTROL Duplicate]**:建立具有相同屬性、表示法、資格規則和約束的聘用。 預設情況下，新優惠 **[!UICONTROL Draft]** 狀態。
* **[!UICONTROL Delete]**:從清單中刪除優惠。

   >[!CAUTION]
   >
   >此服務及其內容將不再可訪問。 此操作無法撤消。
   >
   >如果在集合或決策中使用要約，則不能刪除該要約。 必須首先從任何對象中刪除聘用。

* **[!UICONTROL Archive]**:將聘用狀態設定為 **[!UICONTROL Archived]**。 此優惠仍可從清單中獲得，但您無法將其狀態設定回 **[!UICONTROL Draft]** 或 **[!UICONTROL Approved]**。 您只能複製或刪除它。

您也可以通過選中相應的複選框同時刪除或更改多個優惠的狀態。

![](../../assets/offer_multiple-selection.png)

如果要更改多個狀態不同的聘用的狀態，則只更改相關狀態。

![](../../assets/offer_change-status.png)

一旦建立了優惠，您就可以從清單中按一下其名稱。

![](../../assets/offer_click-name.png)

這使您能夠訪問該服務的詳細資訊。 選擇 **[!UICONTROL Change log]** 頁籤 [監視所有更改](../get-started/user-interface.md#monitoring-changes) 已經提出的。

![](../../assets/offer_information.png)

## 教程視頻 {#video}

>[!NOTE]
>
>此視頻適用於在Adobe Experience Platform上構建的Offer decisioning應用程式服務。 然而，它為在Journey Optimizer背景下使用要約提供了一般性指導。

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
