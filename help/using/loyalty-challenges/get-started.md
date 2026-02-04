---
solution: Journey Optimizer
product: journey optimizer
title: 開始應對忠誠度挑戰
description: 瞭解如何在Adobe Journey Optimizer中建立和管理忠誠度挑戰，以建立吸引人的忠誠度計畫。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人測試版" type="Informative"
source-git-commit: bd98e4dc77a0adde83df6251af749aa6da8c058d
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---


# 開始應對忠誠度挑戰 {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**忠誠度挑戰檔案：**

* **開始解決忠誠度挑戰** ◀︎ **您在這裡** — 總覽、工作流程、必要條件
* [存取忠誠度挑戰](access-loyalty-challenges.md) — 詳細目錄和篩選
* [建立挑戰](create-challenges.md) — 建置並設定挑戰
* [建立任務](create-tasks.md) — 定義挑戰任務
* [管理挑戰](manage-challenges.md) — 編輯、監視、最佳化

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中，可能無法在您的環境中使用。 若要要求存取權，請聯絡您的Adobe代表。 深入瞭解[可用性標籤](../rn/releases.md#availability-labels)。

## 概觀 {#overview}

忠誠度挑戰提供完整解決方案，可大規模建立忠誠度計畫，從定義任務和里程碑，到跨管道提供內容和追蹤效能。

您可以建立三種型別的挑戰體驗：

* **標準挑戰**：客戶以任何順序完成任何指定數量的工作
* **連續挑戰**：客戶連續多次完成相同工作
* **循序挑戰**：客戶以定義的順序完成任務

透過忠誠度挑戰，您可以設定獎勵、在關鍵生命週期階段傳送多管道通知，並透過自動產生的歷程監控效能，同時保持與外部忠誠度管理系統的整合。

<!-- SCREENSHOT: High-level diagram showing Loyalty Challenges architecture with: Data ingestion from source connectors -> Challenge creation in JO -> Content cards & messaging -> Customer device -> Journey tracking -->

## 運作方式 {#how-it-works}

<!-- SCHEMA: Visual workflow diagram showing the 8 steps in the loyalty challenge creation process with icons for each step -->

建立和啟動忠誠度挑戰會遵循此工作流程：

1. **設定資料擷取** — 設定Experience Platform來源聯結器（例如Chariceline聯結器），以擷取追蹤客戶動作和進度的忠誠度事件資料。 此資料可支援挑戰追蹤和任務完成。

1. **建立挑戰** — 定義基本挑戰屬性，包括名稱、型別（標準、連續或循序）、對象和日期範圍。 如需詳細步驟，請參閱[建立挑戰](create-challenges.md)。

1. **新增任務** — 定義客戶必須完成的特定動作，包括任務型別（購買、支出、造訪、參與、自訂事件）、數量、產品篩選器和獎勵。 如需詳細指示，請參閱[建立工作](create-tasks.md)。

1. **設計內容卡** — 使用顯示在客戶裝置上的Journey Optimizer [內容卡](../content-card/create-content-card.md)，建立您挑戰的視覺化呈現。 內容卡會顯示挑戰資訊、進度和獎勵。

1. **設定訊息** （選擇性） — 設定關鍵生命週期階段的多通道訊息（[應用程式內](../in-app/get-started-in-app.md)、[電子郵件](../email/get-started-email.md)、[推播](../push/get-started-push.md)）：啟動、進行中及完成。

1. **檢閱並發佈** — 使用[測試設定檔](../test-approve/test-profiles.md)測試您的挑戰，然後發佈它以供您的目標對象使用。

1. **啟動歷程** — 當您發佈挑戰時，Journey Optimizer會自動建立[歷程](../building-journeys/journey-gs.md) （草稿）狀態，以協調內容卡傳遞和傳訊。 導覽至歷程詳細目錄，找到自動產生的歷程（名為「挑戰： [挑戰名稱]」），並[啟用它](../building-journeys/publishing-the-journey.md)，讓您的客戶可以使用挑戰。

1. **監視效能** — 透過內建報告和歷程畫布，追蹤參與率、完成率、獎勵發佈和訊息參與。 如需監控詳細資訊，請參閱[管理挑戰](manage-challenges.md)。

## 先決條件 {#prerequisites}

使用忠誠度挑戰之前，請確定您擁有：

+++資料擷取設定

忠誠度挑戰需要透過Experience Platform來源聯結器擷取的資料來追蹤客戶進度和任務完成。

1. **設定支援的來源聯結器**：目前，毛細管聯結器一般可用。 未來版本計畫推出其他聯結器。

1. **驗證資料擷取**：確保忠誠度事件和客戶資料流入Experience Platform並在Journey Optimizer中使用。 確認資料結構包含追蹤客戶動作和進度的必要欄位。

如需詳細指示，請參閱：

* [Experience Platform來原始檔](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [在Journey Optimizer中設定來源聯結器](../start/get-started-sources.md)

+++

+++必要權限

若要使用忠誠度挑戰，您需要Journey Optimizer中的適當許可權。 必要的許可權包括：

* 存取&#x200B;**[!UICONTROL 忠誠度挑戰]**&#x200B;功能
* 建立和管理歷程的許可權
* 建立和管理內容卡的許可權
* 建立和管理對象的許可權

如果您無法存取功能或需要其他許可權，請聯絡管理員。

+++

+++目標客群

先在Experience Platform中建立目標對象，然後再建立挑戰。 這些受眾會定義哪些客戶符合參與您的忠誠度挑戰的資格。 有關如何建立對象的詳細資訊，請參閱[開始使用對象](../audience/about-audiences.md)。

+++

## 後續步驟 {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>存取忠誠度挑戰</strong></a>
    </div>
    <p>
    <em>瞭解如何存取詳細目錄並篩選挑戰</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <!--<img alt="Create" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-challenges.md"><strong>建立挑戰</strong></a>
    </div>
    <p>
    <em>建置並設定您的第一個忠誠度挑戰</em>
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
    <!--<img alt="Tasks" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-tasks.md"><strong>建立任務</strong></a>
    </div>
    <p>
    <em>定義挑戰的行動和獎勵</em>
    </p>
  </td>
  <td>
    <a href="manage-challenges.md">
    <!--<img alt="Manage" src="../assets/do-not-localize/monitor-button.svg">-->
    </a>
    <div>
    <a href="manage-challenges.md"><strong>管理挑戰</strong></a>
    </div>
    <p>
    <em>編輯、監視和最佳化挑戰</em>
    </p>
  </td>
</tr>
</table>
