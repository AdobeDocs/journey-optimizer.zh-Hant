---
solution: Journey Optimizer
product: journey optimizer
title: 步驟事件欄位清單
description: 步驟事件欄位清單
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 9%

---

# 步驟事件欄位清單 {#sharing-field-list}

步驟事件欄位會依類別組織。

* 除錯資訊欄位
* 歷程欄位
* 設定檔欄位
* 服務事件欄位

對於identityMap屬性，主要身分依預設會定義為「primary = true」。

## debugInfo {#debuginfo-field}

| 欄位名稱 | 類型 | 說明 |
|---|---|------------|
| requestId | 字串 | Journey Optimizer用來追蹤請求流程的請求ID。 |

## 歷程 {#journey-field}

此欄位群組用於歷程結構描述中（與journeyStepEvent相關）。 它包含下列欄位：

| 欄位名稱 | 類型 | 說明 |
|---|---|------------|
| ID | 字串 | 給定歷程的識別碼 |
| 版本ID | 字串 | 歷程版本的ID。 此ID代表歷程的身分 |
| 名稱 | 字串 | 歷程的名稱 |
| 說明 | 字串 | 歷程描述 |
| 版本 | 字串 | 版本，表示為`major`.`minor` |

## 設定檔 {#profile-field}

此欄位群組是journeyStepEvent專屬的：此事件與歷程有關，且沒有identityMap，說明設定檔身分（如有）。

若為journeyStepEvent，我們還需要新增與身分相關的欄位：

| 欄位名稱 | 類型 | 說明 |
|---|---|------------|
| ID | 字串 | 設定檔識別碼會識別歷程中傳送/使用的設定檔。 例如： foo@adobe.com。 |
| 名稱空間 | 字串 | 此欄位說明歷程中使用的設定檔所參考的名稱空間。 例如：電子郵件、ECID |

## serviceEvents {#servicevents-field}

此Mixin包含與設定檔匯出作業對應的所有欄位。 這些事件是根據&#x200B;**讀取對象**&#x200B;活動產生，以追蹤對象匯出作業（已排入佇列、已開始、已完成、錯誤）的生命週期。 不同於一般步驟事件，serviceEvents不會繫結至個別設定檔，而是繫結至讀取對象節點本身，這表示它們可能沒有相關的設定檔識別碼。

| 欄位名稱 | 類型 | 說明 |
|---|---|------------|
| ID | 字串 | 已觸發的對象匯出工作的識別碼 |
| 狀態 | 字串 | 對象匯出工作的狀態：已排入佇列、已啟動、已完成 |
| exportCountTotal | 整數 | 對象匯出工作的最大可能值 |
| exportCountRealized | 整數 | 透過工作匯出的實際對象數量 |
| exportCountFailed | 整數 | 透過工作匯出時失敗的對象數量 |
| exportsegmentid | 字串 | 正在匯出之對象的識別碼 |
| eventType | 字串 | 事件型別，指出是錯誤事件還是資訊事件：資訊、錯誤 |
| eventcode | 字串 | 指示對應eventType原因的錯誤碼 |

在本節[中進一步瞭解eventTypes &#x200B;](#discarded-events)。

## stepEvents {#stepevents-field}

此類別包含原始步驟事件欄位。 請參閱本[章節](../reports/sharing-legacy-fields.md)。


## 疑難排解歷程步驟事件中的捨棄事件型別  {#discarded-events}

查詢具有`eventCode = 'discard'`的記錄的歷程步驟事件時，您可能會遇到數個eventTypes。

以下是最常捨棄`eventTypes`的定義、常見原因和疑難排解步驟：

* **EXTERNAL_KEY_COMPUTATION_ERROR**：系統無法從事件資料計算客戶的唯一識別碼（外部索引鍵）。

  **常見原因**：事件承載中遺失客戶識別碼（例如電子郵件、客戶ID）或格式錯誤。

  **疑難排解**：檢查必要識別碼的事件設定，確保事件資料完整且格式正確。

* **NO_INTEREST_JOURNEYS_FOR_SEGMENTMEMBERSHIP_EVENT**：已收到區段資格事件，但沒有設定要回應此區段的歷程。

  **常見原因**：沒有任何歷程使用區段作為觸發器、歷程處於草稿/已停止狀態，或區段ID不相符。

  **疑難排解**：確認至少有一個歷程為即時狀態且已針對區段進行設定，驗證區段ID。

* **JOURNEY_INSTANCE_ID_NOT_CREATE**：系統無法為客戶建立歷程執行個體。

  **常見原因**：重複的事件、大量事件、系統資源限制。

  **疑難排解**：實作重複資料刪除、避免流量尖峰、最佳化歷程設計、若持續發生，請聯絡支援人員。

* **EVENT_WITH_NO_JOURNEY**：已收到事件，但未設定使用中歷程來回應

  **常見原因**：事件名稱/ID不相符、歷程未發佈、錯誤的沙箱/組織、測試模式/設定檔不相符。

  **疑難排解**：驗證事件和歷程組態、檢查歷程狀態、使用偵錯工具。

* 對於在暫停的歷程中發生的捨棄：

   * **PAUSED_JOURNEY_VERSION**：捨棄歷程進入點發生的專案
   * **JOURNEY_IN_PAUSED_STATE**：捨棄設定檔在歷程中時發生的

  在[暫停歷程區段](../building-journeys/journey-pause.md#troubleshoot-profile-discards-in-paused-journeys)中進一步瞭解這些事件，以及如何疑難排解它們。

## 其他資源

* [資料集查詢範例 — 歷程步驟事件](../data/datasets-query-examples.md#journey-step-event)。
* [查詢範例 — 事件型查詢](query-examples.md#event-based-queries)。
* [內建結構描述字典](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=zh-Hant)

