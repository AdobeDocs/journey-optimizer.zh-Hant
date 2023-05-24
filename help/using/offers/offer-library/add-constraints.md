---
title: 向優惠添加約束
description: 瞭解如何定義要顯示的優惠條件
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '2357'
ht-degree: 17%

---

# 向優惠添加約束 {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="關於優惠限制"
>abstract="透過限制，您可以指定與其他優惠相比，如何確定優惠的優先順序並呈現給使用者。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_constraints"
>title="關於優惠限制"
>abstract="透過限制，您可以指定與其他優惠相比，如何確定優惠的優先順序並呈現給使用者。"

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="關於優惠優先順序"
>abstract="在此欄位中，您可以指定優惠的優先順序設定。優先順序是一個數字，用於對滿足所有限制 (例如資格、日期和上限) 的優惠進行排名。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="設定優先順序"
>abstract="如果使用者符合資格可獲得多個優惠，則優先順序有助於定義優惠相較於其他優惠的優先順序。優惠的優先順序越高，相較於其他優惠的優先順序就越高。"

約束允許您定義顯示要約的條件。

1. 配置 **[!UICONTROL 提供資格]**。 [了解更多](#eligibility)

   ![](../assets/offer-eligibility.png)

1. 定義 **[!UICONTROL 優先順序]** 如果用戶有資格獲得多個優惠，則與其他優惠相比。 優惠的優先順序越高，相較於其他優惠的優先順序就越高。

   ![](../assets/offer-priority.png)

1. 指定優惠 **[!UICONTROL 封頂]**，即提供要約的次數。 [了解更多](#capping)

   ![](../assets/offer-capping.png)

1. 按一下 **[!UICONTROL 下一個]** 確認所定義的所有約束。

例如，如果設定了以下約束：

![](../assets/offer-constraints-example.png)

* 僅對符合「金會員客戶」決策規則的用戶考慮此優惠。
* 優先順序設為&quot;50&quot;，這意味著在優先順序介於1和49之間的要約之前，以及在優先順序至少為51的要約之後，將提出要約。
* 每個用戶每月只在所有配售中提出一次要約。

## 資格 {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="定義資格"
>abstract="依預設，任何設定檔都有資格獲得優惠，但您可以使用區段或決定規則將優惠限制給特定設定檔。"

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="關於優惠資格"
>abstract="在此部分，您可以使用決定規則來確定哪些使用者有資格獲得優惠。"
>additional-url="https://video.tv.adobe.com/v/329373" text="觀看示範影片"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_total_profile_estimate"
>title="總設定檔估計值"
>abstract="當您選擇區段或決定規則時，您可以看到有關預估合格設定檔的資訊。"

的 **[!UICONTROL 提供資格]** 部分允許您將優惠限制到使用段或決策規則定義的特定配置檔案。

>[!NOTE]
>
>瞭解有關使用的更多資訊 **段** 與 **決策規則** 在 [此部分](#segments-vs-decision-rules)。

* 預設情況下， **[!UICONTROL 所有訪問者]** 選項，即表示任何配置檔案都有資格向您提供優惠。

   ![](../assets/offer-eligibility-default.png)

* 您還可以將提議的演示限於一個或多個成員 [Adobe Experience Platform段](../../segment/about-segments.md)。

   為此，請激活 **[!UICONTROL 陷入一個或多個段的訪問者]** 選項，然後從左窗格中添加一個或多個段，並使用 **[!UICONTROL 和]** / **[!UICONTROL 或]** 邏輯運算子。

   ![](../assets/offer-eligibility-segment.png)

* 如果要關聯特定 [決策規則](../offer-library/creating-decision-rules.md) 選擇 **[!UICONTROL 按定義的決策規則]**，然後將所需規則從左窗格拖動到 **[!UICONTROL 決策規則]** 的子菜單。

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >當前不支援基於事件的服務 [!DNL Journey Optimizer]。 如果根據 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}你將無法在報價中利用它。

當您選擇區段或決定規則時，您可以看到有關預估合格設定檔的資訊。按一下 **[!UICONTROL 刷新]** 更新資料。

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>當規則參數包括不在配置檔案中的資料（如上下文資料）時，配置檔案估計不可用。 例如，要求當前天氣為≥80度的資格規則。

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
>title="關於優惠上限"
>abstract="在此欄位中，您可以指定優惠可以呈現的次數。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="使用上限"
>abstract="為避免過度招攬客戶，請使用上限來定義優惠的呈現次數上限。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints.html#capping-change-date" text="變更日期會影響上限"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="設定上限頻率"
>abstract="您可以選擇每天、每週或每月重設優惠上限計數器。請注意，儲存優惠後，您將無法變更所選頻率。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping_impression"
>title="曝光"
>abstract="使用曝光數做為上限事件僅適用於傳入管道。"

封閉設定用作約束來定義提供的最大次數。

限制用戶獲得特定優惠的次數，可以避免過度取悅客戶，從而以最佳優惠優化每個觸點。

要設定封蓋，請遵循以下主要步驟。

1. 確保 **[!UICONTROL 包括封頂]** 切換按鈕。 預設情況下包括封頂。

   >[!CAUTION]
   >
   >無法為先前建立的優惠啟用或禁用頻率上限設定。 為此，您需要複製優惠或建立新優惠。

1. 定義 **[!UICONTROL 封頂事件]** 會考慮增加計數器。 [了解更多](#capping-event)

1. 設定可以顯示要約的次數。 [了解更多](#capping-count)

1. 選擇是希望將上限設定應用於所有用戶還是僅應用一個配置檔案。 [了解更多](#capping-type)

1. 設定 **[!UICONTROL 頻率]** 定義重置上限計數的頻率。 [了解更多](#frequency-capping)

1. 如果定義了 [表示](add-representations.md) 指定是否要應用封頂 **[!UICONTROL 跨所有位置]** 或 **[!UICONTROL 對於每個位置]**。 [了解更多](#placements)

1. 保存並批准後，如果根據您定義的標準和時間範圍向您提供了在此欄位中指定的次數，則其交付將停止。

在電子郵件準備時間計算建議的次數。 例如，如果您準備包含多個優惠方案的電子郵件，無論是否有傳送電子郵件，這些數量都會計入您的次數上限中。

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>封頂計數器將在要約到期或要約開始日期後兩年（以最先到達的日期為準）時重置。 瞭解如何在中定義優惠日期 [此部分](creating-personalized-offers.md#create-offer)。

### 封頂事件 {#capping-event}

的 **[!UICONTROL 封頂事件]** 欄位，您可以定義 **[!UICONTROL 封頂事件]** 將考慮增加計數器：

![](../assets/offer-capping-event.png)

* **[!UICONTROL 決策事件]** （預設值）:提供優惠的最大次數。
* **[!UICONTROL 印象]**:向用戶顯示優惠的最大次數。

   >[!NOTE]
   >
   >可將印象用作封蓋事件 **入站通道** 只是。

* **[!UICONTROL 按一下]**:用戶可按一下優惠的最大次數。
* **[!UICONTROL 自定義事件]**:您可以定義一個自定義事件，該事件將用於限制發送的聘用數。 例如，您可以限制贖回次數，直到它們等於10000，或直到給定配置檔案已贖回1次。 為此，請使用 [Adobe Experience PlatformXDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"} 架構來構建自定義事件規則。

   <!--For example, you can cap on the number of redemptions so that the offer can be shown until redemptions equal 10000. You can only select XDM ExperienceEvents. -->

   在下例中，您要限制檢出數。

   1. 選擇 **[!UICONTROL 自定義事件]** 清單中的 **[!UICONTROL 添加自定義事件]** 按鈕

      ![](../assets/offer-capping-custom-event-add.png)

   1. 使用 **[!UICONTROL 建立自定義事件規則]** 生成器。 您可以選擇要限制優惠的任何用戶操作。

      此處選擇 **[!UICONTROL 商業]** > **[!UICONTROL 簽出]** > **[!UICONTROL 值]** 選擇 **[!UICONTROL 存在]** 從下拉清單中。

      ![](../assets/offer-capping-custom-event.png)

   1. 建立規則後，將在 **[!UICONTROL 自定義事件查詢]** 的子菜單。

      ![](../assets/offer-capping-custom-event-query.png)

>[!CAUTION]
>
>對於除決策事件之外的所有封閉事件，可能無法自動收集決策管理反饋，這可能導致封閉計數器不能正確遞增。 [了解更多](../data-collection/data-collection.md)
>
>要確保每個上限設定事件都在上限設定計數器中跟蹤和記帳，請確保用於收集體驗事件的架構包含該事件的正確欄位組。 [了解更多](../data-collection/schema-requirement.md)

### 上限計數 {#capping-count}

的 **[!UICONTROL 上限計數]** 欄位中，您可以指定提供服務的次數。

![](../assets/offer-capping-times.png)

>[!NOTE]
>
>該數字必須是大於0的整數。

例如，您定義了自定義封頂事件，例如考慮簽出數。 如果在 **[!UICONTROL 上限計數]** 欄位，在10個簽出後將不再發送任何優惠。

### 封蓋類型 {#capping-type}

您還可以指定是否希望將上限設定應用於所有用戶或某個特定配置檔案：

![](../assets/offer-capping-total.png)

* 選擇 **[!UICONTROL 合計]** 定義在組合目標受眾中建議的服務次數，即在所有用戶中建議。

   例如，如果您是電子零售商，有「電視門衛交易」，則您希望在所有配置檔案中僅返回200次優惠。

* 選擇 **[!UICONTROL 每個配置檔案]** 定義可向同一用戶建議的次數。

   例如，如果您是一家提供「白金信用卡」優惠的銀行，則您不希望此優惠在每個配置檔案中顯示5次以上。 事實上，您認為，如果用戶看過5次並未對其採取行動，他們就更有機會對下一個最佳報價採取行動。

### 頻率限定 {#frequency-capping}

的 **[!UICONTROL 頻率]** 部分允許您定義重置封閉計數的頻率。 為此，請定義盤點的時段（每日、每週或每月），並輸入您選擇的天數/周數/月數。

![](../assets/offer-capping-frequency.png)

>[!NOTE]
>
>重置在UTC的上午12點（在您定義的日期）或適用時在周/月的第一天進行。 周的開始日是星期日。 您選擇的任何持續時間都不能超過2年（即相應的月、周或天數）。

例如，如果希望每2週重置一次封頂計數，請選擇 **[!UICONTROL 每週]** 從 **[!UICONTROL 重複]** 下拉清單和類型 **2** 的下界。 重置將每隔一個星期日下午12點發生一次。

>[!CAUTION]
>
>保存優惠後，您將無法更改為頻率選擇的時段（每月、每週或每天）。

### 封頂和放置 {#placements}

如果定義了 [表示](add-representations.md) 指定是否要應用封頂 **[!UICONTROL 跨所有位置]** 或 **[!UICONTROL 對於每個位置]**。

![](../assets/offer-capping-placement.png)

* **[!UICONTROL 跨所有位置]**:上限計數將匯總與要約關聯的放置中的所有決定。

   例如，如果優惠 **電子郵件** 放置和 **Web** 放置，並將封蓋設定為 **每個配置2個**&#x200B;然後，無論放置組合如何，每個配置檔案總共可收到2次優惠。

* **[!UICONTROL 對於每個位置]**:封閉計數將分別應用每個放置的決策計數。

   例如，如果優惠 **電子郵件** 放置和 **Web** 放置，並將封蓋設定為 **每放置2個輪廓**&#x200B;然後，每個配置檔案最多可以收到兩次電子郵件放置服務，另外兩次則可以收到兩次網路放置服務。

### 更改日期對上限設定的影響 {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="變更日期會影響上限"
>abstract="如果將上限套用到此優惠，則當您變更開始或結束日期時，它可能會受到影響。"

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
