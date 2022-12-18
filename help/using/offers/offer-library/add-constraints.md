---
title: 新增限制至選件
description: 了解如何定義要顯示的優惠方案條件
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: e81e21f714a3c5450defa1129e1e2b9969dc1de7
workflow-type: tm+mt
source-wordcount: '1715'
ht-degree: 2%

---

# 新增限制至選件 {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="關於選件限制"
>abstract="有了限制，您可以指定相較於其他選件，優先順序和呈現給使用者的方式。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_constraints"
>title="關於選件限制"
>abstract="有了限制，您可以指定相較於其他選件，優先順序和呈現給使用者的方式。"

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="關於選件優先順序"
>abstract="在此欄位中，您可以指定選件的優先順序設定。 優先順序是用來對符合資格、日期和上限等所有限制的優惠方案排名的數字。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="設定優先順序"
>abstract="如果使用者符合多個優惠方案的資格，優先順序有助於定義優惠方案的優先順序，而非其他優惠方案。 優惠方案的優先順序越高，優先順序與其他優惠方案相比就越高。"

限制可讓您定義顯示優惠方案的條件。

1. 設定 **[!UICONTROL 優惠方案資格]**. [了解更多](#eligibility)

   ![](../assets/offer-eligibility.png)

1. 定義 **[!UICONTROL 優先順序]** 選件的數量，而非其他選件（如果使用者符合多個選件的資格）。 優惠方案的優先順序越高，優先順序與其他優惠方案相比就越高。

   ![](../assets/offer-priority.png)

1. 指定選件的 **[!UICONTROL 限定]**，表示將呈現選件的次數。 [了解更多](#capping)

   ![](../assets/offer-capping.png)

1. 按一下 **[!UICONTROL 下一個]** 以確認您定義的所有限制。

例如，若您設定下列限制：

![](../assets/offer-constraints-example.png)

* 只有符合「金級忠誠客戶」決策規則的使用者才會考慮此優惠方案。
* 優先順序設為「50」，這表示優惠方案會在優先順序介於1到49之間的優惠方案之前，以及優先順序至少為51的優惠方案之後呈現。
* 優惠方案只會針對所有版位的每位使用者呈現一次。

## 資格 {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="定義資格"
>abstract="依預設，任何設定檔都有資格呈現選件，但您可以使用區段或決策規則，將選件限制在特定設定檔。"

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="關於優惠方案資格"
>abstract="在本節中，您可以使用決策規則來判斷哪些使用者符合該優惠方案的資格。"
>additional-url="https://video.tv.adobe.com/v/329373" text="觀看示範影片"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_total_profile_estimate"
>title="設定檔估計總計"
>abstract="選取區段或決策規則時，您可以看到預估合格設定檔的相關資訊。"

此 **[!UICONTROL 優惠方案資格]** 區段可讓您限制選件使用區段或決策規則定義的特定設定檔。

>[!NOTE]
>
>深入了解使用 **區段** vers **決策規則** in [本節](#segments-vs-decision-rules).

* 依預設， **[!UICONTROL 所有訪客]** 選項，表示任何設定檔都有資格呈現選件。

   ![](../assets/offer-eligibility-default.png)

* 您也可以將優惠方案的呈現方式限制為一或數個 [Adobe Experience Platform區段](../../segment/about-segments.md).

   若要這麼做，請啟用 **[!UICONTROL 落入一或多個區段的訪客]** 選項，然後從左側窗格新增一或多個區段，並使用 **[!UICONTROL 和]** / **[!UICONTROL 或]** 邏輯運算子。

   ![](../assets/offer-eligibility-segment.png)

* 如果您想關聯特定 [決策規則](../offer-library/creating-decision-rules.md) 選取 **[!UICONTROL 依定義的決策規則]**，然後將所需規則從左窗格拖曳至 **[!UICONTROL 決策規則]** 的上界。

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >目前不支援以事件為基礎的選件 [!DNL Journey Optimizer]. 如果您根據 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}，您將無法在選件中運用它。

選取區段或決策規則時，您可以看到預估合格設定檔的相關資訊。 按一下 **[!UICONTROL 重新整理]** 更新資料。

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>當規則參數包含不在設定檔中的資料（例如內容資料）時，設定檔估計將無法使用。 例如，適用性規則要求目前的天氣為≥80度。

### 使用區段與決策規則 {#segments-vs-decision-rules}

要應用約束，可以將選件的選擇限制在一個或多個成員 **Adobe Experience Platform區段**，或者您可以使用 **決策規則**，兩個解決方案會對應不同的使用方式。

基本上，區段的輸出是設定檔清單，而決策規則則是決策過程中針對單一設定檔依需求執行的函式。 以下詳細說明這兩種用法之間的差異。

* **區段**

   一方面，區段是一組Adobe Experience Platform設定檔，會根據設定檔屬性和體驗事件來比對特定邏輯。 不過，Offer Management不會重新計算區段，這在呈現優惠方案時可能不會是最新的。

   進一步了解 [本節](../../segment/about-segments.md).

* **決定規則**

   另一方面，決策規則是以Adobe Experience Platform中可用的資料為基礎，並決定可向誰顯示優惠方案。 在優惠方案中選取或針對指定版位的決策後，每次做出決策時，都會執行規則，以確保每個設定檔都能取得最新和最佳的優惠方案。

   進一步了解中的決策規則 [本節](creating-decision-rules.md).

## 限定 {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="關於選件限定"
>abstract="在此欄位中，您可以指定可呈現選件的次數。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="使用上限設定"
>abstract="為避免過度吸引客戶，請使用上限來定義可呈現選件的次數上限。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="設定限定頻率"
>abstract="您可以選擇每天、每週或每月重設優惠方案限定計數器。"

上限設定是用來定義可呈現選件的最大次數的限制。

限制使用者取得特定優惠方案的次數，可讓您避免過度吸引客戶，進而以最佳優惠方案最佳化每個接觸點。

要設定上限，請執行以下步驟。

1. 定義可呈現選件的次數。

   ![](../assets/offer-capping-times.png)

   >[!NOTE]
   >
   >數字必須是大於0的整數。

1. 指定您要將限定套用至所有使用者或特定設定檔：

   ![](../assets/offer-capping-total.png)

   * 選擇 **[!UICONTROL 總計]** 定義可在合併的目標對象中建議某個優惠方案的次數，亦即在所有使用者中。

      例如，如果您是電子產品零售商，且有「電視門衛交易」，則您希望在所有設定檔中僅傳回選件200次。

   * 選擇 **[!UICONTROL 每個設定檔]** 定義可向相同使用者建議某個優惠方案的次數。

      例如，如果您是擁有「白金信用卡」優惠的銀行，您不希望此優惠在每個設定檔中顯示超過5次。 事實上，您認為如果使用者看過選件5次而未對其採取行動，他們就更有機會對下一個最佳選件採取行動。
   <!--
    Set the **[!UICONTROL Frequency]** to define how often the capping count is reset. To do so, define the time period for the counting (daily, weekly or monthly) and enter the number of days/weeks/months of your choice.
    ![](../assets/offer-capping-frequency.png)
    >[!NOTE]
    >
    >The reset happens at 12am UTC, on the day that you defined or on the first day of the week/month when applicable. The week start day is Sunday.
    
    For example, if you want the capping count to be reset every 2 weeks, select **[!UICONTROL Weekly]** from the **[!UICONTROL Repeat]** drop-down list and type **2** in the other field. The reset will happen every other Sunday at 12pm UTC.
    -->

1. 如果您已定義數個 [表示](add-representations.md) 指定您是否要套用上限 **[!UICONTROL 所有版位]** 或 **[!UICONTROL 對於每個版位]**.

   ![](../assets/offer-capping-placement.png)

   * **[!UICONTROL 所有版位]**:上限計數將總計與優惠方案相關聯之所有版位上的所有決策。

      例如，如果選件具有 **電子郵件** 版位和 **Web** 放置，並且在 **所有版位中每個設定檔2個**，則無論版位組合為何，每個設定檔總共可接收優惠方案最多2次。

   * **[!UICONTROL 對於每個版位]**:上限計數將分別套用每個版位的決策計數。

      例如，如果選件具有 **電子郵件** 版位和 **Web** 放置，並且在 **每個版位每個設定檔2個**，則每個設定檔最多可接收電子郵件版位的2次優惠，而網路版位則可接收2次優惠。

1. 儲存並核准後，如果根據條件和您定義的時間範圍，向選件呈現您在此欄位中指定的次數，則其傳送將停止。

系統會在準備電子郵件時計算建議某個優惠方案的次數。 例如，如果您準備包含多個優惠方案的電子郵件，無論是否有傳送電子郵件，這些數量都會計入您的次數上限中。

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>優惠方案過期或優惠方案開始日期後2年（以先發生者為準）時，設定上限計數器會重設。 了解如何在 [本節](creating-personalized-offers.md#create-offer).

### 變更日期對限定的影響 {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="變更日期可能會影響限定"
>abstract="如果對此選件套用上限設定，當您變更開始或結束日期時，可能會受到影響。"

變更優惠方案的日期時，您必須小心處理，因為若符合下列條件，這可能會對限定產生影響：

* 選件是 [核准](#review).
* [限定](#capping) 已套用至選件。
* 限定是按配置檔案定義的。

>[!NOTE]
>
>了解如何在 [本節](creating-personalized-offers.md#create-offer).

每個設定檔的上限設定會儲存每個設定檔的上限設定計數。 當您變更已核准優惠方案的開始和結束日期時，某些設定檔的上限計數可能會根據下列不同案例受到影響。

![](../assets/offer-capping-change-date.png)

以下是可能的情況： **變更優惠方案開始日期**:

| 案例：<br>如果…… | 結果：<br>然後…… | 可能對上限計數的影響 |
|--- |--- |--- |
| ...優惠方案開始日期會在原始優惠方案開始日期開始之前更新， | ...上限計數將從新開始日期開始。 | 無 |
| ...新開始日期早於目前結束日期， | ...限定會繼續使用新的開始日期，且每個設定檔的先前限定計數會持續。 | 無 |
| ...新開始日期晚於目前結束日期， | ...目前上限將過期，且新上限計數將從新開始日期上所有設定檔的0重新開始。 | 是 |

以下是可能的情況： **延長優惠方案結束日期**:

| 案例：<br>如果…… | 結果：<br>然後…… | 可能對上限計數的影響 |
|--- |--- |--- |
| ...決策請求會在原始選件結束日期之前發生， | ...會更新上限計數，且每個設定檔的先前上限計數會持續。 | 無 |
| ...在原始結束日期之前不會發生決策請求， | ...每個設定檔的原始結束日期將會重設上限計數。 之後，任何將在原始結束日期之後發生的新決策請求，新的上限計數將從0重新開始。 | 是 |

**範例**

假設您的優惠方案將原始開始日期設為 **1月1日**，到期 **1931年1月**.

1. 會呈現選件的設定檔X、Y和Z。
1. 開啟 **2010年1月**，則選件的結束日期會變更為 **2月15日**.
1. **1月11日至1月31日**，只會呈現選件Z。

   * 因為決策請求是在原始結束日期之前發生 **Z**，則選件的結束日期可延長至 **2月15日**.
   * 但是，由於在的原始結束日期之前未發生任何活動 **設定檔X和Y**，其計數器將過期，其上限計數將在上重設為0 **1931年1月**.

![](../assets/offer-capping-change-date-ex.png)
