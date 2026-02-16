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
source-git-commit: bae446ea38a0cb97487201f7dcf4df751578ad0a
workflow-type: tm+mt
source-wordcount: '1938'
ht-degree: 13%

---

# 疑難排解您的即時歷程執行 {#troubleshooting-execution}

在本節中，瞭解如何疑難排解歷程事件、檢查設定檔是否進入您的歷程、如何導覽歷程，以及是否傳送訊息。

您也可以在測試或發佈歷程之前疑難排解錯誤。 在此頁面[上瞭解如何](troubleshooting.md)。

如果您使用輸入動作，請在此頁面[瞭解如何疑難排解](troubleshooting-inbound.md)。

## 檢查是否已正確傳送事件 {#checking-that-events-are-properly-sent}

歷程的起點永遠是一個事件。您可以使用 Postman 等工具執行測試。

您可以檢查您透過這些工具傳送的 API 呼叫是否都已正確傳送。如果您收到錯誤，則表示您的呼叫發生問題。再次檢查有效負載、標題（特別是組織 Id）和目的地 URL。您可以諮詢管理員哪個是要點擊的正確 URL。

不會直接將事件從來源推送到歷程。 事實上，歷程依賴[!DNL Adobe Experience Platform]的串流獲取API。 因此，如果發生與事件相關的問題，您可以參閱[[!DNL Adobe Experience Platform] 檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=zh-Hant){target="_blank"}以疑難排解串流獲取API。

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

* **事件條件和結構描述資料型別** — 請確定事件條件（規則）中使用的資料型別符合事件結構描述。 不相符的型別（例如，字串與整數）會導致規則評估失敗並捨棄事件。 請參閱[驗證事件身分](#verify-event-identity-and-rule-data-types)。

* **已捨棄事件 — 不符合資格條件** — 對於規則型事件，如果事件裝載不符合&#x200B;**資格條件** （例如，必要欄位空白或遺失，或欄位上的條件`isNotEmpty`失敗），則事件為&#x200B;**已接收但已捨棄**，且未觸發歷程。 記錄檔和Splunk追蹤可顯示已接收事件但已捨棄該事件，因為它不符合資格條件，並含有捨棄程式碼，例如`notSuitableInitialEvent`。 這是預期行為：若不符合資格條件，將會捨棄事件，且不會為該設定檔觸發歷程。 確認事件裝載包含預期的欄位和值，並確認事件設定中的規則符合您傳送的資料。 如果事件是由另一個歷程的&#x200B;**自訂動作**&#x200B;所觸發，請參閱自訂動作疑難排解中的[處理捨棄事件和閒置逾時](../action/troubleshoot-custom-action.md#handling-discard-events-and-idle-timeouts)。

&#x200B;>>
**針對具有串流對象的對象資格歷程**：如果您使用對象資格活動作為歷程進入點，請注意，由於時間因素、對象快速退出，或設定檔在發佈前已在對象中，並非所有符合對象資格的設定檔都一定會進入歷程。 深入瞭解[串流對象資格計時考量事項](audience-qualification-events.md#streaming-entry-caveats)。

### 驗證事件身分 {#verify-event-identity-and-rule-data-types}

設定事件型歷程時，請確認裝載的身分欄位符合在事件[中選取的](../event/about-creating.md#select-the-namespace)名稱空間。 如果事件包含設定檔比對的欄位，請驗證事件條件中的&#x200B;**字母大小寫**&#x200B;和&#x200B;**資料型別**&#x200B;是否完全符合傳入資料。 例如，如果事件結構描述將`roStatus`定義為字串，則歷程規則也必須將其評估為字串。 不相符的資料型別（例如，字串與整數）會導致規則評估失敗，並捨棄有效事件。 同樣地，如果事件具有&#x200B;**資格條件** （例如，欄位必須是非空白的），則不符合該條件的事件為&#x200B;**捨棄**，且不會觸發歷程；記錄檔可能會顯示捨棄的程式碼，例如`notSuitableInitialEvent`。

若要在[!DNL Journey Optimizer]中驗證您的事件條件，請在事件設定中使用裝載預覽，並確保規則中的型別和值符合裝載結構。 瞭解如何[預覽承載](../event/about-creating.md#preview-the-payload)和[設定規則型事件](../event/about-creating.md)。

## 測試模式轉換疑難排解 {#troubleshooting-test-transitions}

如果測試設定檔在測試模式下無法通過您的歷程，或視覺流程未顯示指示步驟進度的綠色箭頭，則此問題可能與轉變驗證有關。 本節提供診斷和解決常見測試模式問題的指引。

### 測試設定檔未進行中

如果測試設定檔進入歷程但未前進通過初始步驟，請檢查以下內容：

* **歷程開始日期** — 最常見的原因是歷程的開始日期設定在未來。 如果目前時間在歷程設定的[開始和結束日期/時間](journey-properties.md#dates)視窗之外，則會立即捨棄測試設定檔。 若要解決：
   * 確認歷程開始日期未設定在未來
   * 確保目前時間在歷程的有效日期範圍內
   * 如有必要，請更新歷程屬性以調整開始日期

* **測試設定檔組態** — 確認設定檔在[!DNL Adobe Experience Platform]中被正確標示為測試設定檔。 如需詳細資訊，請參閱[如何建立測試設定檔](../audience/creating-test-profiles.md)。

* **身分名稱空間** — 確保事件設定中使用的身分名稱空間符合測試設定檔的名稱空間。

### Null轉變指標

在技術疑難排解期間，您可能會在歷程的技術詳細資料中遇到設定為null的`isValidTransition`屬性。 此僅限UI的屬性不會影響後端處理或歷程效能。 但是，null值可以表示：

* **歷程設定錯誤** — 歷程開始日期設定在未來，導致測試事件被無訊息捨棄
* **已損毀的轉換** — 在極少數情況下，可能需要重新連線歷程節點

如果您遇到持續的轉換問題：

1. 確認歷程開始日期為目前日期
1. 停用及重新啟用測試模式
1. 如果問題仍然存在，請考慮複製受影響的歷程節點並重新連線它們
1. 對於未解決的情況，請聯絡支援人員並提供歷程記錄、受影響的設定檔ID以及空轉變的詳細資訊

>[!NOTE]
>
>請記住，在歷程的有效日期視窗之外傳送的事件會在無訊息的情況下捨棄，不會出現錯誤訊息。 疑難排解測試設定檔進度時，務必先驗證您的歷程計時設定。

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

請利用本節瞭解為什麼重複列會出現在歷程步驟事件中。

### 為什麼會看到具有相同歷程例項、設定檔、節點和請求ID的多個專案？

查詢歷程步驟事件資料時，您可能會偶爾觀察同一歷程執行的重複記錄專案。 這些專案會針對以下專案共用相同的值：

* `profileID` — 設定檔身分
* `instanceID` — 歷程執行個體識別碼
* `nodeID` — 特定歷程節點
* `requestID` — 要求識別碼

但是，這些專案有&#x200B;**個不同的`_id`值**，這是區分此案例與實際資料複製的關鍵指標。

### 導致此行為的原因是什麼？

這是因為[!DNL Adobe Journey Optimizer]的微服務架構中的後端自動縮放作業（也稱為「重新平衡」）所導致。 在高負載或系統最佳化期間：

1. 歷程步驟事件開始處理並記錄到歷程步驟事件資料集
2. 自動縮放作業會重新分配各服務執行處理的工作負載
3. 另一個服務執行個體可能會重新處理相同的事件，以不同的`_id`建立第二個記錄專案

這是預期的系統行為，且&#x200B;**運作方式符合設計**。

### 對歷程執行或訊息傳送是否有任何影響？

**否**&#x200B;影響僅限於記錄。 [!DNL Adobe Journey Optimizer]在訊息執行層具有內建的重複資料刪除機制，可確保：

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
