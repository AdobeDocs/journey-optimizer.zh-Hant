---
solution: Journey Optimizer
product: journey optimizer
title: 建置您的第一個規則
description: 瞭解如何為您的協調行銷活動建立規則
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 5e956a6a-0b89-4d78-8f16-fe9fceb25674
source-git-commit: 6574735581de0872e78e8e05efea5c6a50dc59b1
workflow-type: tm+mt
source-wordcount: '1801'
ht-degree: 7%

---

# 建置您的第一個規則 {#build-query}

+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調的行銷活動活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](configuration-steps.md)<br/><br/>[存取及管理協調的行銷活動](access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的重要步驟](gs-campaign-creation.md)<br/><br/>[建立並設定行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[傳送包含協調行銷活動的訊息](send-messages.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/><b>[建立您的第一個查詢](build-query.md)</b><br/><br/>[編輯運算式](edit-expressions.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[並加入](activities/and-join.md) - [建置對象](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調解](activities/reconciliation.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

為您協調的行銷活動建立規則的主要步驟如下：

1. **新增條件** — 使用資料庫和進階運算式的屬性建立您自己的條件，以建立自訂條件來篩選查詢。
1. **合併條件** — 使用群組和邏輯運運算元排列畫布中的條件。
1. **檢查並驗證規則** — 在儲存規則之前，先檢查規則的結果資料。

## 新增條件 {#conditions}

若要在查詢中新增條件，請遵循下列步驟：

1. 從&#x200B;**[!UICONTROL 建置對象]**&#x200B;活動存取規則產生器。

1. 按一下&#x200B;**新增條件**&#x200B;按鈕，為您的查詢建立第一個條件。

   您也可以使用預先定義的篩選器來開始查詢。 若要這麼做，請按一下&#x200B;**[!UICONTROL 選取或儲存篩選器]**&#x200B;按鈕，然後選擇&#x200B;**[!UICONTROL 選取預先定義的篩選器]**。

   ![影像顯示規則產生器](assets/rule-builder-add.png)

1. 識別資料庫中的屬性，以用作條件的條件。 屬性旁的「i」圖示提供有關其儲存位置及其資料型別的表格資訊。

   顯示屬性選取範圍的![影像](assets/rule-builder-select-attribute.png)

   >[!NOTE]
   >
   >**編輯運算式**&#x200B;按鈕可讓您使用運算式編輯器，使用資料庫和協助程式函式的欄位來手動定義運算式。 [瞭解如何編輯運算式](../orchestrated/edit-expressions.md)

1. 按一下屬性旁顯示[更多動作]按鈕![&#128279;](assets/do-not-localize/rule-builder-icon-more.svg)的影像，以存取這些其他選項：

+++ 值分佈

   分析表格中指定屬性的值分佈。 此功能對於了解可用的數值、其計數和百分比相當有用。在建立查詢或建立運算式時，此功能還有助於避免出現大小寫或拼字不一致等問題。

   對於具有較多數值的屬性，該工具只會顯示前二十個數值。在這種情況下，會出現&#x200B;**[!UICONTROL 部分載入]**&#x200B;通知來表示有這個限制。您可以套用進階篩選器來調整顯示的結果，並聚焦於特定值或資料子集。

   ![影像顯示值分佈介面](assets/rule-builder-distribution-values.png)

+++

+++ 新增至我的最愛

   將屬性新增至我的最愛功能表，可讓您快速存取最常使用的屬性。 您最多可以新增20個屬性至我的最愛。 最愛和最近使用的屬性與組織內的每位使用者相關聯，確保在不同機器上也能方便存取，並提供跨裝置的順暢體驗。

   若要存取您最喜愛的屬性，請使用&#x200B;**[!UICONTROL 我的最愛和最近]**&#x200B;功能表。 最愛屬性會先出現，接著出現最近使用的屬性，讓您輕鬆找到所需屬性。 若要從最愛中移除屬性，請再次選取星形圖示。

   ![顯示我的最愛介面的影像](assets/rule-builder-favorites.png)

+++

1. 按一下&#x200B;**[!UICONTROL 確認]**，將選取的屬性新增至您的條件。

1. 會顯示屬性窗格，您可以在其中設定所需的屬性值。

   ![影像顯示新增了條件的規則產生器](assets/rule-builder-condition.png)

1. 從下拉式清單中選取要套用的&#x200B;**[!UICONTROL 運運算元]**。 可以使用各種運運算元。 下拉式清單中可用的運運算元取決於屬性的資料型別。

   +++可用運運算元清單

   | 運算子 | 目的 | 範例 |
   |---|---|---|
   | 等於 | 傳回與第二個「值」欄中所輸入資料相同的結果。 | 姓氏(@lastName)等於&#39;Jones&#39;只會傳回姓氏為Jones的收件者。 |
   | 不等於 | 傳回所有與輸入值不相同的值。 | 語言(@language)不等於&#39;English&#39;。 |
   | 大於 | 傳回大於輸入值的值。 | 年齡(@age)大於50會傳回所有大於「50」的值，例如「51」、「52」。 |
   | 小於 | 傳回小於輸入值的值。 | 「DaysAgo(100)」之前的建立日期(@created)將傳回所有在100天前建立的收件者。 |
   | 大於或等於 | 傳回等於或大於輸入值的所有值。 | 年齡(@age)大於或等於「30」將會傳回年齡等於或大於30歲的所有收件者。 |
   | 小於或等於 | 傳回等於或小於輸入值的所有值。 | 年齡(@age)小於或等於「60」將會傳回年齡等於或小於60歲的所有收件者。 |
   | 包含在 | 傳回指定值中包含的結果。 這些值必須以逗號分隔。 | 包含在「12/10/1979,12/10/1984」中的出生日期(@birthDate)將傳回這些日期之間出生的收件者。 |
   | 不在 | 其運作方式與「包含於」運運算元類似。 在這裡，收件者會根據輸入的值排除。 | 出生日期(@birthDate)不包含在&#39;12/10/1979,12/10/1984&#39;中。 將不會傳回在這些日期內出生的收件者。 |
   | 是空的 | 傳回與第二個「值」欄中的空值相符的結果。 | 行動裝置(@mobilePhone)為空白會傳回所有沒有行動號碼的收件者。 |
   | 不是空的 | 與Is empty運運算元相反的運作方式。 不需要在第二個「值」欄中輸入資料。 | 電子郵件(@email)不是空的。 |
   | 開始於 | 傳回以輸入值開頭的結果。 | 帳戶# (@account)以「32010」開頭。 |
   | 開頭不是 | 傳回不是以輸入值開頭的結果。 | 帳戶# (@account)的開頭不是&#39;20&#39;。 |
   | 包含 | 傳回至少包含輸入值的結果。 | 包含&#39;mail&#39;的電子郵件網域(@domain)將傳回包含&#39;mail&#39;的所有網域名稱，例如&#39;gmail.com&#39;。 |
   | 不包含 | 傳回不包含輸入值的結果。 | 電子郵件網域(@domain)不包含「vo」。 包含&#39;vo&#39;的網域名稱（例如&#39;voila.fr&#39;）將不會顯示在結果中。 |
   | 類似 | 與Contains運運算元類似，它可讓您在值中插入%萬用字元。 | 姓氏(@lastName)類似&#39;Jon%s&#39;。 萬用字元可當做「小丑」來尋找「Jones」之類的名稱。 |
   | Not like | 與Contains運運算元類似，它可讓您在值中插入%萬用字元。 | 姓氏(@lastName)不像&#39;Smi%h&#39;。 不會傳回姓氏為&#39;Smith&#39;的收件者。 |

   +++

1. 在&#x200B;**值**&#x200B;欄位中，定義預期的值。 您也可以使用運算式編輯器，以使用資料庫和協助程式函式的欄位，手動定義運算式。 若要這麼做，請按一下顯示運算式編輯器圖示![&#128279;](assets/do-not-localize/rule-builder-icon-editor.svg)圖示的影像。 [瞭解如何編輯運算式](../orchestrated/edit-expressions.md)

   對於日期型別屬性，預先定義的值可使用&#x200B;**[!UICONTROL 預設集]**&#x200B;選項。

   +++請參閱範例

   ![影像顯示預設集選項](assets/rule-builder-attribute-preset.png)

   +++

### 連結表格的自訂條件（1-1和1-N連結）{#links}

自訂條件可讓您查詢連結至規則目前使用之表格的表格。 這包括具有1-1基數連結的表格，或集合表格（1-N連結）。

若為&#x200B;**1-1連結**，請瀏覽至連結的資料表，選取所需的屬性並定義預期值。

您也可以直接選取&#x200B;**值**&#x200B;選擇器中的資料表連結並進行確認。 在此情況下，必須使用專用的選擇器來選取可用於所選表格的值，如以下範例所示。

+++查詢範例

在此，查詢會鎖定其標籤為「執行中」的品牌。

1. 在&#x200B;**Brand**&#x200B;資料表中導覽，並選取&#x200B;**標籤**&#x200B;屬性。

   ![品牌資料表的熒幕擷圖](assets/rule-builder-1-1-attribute.png)

1. 定義屬性的預期值。

   ![品牌資料表的熒幕擷圖](assets/rule-builder-1-1-attribute-value.png)

以下是已直接選取表格連結的查詢範例。 必須從專用選擇器選取此資料表的可用值。

![品牌資料表的熒幕擷圖](assets/rule-builder-1-1-attribute-table.png)

+++

對於&#x200B;**1-N連結**，您可以定義子條件來調整查詢，如下列範例所示。

+++查詢範例

在此，查詢會鎖定購買與Brewmsaster產品相關且價格超過100$的收件者。

1. 選取&#x200B;**Purchases**&#x200B;資料表並確認。

1. 按一下&#x200B;**[!UICONTROL 新增條件]**&#x200B;以定義要套用至所選資料表的子條件。

   ![購買資料表的熒幕擷圖](assets/rule-builder-1-n-purchase.png)

1. 新增子條件以符合您的需求。

   ![購買資料表的熒幕擷圖](assets/rule-builder-1-n-collection.png)

+++

### 包含彙總資料的自訂條件 {#aggregate}

自訂條件可讓您執行彙總作業。 若要這麼做，您必須直接從集合表格中選取屬性：

1. 在所需的集合表格內導覽，並選取您要執行彙總作業的屬性。

1. 在屬性窗格中，開啟&#x200B;**彙總資料**&#x200B;選項並選取所需的彙總函式。

   ![彙總資料選項的熒幕擷圖](assets/rule-builder-aggregate.png)

## 使用運運算元結合條件 {#operators}

每次在規則中新增條件時，就會使用&#x200B;**AND**&#x200B;運運算元自動連結至現有條件。 這表示兩個條件產生的結果會結合在一起。

若要變更條件之間的運運算元，請按一下該運運算元，然後選取所需的運運算元。

![查詢範例](assets/rule-builder-change-operator.png)

可用的運運算元包括：

* **AND （交集）**：結合符合出站轉變中所有篩選元件的結果。
* **OR （聯集）**：包含至少符合出站轉變中一個篩選元件的結果。
* **EXCEPT （排除）**：排除符合出站轉變中所有篩選元件的結果。

## 操作條件 {#manipulate}

規則產生器畫布工具列提供了可輕鬆操控規則內條件的選項：

| 工具列圖示 | 說明 |
|--- |--- |
| ![上移選取範圍圖示](assets/do-not-localize/rule-builder-icon-up.svg) | 將元件向上移動一列。 |
| ![下移選取範圍圖示](assets/do-not-localize/rule-builder-icon-down.svg) | 將元件下移一列。 |
| ![群組選擇圖示](assets/do-not-localize/rule-builder-icon-group.svg) | 將兩個元件放在一個群組中。 |
| ![取消群組選取範圍圖示](assets/do-not-localize/rule-builder-icon-ungroup.svg) | 將單一群組的元件分開。 |
| ![全部展開圖示](assets/do-not-localize/rule-builder-icon-expand.svg) | 展開所有群組。 |
| ![摺疊所有圖示](assets/do-not-localize/rule-builder-icon-collapse.svg) | 摺疊所有群組。 |
| ![移除所有圖示](assets/do-not-localize/rule-builder-icon-delete.svg) | 移除所有群組和元件。 |

視您的需求而定，您可能需要將元件分組到相同群組並將它們連結在一起，以建立中繼元件群組。

* 若要群組兩個現有條件，請選取兩個條件之一，然後按一下![向上移動選取範圍圖示](assets/do-not-localize/rule-builder-icon-up.svg)或![向下移動選取範圍圖示](assets/do-not-localize/rule-builder-icon-down.svg)按鈕，以群組條件高於或低於。

* 若要將現有條件群組為新條件，請選取條件，按一下顯示[更多動作]按鈕(assets/do-not-localize/rule-builder-icon-more.svg)按鈕的![影像，然後選取[新增群組]]&#x200B;**。**&#x200B;選取要新增至群組的新屬性，然後確認。

  ![](assets/rule-builder-edit-groups.png)

在下列範例中，我們已建立中繼群組，將目標鎖定於購買BrewMaster或VanillaVelvet產品的客戶。

![](assets/rule-builder-groups.png)

## 檢查並驗證您的查詢

在畫布中建立查詢後，您可以使用&#x200B;**規則屬性**&#x200B;窗格來檢查查詢。 可用的操作包括：

* **檢視結果：**&#x200B;顯示查詢產生的資料。
* **程式碼檢視**：顯示SQL查詢的程式碼型版本。
* **計算**：更新並顯示規則所定位的記錄數目。
* **選取或儲存篩選器**：選擇現有的預先定義篩選器以用於畫布中，或將您的查詢儲存為預先定義的篩選器，以供日後重複使用。

<br/>

    >[！IMPORTANT]
    >
    >從[規則屬性]窗格中選取預先定義的篩選器，以選取的篩選器取代畫布中建置的規則。

當您的規則準備就緒時，請按一下中的&#x200B;**[!UICONTROL 確認]**&#x200B;按鈕以儲存。
