---
solution: Journey Optimizer
product: journey optimizer
title: 發佈歷程
description: 瞭解如何報告您的歷程量度
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 發佈，歷程，即時，有效性，檢查
exl-id: 95d0267e-fab4-4057-8ab5-6f7c9c866b0f
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/iHr0CFVSDz-4tOxNKyCyPZdwva3nfDyuU0Y5XHZEdjk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1153
ht-degree: 3%

---

# 設定並追蹤歷程量度 {#success-metrics}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何設定並指派歷程量度，以根據您的KPI追蹤效能，並即時衡量客戶歷程的成效。

>[!ENDSHADEBOX]

透過歷程量度清楚掌握客戶歷程的成效。 此功能可讓您根據定義的KPI追蹤效能、發掘有效方法的深入分析，以及識別最佳化區域。 透過即時衡量影響，您可以推動持續改善，並以資料為基礎做出提升客戶參與度的決策。

## 先決條件 {#prerequisites}

在使用歷程量度之前，您必須在[!DNL Adobe Experience Platform]中的設定>報告下新增包含`Commerce Details`、`Web`和`Mobile` [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant#field-group){target="_blank"}的資料集。

這些欄位群組必須從內建選項中選取，而不是從自訂群組中選取。 請參閱[新增資料集](../reports/reporting-configuration.md#add-datasets)區段。

## 可用量度 {#metrics}

量度清單會依資料集所包含的[欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant#field-group){target="_blank"}而有所不同。

如果您的資料集未設定，則只有下列量度可供使用： **[!UICONTROL 點按]**、**[!UICONTROL 不重複點按]**、**[!UICONTROL 點進率]**&#x200B;和&#x200B;**[!UICONTROL 開啟率]**。

請注意，使用Customer Journey Analytics授權可讓您建立自訂成功量度。 [了解更多](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/participation-metric)


| 量度 | 相關欄位群組 |
|-|-|
| 點按次數 | 不需要欄位群組 |
| 不重複點按 | 不需要欄位群組 |
| 點進率(CTR) | 不需要欄位群組 |
| 點進開啟率(CTOR) | 不需要欄位群組 |
| 頁面檢視 | 網站欄位群組 |
| 應用程式啟動次數 | 行動欄位群組 |
| 首次應用程式啟動次數 | 行動欄位群組 |
| 應用程式安裝 | 行動欄位群組 |
| 應用程式升級 | 行動欄位群組 |
| 購買 | Commerce詳細資料欄位群組 |
| 結帳 | Commerce詳細資料欄位群組 |
| 購物車新增次數 | Commerce詳細資料欄位群組 |
| 購物車開啟次數 | Commerce詳細資料欄位群組 |
| 購物車檢視 | Commerce詳細資料欄位群組 |
| 購物車移除次數 | Commerce詳細資料欄位群組 |
| 產品檢視 | Commerce詳細資料欄位群組 |
| 儲存供日後使用 | Commerce詳細資料欄位群組 |

## 歸因 {#attribution}

每個量度都隨附一組歸因，可判斷哪些接觸點或互動對特定結果有貢獻。

* **具有Journey Optimizer授權的量度歸因**：

  僅使用Journey Optimizer授權時，任何選定量度的可用回顧期間上限會設為7天。 對於這些量度，歸因模型預設會設為&#x200B;**上次接觸**，也就是轉換前的最近互動。

  例如，您可以追蹤客戶在過去7天內與您的歷程互動後是否進行了購買。

* **具有Customer Journey Analytics授權的量度歸因**：

  透過Journey Optimizer和Customer Journey Analytics授權，您可以建立具有特定歸因設定的自訂量度，或變更內建量度的歸因。

  深入瞭解[歸因模型](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/attribution#attribution-models)

## 指派您的歷程量度 {#assign}

>[!IMPORTANT]
>
>每個歷程只允許一個歷程量度。

若要開始追蹤您的歷程量度，請遵循下列步驟：

1. 從您的&#x200B;**[!UICONTROL 歷程]**&#x200B;功能表，按一下&#x200B;**[!UICONTROL 建立歷程]**。

1. 編輯歷程的設定窗格以定義歷程的名稱並設定其屬性。 瞭解如何在[此頁面](../building-journeys/journey-properties.md)上設定您的歷程屬性。

1. 選擇您的&#x200B;**[!UICONTROL 歷程量度]**，用於測量歷程的成效。

   請注意，量度適用於歷程本身，並適用於歷程的所有元素。

   歷程屬性中的![成功量度設定面板](assets/success_metric.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

1. 使用必要的&#x200B;**[!UICONTROL 活動]**&#x200B;設計您的歷程。

1. 測試並發佈您的歷程。

1. 開啟您的歷程報告，以追蹤您指派的成功量度的效能。

   您選擇的量度會顯示在報告的KPI和歷程統計資料表中。

   ![成功量度下拉式清單，顯示目標追蹤的可用事件](assets/success_metric_2.png)

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;本頁說明如何將KPI指派給歷程並在歷程報告中檢閱其效能，以設定和追蹤Adobe Journey Optimizer中的歷程成功量度。

**意圖：**
* 新增必要的AEP資料集欄位群組（Commerce詳細資訊、Web、行動）作為歷程量度的先決條件
* 在歷程建立或設定期間指派歷程量度(KPI)到歷程
* 根據設定的資料集欄位群組瞭解哪些量度可供使用
* 解譯Journey Optimizer和Customer Journey Analytics授權底下歷程量度的歸因模型
* 使用Customer Journey Analytics授權建立自訂成功量度
* 根據在歷程報告中指派的KPI追蹤歷程績效

**字彙表：**
* **歷程量度**：指派給歷程以測量其成效的KPI，會顯示在歷程報告&#x200B;*（產品專屬）*&#x200B;中
* **上次接觸歸因**：將轉換前最近的互動歸因的預設歸因模型
* **Commerce詳細資料欄位群組**： XDM欄位群組會啟用與商業相關的量度，例如購買、結帳和購物車事件
* **回顧期間**：評估歸因的時間範圍；僅使用Journey Optimizer授權時，最多可設定7天

**護欄：**
* 每個歷程只允許一個歷程量度
* 資料集欄位群組（Commerce詳細資訊、Web、行動）必須從內建選項中選取，而非自訂群組，並新增至Adobe Experience Platform的「設定>報表」下
* 若沒有已設定的資料集，則只能使用點按數、不重複點按數、點進率和開啟率
* 僅限Journey Optimizer授權的最大回顧期間為7天
* 自訂量度和自訂歸因設定需要Customer Journey Analytics授權

**術語：**
* 正式名稱：歷程量度 — 縮寫：none — 變體：成功量度、歷程成功量度
* 正式名稱：點進率 — 縮寫：CTR — 變體：無
* 正式名稱：點進開啟率 — 縮寫：CTOR — 變體：無
* 同義字：&quot;journey metrics&quot; = &quot;success metrics&quot; （在UI和檔案中可互換使用）
* 請勿混淆：「Journey Optimizer授權歸因」≠「Customer Journey Analytics歸因」 — CJA授權可啟用自訂歸因模型和較長的回顧期間

**常見問題集：**
* **問：我可以指派多少歷程量度給單一歷程？**  — 每個歷程只允許一個歷程量度。
* **問：如果尚未設定包含欄位群組的資料集，有哪些量度可供使用？**  — 只有點按數、不重複點按數、點進率和開啟率可供使用，不需要額外的欄位群組設定。
* **問：我需要哪些欄位群組才能啟用購買和商務量度？**  — 您需要將Commerce詳細資料欄位群組新增到Adobe Experience Platform中的報表資料集。
* **問：歷程量度的預設歸因模型為何？**  — 上次接觸，將轉換前的最新互動歸功，Journey Optimizer授權下最多7天的回顧期間。
* **問：我可以建立自訂成功量度嗎？**  — 可以，但只能使用Customer Journey Analytics授權。
* **問：發佈後，我可以在哪裡檢視歷程量度結果？**  — 在歷程報告的KPI和歷程統計資料表中。

+++
