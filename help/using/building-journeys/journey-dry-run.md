---
solution: Journey Optimizer
product: journey optimizer
title: 歷程試運行
description: 瞭解如何在練習模式下發佈歷程
feature: Journeys
role: User
level: Intermediate
badge: label="可用性限制" type="Informative"
keywords: 發佈，歷程，即時，有效性，檢查
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
source-git-commit: 62525caa9b065538c090b98d38c15dbd960dafe7
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 24%

---

# 歷程試運行 {#journey-dry-run}

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="試執行模式"
>abstract="本次歷程處於試執行階段。歷程試執行是 Adobe Journey Optimizer 中的特殊歷程發佈模式，允許歷程實踐者使用真實的生產資料測試歷程，而無需聯絡真實客戶或更新輪廓資訊。此功能可協助歷程從業人員，針對歷程設計、客群目標市場選擇，累積信心，然後再將歷程發佈上線。"


>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run_start"
>title="在試執行模式中發佈歷程"
>abstract="歷程試執行是 Adobe Journey Optimizer 中的特殊歷程發佈模式，允許歷程實踐者使用真實的生產資料測試歷程。設計歷程後，請進行模擬演練執行來確認其運作正常，確保步驟正確。 此發布模式可讓您煙霧測試歷程，無需傳送通訊給任何輪廓。"

歷程試執行是 Adobe Journey Optimizer 中的特殊歷程發佈模式，允許歷程實踐者使用真實的生產資料測試歷程，而無需聯絡真實客戶或更新輪廓資訊。此功能可協助歷程從業人員，針對歷程設計、客群目標市場選擇，累積信心，然後再將歷程發佈上線。


>[!AVAILABILITY]
>
>此功能僅適用於某個組織（可用性限制），可在全球推出未來的版本。


## 主要優點 {#journey-dry-run-benefits}

Journey Diry run使用真實的生產資料對客戶歷程進行安全、資料導向的測試，免除聯絡客戶或變更設定檔資訊的風險，進而提高從業人員信心和歷程成功。 此功能讓歷程從業人員在上線前驗證受眾觸及範圍和分支邏輯，確保歷程與其預期業務目標一致。

有了歷程練習，您就能根據實際資料（而非假設）及早識別問題、最佳化鎖定目標策略，以及改善歷程設計。 練習版直接整合至歷程畫布，提供直覺式報告功能，並洞察關鍵績效指標，讓團隊充滿信心地反複交流，並簡化核准工作流程。 如此可提升營運效率、降低上市風險，並帶來更佳的客戶參與成果。

最終，此功能可改善實現價值的時間並減少歷程失敗。

Journey Dirun提供：

1. **安全測試環境**：未連絡處於試執行模式的設定檔，確保沒有傳送通訊或影響即時資料的風險。
1. **對象深入分析**：歷程從業人員可以預測對象在各種歷程節點上的可達性，包括退出、排除和其他條件。
1. **即時回饋**：量度會直接顯示在歷程畫布中，類似即時報告，讓歷程參與者能夠調整其歷程設計。

在模擬執行期間，歷程會以下列特性執行：

* 未執行&#x200B;**頻道動作**&#x200B;節點，包括電子郵件、簡訊或推播通知
* **自訂動作**&#x200B;已在試執行期間停用，而且其回應設定為Null
* 在試執行期間略過&#x200B;**等待節點**。
  <!--You can override the wait block timeouts, then if you have wait blocks duration longer than allowed dry run journey duration, then that branch will not execute completely.-->
* **預設會執行**&#x200B;資料來源，包括外部資料來源

>[!CAUTION]
>
>* 啟動試執行許可權僅限於具有&#x200B;**[!DNL Publish journeys]**&#x200B;高階許可權的使用者。 停止試執行的許可權僅限於具有&#x200B;**[!DNL Manage journeys]**&#x200B;高階許可權的使用者。 在[!DNL Journey Optimizer]本節[中進一步瞭解如何管理](../administration/permissions-overview.md)使用者的存取權。
>
>* 開始使用試執行功能之前，[請先閱讀護欄和限制](#journey-dry-run-limitations)。


## 開始試用 {#journey-dry-run-start}

您可以在任何草稿歷程中使用練習功能，不會發生錯誤。

若要啟動「試執行」，請遵循下列步驟：

1. 開啟您要測試的歷程。
1. 選取&#x200B;**試執行**&#x200B;按鈕。

   ![開始歷程試運行](assets/dry-run-button.png)

1. 確認發佈。

   轉換發生時，會出現狀態訊息&#x200B;**啟動試用**。

1. 一旦啟動，歷程就會進入&#x200B;**試執行**&#x200B;模式。

## 監視練習 {#journey-dry-monitor}

啟動乾模式發佈後，您可以視覺化歷程執行以及設定檔如何通過歷程分支和節點進展。

量度會直接顯示在歷程畫布中。 在歷程畫布的[即時報告中，進一步瞭解歷程即時報告和量度](report-journey.md)。

![監視歷程練習執行](assets/dry-run-metrics.png)


您也可以存取&#x200B;**過去24小時的報告**&#x200B;和&#x200B;**所有時間報告**&#x200B;來試用。 若要存取這些報告，請按一下歷程畫布右上角的&#x200B;**檢視報告**&#x200B;按鈕。

![存取歷程試執行的報告](assets/dry-run-report.png)

>[!CAUTION]
>
> 報告資料僅在試執行為&#x200B;**作用中**&#x200B;時可用。  停止後，將無法再存取報表資料。 使用報表上方的&#x200B;**匯出**&#x200B;按鈕，視需要下載報表。


## 停止試用 {#journey-dry-run-stop}

試執行歷程&#x200B;**必須**&#x200B;手動停止。

按一下&#x200B;**關閉**&#x200B;按鈕以結束測試，然後按一下&#x200B;**返回草稿**&#x200B;以確認。

<!-- After 14 days, Dry run journeys automatically transition to the **Draft** status.-->

## 護欄與限制 {#journey-dry-run-limitations}

* 試執行模式不適用於包含反應事件的歷程
* 處於試執行模式的設定檔計入可參與的設定檔
* 處於試執行模式的歷程計入即時歷程配額
* 練習歷程不會影響商業規則
* 建立新歷程版本時，如果先前的歷程版本為&#x200B;**即時**，則新版本不允許試執行啟動。
* 歷程練習會產生stepEvents。 這些stepEvents具有特定標幟和Derun ID：
   * 如果已啟動試運行，`_experience.journeyOrchestration.stepEvents.inDryRun`會傳回`true`，否則會傳回`false`
   * `_experience.journeyOrchestration.stepEvents.dryRunID`傳回試執行個體的識別碼

* 使用Adobe Experience Platform查詢服務分析歷程報告量度時，必須排除練習產生的步驟事件。 若要執行此動作，請將`inDryRun`標幟設定為`false`。