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
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 2%

---


# 開始應對忠誠度挑戰 {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**忠誠度挑戰檔案：**

* **開始解決忠誠度挑戰** ◀︎ **您在這裡** — 總覽、工作流程、必要條件
* [存取忠誠度挑戰](access-loyalty-challenges.md) — 詳細目錄和篩選
* [建立挑戰](create-challenges.md) — 建置並設定挑戰
* [管理挑戰](manage-challenges.md) — 編輯、監視、最佳化

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="關於忠誠度挑戰"
>abstract="忠誠度挑戰可讓您建立個人化的參與優惠，以激勵客戶完成特定動作並獲得獎勵。"

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中，可能無法在您的環境中使用。 請聯絡您的 Adobe 代表以取得存取權。

## 概觀 {#overview}

「忠誠度挑戰」提供完整解決方案，可大規模建立忠誠度計畫，從定義任務和里程碑，到跨管道提供內容和追蹤效能。 您可以建立三種型別的挑戰體驗、設定獎勵、在關鍵生命週期階段傳送多管道通知，並透過自動產生的歷程來監控效能，同時保持與外部忠誠度管理系統的整合。

## 主要功能 {#key-capabilities}

使用忠誠度挑戰來：

* **建立三種型別的挑戰**：
   * **Standard**：客戶以任何順序完成任何數量的工作以取得獎勵
   * **連續執行**：客戶連續多次完成相同的工作
   * **循序**：客戶以特定順序完成工作

* **設計挑戰內容**：使用Journey Optimizer內容卡在客戶裝置上建立您挑戰的視覺化呈現。 內容卡會顯示挑戰資訊、進度和獎勵。

* **設定任務需求**：定義客戶必須做什麼才能獲得獎勵，包括：
   * 任務型別（購買、支出金額、造訪、參與、自訂事件）
   * 數量需求
   * 使用SKU、類別或屬性的產品包含/排除
   * 自訂屬性和條件

* **設定獎勵**：定義客戶在完成任務時（漸進式獎勵）或完成整個挑戰後（最終獎勵）獲得的獎勵。

* **傳送多頻道通知**：在關鍵階段跨多個頻道（應用程式內、電子郵件、推播）傳遞訊息：
   * **啟動**：挑戰開始時
   * **進行中**：客戶在中途進出
   * **完成**：客戶完成挑戰時

* **追蹤效能**：監視自動產生的歷程，並透過內建報告檢閱挑戰效能。

## 運作方式 {#how-it-works}

建立和啟動忠誠度挑戰會遵循此工作流程：

1. **設定資料擷取** — 設定Experience Platform來源聯結器（如Chariceline）以擷取忠誠度事件資料，並追蹤客戶動作和進度。

2. **建立挑戰** — 定義基本挑戰屬性，包括名稱、型別（標準、連續或循序）、對象和日期範圍。

3. **新增任務** — 定義客戶必須完成的特定動作，包括任務型別（購買、支出、造訪等）、數量、產品篩選器和獎勵。

4. **設計內容卡** — 使用顯示在客戶裝置上的Journey Optimizer內容卡，以視覺化方式呈現您的挑戰。

5. **設定訊息** （選擇性） — 設定主要階段的多通道訊息（應用程式內、電子郵件、推播）：啟動、進行中及完成。

6. **檢閱並發佈** — 使用測試設定檔測試您的挑戰，然後發佈它以供您的目標對象使用。

7. **自動產生的歷程** — 當您發佈時，Journey Optimizer會自動建立協調內容卡傳遞和傳訊的歷程。

8. **啟用歷程** — 自動產生的歷程會在您的挑戰開始日期啟用，並管理所有客戶互動。

9. **監視效能** — 透過內建報告和歷程畫布，追蹤參與率、完成率、獎勵發佈和訊息參與。

>[!NOTE]
>
>自動產生的歷程會顯示在您的歷程詳細資料中，並可視需要自訂。 不過，直接對歷程進行的變更不會同步回挑戰設定。

## 先決條件 {#prerequisites}

使用忠誠度挑戰之前，請確定您擁有：

### 資料擷取設定 {#data-ingestion}

忠誠度挑戰需要透過Experience Platform來源聯結器擷取的資料來追蹤客戶進度和任務完成。

1. **設定支援的來源聯結器**：目前，毛細管聯結器一般可用。 已規劃其他聯結器。

2. **驗證資料擷取**：確保忠誠度事件和客戶資料流入Experience Platform並在Journey Optimizer中使用。

如需詳細指示，請參閱：

* [Experience Platform來原始檔](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [在Journey Optimizer中設定來源聯結器](../start/get-started-sources.md)

### 必要權限 {#required-permissions}

若要使用忠誠度挑戰，您需要Journey Optimizer中的適當許可權。 如果您無法存取此功能，請聯絡管理員。

### 目標客群 {#target-audiences}

先在Experience Platform中建立目標對象，然後再建立挑戰。 您可以選取現有對象，但無法從忠誠度挑戰UI建立新對象。

## 重要限制 {#limitations}

* **沒有分類帳系統**：忠誠度挑戰不會追蹤貨幣值或點數餘額。 當客戶完成挑戰並獲得獎勵時，Journey Optimizer會呼叫您的外部忠誠度管理系統以處理點數分配。

* **僅限對象選擇**：您可以選取現有對象，但無法從「忠誠度挑戰」UI建立新對象。

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
    <p>
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
    <p>
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
    <p>
  </td>
</tr>
</table>
