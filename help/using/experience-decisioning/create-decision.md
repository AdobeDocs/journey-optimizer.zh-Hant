---
title: 建立決定原則
description: 瞭解如何建立決定原則
feature: Experience Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="有限可用性"
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '1481'
ht-degree: 18%

---

# 建立決定原則 {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="什麼是決定？"
>abstract="決定原則包含決策引擎選擇最佳內容的所有選擇邏輯。決定原則是針對行銷活動的。其目標是為每個設定檔選擇最佳優惠，而行銷活動製作允許您指明如何呈現所選決定項目，包括要在訊息中包含哪些項目屬性。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="關於體驗決策"

決策原則是優惠方案的容器，可運用體驗決策引擎，根據對象挑選最佳內容進行傳遞。

決定原則包含決策引擎選擇最佳內容的所有選擇邏輯。決定原則是針對行銷活動的。其目標是為每個設定檔選擇最佳優惠，而行銷活動製作允許您指明如何呈現所選決定項目，包括要在訊息中包含哪些項目屬性。

>[!NOTE]
>
>在[!DNL Journey Optimizer]使用者介面中，決定原則會標示為決定<!--but they are decision policies. TBC if this note is needed-->。

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
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="建立策略"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="評估順序"

若要在您的網站或行動應用程式上向訪客呈現最佳動態優惠和體驗，請將決定原則新增至程式碼型行銷活動。 若要執行此操作，請遵循下列步驟。

1. 建立行銷活動並選取&#x200B;**[!UICONTROL 程式碼型體驗]**&#x200B;動作。 [了解更多](../code-based/create-code-based.md)

1. 從[程式碼編輯器](../code-based/create-code-based.md#edit-code)，選取&#x200B;**[!UICONTROL 決定原則]**&#x200B;圖示，然後按一下&#x200B;**[!UICONTROL 新增決定原則]**。

   ![](assets/decision-code-based-create.png)

1. 填寫決策原則的詳細資訊：新增名稱並選取目錄。

   >[!NOTE]
   >
   >目前僅提供預設的&#x200B;**[!UICONTROL 選件]**&#x200B;目錄。

   ![](assets/decision-code-based-details.png)

1. 選取要傳回的專案數。 例如，如果您選取2，則會針對目前曲面顯示最佳的2個合格選件。 按一下&#x200B;**[!UICONTROL 下一步]**

1. 使用&#x200B;**[!UICONTROL 新增策略]**&#x200B;按鈕，為您的決定原則定義選擇策略。 每個策略都包含與適用性限制相關聯的優惠方案集合，以及決定要顯示的優惠方案的排名方法。 [了解更多](selection-strategies.md)

   ![](assets/decision-code-based-strategies.png)

   >[!NOTE]
   >
   >至少需要一個策略。您無法新增超過10個策略。

1. 從&#x200B;**[!UICONTROL 新增策略]**&#x200B;畫面，您也可以建立策略。 **[!UICONTROL 建立選擇策略]**&#x200B;按鈕會將您重新導向至&#x200B;**[!UICONTROL 體驗決策]** > **[!UICONTROL 策略設定]**&#x200B;功能表。 [了解更多](selection-strategies.md)

   ![](assets/decision-code-based-add-strategy.png)

1. 新增數個策略時，會以特定順序評估策略。 系統會先評估新增至序列的第一個策略，依此類推。 [了解更多](#evaluation-order)

   若要變更預設順序，您可以拖放策略及/或群組以視需要重新排序。

   ![](assets/decision-code-based-strategy-groups.png)

1. 新增遞補。 如果上述選取策略均不合格，則會向使用者顯示後援專案。

   ![](assets/decision-code-based-strategy-fallback.png)

   您可以從清單中選取任何專案，這會顯示在目前沙箱上建立的所有決定專案。 如果沒有合格的選取策略，則無論套用至所選專案<!--nor frequency capping when available - TO CLARIFY-->的日期和適用性限制，都會對使用者顯示遞補。

   >[!NOTE]
   >
   >遞補內容為選用。 如果未選取遞補策略，且沒有符合資格的策略，[!DNL Journey Optimizer]將不會顯示任何內容。

1. 儲存您的選取專案，然後按一下[建立]。**** 現在決定原則已建立，您可以在程式碼型體驗內容中使用決定屬性。 [了解更多](#use-decision-policy)

   ![](assets/decision-code-based-decision-added.png)

## 評估順序 {#evaluation-order}

如上所述，策略包含集合、排名方法和資格限制。

您可以：

* 設定您要評估策略的循序順序，
* 結合多個策略，以便一起評估而不是分別評估。

多個策略及其分組決定策略的優先順序以及合格優惠的排名。 第一個策略具有最高優先順序，且在相同群組內合併的策略具有相同優先順序。

例如，您有兩個集合，一個在策略A中，另一個在策略B中。此請求是為了傳回兩個決定專案。 假設有兩個來自策略A的合格優惠方案和三個來自策略B的合格優惠方案。

* 如果兩個策略&#x200B;**未合併**&#x200B;或依序順序（1和2），則第一列中會傳回第一個策略中前兩個符合資格的優惠。 如果第一個策略沒有兩個符合資格的優惠，決定引擎會依序移至下一個策略，以找出仍需要多少優惠方案，最終在需要時傳回遞補。

  ![](assets/decision-code-based-consecutive-strategies.png)

* 如果兩個集合約時進行&#x200B;**評估**，因為有來自策略A的兩個合格優惠和來自策略B的三個合格優惠，這五個優惠都將根據各自排名方法決定的值棧疊在一起。 已要求兩個優惠方案，因此將傳回這五個優惠方案中的前兩個合格優惠方案。

  ![](assets/decision-code-based-combined-strategies.png)

+++ 具有多個策略的&#x200B;**範例**

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

選件1 - 10
選件2 - 20
策略1的優惠3 - 30，策略2的優惠45。 兩者中的最高會納入考量，因此會考慮45。
選件4 - 40
選件5 - 50

排名優惠方案現在如下：優惠方案5、優惠方案3、優惠方案4、優惠方案2、優惠方案1。

**反複專案2：**

已評估策略3選件（選件5、選件6）。 假設結果為：

* 選件5 — 將不進行評估，因為它已存在於上述結果中。
* 選件6 - 60

排名優惠方案現在如下：優惠方案5 、優惠方案3、優惠方案4、優惠方案2、優惠方案1、優惠方案6。

+++

## 在程式碼編輯器中使用決定原則 {#use-decision-policy}

建立後，決定原則便可用於[個人化編輯器](../code-based/create-code-based.md#edit-code)。 若要執行此操作，請遵循下列步驟。

>[!NOTE]
>
>程式碼型體驗運用[!DNL Journey Optimizer]個人化編輯器及其所有個人化和編寫功能。 [了解更多](../personalization/personalization-build-expressions.md)

1. 按一下&#x200B;**[!UICONTROL 插入原則]**&#x200B;按鈕。 已新增與決定原則對應的程式碼。

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >此序列將重複執行您想要傳回決定原則的次數。 例如，如果您選擇在[建立決定](#add-decision)時傳回2個專案，則相同的順序將重複兩次。

1. 現在，您可以在該程式碼中新增所有需要的決定屬性。 可用的屬性儲存在&#x200B;**[!UICONTROL 選件]**&#x200B;目錄的結構描述中。 自訂屬性儲存在&#x200B;**`_<imsOrg`>**&#x200B;資料夾中，而標準屬性儲存在&#x200B;**`_experience`**&#x200B;資料夾中。 [進一步瞭解優惠方案目錄的結構描述](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

   >[!NOTE]
   >
   >針對決定原則專案追蹤，決策原則內容需要新增`trackingToken`屬性，如下所示：
   >`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

1. 按一下每個資料夾以展開。 將滑鼠游標置於所需位置，然後按一下您要新增的屬性旁的+圖示。 您可以對程式碼新增任意數量的屬性。

   ![](assets/decision-code-based-add-decision-attributes.png)

1. 您也可以新增個人化編輯器中可用的任何其他屬性，例如設定檔屬性。

   ![](assets/decision-code-based-decision-profile-attribute.png)

## 客戶歷程分析報告 {#cja}

如果您使用Customer Journey Analytics，您可以運用Experience Decisioning為您的程式碼型行銷活動建立自訂報告儀表板。

主要步驟列於下方。 有關如何使用Customer Journey Analytics的詳細資訊，請參閱[Customer Journey Analytics檔案](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"}。

1. 在Customer Journey Analytics中建立並設定&#x200B;**連線**。 這可讓您連線至您要製作報表的資料集。 [瞭解如何建立連線](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. 建立&#x200B;**資料檢視**，並將其與先前建立的連線建立關聯。 在&#x200B;**[!UICONTROL 元件]**&#x200B;索引標籤中，選擇您要顯示在報告中的相關結構描述欄位。 對於Experience Decisioning，請確定您包含&#x200B;**propositioninteract**&#x200B;和&#x200B;**propositiondisplay**&#x200B;欄位。 [瞭解如何建立和設定資料檢視](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. 在&#x200B;**工作區專案**&#x200B;中結合資料元件、表格和視覺效果，以建立和共用程式碼型行銷活動的報告。[瞭解如何建立工作區專案](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
