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
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 1%

---


# 開始應對忠誠度挑戰 {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**忠誠度挑戰檔案：**

* **開始解決忠誠度挑戰** ◀︎ **您在這裡** — 總覽、工作流程、必要條件
* [存取及管理忠誠度挑戰](access-loyalty-challenges.md) — 詳細目錄、挑戰及工作管理
* [建立挑戰](create-challenges.md) — 建置並設定挑戰
* [建立任務](create-tasks.md) — 定義挑戰任務

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

## 運作方式 {#how-it-works}

建立和啟動忠誠度挑戰會遵循此工作流程：

1. **設定資料擷取** — 設定Experience Platform來源聯結器（例如Chariceline聯結器），以擷取追蹤客戶動作和進度的忠誠度事件資料。 此資料可支援挑戰追蹤和任務完成。

1. **選取目標對象** — 從Adobe Experience Platform選取對象，以定義哪些客戶可以參與您的挑戰。

1. **建立挑戰** — 定義基本挑戰屬性，包括名稱、型別（標準、條紋或循序）和日期範圍。

1. **新增任務** — 定義客戶必須完成的特定動作，包括任務型別（購買、支出、造訪、參與、自訂事件）、數量、產品篩選器和獎勵。

1. **設計內容卡** — 使用顯示在客戶裝置上的Journey Optimizer內容卡，以視覺化方式呈現您的挑戰。 內容卡會顯示挑戰資訊、進度和獎勵。

1. **設定訊息** （選擇性） — 設定關鍵生命週期階段的多通道訊息（應用程式內、電子郵件、推播）：啟動、進行中及完成。

1. **發佈歷程** - Journey Optimizer會自動為您挑戰產生歷程。 導覽至歷程詳細目錄並發佈自動產生的歷程，讓客戶可提出挑戰。

如需詳細逐步指示，請參閱[建立挑戰](create-challenges.md)。

## 先決條件 {#prerequisites}

使用忠誠度挑戰之前，請確定您擁有：

+++資料擷取設定

忠誠度挑戰需要透過Experience Platform來源聯結器擷取的資料來追蹤客戶進度和任務完成。

1. **設定支援的來源聯結器**：目前，毛細管聯結器一般可用。 未來版本計畫推出其他聯結器。

1. **驗證資料擷取**：確保忠誠度事件和客戶資料流入Experience Platform並在Journey Optimizer中使用。 確認資料結構包含追蹤客戶動作和進度的必要欄位。

如需詳細指示，請參閱：

* [Experience Platform來原始檔](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/sources/home)
* [在Journey Optimizer中設定來源聯結器](../start/get-started-sources.md)

+++

+++必要權限

若要使用忠誠度挑戰，您需要Journey Optimizer中的適當許可權。 必要的許可權包括：

* 存取&#x200B;**[!UICONTROL 忠誠度挑戰(Beta)]**&#x200B;功能
* 建立和管理歷程的許可權
* 建立和管理內容卡的許可權
* 建立和管理對象的許可權

如果您無法存取功能或需要其他許可權，請聯絡管理員。

+++

+++目標客群

定義目標對象，指定哪些客戶有資格參與您的忠誠度挑戰。 您可以選取現有對象，或直接從挑戰建立介面建立新對象。 [瞭解如何使用對象](../audience/about-audiences.md)。

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
