---
solution: Journey Optimizer
product: Journey Optimizer
title: AI模型監視
description: 監視個人化最佳化模型的AI排名模型健康情況、訓練狀態和效能
feature: Ranking, Decisioning
topic: Artificial Intelligence
role: User
level: Intermediate
version: Journey Orchestration
exl-id: 90e71c42-94f3-4cc5-bd6e-1df29def4d39
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 2%

---

# 監視您的AI模型 {#ai-model-observability}

無論您是行銷人員、資料科學家或決策管理員，瞭解您的個人化最佳化模型的表現和行為方式可協助您使用AI為每位客戶選取最佳優惠方案。

若要這麼做，您可以直接在[!DNL Journey Optimizer]中監視AI模型的健康狀態、訓練狀態和演變。

這可讓您清楚瞭解模型是否運作、上次訓練時間、訓練期間發生的情況、如何推動業務成果（例如轉換或收入），以及運作不正常時的疑難排解<!-- (for example, unexpected decision item count, training data date range, or insufficient events)-->。

>[!AVAILABILITY]
>
>目前此功能僅支援[個人化最佳化](personalized-optimization-model.md)模型。

➡️ [在影片中探索此功能](#video)

## 檢視訓練狀態 {#from-ai-model-list}

一旦模型設定為有效，它就會進入持續的生命週期：收集資料並定期重新訓練模型，以最佳化優惠排名。 您可以在AI模型清單中檢視個人化最佳化模型的訓練狀態。

1. 移至&#x200B;**[!UICONTROL 決策]** > **[!UICONTROL 策略設定]** > **[!UICONTROL AI模型]**&#x200B;以開啟AI模型詳細目錄。

1. 您可以檢視所有可用的AI模型及其狀態。

1. 對於個人化最佳化型別的每個&#x200B;**[!UICONTROL 即時]** AI模型，有兩個欄可讓您看到：
   * 上次訓練工作執行時間（**[!UICONTROL 上次訓練時間]**），以及
   * 每個模型是否已成功訓練（**[!UICONTROL 訓練結果]**）。

   ![](../assets/ai-model-list-training.png)

   這可讓您快速找出需要進一步調查或疑難排解的模型。

## 存取模型狀態報表 {#access-ai-model-details}

從清單按一下進入個人化最佳化AI模型。 您可以在該處檢視下列元素：

* **[!UICONTROL 目前部署的模型]** — 此區段顯示目前部署的模型、部署時間、使用的資料日期範圍、包含和個人化的決定專案（優惠）數目，以及子模型間的目前流量分配<!-- (random exploration, new offer booster?, contextual bandit, neural network)-->。

  ![](../assets/ai-model-deployed-model.png)

  在此範例中，模型已接受五個決定專案的訓練，且模型有足夠的流量為三個決定專案開發個人化預測。 其餘兩個決定專案會隨機提供。

  您還可以看到模型目前將40%的流量分配給個人化神經網路、40%的流量分配給情境賭博機，以及20%的流量分配給隨機探索。

* **[!UICONTROL 上次訓練工作]** — 此區段顯示上次訓練工作的狀態、執行時間以及任何錯誤訊息。 [進一步瞭解錯誤狀態](#check-for-error-states)

  ![](../assets/ai-model-last-training-job.png)

  在此範例中，您可以觀察到，部署的模型如預期般符合培訓工作。

* **[!UICONTROL 屬性]** — 此區段顯示模型的屬性，例如使用的資料集、最佳化量度，以及用來訓練個人化最佳化模型的對象。

  ![](../assets/ai-model-properties.png)

  按一下&#x200B;**[!UICONTROL 編輯屬性]**&#x200B;以修改這些元素。 系統會將您重新導向至「建立AI模型」畫面。 [了解更多](create-ai-models.md)

* **[!DNL Model performance]** — 此段落顯示模型各元件在一段時間內的效能，例如每個子模型的流量分配和轉換率。 您可以在&#x200B;**最近7天**&#x200B;與&#x200B;**最近30天**&#x200B;之間切換。 提升度和統計顯著性是模型是否實際改善行銷結果的關鍵指標。

  ![](../assets/ai-model-performance.png)

  在此範例中，您可以看到在過去30天內，個人化子模型的轉換率提升超過60%，而且此提升在統計上是顯著的，表示此AI模型正對您的業務造成影響。

* **[!UICONTROL 隨時間變化的模型流量分配]** — 本節說明模型如何隨時間演化。 首次部署模型時，100%的流量是隨機的，因為尚未收集任何選件資料。 在第一次重新訓練後，流量通常會轉向個人化手臂。

  ![](../assets/ai-model-trafic-allocation.png)

  在此範例中，您可以看到流量分配已從100%隨機探索移至神經網路和關聯式吃角子老虎機流量，因為模型會隨著時間重新訓練。

## 瞭解訓練錯誤 {#check-for-error-states}

若要檢視個人化最佳化AI模型（其上次訓練工作失敗）的錯誤詳細資料，請遵循下列步驟。

1. 從清單中按一下進入模型。 模型狀態詳細資訊隨即顯示。

   ![](../assets/ai-model-no-model-deployed.png){width="95%"}

   在此範例中，您可以看到由於上次訓練工作失敗，因此未部署任何模型。

   >[!NOTE]
   >
   >未部署任何模型時，決策請求會使用統一的隨機流量分配來提供。

1. 瀏覽&#x200B;**[!UICONTROL 上次訓練工作]**&#x200B;區段中的錯誤詳細資料。

   ![](../assets/ai-model-training-job-failed.png){width="70%"}

   當您為此模型選取的資料集內沒有意見回饋事件時，訓練工作通常會失敗。 這表示您需要填入資料集，或選取包含適當轉換事件的新資料集。

1. 您可以檢查在模型的&#x200B;**[!UICONTROL 屬性]**&#x200B;中選取的資料集。 按一下&#x200B;**[!UICONTROL 編輯屬性]**&#x200B;以選取其他資料集。 [了解更多](create-ai-models.md)

   ![](../assets/ai-model-properties-edit-dataset.png){align="left" width="45%"}

## 常見問題 {#faq}

+++ 我可以監視哪些AI模型？

目前僅支援[個人化最佳化](personalized-optimization-model.md)模型的AI模型監視。 其他排名模型型別尚未公開模型狀態報表。
+++

+++ 為什麼我的模型訓練工作失敗？

為模型選取的資料集沒有或只有很少的反饋（轉換）事件時，訓練工作通常會失敗。 檢查&#x200B;**[!UICONTROL 上次訓練工作]**&#x200B;區段以取得錯誤詳細資料，然後檢閱模型的&#x200B;**[!UICONTROL 屬性]**&#x200B;以確認資料集和最佳化量度。 將正確的事件填入資料集，或[選取包含適當轉換資料的其他資料集](create-ai-models.md)。
+++

+++ AI模型監視與行銷活動和歷程報告有何關係？

AI模型監視不同於行銷活動或歷程報告。 單一AI模型可用於多個行銷活動或多個歷程，且行銷活動或歷程報告不顯示用於給定傳送的模型。 使用AI模型狀態監視來瞭解並監視模型本身；針對傳遞層級的量度使用[行銷活動報告](../../reports/campaign-global-report-cja.md)和[歷程報告](../../reports/journey-global-report-cja.md)。
+++

+++ 我的最佳化量度是持續量度（如收入或訂單值），而非二進位量度（如點按或轉換）。 如何解譯報告的轉換和轉換率值？

當使用連續量度（例如收入或訂單值）時，模型會嘗試預測與特定優惠方案呈現相關的估計值（而不是轉換的可能性）。 報告的「轉換」值是與每個模型臂所記錄的選件顯示相關聯的總收入（或訂單值）。 報告的「轉換率」是「轉換」值除以「顯示」值，如果為連續量度，可能會超過100%。
+++

+++ 提升度顯著性為何？

提升度顯著性是報告的提升度與隨機探索的統計顯著性。 顯著性使用比例差異的Chi平方測試來計算，這可提供與兩個母體比例的Z測試顯著性計算相同的結果。
+++

+++ 什麼是模型基尼指數？ 基尼指數的「好」值為何？

模型基尼指數（也稱為基尼係數）是模型預測能力的離線測量。 模型基尼指數介於0 （無預測能力）至1 （可完美預測每個客戶每個優惠方案的轉換或量度值）之間。 沒有通用的「良好」基尼索引值，因為不同的決策使用案例會導致不同的使用者行為，從而產生不同的模型結果。 在相同的使用案例中，較高的Gini索引值表示較高的品質模型。
+++

+++ 如何計算基尼指數？

根據最佳化量度是二進位還是連續，每個模型臂的Gini索引計算方式不同：

**二進位最佳化量度** （例如點按數、訂購）：Gini索引是根據接收者操作特性(ROC)曲線的曲線(AUC)下的區域計算，通常稱為ROC AUC或簡稱為AUC。 ROC AUC的範圍從0.5 （零預測能力的隨機模型）到1.0 （完美預測能力）。 使用公式Gini = 2 x (ROC AUC) - 1將ROC AUC轉換為Gini索引。

**持續最佳化量度** （例如收入、訂購值）：Gini索引是根據與模型的累積預測正向相對母體中的累積真實正向相關的Lorenz曲線下的區域來計算的。 Lorenz曲線下方的區域介於0.0 （完美預測能力）到0.5 （零預測能力的隨機模型）之間。 使用公式Gini = 1 - 2 x (Lorenz AUC)將Lorenz AUC轉換為Gini索引。
+++

+++ 哪一個是模型品質較好的測量值：基尼指數或提升度/提升度顯著性？

一般而言，模型品質的線上測量（例如提升度和提升度顯著性）會被視為測量模型品質的「黃金標準」方法。 據報告，基尼指數可為評估決策模型的客戶資料科學團隊提供額外的資料點。
+++

<!--
## Understanding statuses and errors {#statuses-errors}

* **Success** – The latest training job completed successfully. The model is trained and deployed for ranking.
* **Failed** – The latest training job failed (for example, no events in the datasets). The UI shows an error message and a request ID; use these when troubleshooting or contacting support.
* **In progress** – A training job is running. Some metrics may be temporarily unavailable until it finishes.
* **Pending** – No result yet (for example, model recently activated or settings recently changed).

If no model has been successfully deployed yet, the "currently deployed model" section and some performance fields will be empty or show the initial-state messaging.
-->

## 作法影片 {#video}

瞭解如何監視您的AI排名模型，並解譯[!DNL Journey Optimizer]中的訓練狀態和績效。

>[!VIDEO](https://video.tv.adobe.com/v/3479849?quality=12)

## 相關檔案 {#related}

* [關於 AI 模型](ai-models.md)
* [個人化最佳化模型](personalized-optimization-model.md)
* [建立 AI 模型](create-ai-models.md)
* [建立資料集以收集事件](../data-collection/create-dataset.md)
