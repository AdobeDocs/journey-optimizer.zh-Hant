---
title: Experience decisioning使用案例
description: 瞭解如何使用程式碼型管道的實驗建立決策
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 10%

---

# Experience decisioning使用案例 {#experience-decisioning-uc}

>[!BEGINSHADEBOX 「本檔案指南提供哪些內容」]

* [開始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的決定專案： [設定專案目錄](catalogs.md) -[建立決定專案](items.md) - [管理專案集合](collections.md)
* 設定專案的選取範圍： [建立決定規則](rules.md) - [建立排名方法](ranking.md)
* [建立選擇策略](selection-strategies.md)
* [建立決定原則](create-decision.md)

>[!ENDSHADEBOX]

在此使用案例中，您會定義兩個傳遞處理，每個處理包含不同的決定原則，以評估哪個處理對目標對象執行時效果最佳。

## 建立專案和策略

您首先需要建立專案、在集合中將它們分組、設定規則和排名方法。 這些元素可讓您建置選取策略。

1. 瀏覽至 **[!UICONTROL 體驗決策]** > **[!UICONTROL 專案]** 並建立多個選件專案。 使用對象或規則設定限制，將每個專案限製為僅限特定設定檔。 [了解更多](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. 建立 **集合** 根據您的偏好設定將您的決定專案分類及分組。 [了解更多](collections.md)

1. 建立 **決定規則** 以決定可向誰顯示決定專案。 [了解更多](rules.md)

1. 建立 **排名方法** 並將它們套用至決定策略中，以決定選取決定專案的優先順序。 [了解更多](ranking.md)

1. 建置 **選取策略** 運用集合、決定規則和排名方法來識別適合顯示給設定檔的決定專案。 [了解更多](selection-strategies.md)

## 建立決定原則

若要在您的網站或行動應用程式上向訪客呈現最佳動態優惠和體驗，請將決定原則新增至程式碼型行銷活動。

定義兩個傳遞處理，每個處理包含不同的決定原則。

1. 建立行銷活動並選取 **[!UICONTROL 程式碼型體驗(Beta)]** 動作。 [了解更多](../code-based/create-code-based.md)

   >[!NOTE]
   >
   >程式碼型體驗功能目前僅供特定使用者測試版。 若要加入 Beta 版計畫，請連絡 Adobe 客戶服務。

1. 從行銷活動摘要頁面，按一下 **[!UICONTROL 建立實驗]** 以開始設定您的內容實驗。 [了解更多](../campaigns/content-experiment.md)

1. 選取 **[!UICONTROL 決定]** 圖示，按一下 **[!UICONTROL 建立決定]** 並填寫決定詳細資訊。 [了解更多](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. 為您的決定定義選取策略。 按一下 **[!UICONTROL 新增策略]**.

1. 按一下 **[!UICONTROL 建立]**。新決定新增到 **[!UICONTROL 決定]**.

   ![](assets/decision-code-based-decision-added.png)

1. 按一下更多動作圖示（三個點）並選取 **[!UICONTROL 新增]**. 現在，您可以在此新增所有需要的決定屬性。

   ![](assets/decision-code-based-add-decision.png)

1. 您也可以新增運算式編輯器中可用的任何其他屬性，例如設定檔屬性。

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. 建立處理B並重複上述步驟以建立另一個決策。

1. 儲存您的內容。


