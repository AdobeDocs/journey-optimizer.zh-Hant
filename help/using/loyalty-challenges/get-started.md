---
solution: Journey Optimizer
product: journey optimizer
title: 開始應對忠誠度挑戰
description: 瞭解如何在Adobe Journey Optimizer中建立和管理忠誠度挑戰，以建立吸引人、獎勵的忠誠度計畫。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="私人測試版" type="Informative"
mini-toc-levels: 1
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
feature_v2: []
subfeature_v2: id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: c2322ea4081f43aadf8abc8ea9791ebcc91f78bd
workflow-type: tm+mt
source-wordcount: 900
ht-degree: 14%

---

# 開始應對忠誠度挑戰 {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**目錄**

**[開始解決忠誠度挑戰](get-started.md)** ◀︎ **您在這裡**

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**建立和管理挑戰**

* [存取及管理挑戰與工作](access-loyalty-challenges.md)
* [創造挑戰](create-challenges.md)
* [建立任務](create-tasks.md)
* [監視忠誠度挑戰績效](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**設定並整合**

* [設定忠誠度挑戰](loyalty-admin.md)
* [熟客資料與資料集](loyalty-data-and-datasets.md)
* [忠誠度挑戰API參考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](../rn/releases.md)。

## 概觀 {#overview}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_inventory"
>title="忠誠度挑戰"
>abstract="您可以透過忠誠度挑戰建立吸引人、遊戲化的忠誠度方案，推動客戶行為及深化品牌關係。 建置挑戰，獎勵客戶的特定動作，包括從購買和撰寫評論，到參與社交媒體和轉介朋友。"

您可以透過忠誠度挑戰建立吸引人、遊戲化的忠誠度方案，推動客戶行為及深化品牌關係。 建置挑戰，獎勵客戶的特定動作，包括從購買和撰寫評論，到參與社交媒體和轉介朋友。

透過忠誠度挑戰，您可以：

* **設計彈性的挑戰型別**：建立符合您業務目標的標準、連續或循序挑戰
* **策略性地設定獎勵**：在任務里程碑或完全完成時傳遞點數以維持參與
* **個人化體驗**：使用內容卡和多通道傳訊功能，建立沈浸式品牌體驗
* **緊密整合**：與您現有的忠誠度提供者連絡並運用Experience Platform資料
* **自動追蹤**：透過自動產生的歷程（無需自訂開發）監視客戶進度
* **測量效能**：使用內建的報告儀表板來追蹤方案KPI、挑戰結果和任務層級的量度

![](assets/challenges-gs.png)

您可以建立下列型別的挑戰體驗：

* **標準挑戰**：客戶以任何順序完成任何指定數量的工作。 當您想要彈性及多個完成路徑時，請使用此型別。\
  *範例：「夏季健康挑戰」 — 完成5項任務中的3項：購買健康產品、在社群媒體上分享、介紹朋友、撰寫評論或參加虛擬活動*

* **連續挑戰**：客戶連續多次完成相同的工作。 使用此型別鼓勵隨著時間推移一致的重複行為。\
  *範例：「咖啡愛好者週」 — 連續7天購買咖啡產品以取得免費飲品獎勵*

* **循序挑戰**：客戶以定義的順序完成任務。 使用此型別引導客戶完成特定歷程或上線流程。\
  *範例：「新成員歷程」 — 註冊電子郵件→進行第一次購買→撰寫產品評論→推薦朋友（以此確切順序完成）*

* **自備資料挑戰** （可用性受限）：挑戰框架（任務和獎勵）是由您的「忠誠度挑戰」資料整合所組成。 您可以像處理任何其他挑戰型別一樣設定「設定」、「內容」和「傳訊」。

## 運作方式 {#how-it-works}

建立和啟動忠誠度挑戰會遵循此工作流程：

1. **建立挑戰** — 選擇挑戰型別(標準、條紋、循序或自備資料（可用時）。 [瞭解如何選擇挑戰型別](create-challenges.md#create-the-challenge)。

1. **設定設定** — 在[設定]索引標籤中，定義挑戰詳細資料、對象、排程、規則（選擇加入、進度追蹤、重複限制）和選用的中繼資料。 [瞭解挑戰設定](create-challenges.md#settings)。

1. **新增任務和獎勵** — 在[結構]索引標籤中，定義任務和獎勵（自帶資料挑戰不需要）。

1. **設計內容卡** — 使用顯示在客戶裝置上的Journey Optimizer內容卡，以視覺化方式呈現您的挑戰。

1. **設定訊息** （選擇性） — 設定關鍵生命週期階段的多通道訊息（應用程式內、電子郵件、推播）：啟動、進行中及完成。

1. **啟動挑戰** — 發佈挑戰，然後產生歷程。 Journey Optimizer會自動建立挑戰歷程。 發佈自動產生的歷程，讓客戶瞭解挑戰。

如需詳細逐步指示，請參閱[建立挑戰](create-challenges.md)。

## 先決條件 {#prerequisites}

使用忠誠度挑戰之前，請確定您擁有：

+++必要權限

若要使用忠誠度挑戰，您需要在Journey Optimizer和Adobe Experience Platform中擁有適當許可權。

**Journey Optimizer：**

* `journeys.read`
* `journeys.write`
* `journeys.delete`
* `journeys.publish`
* `journeys_events.read`
* `journeys_events.write`
* `journeys_events.delete`
* `journeys_report.read`
* `messages.read`
* `messages_report.read`

**Adobe Experience Platform：**

* `segments.read`
* `profiles.read`
* `identity_namespace.read`

如果您無法存取功能或需要其他許可權，請聯絡管理員。

+++

+++設定熟客方案（管理員）

管理員可在&#x200B;**[!UICONTROL 忠誠度管理員]**&#x200B;功能表中設定獎勵提供者、事件定義、產品詳細目錄、排除專案和全域設定。 僅能帶來挑戰的行銷人員不需要存取此選單。 [瞭解如何設定忠誠度挑戰](loyalty-admin.md)

如果左側導覽中看不到&#x200B;**[!UICONTROL 忠誠度管理員]**&#x200B;功能表，請聯絡您的管理員。

+++

+++目標客群

在建立挑戰之前，請先確定Adobe Experience Platform中已有您需要的目標對象。 在挑戰設定期間，您將選取定義哪些客戶有資格參與的受眾。 [瞭解如何使用對象](../audience/about-audiences.md)。

+++

## 讓我們深入探討 {#lets-dive-deeper}

現在您已經知道什麼是忠誠度挑戰及其運作方式，您可以開始深入瞭解詳細資訊。 探索以下主題以存取介面、建立您的第一個挑戰，並定義您的客戶將完成的任務。

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
      <img alt="存取權" src="assets/do-not-localize/icon-access.png" width="200"/>
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>存取及管理挑戰與任務</strong></a>
    </div>
    <p>
    <em>瞭解如何存取詳細目錄及管理挑戰與工作</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <img alt="建立" src="assets/do-not-localize/icon-challenge.png" width="200"/>
    </a>
    <div>
    <a href="create-challenges.md"><strong>建立挑戰</strong></a>
    </div>
    <p>
    <em>瞭解如何建立及設定您的第一個忠誠度挑戰</em>
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
      <img alt="任務" src="assets/do-not-localize/icon-task.png" width="200"/>
    </a>
    <div>
    <a href="create-tasks.md"><strong>建立任務</strong></a>
    </div>
    <p>
    <em>瞭解如何定義客戶為挑戰完成的工作</em>
    </p>
  </td>
  <td>
    <a href="loyalty-reporting.md">
      <img alt="報表" src="assets/do-not-localize/icon-reporting.png" width="200"/>
    </a>
    <div>
    <a href="loyalty-reporting.md"><strong>監控效能</strong></a>
    </div>
    <p>
    <em>使用內建儀表板追蹤計畫KPI、挑戰結果和任務量度</em>
    </p>
  </td>
  <!--
    <a href="loyalty-admin.md"><strong>Configure the loyalty program</strong></a>
  <td>
    <a href="loyalty-admin.md">
    <em>Set up reward providers, event definitions, and org settings for fulfillment</em>
    </a>
    <div>
-->
    <a href="loyalty-admin.md"><strong>設定忠誠度挑戰</strong></a>
    </div>
    <p>
    <em>設定獎勵提供者、事件定義和組織設定</em>
    </p>
  </td>
</tr>
</table>

## API 參考 {#api-reference}

若要以程式設計方式管理忠誠度挑戰，請使用[忠誠度挑戰API](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}。 此API可讓您透過REST端點建立、更新和管理挑戰與工作。
