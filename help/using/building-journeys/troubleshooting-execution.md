---
solution: Journey Optimizer
product: journey optimizer
title: 疑難排解您的即時歷程執行
description: 瞭解如何疑難排解即時歷程執行中的錯誤
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: 疑難排解，疑難排解，歷程，檢查，錯誤
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '1260'
ht-degree: 20%

---

# 疑難排解您的即時歷程執行 {#troubleshooting-execution}

在本節中，瞭解如何疑難排解歷程事件、檢查設定檔是否進入您的歷程、如何導覽歷程，以及是否傳送訊息。

您也可以在測試或發佈歷程之前疑難排解錯誤。 在此頁面[上瞭解如何](troubleshooting.md)。

如果您使用輸入動作，請在此頁面[瞭解如何疑難排解](troubleshooting-inbound.md)。

## 檢查是否已正確傳送事件 {#checking-that-events-are-properly-sent}

歷程的起點永遠是一個事件。您可以使用 Postman 等工具執行測試。

您可以檢查您透過這些工具傳送的 API 呼叫是否都已正確傳送。如果您收到錯誤，則表示您的呼叫發生問題。再次檢查有效負載、標題（特別是組織 Id）和目的地 URL。您可以諮詢管理員哪個是要點擊的正確 URL。

不會直接將事件從來源推送到歷程。 事實上，歷程依賴Adobe Experience Platform的串流獲取API。 因此，如果發生與事件相關的問題，您可以參閱[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=zh-Hant){target="_blank"}，以疑難排解串流獲取API。

如果您的歷程無法啟用測試模式，錯誤為`ERR_MODEL_RULES_16`，請確定使用的事件包含使用通道動作時的[身分名稱空間](../audience/get-started-identity.md)。

身分名稱空間會用於唯一識別測試設定檔。 例如，如果使用電子郵件來識別測試設定檔，則應選取身分名稱空間&#x200B;**電子郵件**。 如果唯一識別碼是電話號碼，則應該選取識別名稱空間&#x200B;**電話**。

## 檢查是否有人進入歷程 {#checking-if-people-enter-the-journey}

歷程報告會即時衡量歷程中的人員入口。

如果您成功傳送事件，但未看到有人進入歷程，則表示在事件傳送與事件接收之間發生錯誤。

您可以透過下列問題開始進行疑難排解：

* 您確定您預期會發生傳入事件的歷程處於測試模式或是即時狀態？
* 在從有效負載預覽複製有效負載之前，您是否已儲存事件？
* 您的事件有效負載是否包含事件 ID？
* 您是否點按了正確的 URL？
* 您是否依照串流獲取 API 有效負載結構，而在事件設定窗格中使用有效負載結構預覽？請參閱[此頁面](../event/about-creating.md#preview-the-payload)。
* 您在事件標題中是否使用正確的機碼值組？

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

>[!NOTE]
>
>**針對具有串流對象的對象資格歷程**：如果您使用對象資格活動作為歷程進入點，請注意，由於時間因素、對象快速退出，或設定檔在發佈前已在對象中，並非所有符合對象資格的設定檔都一定會進入歷程。 深入瞭解[串流對象資格計時考量事項](audience-qualification-events.md#streaming-entry-caveats)。

## 檢查人們如何導覽歷程 {#checking-how-people-navigate-through-the-journey}

歷程報告會衡量歷程中個人的進度。 可輕鬆識別人員停止的位置及原因。

以下是一些要檢查的事項：

* 是否是因為某個條件排除此人？例如，條件是 &quot;gender = male&quot;，但人員是女性。如果條件並非太複雜，則可由業務使用者執行此檢查。
* 是否是因為呼叫資料來源未回應？當歷程處於測試模式時，可在測試模式日誌中看到此資訊。當歷程為即時狀態時，管理員可測試直接呼叫資料來源並檢查收到的答案。管理員也可以複製歷程並進行測試。

## 檢查訊息是否成功傳送 {#checking-that-messages-are-sent-successfully}

如果個人在歷程中的進度正常，但沒有收到應接收的訊息，您可以檢查：

* [!DNL Journey Optimizer]已正確考慮傳送郵件的要求。 業務使用者可以存取應傳送的訊息，並檢查最新執行的時間是否與歷程的執行時間對應。 他們也可以檢查收到的最新API呼叫/事件。
* [!DNL Journey Optimizer]已成功傳送訊息。 檢查歷程報告以確定沒有錯誤。

若是透過自訂動作傳送訊息，在歷程測試期間唯一可以檢查的事項，就是自訂動作系統的呼叫是否會導致錯誤。 如果呼叫與自訂動作相關聯的外部系統並未導致錯誤，但並未導致訊息傳送，則應在外部系統端進行一些調查。

## 瞭解歷程步驟事件中的重複專案 {#duplicate-step-events}

### 為什麼會看到具有相同歷程例項、設定檔、節點和請求ID的多個專案？

查詢歷程步驟事件資料時，您可能會偶爾觀察同一歷程執行的重複記錄專案。 這些專案會針對以下專案共用相同的值：

* `profileID` — 設定檔身分
* `instanceID` — 歷程執行個體識別碼
* `nodeID` — 特定歷程節點
* `requestID` — 要求識別碼

但是，這些專案有&#x200B;**個不同的`_id`值**，這是區分此案例與實際資料複製的關鍵指標。

### 導致此行為的原因是什麼？

這是因為Adobe Journey Optimizer微服務架構中的後端自動縮放操作（也稱為「重新平衡」）所導致。 在高負載或系統最佳化期間：

1. 歷程步驟事件開始處理並記錄到歷程步驟事件資料集
2. 自動縮放作業會重新分配各服務執行處理的工作負載
3. 另一個服務執行個體可能會重新處理相同的事件，以不同的`_id`建立第二個記錄專案

這是預期的系統行為，且&#x200B;**運作方式符合設計**。

### 對歷程執行或訊息傳送是否有任何影響？

**否**&#x200B;影響僅限於記錄。 Adobe Journey Optimizer在訊息執行層設有內建的重複資料刪除機制，可確保：

* 每個設定檔僅會傳送一則訊息（電子郵件、簡訊、推播通知等）
* 動作只會執行一次
* 歷程執行正確進行

您可查詢`ajo_message_feedback_event_dataset`或檢查動作執行記錄來驗證此訊息 — 即使有重複的歷程步驟事件專案，您仍會看到實際只傳送了一則訊息。

### 如何在查詢中識別這些案例？

分析歷程步驟事件資料時：

1. **檢查`_id`欄位**： True系統層級重複專案會有相同的`_id`。 不同的`_id`值表示與上述重新平衡案例不同的記錄專案。

2. **確認訊息傳送**：與訊息回饋資料互動參照，以確認只傳送了一則訊息：

   ```sql
   SELECT
     timestamp,
     _experience.customerJourneyManagement.messageExecution.messageExecutionID,
     _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
   FROM ajo_message_feedback_event_dataset
   WHERE
     _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journeyVersionID>'
     AND TO_JSON(identityMap) like '%<profileID>%'
   ORDER BY timestamp DESC;
   ```

3. **依唯一識別碼群組**：計算執行次數時，請使用`_id`取得正確計數：

   ```sql
   SELECT
     COUNT(DISTINCT _id) as unique_executions
   FROM journey_step_events
   WHERE
     _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
     AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID>'
   ```

### 如果我觀察到此現象該怎麼辦？

這是正常的系統行為，**不需要任何動作**。 重複的記錄並不表示您的歷程設定或訊息傳送有問題。

如果您是根據歷程步驟事件建置報表或分析：

* 使用`_id`作為計算唯一事件的主索引鍵
* 分析訊息傳遞時，與訊息意見回饋資料集互動參照
* 請注意，計時分析可能會顯示彼此在幾秒內叢集的專案

如需有關查詢歷程步驟事件的詳細資訊，請參閱[查詢範例](../reports/query-examples.md)。

## 疑難排解儀表板量度差異 {#dashboard-metrics}

如果&#x200B;**總覽**&#x200B;儀表板中顯示的度量不符合&#x200B;**瀏覽**&#x200B;索引標籤中的實際歷程次數，請驗證下列專案：

* 確保問題歷程在過去24小時內曾有流量，因為沒有最近活動的歷程會從儀表板排除。
* 檢查您是否有適當的存取許可權可檢視組織中的所有歷程。
* 在您的歷程進行變更後，最多可等待30分鐘讓量度重新整理。

如果差異持續存在，請聯絡Adobe支援，提供「概觀」和「瀏覽」索引標籤的熒幕擷取畫面以供調查。
