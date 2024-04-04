---
title: 在優惠中新增限制
description: 瞭解如何定義優惠方案顯示的條件
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: 4342c13d7f2cff4eea3bb3cdddad8f403f0cba90
workflow-type: tm+mt
source-wordcount: '2617'
ht-degree: 15%

---

# 在優惠中新增限制 {#add-constraints}

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

限制可讓您定義優惠的顯示條件。

1. 設定 **[!UICONTROL 優惠資格]**. [了解更多](#eligibility)

   ![](../assets/offer-eligibility.png)

1. 定義 **[!UICONTROL 優先順序]** 相較於其他優惠方案（如果使用者符合多個優惠方案的資格）。 優惠的優先順序越高，相較於其他優惠的優先順序就越高。

   ![](../assets/offer-priority.png)

   >[!NOTE]
   >
   >優惠優先順序必須為整數值（無小數）。

1. 指定優惠方案的 **[!UICONTROL 上限]**，表示選件出現的次數。 [了解更多](#capping)

   ![](../assets/offer-capping.png)

1. 按一下 **[!UICONTROL 下一個]** 以確認您所定義的所有限制。

例如，如果您設定下列限制：

![](../assets/offer-constraints-example.png)

* 只有符合「金級忠誠客戶」決策規則的使用者才會考量此優惠。
* 優惠方案的優先順序設為「50」，這表示將會在優先順序介於1到49的優惠方案之前以及優先順序至少為51的優惠方案之後顯示優惠方案。
* 每個使用者在所有位置每月只會顯示一次選件。

## 適用性 {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="定義資格"
>abstract="依預設，任何設定檔都有資格獲得優惠，但您可以使用對象或決定規則將優惠限制給特定設定檔。"

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="關於優惠資格"
>abstract="在此部分，您可以使用決定規則來確定哪些使用者有資格獲得優惠。"
>additional-url="https://video.tv.adobe.com/v/329373" text="觀看示範影片"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_total_profile_estimate"
>title="總設定檔估計值"
>abstract="當您選取對象或決定規則時，您可以看到有關預估合格設定檔的資訊。"

此 **[!UICONTROL 優惠資格]** 區段可讓您將優惠限制在您使用對象或決定規則定義的特定設定檔中。

>[!NOTE]
>
>進一步瞭解使用 **對象** 與 **決定規則** 在 [本節](#segments-vs-decision-rules).

* 根據預設， **[!UICONTROL 所有訪客]** 選項已選取，這表示任何設定檔都符合呈現優惠方案的資格。

  ![](../assets/offer-eligibility-default.png)

* 您也可以將優惠方案的呈現方式限制在一或多個成員中 [Adobe Experience Platform對象](../../audience/about-audiences.md).

  若要這麼做，請啟動 **[!UICONTROL 屬於一或多個對象的訪客]** 選項，然後從左窗格新增一或多個對象，並使用 **[!UICONTROL 與]** / **[!UICONTROL 或]** 邏輯運運算元。

  ![](../assets/offer-eligibility-segment.png)

* 如果您想要關聯特定 [決定規則](../offer-library/creating-decision-rules.md) 若要選取選件，請選取 **[!UICONTROL 依定義的決定規則]**，然後將所需的規則從左窗格拖曳至 **[!UICONTROL 決定規則]** 區域。

  ![](../assets/offer-rule.png)

  >[!CAUTION]
  >
  >目前不支援事件型優惠方案 [!DNL Journey Optimizer]. 如果您根據 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events){target="_blank"}，您將無法在選件中運用它。

當您選取對象或決定規則時，您可以檢視有關預估合格設定檔的資訊。 按一下 **[!UICONTROL 重新整理]** 以更新資料。

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>當規則引數包含不在設定檔中的資料（例如內容資料）時，設定檔預估無法使用。 例如，適用性規則要求目前天氣為≥80度。

### 使用對象與決定規則 {#segments-vs-decision-rules}

若要套用限制，您可以將優惠方案選取限制在一或多個成員中 **Adobe Experience Platform對象**，或您可以使用 **決定規則**，這兩個解決方案分別對應不同的使用方式。

基本上，對象的輸出是設定檔清單，而決定規則是在決策流程期間根據單一設定檔執行的函式。 這兩種使用方式的差異詳述如下。

* **對象**

  一方面，受眾是一組Adobe Experience Platform設定檔，根據設定檔屬性和體驗事件符合特定邏輯。 不過，Offer Management不會重新計算對象，在展示優惠方案時，該對象可能不是最新狀態。

  進一步瞭解中的對象 [本節](../../audience/about-audiences.md).

* **決定規則**

  另一方面，決定規則會根據Adobe Experience Platform中的可用資料，並決定可向誰顯示優惠方案。 在優惠或指定位置的決定中選取後，每次做出決定時都會執行規則，以確保每個設定檔取得最新和最佳優惠。

  進一步瞭解中的決定規則 [本節](creating-decision-rules.md).

## 頻率限定 {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="關於優惠上限"
>abstract="在此欄位中，您可以指定優惠可以呈現的次數。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="使用上限"
>abstract="為避免過度招攬客戶，請使用上限來定義優惠的呈現次數上限。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints.html?lang=zh-Hant#capping-change-date" text="變更日期會影響上限"

上限會用作限制，以定義可顯示優惠方案的次數上限。

限制使用者取得特定優惠方案的次數，可讓您避免過度向客戶提供需求，進而使用最佳優惠方案將每個接觸點最佳化。

若要設定上限，請遵循下列主要步驟。

1. 確定 **[!UICONTROL 啟用上限]** 切換按鈕已選取。 上限預設為啟用。

   >[!CAUTION]
   >
   >無法啟用或停用先前建立之優惠方案的頻率限定。 若要這麼做，您需要建立新的選件。

1. 定義哪些 **[!UICONTROL 事件上限]** 將考慮以增加計數器。 [了解更多](#capping-event)

1. 設定可顯示優惠方案的次數。 [了解更多](#capping-count)

1. 選取要將上限套用至所有使用者或僅套用至一個設定檔。 [了解更多](#capping-type)

1. 設定 **[!UICONTROL 頻率]** 以定義上限計數的重設頻率。 [了解更多](#frequency-capping)

1. 如果您已定義數個 [表示方式](add-representations.md) 針對您的優惠，指定是否要套用上限 **橫跨所有位置** 或 **至每個位置**. [了解更多](#placements)

1. 在儲存並核准後，如果根據您定義的條件和時間範圍，已根據您在此欄位中指定的次數向優惠方案顯示次數，則其傳送將停止。

系統會在準備電子郵件時計算建議某個優惠方案的次數。 例如，如果您準備包含多個優惠方案的電子郵件，無論是否有傳送電子郵件，這些數量都會計入您的次數上限中。

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>優惠到期時或優惠方案開始日期後2年（以先到者為準）時，上限計數器會重設。 瞭解如何在中定義優惠方案的日期 [本節](creating-personalized-offers.md#create-offer).

### 頻率限定事件 {#capping-event}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping_impression"
>title="曝光"
>abstract="使用曝光數做為上限事件僅適用於傳入管道。"

此 **[!UICONTROL 事件上限]** 欄位可讓您定義要考慮哪個事件以增加計數器：

![](../assets/offer-capping-event.png)

* **[!UICONTROL 決定事件]** （預設值）：可顯示優惠方案的次數上限。
* **[!UICONTROL 印象]**：優惠方案可向使用者顯示的最大次數。

  >[!NOTE]
  >
  >將曝光次數用作上限事件可供使用 **傳入頻道** 僅限。

* **[!UICONTROL 點按次數]**：使用者可點按選件的最大次數。
* **[!UICONTROL 自訂事件]**：您可以定義自訂事件，用於限制傳送的優惠方案數量。 例如，您可以限制贖回次數，直到它們相等10000或直到指定的設定檔已贖回1次。 若要這麼做，請使用 [ADOBE EXPERIENCE PLATFORM XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"} 用於建置自訂事件規則的結構描述。

  <!--For example, you can cap on the number of redemptions so that the offer can be shown until redemptions equal 10000. You can only select XDM ExperienceEvents. -->

  在下列範例中，您想要限制結帳次數。

   1. 選取 **[!UICONTROL 自訂事件]** 從清單中使用 **[!UICONTROL 新增自訂事件]** 按鈕。

      ![](../assets/offer-capping-custom-event-add.png)

   1. 使用 **[!UICONTROL 建立自訂事件規則]** 產生器以選取相關事件。 您可以選擇任何您想要限制選件的使用者動作。

      在這裡選擇 **[!UICONTROL 商務]** > **[!UICONTROL 結帳]** > **[!UICONTROL 值]** 並選取 **[!UICONTROL 已存在]** 下拉式清單中的。

      ![](../assets/offer-capping-custom-event.png)

   1. 規則建立後，會顯示在 **[!UICONTROL 自訂事件查詢]** 欄位。

      ![](../assets/offer-capping-custom-event-query.png)

>[!CAUTION]
>
>對於決策事件以外的所有上限事件，決策管理意見可能不會自動收集，這可能會導致上限計數器未正確增加。 [了解更多](../data-collection/data-collection.md)
>
>若要確保在上限計數器中已追蹤和說明每個上限事件，請確定用於收集體驗事件的結構描述包含該事件的正確欄位群組。 [了解更多](../data-collection/schema-requirement.md)

### 上限計數 {#capping-count}

此 **[!UICONTROL 上限計數限制]** 欄位可讓您指定可顯示優惠方案的次數。

![](../assets/offer-capping-times.png)

>[!NOTE]
>
>數字必須是大於0的整數。

例如，您定義了自訂上限事件，例如將結帳次數納入考量。 如果您在 **[!UICONTROL 上限計數限制]** 欄位，10次結帳後不會傳送其他優惠。

### 上限型別 {#capping-type}

您也可以指定是否要將上限套用至所有使用者或一個特定設定檔：

![](../assets/offer-capping-total.png)

* 選取 **[!UICONTROL 總計]** 定義一個優惠方案在合併目標對象中可建議的次數，亦即在所有使用者中均可建議。

  例如，如果您是具有「電視看門人交易」的電子零售商，您只想要在所有設定檔中傳回200次選件。

* 選取 **[!UICONTROL 每個設定檔]** 以定義可向同一位使用者建議某個優惠方案的次數。

  例如，如果您是具有「白金信用卡」優惠方案的銀行，您不希望此優惠方案在每個設定檔中顯示超過5次。 事實上，您相信，如果使用者看過5次選件且未採取行動，則他們有較高機會對下一個最佳選件採取行動。

### 頻率限定 {#frequency-capping}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="設定上限頻率"
>abstract="您可以選擇每天、每週或每月重設優惠上限計數器。請注意，啟用頻率限定並發佈優惠後，您將無法變更已定義的頻率。"

此 **[!UICONTROL 頻率]** 區段可讓您定義上限計數的重設頻率。 若要這麼做，請定義盤點的期間（每日、每週或每月），並輸入您選擇的天數/周數/月數。 例如，如果您希望每兩週重設一次上限計數，請選取 **[!UICONTROL 每週]** 從對應的下拉式清單及型別 **2** 在另一個欄位中。

![](../assets/offer-capping-frequency.png)

>[!NOTE]
>
>頻率限定計數器重設發生於 **UTC上午12點**，日期為您定義的日期，或在一週/月的第一天（若適用）。 周開始日為 **星期日**. 您選擇的任何期間不能超過 **2年** （即對應的月數、周數或天數）。
>
>發佈優惠方案後，您將無法變更您為頻率選取的時間期間（每月、每週或每日）。 如果優惠方案具有 **[!UICONTROL 草稿]** 狀態且之前從未發佈，並啟用了頻率限定。

+++ **必讀：頻率限定和邊緣決策API**

頻率上限計數器已更新，並可在不到3秒的時間內用於邊緣決策API決策。

每個中心區域都與一個或多個邊緣區域相關聯。 頻率限定規則會從每個中心區域產生並匯出至其關聯的邊緣區域。 每當使用邊緣決策API做出決策時，系統都會強制實施相同邊緣區域中可用的規則：

* 如果有相符的規則，則設定檔的頻率上限計數器會增加。
* 否則，不會為設定檔建立計數器，且頻率上限規則不適用。 因此，即使超過上限臨界值，設定檔仍會繼續收到個人化優惠。

例如，我們將貴組織的中心區域視為 *NLD2*，而您正在傳送來自歐洲的決策請求(*IRL1* 邊緣區域)。 在此案例中，決策請求將遞增設定檔的計數器，因為規則可在（愛爾蘭）中使用 *IRL1* 區域。 但是，如果決策請求來自日本等地區(*日文3*)，這不是繫結至（荷蘭）的邊緣區域 *NLD2* 中樞區域，將不會建立計數器，且不會強制執行頻率限定規則。

如需瞭解哪些中心與邊緣區域與貴組織建立關聯，請洽詢您的Adobe代表。

+++

### 上限和版位 {#placements}

如果您已定義數個 [表示方式](add-representations.md) 針對您的選件，指定是否要對所有版位或每個版位套用上限。

![](../assets/offer-capping-placement.png)

* **[!UICONTROL 對所有位置套用上限]**：上限計數會加總與優惠方案相關之各個版位的所有決策。

  例如，如果選件具有 **電子郵件** 位置和 **Web** 位置，並將上限設定在 **所有位置中每個設定檔2個**，則無論版位組合為何，每個設定檔最多可以收到選件2次。

* **[!UICONTROL 將上限套用至每個位置]**：上限計數將分別套用每個位置的決定計數。

  例如，如果選件具有 **電子郵件** 位置和 **Web** 位置，並將上限設定在 **每個位置每個設定檔2個**，則每個設定檔最多可收到電子郵件版2次選件，以及額外的2次網路版。

### 變更日期對頻率限定的影響 {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="變更日期會影響上限"
>abstract="如果將上限套用到此優惠，則當您變更開始或結束日期時，它可能會受到影響。"

變更優惠方案的日期時，您必須謹慎進行，因為如果符合以下條件，這可能會對上限產生影響：

* 選件為 [已核准](#review).
* [上限](#capping) 已套用至優惠方案。
* 上限是按設定檔定義的。

>[!NOTE]
>
>瞭解如何在中定義優惠方案的日期 [本節](creating-personalized-offers.md#create-offer).

每個設定檔的上限會儲存每個設定檔的上限計數。 當您變更已核准優惠方案的開始和結束日期時，部分設定檔的上限計數可能會根據以下所述的不同情況而受到影響。

![](../assets/offer-capping-change-date.png)

以下是以下可能的情況 **變更優惠方案開始日期**：

| 案例：<br>若…… | 發生什麼情況：<br>然後…… | 對上限計數的可能影響 |
|--- |--- |--- |
| ...優惠方案開始日期會在原始優惠方案開始日期之前更新， | ...上限計數將從新的開始日期開始。 | 無 |
| ...新的開始日期在目前的結束日期之前， | ...上限會以新的開始日期繼續，而每個設定檔的先前上限計數則會延續。 | 無 |
| ...新的開始日期在目前結束日期之後， | ...目前的上限將會到期，而新的上限計數將會從新開始日期的所有設定檔的0重新開始。 | 是 |

以下是以下可能的情況 **延長優惠方案結束日期**：

| 案例：<br>若…… | 發生什麼情況：<br>然後…… | 對上限計數的可能影響 |
|--- |--- |--- |
| ...決策請求在原始優惠方案結束日期之前發生， | ...上限計數將更新，每個設定檔的先前上限計數將結轉。 | 無 |
| ...在原始結束日期之前不會發生任何決策請求， | ...上限計數將在每個設定檔的原始結束日期重設。 新的上限計數隨後將從0開始，任何新決策請求將發生在原始結束日期之後。 | 是 |

**範例**

假設您有一個優惠方案，其原始開始日期設為 **1月1日**，到期日 **1,31日**.

1. 選件中會顯示設定檔X、Y和Z。
1. 開啟 **10年1月**，優惠方案的結束日期會變更為 **2月15日**.
1. **從1月11日至1月31日**，只有設定檔Z會呈現選件。

   * 因為決策請求發生在原始結束日期之前 **設定檔Z**，優惠方案的結束日期可延長至 **2月15日**.
   * 不過，因為沒有活動在的原始結束日期之前發生 **設定檔X和Y**，其計數器將會過期，且其上限計數將於重設為0 **1,31日**.

![](../assets/offer-capping-change-date-ex.png)
