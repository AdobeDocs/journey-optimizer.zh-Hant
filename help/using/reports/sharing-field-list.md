---
solution: Journey Optimizer
product: journey optimizer
title: 步驟事件欄位清單
description: 步驟事件欄位清單
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 18%

---

# 步驟事件欄位清單 {#sharing-field-list}

步驟事件欄位會依類別組織。

* 除錯資訊欄位
* 歷程欄位
* 設定檔欄位
* 服務事件欄位

## debugInfo {#debuginfo-field}

| 欄位名稱 | 類型 | 說明 |
|---|---|------------|
| requestId | 字串 | Journey Optimizer用來追蹤請求流程的請求ID。 |

## 歷程 {#journey-field}

此欄位群組用於歷程綱要（與journeyStepEvent相關）。 它包含下列欄位：

| 欄位名稱 | 類型 | 說明 |
|---|---|------------|
| ID | 字串 | 指定歷程的識別碼 |
| VersionID | 字串 | 歷程版本的ID。 此ID代表歷程的身分 |
| 名稱 | 字串 | 歷程名稱 |
| 說明 | 字串 | 歷程描述 |
| version | 字串 | 版本，表示為 `major`.`minor` |

## 設定檔 {#profile-field}

此欄位群組是journeyStepEvent的專屬群組：此事件與歷程有關，且沒有identityMap，說明設定檔身分（如有）。

若為journeyStepEvent，我們還需要新增與身分相關的欄位：

| 欄位名稱 | 類型 | 說明 |
|---|---|------------|
| ID | 字串 | 設定檔識別碼會識別歷程中傳送/使用的設定檔。 例如： foo@adobe.com。 |
| namespace | 字串 | 此欄位說明歷程中使用的設定檔所參考的名稱空間。 例如：電子郵件、ECID |

## serviceEvents {#servicevents-field}

此Mixin包含與設定檔匯出作業對應的所有欄位。

| 欄位名稱 | 類型 | 說明 |
|---|---|------------|
| ID | 字串 | 已觸發的對象匯出工作的識別碼 |
| 狀態 | 字串 | 對象匯出工作的狀態：已排入佇列、已啟動、已完成 |
| exportCountTotal | 整數 | 受眾匯出工作的最大可能值 |
| exportCountRealized | 整數 | 透過工作匯出的實際對象數量 |
| exportCountFailed | 整數 | 透過工作匯出時失敗的對象數量 |
| exportSegmentID | 字串 | 正在匯出的對象的識別碼 |
| 事件型別 | 字串 | 表示它是否為資訊事件的錯誤事件的事件型別：資訊、錯誤 |
| eventcode | 字串 | 指示對應eventType原因的錯誤代碼 |

## stepEvents {#stepevents-field}

此類別包含原始步驟事件欄位。 請參閱本[章節](../reports/sharing-legacy-fields.md)。
