---
title: 在電子郵件中使用個人化優惠方案
description: 探索端對端範例，展示設定優惠方案並在電子郵件中使用這些優惠方案所需的所有步驟。
feature: 優惠
topic: 整合
role: User
level: Intermediate
source-git-commit: a6a421fc23f4564bb24061c019c9418b491e7eee
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 3%

---

# 使用案例：設定個人化優惠方案以在電子郵件{#configure-add-personalized-offers-email}中使用

本節提供端對端範例，說明如何根據您先前建立的決策，設定優惠方案並在電子郵件中使用優惠方案。

## 主要步驟

設定優惠方案、將優惠方案納入決策以及在電子郵件中運用此決策的關鍵步驟如下：

1. 建立選件之前，請[定義元件](#define-components)

   * 建立位置
   * 建立決定規則
   * 建立標籤
   * 建立排名（可選）

1. [設定優惠方案](#configure-offers)

   * 建立優惠方案
   * 對於每個選件：

      * 建立表示，並為每個表示選擇放置和資產
      * 為每個選件新增規則
      * 為每個選件定義優先順序

1. [建立遞補優惠](#create-fallback)

1. [建立集合](#create-collection) 以包含您建立的個人化優惠方案

1. [設定決策](#configure-decision)

   * 建立決定
   * 選取您建立的版位
   * 為每個版位選取集合
   * 對於每個版位，選取排名（選用）
   * 選擇回退

1. [在電子郵件中插入決策](#insert-decision-in-email)

   * 選取符合您要顯示之優惠方案的版位
   * 從與所選位置相容的項目中選擇決策
   * 預覽優惠方案

在電子郵件中使用優惠方案的整體決策管理程式如下：

![](../assets/offers-e2e-process.png)

## 定義元件{#define-components}

開始建立選件之前，您必須定義要在選件中使用的數個元件。

您會在&#x200B;**[!UICONTROL Decision Management]** > **[!UICONTROL Components menu]**&#x200B;下找到它們。

1. 首先，為優惠方案建立&#x200B;**版位**。

   定義優惠方案決策時，您將使用這些版位來定義結果優惠方案的顯示位置。

   在此範例中，建立三個版位，其中包含下列管道和內容類型：

   * *Web — 影像*
   * *電子郵件 — 影像*
   * *非數位 — 文字*

   ![](../assets/offers-e2e-placements.png)

   建立版位的詳細步驟在[本節](../../using/offers/offer-library/creating-placements.md)中有說明。

1. 建立&#x200B;**決策規則**。

   決策規則會為Adobe Experience Platform中的設定檔提供最佳選件。

   使用&#x200B;**[!UICONTROL XDM Individual Profile > Person > Gender]**&#x200B;屬性設定兩個簡單規則：

   * *女性客戶*
   * *男性客戶*

   ![](../assets/offers-e2e-rules.png)

   建立規則的詳細步驟在[本節](../../using/offers/offer-library/creating-decision-rules.md)中介紹。

1. 您也可以建立&#x200B;**標籤**。

   然後，您就能將選件與選件建立關聯，並使用此標籤將您的選件群組到集合中。

   在此範例中，建立&#x200B;*Yoga*&#x200B;標籤。

   ![](../assets/offers-e2e-tag.png)

   建立標籤的詳細步驟在[本區段](../../using/offers/offer-library/creating-tags.md)中說明。

1. 如果您想要定義規則，以決定應先針對指定版位呈現哪個優惠方案（而非考慮優惠方案的優先順序分數），您可以建立&#x200B;**排名公式**。

   [本節](../../using/offers/offer-library/create-ranking-formulas.md#create-ranking-formula)中描述了建立排名公式的詳細步驟。

   >[!NOTE]
   >
   >在此範例中，我們只會使用優先順序分數。 深入了解[適用性規則和限制](../../using/offers/offer-library/creating-personalized-offers.md#eligibility)。

## 設定選件{#configure-offers}

您現在可以建立和設定優惠方案。 在此範例中，您將建立四個要根據每個特定設定檔顯示的選件。

1. 建立優惠方案. 進一步了解[本節](../../using/offers/offer-library/creating-personalized-offers.md#create-offer)。

1. 在此選件中，建立三個表示法。 每個表示都必須是您先前建立的版位與資產的組合：

   * 對應於&#x200B;*Web — 影像*&#x200B;放置的一個
   * 與&#x200B;*電子郵件 — 影像*&#x200B;位置對應的一個
   * 與&#x200B;*非數字 — 文字*&#x200B;位置對應的一個

   >[!NOTE]
   >
   >優惠方案可顯示在訊息中的不同位置，以建立更多機會，以便在不同版位內容中使用優惠方案。

   進一步了解[本節](../../using/offers/offer-library/creating-personalized-offers.md#representations)中的表示法。

1. 為前兩個版位選取適當的影像。 輸入&#x200B;*非數字 — 文字*&#x200B;版位的自訂文字。

   ![](../assets/offers-e2e-representations.png)

1. 在&#x200B;**[!UICONTROL Offer eligiblity]**&#x200B;區段中，選取&#x200B;**[!UICONTROL By defined decision rule]**&#x200B;並拖放您選取的規則。

   ![](../assets/offers-e2e-eligibility.png)

1. 填寫&#x200B;**[!UICONTROL Priority]**。 在此範例中，新增&#x200B;*25*。

1. 檢閱您的選件，然後按一下&#x200B;**[!UICONTROL Save and approve]**。

   ![](../assets/offers-e2e-review.png)

1. 在此範例中，使用相同表示法建立另外三個選件，但使用不同的資產。 以不同的規則和優先順序指派給使用者，例如：

   * 第一個選件 — 決策規則：*女性客戶*，優先順序：*25*
   * 第二個選件 — 決策規則：*女性客戶*，優先順序：*15*
   * 第三個選件 — 決策規則：*男性客戶*，優先順序：*25*
   * 第四個優惠方案 — 決策規則：*男性客戶*，優先順序：*15*

   ![](../assets/offers-e2e-offers-created.png)

建立和設定選件的詳細步驟在[本區段](../../using/offers/offer-library/creating-personalized-offers.md)中說明。

## 建立遞補優惠 {#create-fallback}

1. 建立遞補優惠.

1. 為選件定義相同的表示法，並搭配適當的資產（這些表示法應與選件中使用的表示法不同）。

   每個表示都必須是您先前建立的版位與資產的組合：

   * 對應於&#x200B;*Web — 影像*&#x200B;放置的一個
   * 與&#x200B;*電子郵件 — 影像*&#x200B;位置對應的一個
   * 與&#x200B;*非數字 — 文字*&#x200B;位置對應的一個

   ![](../assets/offers-e2e-fallback-representations.png)

1. 檢閱您的備援優惠方案，然後按一下&#x200B;**[!UICONTROL Save and approve]**。

![](../assets/offers-e2e-fallback.png)

您的備援優惠方案現在已準備好用於決策。

建立和設定備援優惠方案的詳細步驟在[本節](../../using/offers/offer-library/creating-fallback-offers.md)中有說明。

## 建立集合 {#create-collection}

設定決策時，您需要將個人化優惠方案新增為集合的一部分。

1. 若要加速決策程式，請建立動態集合。

1. 使用&#x200B;*Yoga*&#x200B;標籤來選取您先前建立的四個個人化選件。

   ![](../assets/offers-e2e-collection-using-tag.png)

建立集合的詳細步驟在[本節](../../using/offers/offer-library/creating-collections.md)中有說明。

## 配置決策{#configure-decision}

現在，您必須建立決策，將版位與您剛建立的個人化優惠方案和備援優惠方案結合。

此組合將供Offer decisioning引擎用來尋找特定設定檔的最佳選件：在此範例中，它將以您指派給每個選件的優先順序和決策規則為基礎。

若要建立和設定優惠方案決策，請遵循下列主要步驟：

1. 建立決定. 進一步了解[本節](../../using/offers/offer-activities/create-offer-activities.md#create-activity)。

1. 選取&#x200B;*Web - Image*、*Email - Image*&#x200B;和&#x200B;*Non-digital - Text*&#x200B;版位。

   ![](../assets/offers-e2e-decision-placements.png)

1. 對於每個版位，新增您建立的集合。

   ![](../assets/offers-e2e-decision-collection.png)

1. 如果您在[建立元件](#define-components)時定義了排名，則可將其指派給決策中的位置。 如果有多個優惠方案符合在此版位中呈現的資格，決策會使用此公式計算要先傳送的優惠方案。

   [本節](../../using/offers/offer-activities/configure-offer-selection.md#assign-ranking-formula)中描述了將排名公式分配給版位的詳細步驟。

1. 選取您建立的備援優惠方案。 它會顯示為三個所選版位的可用後援優惠方案。

   ![](../assets/offers-e2e-decision-fallback.png)

1. 檢閱您的決定，然後按一下&#x200B;**[!UICONTROL Save and approve]**。

   ![](../assets/offers-e2e-review-decision.png)

您的決策現在已準備好用於提供最佳化和個人化的優惠方案。

建立和配置決策的詳細步驟在[本部分](../../using/offers/offer-activities/create-offer-activities.md)中介紹。

## 在電子郵件{#insert-decision-in-email}中插入決策

現在您的決策已上線，您可以將其插入電子郵件訊息中。 要執行此操作，請遵循下列步驟：

1. 建立電子郵件，然後開啟[電子郵件設計工具](../../using/design-emails.md)以設定其內容。

1. 從左側浮動視窗新增結構元件。

1. 新增&#x200B;**[!UICONTROL Offer decision]**&#x200B;內容元件。 了解如何在[本小節](../../using/content-components.md)中使用內容元件。

   ![](../assets/offers-e2e-decision-component.png)

1. 請選取模式。在右側浮動視窗中，按一下&#x200B;**[!UICONTROL Select offer decision]**&#x200B;以新增決策。

   ![](../assets/offers-e2e-select-offer-decision.png)

1. 從&#x200B;**[!UICONTROL Placements]**&#x200B;下拉式清單中，選取與您要顯示之優惠方案相對應的位置。

   在此案例中，您先前在此範例中建立的版位中，只有&#x200B;**電子郵件 — 影像**&#x200B;版位可供您在電子郵件中使用決策時使用。 深入了解[建立版位](../../using/offers/offer-library/creating-placements.md)。

   ![](../assets/offers-e2e-select-placement-in-decision.png)

1. 會顯示與&#x200B;**電子郵件 — 影像**&#x200B;位置相符的決策。 選取要在內容元件中使用的決策，然後按一下&#x200B;**[!UICONTROL Add]**。

   ![](../assets/offers-e2e-matching-placement-in-decision.png)

   >[!NOTE]
   >
   >只有與所選位置相容的決策才會顯示在清單中。

您現在可以在電子郵件設計工具中看到所有個人化優惠方案，以及後援優惠方案正在視覺化。

![](../assets/offers-e2e-offers-displayed.png)

使用&#x200B;**[!UICONTROL Offers]**&#x200B;區段或內容元件箭頭（向右和向左箭頭）來瀏覽資料。 您也可以使用客戶設定檔來顯示屬於決策一部分的不同選件。 進一步了解[本節](../../using/deliver-personalized-offers.md#preview-offers-in-email)。

儲存變更後及發佈訊息後，您的選件就可以在歷程中傳送訊息時，顯示給相關設定檔。

**相關主題：**

* 了解如何在[此區段](../../using/preview.md#preview-your-messages)中檢查訊息預覽。

* 了解如何在[此小節](../../using/publish-manage-message.md)中發佈訊息。

* 在[本區段](../building-journeys/journey.md)中了解一或多個歷程如何觸發訊息。

