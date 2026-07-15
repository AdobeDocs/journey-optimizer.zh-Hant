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
TQID: https://experienceleague.adobe.com/2YZ6Cjph9Le-HtwKdz4GBgEdhwIMPpVtj9yWKlV3hQ4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 8d9c09a7be3757624c72a0a9d2739d0dbb48adeb
workflow-type: tm+mt
source-wordcount: 3051
ht-degree: 8%

---

# 疑難排解您的即時歷程執行 {#troubleshooting-execution}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何疑難排解即時歷程的執行，包括驗證是否已傳送事件、確認設定檔已進入並透過歷程進行，以及檢查是否已傳送訊息。

>[!ENDSHADEBOX]

在本節中，瞭解如何疑難排解歷程事件、檢查設定檔是否進入您的歷程、如何導覽歷程，以及是否傳送訊息。

您也可以在測試或發佈歷程之前疑難排解錯誤。 在此頁面[&#128279;](troubleshooting.md)上瞭解如何。

如果您使用輸入動作，請在此頁面[&#128279;](troubleshooting-inbound.md)瞭解如何疑難排解。

## 檢查是否已正確傳送事件 {#checking-that-events-are-properly-sent}

歷程的起點永遠是一個事件。 您可以使用 Postman 等工具執行測試。

您可以檢查您透過這些工具傳送的 API 呼叫是否都已正確傳送。 如果您收到錯誤，則表示您的呼叫發生問題。 再次檢查有效負載、標題（特別是組織 Id）和目的地 URL。 您可以諮詢管理員哪個是要點擊的正確 URL。

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
* 您是否依照串流獲取 API 有效負載結構，而在事件設定窗格中使用有效負載結構預覽？ 請參閱[此頁面](../event/about-creating.md#preview-the-payload)。
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

設定事件型歷程時，請確認裝載的身分欄位符合在事件[&#128279;](../event/about-creating.md#select-the-namespace)中選取的名稱空間。 如果事件包含設定檔比對的欄位，請驗證事件條件中的&#x200B;**字母大小寫**&#x200B;和&#x200B;**資料型別**&#x200B;是否完全符合傳入資料。 例如，如果事件結構描述將`roStatus`定義為字串，則歷程規則也必須將其評估為字串。 不相符的資料型別（例如，字串與整數）會導致規則評估失敗，並捨棄有效事件。 同樣地，如果事件具有&#x200B;**資格條件** （例如，欄位必須是非空白的），則不符合該條件的事件為&#x200B;**捨棄**，且不會觸發歷程；記錄檔可能會顯示捨棄的程式碼，例如`notSuitableInitialEvent`。

若要在[!DNL Journey Optimizer]中驗證您的事件條件，請在事件設定中使用裝載預覽，並確保規則中的型別和值符合裝載結構。 瞭解如何[預覽承載](../event/about-creating.md#preview-the-payload)和[設定規則型事件](../event/about-creating.md)。

## 測試模式轉換疑難排解 {#troubleshooting-test-transitions}

如果測試設定檔在測試模式下無法通過您的歷程，或視覺流程未顯示指示步驟進度的綠色箭頭，則此問題可能與轉變驗證有關。 本節提供診斷和解決常見測試模式問題的指引。

### 測試設定檔未進行中

如果測試設定檔進入歷程但未前進通過初始步驟，請檢查以下內容：

* **歷程開始日期** — 最常見的原因是歷程的開始日期設定在未來。 如果目前時間在歷程設定的[開始和結束日期/時間](journey-properties.md#dates)視窗之外，產生記錄專案： `DISPATCHER DISCARD #16 — unqualified on journey version enablements`，則會立即捨棄測試設定檔。 若要解決：
   * 確認歷程開始日期未設定在未來
   * 確保目前時間在歷程的有效日期範圍內
   * 如有必要，請將開始日期暫時設定為目前時間之前的測試時間，然後在發佈之前還原

* **測試設定檔組態** — 確認設定檔在[!DNL Adobe Experience Platform]中被正確標示為測試設定檔。 如需詳細資訊，請參閱[如何建立測試設定檔](../audience/creating-test-profiles.md)。

* **身分名稱空間不符** — 名稱空間不符會導致無訊息下降：事件被接受並傳回成功回應，但設定檔從未進入歷程，且UI中未出現任何錯誤。 請確定&#x200B;**設定檔識別碼**&#x200B;中的名稱空間完全符合事件結構描述中定義的名稱空間（區分大小寫）。 如需詳細資訊，請參閱[設定檔識別碼運算式格式](testing-the-journey.md#trigger-events-prerequisites)。

### Null轉變指標

在技術疑難排解期間，您可能會在歷程的技術詳細資料中遇到設定為null的`isValidTransition`屬性。 此僅限UI的屬性不會影響後端處理或歷程效能。 但是，null值可以表示：

* **歷程設定錯誤** — 歷程開始日期設定在未來，導致測試事件被無訊息捨棄
* **已損毀的轉換** — 在極少數情況下，可能需要重新連線歷程節點

如果您遇到持續的轉換問題：

1. 確認歷程開始日期為目前日期
1. 停用及重新啟用測試模式
1. 如果問題仍然存在，請考慮複製受影響的歷程節點並重新連線它們
1. 對於未解決的情況，[聯絡支援人員](../start/user-interface.md#support-ticket-guidelines)並提供歷程記錄、受影響的設定檔ID以及有關null轉變的詳細資訊

>[!NOTE]
>
>在歷程的有效日期視窗之外傳送的事件，會以記錄專案`DISPATCHER DISCARD #16 — unqualified on journey version enablements`自動捨棄，且不會出現UI錯誤。 疑難排解測試設定檔進度時，務必先驗證您的歷程計時設定。

## 檢查人們如何導覽歷程 {#checking-how-people-navigate-through-the-journey}

歷程報告會衡量歷程中個人的進度。 可輕鬆識別人員停止的位置及原因。

以下是一些要檢查的事項：

* 是否是因為某個條件排除此人？ 例如，條件是 &quot;gender = male&quot;，但人員是女性。 如果條件並非太複雜，則可由業務使用者執行此檢查。
* 是否是因為呼叫資料來源未回應？ 當歷程處於測試模式時，可在測試模式日誌中看到此資訊。 當歷程為即時狀態時，管理員可測試直接呼叫資料來源並檢查收到的答案。 管理員也可以複製歷程並進行測試。

## 由於封鎖歷程執行個體，已捨棄事件 {#max-instance-stack-events-reached}

如果您看到以`maxInstanceStackEventsReached`原因捨棄的事件，表示歷程執行階段已達到其內部每個設定檔事件棧疊限制，即特定歷程版本的10個事件。 這是安全護欄，可防止當相同設定檔的另一個事件仍在處理中時，棧疊過多待處理事件。

這是&#x200B;**不是**&#x200B;時間範圍或輸送量限制。 當設定檔的歷程執行個體在長時間執行的步驟（例如，長時間等待、擴充或自訂動作重試）上遭到封鎖，以及相同設定檔（也用於該歷程）的事件累積超過10個事件的限制時，就會發生這種情況。

若要識別，查詢捨棄原因等於`maxInstanceStackEventsReached`的歷程步驟事件（例如，`serviceEvents.stateMachine.eventType`或類似欄位中）。 在[步驟事件欄位清單](../reports/sharing-field-list.md#discarded-events)中進一步瞭解捨棄的事件型別。

**您可以做什麼**

* 減少可能頻繁重新觸發的路徑上的長時間等待或緩慢步驟。
* 儘可能刪除重複或取消退回上游事件。
* 將長期執行的情境分割為多個歷程，以避免棧疊。

## 檢查訊息是否成功傳送 {#checking-that-messages-are-sent-successfully}

如果個人在歷程中的進度正常，但沒有收到應接收的訊息，您可以檢查：

* [!DNL Journey Optimizer]已正確考慮傳送郵件的要求。 業務使用者可以存取應傳送的訊息，並檢查最新執行的時間是否與歷程的執行時間對應。 他們也可以檢查收到的最新API呼叫/事件。
* [!DNL Journey Optimizer]已成功傳送訊息。 檢查歷程報告以確定沒有錯誤。

若是透過自訂動作傳送訊息，在歷程測試期間唯一可以檢查的事項，就是自訂動作系統的呼叫是否會導致錯誤。 如果呼叫與自訂動作相關聯的外部系統並未導致錯誤，但並未導致訊息傳送，則應在外部系統端進行一些調查。

## 瞭解歷程步驟事件中的重複專案 {#duplicate-step-events}

請利用本節瞭解為什麼重複列會出現在歷程步驟事件中。

### 為什麼會看到多個具有相同歷程例項、設定檔、節點和請求ID的專案？

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

**編號** 影響僅限於記錄。 [!DNL Adobe Journey Optimizer]在訊息執行層具有內建的重複資料刪除機制，可確保：

* 只有一個訊息（電子郵件、簡訊、推播通知等） 會傳送至每個設定檔
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

如果差異持續存在，請[聯絡Adobe支援](../start/user-interface.md#support-ticket-guidelines)，取得「概述」和「瀏覽」索引標籤的熒幕擷取畫面以進行調查。

## 追蹤引數在已關閉歷程中顯示空白的預留位置 {#tracking-parameters-closed-journeys}

如果已傳送電子郵件中的追蹤URL包含空白的預留位置，例如`cid=em-acou-adob{}`，這可能表示無法解析內容欄位，例如`context.system.source.actionId`。 這通常發生在歷程關閉且相關產品變更後尚未重新發佈時 — 重新發佈的歷程只會正確填入追蹤URL中的這些內容欄位。

若要解決此問題，請重新發佈歷程（[建立新版本並發佈](publish-journey.md#journey-create-new-version)），或從頻道設定或電子郵件內容中的[URL追蹤引數](../email/url-tracking.md)移除受影響內容欄位的參考。

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面為Adobe Journey Optimizer中即時歷程執行的完整疑難排解參考，涵蓋事件傳送、設定檔專案失敗、測試模式轉換問題、捨棄事件、重複步驟事件記錄檔、訊息傳送檢查，以及儀表板量度差異。

**意圖：**
* 檢查裝載結構、標題和資格條件，以診斷事件未觸發歷程專案的原因
* 驗證設定檔是否正在進入及進行即時或測試模式歷程
* 解決未來開始日期或身分名稱空間設定錯誤所導致的測試模式轉換失敗
* 瞭解並處理封鎖之歷程執行個體的`maxInstanceStackEventsReached`捨棄原因
* 識別並正確查詢後端自動縮放導致的重複歷程步驟事件記錄專案
* 透過檢查歷程報告和自訂動作呼叫結果來調查缺少的訊息
* 修正已關閉歷程之電子郵件中的空白追蹤URL預留位置

**字彙表：**
* **歷程步驟事件**：記錄歷程中每個執行之設定檔步驟的資料集，用於報告和偵錯&#x200B;*（產品特定）*
* **notSuitableInitialEvent**：已收到表示事件的捨棄代碼，但因不符合資格條件而捨棄&#x200B;*（產品特定）*
* **maxInstanceStackEventsReceived**：表示每個設定檔歷程執行個體事件棧疊限制10的捨棄程式碼已超過&#x200B;*（產品特定）*
* **isValidTransition**：歷程技術詳細資料中的僅限UI屬性；null值可能表示未來的開始日期或損壞的節點連線，但不會影響後端處理&#x200B;*（產品特定）*
* **資格條件**：在事件上定義的規則，必須滿足該規則才能觸發歷程；若未滿足此條件，則會捨棄事件
* **重新平衡**： AJO微服務中的後端自動縮放作業，可建立具有不同值`_id`的重複Journey Step事件記錄檔專案

**護欄：**
* 在歷程的作用中日期/時間範圍以外傳送的事件會無訊息地捨棄，不會出現錯誤訊息
* 每個設定檔歷程執行個體事件棧疊限製為10個事件；超過此限制會導致事件與`maxInstanceStackEventsReached`一起捨棄
* 具有不同`_id`值的重複歷程步驟事件專案是預期的系統行為，不表示訊息重複
* 控制面板概觀量度僅包含過去24小時內具有流量的歷程；量度可能需要最多30分鐘才能重新整理
* 產品變更後尚未重新發佈的已關閉歷程可能會在追蹤URL中產生空白預留位置

**術語：**
* 正式名稱：歷程步驟事件 — 首字母縮寫：none — 變體：步驟事件，歷程執行記錄
* 正式名稱：資格條件 — 縮寫：無 — 變體：事件資格規則、事件條件
* 同義字：「重新平衡」=「自動縮放」（後端作業造成重複記錄專案）
* 請勿混淆：「重複`_id`」≠「來自重新平衡的重複記錄專案」 — true重複專案共用相同的`_id`；重新平衡重複專案有不同的`_id`值

**常見問題集：**
* **問：為什麼我的事件沒有觸發歷程，即使它們已成功傳送？**  — 檢查歷程是否為即時或處於測試模式、裝載符合事件結構描述結構、符合資格條件且包含正確的標頭(`X-gw-ims-org-id`、`Content-type`)。
* **問：為什麼測試設定檔會進入歷程但不會前進到超過第一個步驟？**  — 最常見的原因是歷程開始日期設定在未來；事件會在作用中日期範圍外自動捨棄。 同時確認測試設定檔標幟與身分名稱空間相符。
* **問：`maxInstanceStackEventsReached`是什麼意思？**  — 歷程執行階段已達到特定設定檔執行個體的內部10事件棧疊限制，通常是因為長時間執行的步驟會阻止處理。 減少長時間的等待、去除重複的上游事件，或將案例分割為多個歷程。
* **問：我在歷程步驟事件中看到重複的列 — 發生錯誤嗎？**  — 否。 需要不同`_id`值的重複專案，且結果來自後端自動縮放。 實際只傳送一封郵件；請使用`ajo_message_feedback_event_dataset`進行驗證。
* **問：為什麼電子郵件中的追蹤URL會顯示空白的預留位置，例如`cid=em-acou-adob{}`？**  — 歷程在產品變更後已關閉且未重新發佈；無法解析內容欄位。 重新發佈歷程或從URL追蹤引數中移除受影響的內容欄位參考。
* **問：為什麼[概觀]儀表板顯示的數字與[瀏覽]索引標籤不同？**  — 儀表板只會計算過去24小時內具有流量的歷程，量度最多需要30分鐘才能重新整理，而且存取許可權可能會限制可見度。

+++
