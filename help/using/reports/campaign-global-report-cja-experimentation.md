---
solution: Journey Optimizer
product: journey optimizer
title: 行銷活動報告
description: 瞭解如何使用Campaign報告中的實驗資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 69742163-7378-49ab-929e-86213d6e65e3
TQID: https://experienceleague.adobe.com/m11Vxa3bSvaOHe1kFs5tU9oQS08lzcL0DSPyrABbXBI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 339
ht-degree: 9%

---

# 實驗行銷活動報告 {#campaign-global-report-cja-experimentation}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="成功量度"
>abstract="先前在建立實驗時選取的成功量度的總值除以設定檔的數量。"

## 實驗 {#experimentation}

**[!UICONTROL Experimentation]**&#x200B;索引標籤提供每個變體效能的重要深入分析，並識別最成功的變體。

請注意，定義績效最佳者可能需要一些時間。 如果您的實驗不成功，它將會設定為&#x200B;**尚無結果**。

![](assets/cja-experimentation-1.png)

### 實驗KPI {#experimentation-kpis}

![](assets/cja-experimentation-kpis.png)

**[!UICONTROL Experimentation]**&#x200B;關鍵績效指標(KPI)可作為全方位儀表板，提供與您的實驗相關之基本量度的分析。

+++ 進一步瞭解實驗KPI量度

* **[!UICONTROL 提升度]**：測量指定處理的轉換率相對於基準的提升百分比。

* **[!UICONTROL 信賴度]**：指定處理與基準處理相同的證據。 [了解更多](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

+++

### 依成功量度的變體 {#variant-inbound}

![](assets/cja-experimentation-variants.png)

成功量度的&#x200B;**變體**&#x200B;表格會根據設定實驗時選取的成功量度，顯示每個變體的執行方式。
如需深入瞭解這些結果以及如何解譯，請參閱[此頁面](../content-management/get-started-experiment.md#interpret-results)。

+++ 進一步瞭解「依成功量度區分的變體」

* **[!UICONTROL 人員]**：符合訊息目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 傳入點按次數]**：建立實驗時，先前選取的成功量度總值。

* **[!UICONTROL 轉換率]**：建立實驗時先前選取的成功量度總值除以設定檔數目。

* **[!UICONTROL 提升度]**：測量指定處理的轉換率相對於基準的提升百分比。

* **[!UICONTROL 信賴下限]**：在選擇的信賴區間內，處理與基準之間轉換率差異的最低預估值。

* **[!UICONTROL 信賴度]**：指定處理與基準處理相同的證據。 [了解更多](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

* **[!UICONTROL 信賴上限]**：在選擇的信賴區間內，處理與基準之間轉換率差異的最大估計值。

+++

### 成功量度的轉換率 {#conversion-rate}

![](assets/cja-experimentation-conversion.png)


**[!UICONTROL 信賴區間]**&#x200B;圖表會顯示可能的改善範圍，比較基準與所選成功量度的最佳績效處理方式。 [了解更多](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)。