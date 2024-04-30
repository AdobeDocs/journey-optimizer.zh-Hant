---
title: 建立決定
description: 瞭解如何建立決定
feature: Experience Decisioning
topic: Integrations
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: d26b35ea680eae0e71eb3164b4225a49610e1563
workflow-type: tm+mt
source-wordcount: '1443'
ht-degree: 12%

---

# 建立決定原則 {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="什麼是決定？"
>abstract="決定原則利用體驗決定引擎，根據對象選擇要傳遞的最佳內容。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=zh-Hant" text="關於體驗決定"

>[!BEGINSHADEBOX 「本檔案指南提供哪些內容」]

* [開始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的決定專案： [設定專案目錄](catalogs.md) - [建立決定專案](items.md) - [管理專案集合](collections.md)
* 設定專案的選取範圍： [建立決定規則](rules.md) - [建立排名方法](ranking.md)
* [建立選擇策略](selection-strategies.md)
* **[建立決定原則](create-decision.md)**

>[!ENDSHADEBOX]

決策原則是優惠方案的容器，可運用體驗決策引擎，根據對象挑選最佳內容進行傳遞。

>[!NOTE]
>
>在 [!DNL Journey Optimizer] 使用者介面，決策原則會標示為決策<!--but they are decision policies. TBC if this note is needed-->.

## 將決定原則新增至基於程式碼的行銷活動 {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="定義要傳回的項目數量"
>abstract="選取您想要傳回的決定項目數量。例如，如果您選取 2，則目前表面將顯示最佳的 2 個符合資格優惠。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="選取遞補"
>abstract="當為該決定原則定義的所有選擇策略都不合格時，會向使用者顯示遞補項目。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="什麼是策略？"
>abstract="選擇策略的順序決定了先評估哪個策略。至少需要一個策略。組合策略中的決定項目將一起評估。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=zh-Hant" text="建立策略"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=zh-Hant" text="評估順序"

若要在您的網站或行動應用程式上向訪客呈現最佳動態優惠和體驗，請將決定原則新增至程式碼型行銷活動。 若要執行此操作，請遵循下列步驟。

1. 建立行銷活動並選取 **[!UICONTROL 程式碼型體驗(Beta)]** 動作。 [了解更多](../code-based/create-code-based.md)

   >[!NOTE]
   >
   >程式碼型體驗功能目前僅供特定使用者測試版。

1. 從 [程式碼編輯器](../code-based/create-code-based.md#edit-code)，選取 **[!UICONTROL 決定]** 圖示並按一下 **[!UICONTROL 建立決定]**.

   ![](assets/decision-code-based-create.png)

1. 填寫決策原則的詳細資訊：新增名稱並選取目錄。

   >[!NOTE]
   >
   >目前僅預設 **[!UICONTROL 選件]** 目錄可供使用。

   ![](assets/decision-code-based-details.png)

1. 選取要傳回的專案數。 例如，如果您選取2，則會針對目前曲面顯示最佳的2個合格選件。 按一下 **[!UICONTROL 下一個]**

1. 使用 **[!UICONTROL 新增策略]** 按鈕來定義決定原則的選取策略。 每個策略都包含與適用性限制相關聯的優惠方案集合，以及決定要顯示的優惠方案的排名方法。 [了解更多](selection-strategies.md)

   ![](assets/decision-code-based-strategies.png)

   >[!NOTE]
   >
   >至少需要一個策略。您無法新增超過10個策略。

1. 從 **[!UICONTROL 新增策略]** 畫面，您也可以建立策略。 此 **[!UICONTROL 建立選擇策略]** 按鈕會將您重新導向至 **[!UICONTROL 體驗決策]** > **[!UICONTROL 設定]** 功能表。 [了解更多](selection-strategies.md)

   ![](assets/decision-code-based-add-strategy.png)

1. 新增數個策略時，會以特定順序評估策略。 系統會先評估新增至序列的第一個策略，依此類推。 [了解更多](#evaluation-order)

   若要變更預設順序，您可以拖放策略及/或群組以視需要重新排序。

   ![](assets/decision-code-based-strategy-groups.png)

1. 新增遞補。 如果上述選取策略均不合格，則會向使用者顯示後援專案。

   ![](assets/decision-code-based-strategy-fallback.png)

   您可以從清單中選取任何專案，這會顯示在目前沙箱上建立的所有決定專案。 如果沒有合格的選取策略，則無論套用至所選專案的日期和適用性限製為何，都會對使用者顯示遞補<!--nor frequency capping when available - TO CLARIFY-->.

   >[!NOTE]
   >
   >遞補內容為選用。 如果未選取遞補策略，且沒有限定策略，則不會顯示任何專案。 [!DNL Journey Optimizer].

1. 儲存您的選取範圍並按一下 **[!UICONTROL 建立]**. 新的決定原則已新增到 **[!UICONTROL 決定]**.

   ![](assets/decision-code-based-decision-added.png)

現在決定原則已建立，您可以在程式碼型體驗內容中使用決定屬性。 [了解更多](#use-decision-policy)

## 評估順序 {#evaluation-order}

如上所述，策略包含集合、排名方法和資格限制。

您可以：

* 設定您要評估策略的循序順序，
* 結合多個策略，以便一起評估而不是分別評估。

多個策略及其分組決定策略的優先順序以及合格優惠的排名。 第一個策略具有最高優先順序，且在相同群組內合併的策略具有相同優先順序。

例如，您有兩個集合，一個在策略A中，另一個在策略B中。此請求是為了傳回兩個決定專案。 假設有兩個來自策略A的合格優惠方案和三個來自策略B的合格優惠方案。

* 如果兩個策略為 **未合併** 或依序順序（1和2），第一列中會傳回第一個策略的前兩個合格優惠方案。 如果第一個策略沒有兩個符合資格的優惠，決定引擎會依序移至下一個策略，以找出仍需要多少優惠方案，最終在需要時傳回遞補。

  ![](assets/decision-code-based-consecutive-strategies.png)

* 如果兩個集合為 **同時評估**，由於策略A有兩個合格優惠方案，策略B有三個合格優惠方案，因此這五個優惠方案都會根據各自的排名方法決定的值棧疊在一起。 已要求兩個優惠方案，因此將傳回這五個優惠方案中的前兩個合格優惠方案。

  ![](assets/decision-code-based-combined-strategies.png)

+++ **具有多種策略的範例**

現在，讓我們舉一個例子，您有劃分為不同群組的多個策略。

您定義了三種策略。 策略1和策略2在群組1中結合，而策略3是獨立的（群組2）。

每個策略的合格優惠方案及其優先順序（用於排名函式評估）如下：

* 群組1：
   * 策略1 - （選件1、選件2、選件3） — 優先順序1
   * 策略2 - （選件3、選件4、選件5） — 優先順序1

* 群組2：
   * 策略3 - （選件5、選件6） — 優先順序0

系統會先評估最高優先順序的策略選件，並將其新增至排名選件清單。

**反複專案1：**

策略1和策略2選件會一起評估（選件1、選件2、選件3、選件4、選件5）。 假設結果為：

選件1 - 10選件2 - 20選件3 - 30來自策略1,45來自策略2。 兩者中的最高會納入考量，因此會考慮45。
選件4 - 40選件5 - 50

排名優惠方案現在如下：優惠方案5、優惠方案3、優惠方案4、優惠方案2、優惠方案1。

**反複專案2：**

已評估策略3選件（選件5、選件6）。 假設結果為：

* 選件5 — 將不進行評估，因為它已存在於上述結果中。
* 選件6 - 60

排名優惠方案現在如下：優惠方案5 、優惠方案3、優惠方案4、優惠方案2、優惠方案1、優惠方案6。

+++

## 在程式碼編輯器中使用決定原則 {#use-decision-policy}

建立後，決策原則便可用於以下專案中 [運算式編輯器](../code-based/create-code-based.md#edit-code). 若要執行此操作，請遵循下列步驟。

>[!NOTE]
>
>程式碼型體驗會利用 [!DNL Journey Optimizer] 運算式編輯器及其所有個人化和編寫功能。 [了解更多](../personalization/personalization-build-expressions.md)

1. 按一下+圖示。 已新增與決定原則對應的程式碼。 現在，您可以在該程式碼中新增所有需要的決定屬性。

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >此序列將重複執行您想要傳回決定原則的次數。 例如，如果您選擇在下列情況下傳回2個專案： [建立決定](#add-decision)，相同的序列將重複兩次。

1. 按一下決定原則。 此時會顯示決定屬性。

   這些屬性儲存在 **[!UICONTROL 選件]** 目錄的結構描述。 自訂屬性會儲存在 **`_<imsOrg`>** 資料夾和中的標準屬性 **`_experience`** 資料夾。 [進一步瞭解優惠方案目錄的結構描述](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

1. 按一下每個資料夾以展開。 將滑鼠游標置於所需位置，然後按一下您要新增的屬性旁的+圖示。 您可以對程式碼新增任意數量的屬性。

   ![](assets/decision-code-based-add-decision-attributes.png)

1. 若要導覽回決策原則根目錄，請按一下資料夾圖示。

   ![](assets/decision-code-based-decision-folder.png)

1. 您也可以新增運算式編輯器中可用的任何其他屬性，例如設定檔屬性。

   ![](assets/decision-code-based-decision-profile-attribute.png)

## Customer Journey Analytics中的報告 {#cja}

如果您使用Customer Journey Analytics，您可以運用Experience Decisioning為您的程式碼型行銷活動建立自訂報告儀表板。

主要步驟列於下方。 有關如何使用Customer Journey Analytics的詳細資訊，請參閱 [Customer Journey Analytics檔案](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. 建立及設定 **連線** 在Customer Journey Analytics中。 這可讓您連線至您要製作報表的資料集。 [瞭解如何建立連線](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. 建立 **資料檢視** 並將它與先前建立的連線建立關聯。 在 **[!UICONTROL 元件]** 索引標籤中，選擇要顯示在報告中的相關結構描述欄位。 對於Experience Decisioning，請務必包含 **主張互動** 和 **propositiondisplay** 欄位。 [瞭解如何建立和設定資料檢視](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. 在中結合資料元件、表格和視覺效果 **工作區專案** 以建立和共用程式碼型行銷活動的報表。[瞭解如何建立工作區專案](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
