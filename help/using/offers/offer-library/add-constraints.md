---
title: 向優惠添加約束
description: 瞭解如何定義要顯示的優惠條件
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: 8766f64c4ea7985c6c9d6e4ba022ef6b1fc0dbed
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 2%

---

# 向優惠添加約束 {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="關於提供約束"
>abstract="有了約束，您可以指定與其他優惠相比如何優先化並呈現給用戶。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_constraints"
>title="關於提供約束"
>abstract="有了約束，您可以指定與其他優惠相比如何優先化並呈現給用戶。"

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="關於優惠優先順序"
>abstract="在此欄位中，可以指定優惠的優先順序設定。 優先順序是用於對滿足所有約束（如資格、日期和上限設定）的優惠進行評級的數字。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="設定優先順序"
>abstract="如果用戶有資格獲得多個優惠，則優先順序有助於定義優惠與其他優惠相比的優先順序。 優先順序越高，優先順序就越高。"

約束允許您定義顯示要約的條件。

1. 配置 **[!UICONTROL Offer eligibility]**。 [了解更多](#eligibility)

   ![](../assets/offer-eligibility.png)

1. 定義 **[!UICONTROL Priority]** 如果用戶有資格獲得多個優惠，則與其他優惠相比。 優先順序越高，優先順序就越高。

   ![](../assets/offer-priority.png)

1. 指定優惠 **[!UICONTROL Capping]**，即提供要約的次數。 [了解更多](#capping)

   ![](../assets/offer-capping.png)

1. 按一下 **[!UICONTROL Next]** 確認所定義的所有約束。

例如，如果設定了以下約束：

![](../assets/offer-constraints-example.png)

* 僅對符合「金會員客戶」決策規則的用戶考慮此優惠。
* 優先順序設為&quot;50&quot;，這意味著在優先順序介於1和49之間的要約之前，以及在優先順序至少為51的要約之後，將提出要約。
* 該要約將在所有配售中按用戶僅提供一次。

## 資格 {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="定義資格"
>abstract="預設情況下，任何配置檔案都有資格向您提供優惠，但您可以使用段或決策規則將優惠限制到特定配置檔案。"

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="關於提供資格"
>abstract="在本節中，您可以使用決策規則來確定哪些用戶有資格獲得此優惠。"
>additional-url="https://video.tv.adobe.com/v/329373" text="觀看示範影片"

的 **[!UICONTROL Offer eligibility]** 部分允許您將優惠限制到使用段或決策規則定義的特定配置檔案。

>[!NOTE]
>
>瞭解有關使用的更多資訊 **段** 與 **決策規則** 在 [此部分](#segments-vs-decision-rules)。

* 預設情況下， **[!UICONTROL All visitors]** 選項，即表示任何配置檔案都有資格向您提供優惠。

   ![](../assets/offer-eligibility-default.png)

* 您還可以將提議的演示限於一個或多個成員 [Adobe Experience Platform段](../../segment/about-segments.md)。

   為此，請激活 **[!UICONTROL Visitors who fall into one or multiple segments]** 選項，然後從左窗格中添加一個或多個段，並使用 **[!UICONTROL And]** / **[!UICONTROL Or]** 邏輯運算子。

   ![](../assets/offer-eligibility-segment.png)

* 如果要關聯特定 [決策規則](../offer-library/creating-decision-rules.md) 選擇 **[!UICONTROL By defined decision rule]**，然後將所需規則從左窗格拖動到 **[!UICONTROL Decision rule]** 的子菜單。

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >當前不支援基於事件的服務 [!DNL Journey Optimizer]。 如果根據 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}，您將無法在優惠中利用它。

在選擇段或決策規則時，可以查看有關估計的限定配置檔案的資訊。 按一下 **[!UICONTROL Refresh]** 更新資料。

![](../assets/offer-eligibility-segment-estimate.png)

### 使用段與決策規則 {#segments-vs-decision-rules}

要應用約束，可以將聘用的選擇限制為一個或多個成員 **Adobe Experience Platform段**，或者 **決策規則**，兩個解決方案對應於不同的用途。

基本上，段的輸出是簡檔清單，而決策規則是在決策過程中根據需要針對單個簡檔執行的函式。 下面詳細說明了這兩種用途的區別。

* **區段**

   一方面，段是一組基於配置檔案屬性和經驗事件的Adobe Experience Platform配置檔案，它們與特定邏輯匹配。 然而，要約管理不會重新計算該段，該段在提出要約時可能不是最新的。

   瞭解有關 [此部分](../../segment/about-segments.md)。

* **決定規則**

   另一方面，決策規則基於Adobe Experience Platform的可用資料，並確定可向誰顯示報價。 一旦在某個要約或某個給定位置的決定中選擇了該規則，則每次作出決定時都會執行該規則，這可確保每個配置檔案都獲得最新和最佳的要約。

   瞭解有關中的決策規則的詳細資訊 [此部分](creating-decision-rules.md)。

## 封頂 {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="關於服務封頂"
>abstract="在此欄位中，您可以指定提供優惠的次數。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="使用封蓋"
>abstract="為避免過度吸引客戶，請使用上限設定來定義提供服務的最大次數。"

封閉設定用作約束來定義提供的最大次數。

限制用戶獲得特定優惠的次數，可以避免過度取悅客戶，從而以最佳優惠優化每個觸點。

要設定封蓋，請執行以下步驟。

1. 定義提供服務的次數。

   ![](../assets/offer-capping-times.png)

   >[!NOTE]
   >
   >該數字必須是大於0的整數。

1. 指定是希望將上限設定應用於所有用戶還是某個特定配置檔案：

   ![](../assets/offer-capping-total.png)

   * 選擇 **[!UICONTROL In total]** 定義在組合目標受眾中建議的服務次數，即在所有用戶中建議。

      例如，如果您是電子零售商，有「電視門衛交易」，則您希望在所有配置檔案中僅返回200次優惠。

   * 選擇 **[!UICONTROL Per profile]** 定義可向同一用戶建議的次數。

      例如，如果您是一家提供「白金信用卡」優惠的銀行，則您不希望此優惠在每個配置檔案中顯示5次以上。 事實上，您認為，如果用戶看過5次並未對其採取行動，他們就更有機會對下一個最佳報價採取行動。

1. 如果定義了 [表示](#representations) 指定是否要應用封頂 **[!UICONTROL Across all placements]** 或 **[!UICONTROL For each placement]**。

   ![](../assets/offer-capping-placement.png)

   * **[!UICONTROL Across all placements]**:上限計數將匯總與要約關聯的放置中的所有決定。

      例如，如果優惠 **電子郵件** 放置和 **Web** 放置，並將封蓋設定為 **每個配置2個**&#x200B;然後，無論放置組合如何，每個配置檔案總共可收到2次優惠。

   * **[!UICONTROL For each placement]**:封閉計數將分別應用每個放置的決策計數。

      例如，如果優惠 **電子郵件** 放置和 **Web** 放置，並將封蓋設定為 **每放置2個輪廓**&#x200B;然後，每個配置檔案最多可以收到兩次電子郵件放置服務，另外兩次則可以收到兩次網路放置服務。

1. 保存並批准後，如果根據您定義的條件顯示了您在此欄位中指定的次數，則其交付將停止。

在電子郵件準備時間計算建議的次數。 例如，如果您準備包含多個優惠方案的電子郵件，無論是否有傳送電子郵件，這些數量都會計入您的次數上限中。

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>封頂計數器將在要約到期或要約開始日期後兩年（以最先到達的日期為準）時重置。 瞭解如何在中定義優惠日期 [此部分](creating-personalized-offers.md#create-offer)。

### 更改日期對上限設定的影響 {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="更改日期會影響封頂"
>abstract="如果對此優惠應用了上限設定，則更改起始日期或終止日期時可能會影響它。"

更改要約日期時，必須小心行事，因為如果滿足以下條件，這可能會對封頂產生影響：

* 我的提議是 [批准](#review)。
* [封頂](#capping) 已應用於要約。
* 按配置檔案定義封頂。

>[!NOTE]
>
>瞭解如何在中定義優惠日期 [此部分](creating-personalized-offers.md#create-offer)。

每個配置檔案的封頂儲存每個配置檔案的封頂計數。 更改批准的優惠的開始和結束日期時，某些配置檔案的上限設定計數可能會根據下面介紹的不同方案受到影響。

![](../assets/offer-capping-change-date.png)

以下是可能的情況 **更改聘用開始日期**:

| 方案：<br>如果…… | 結果是：<br>然後…… | 可能對上限計數的影響 |
|--- |--- |--- |
| ...在原始要約開始日期開始之前更新要約開始日期， | ...封頂計數將從新開始日期開始。 | 無 |
| ...新開始日期早於當前結束日期， | ...封頂將繼續使用新的開始日期，並且每個配置檔案的上一個封頂計數將繼續。 | 無 |
| ...新開始日期晚於當前結束日期， | ...當前上限設定將過期，新上限設定計數將從新開始日期的所有配置檔案的0重新開始。 | 是 |

以下是可能的情況 **延長聘用結束日期**:

| 方案：<br>如果…… | 結果是：<br>然後…… | 可能對上限計數的影響 |
|--- |--- |--- |
| ...在原始要約結束日期之前發生決定請求， | ...將更新封頂計數，並且每個配置檔案的上一個封頂計數將繼續。 | 無 |
| ...在原始結束日期之前不發生決定請求， | ...每個配置檔案的封頂計數將在原始結束日期重置。 然後，對於將在原始結束日期之後發生的任何新決定請求，新的上限設定計數將從0重新開始。 | 是 |

**範例**

假設您的報價原始開始日期設定為 **1月1日**，過期 **1月31日**。

1. 給出X、Y和Z輪廓。
1. 開 **1月10日**，優惠的結束日期更改為 **2月15日**。
1. **1月11日至1月31日**，只提供輪廓Z。

   * 因為在原始結束日期之前發生了決策請求 **對於配置檔案Z**，可將要約的結束日期延長到 **2月15日**。
   * 但是，由於在原始結束日期之前未發生任何活動 **配置檔案X和Y**，其計數器將過期，其上限計數將重置為0 **1月31日**。

![](../assets/offer-capping-change-date-ex.png)
