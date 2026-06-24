---
solution: Journey Optimizer
product: journey optimizer
title: 從對象資格歷程移轉批次對象
description: 瞭解如何在2026年8月3日執行日期前移轉在對象資格節點中使用批次對象的歷程。
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: 對象資格，批次對象，淘汰，移轉，讀取對象，串流對象
exl-id: f3c2a7d1-b58e-4a92-c3d5-0e871f2a9b4c
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
source-git-commit: 6560a168d3ea7c6c27b47829ac4158b6a69b5d88
workflow-type: tm+mt
source-wordcount: 874
ht-degree: 0%

---


# 從對象資格歷程移轉批次對象 {#aq-batch-migration}

自2026年8月3日起，Journey Optimizer將封鎖在「對象資格」節點中使用批次對象之歷程的發佈。 在下方識別您的使用案例，並遵循建議的移轉路徑。

>[!CAUTION]
>
>**強制日期： 2026年8月3日。** 在此日期之後，將無法發佈在「對象資格」節點中使用批次對象的新歷程、草稿歷程和重複歷程。 自2026年6月發行版本以來，歷程畫布中已出現驗證警告。

## 為何發生此變更 {#why}

**[對象資格](audience-qualification-events.md)**&#x200B;節點的設計可在個別設定檔進入或退出對象時近乎即時地回應 — 資格事件會逐一持續到達。 其適用於&#x200B;**[串流對象](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)**。

當批次對象改為搭配對象資格節點使用時，所有資格事件會在擷取期間同時到達。 這可能會同時觸發數萬或數百萬個歷程專案，造成嚴重的系統負擔，以及下游系統中無法預測的行為。 這不是「對象資格」節點的預期設計。

**[讀取對象](read-audience.md)**&#x200B;活動是批次式使用案例的正確工具：它是用來以可控且可預測的方式處理排程、大量處理。

## 您的歷程會如何受影響 {#impact}

在「對象資格」節點中使用批次對象的即時歷程在2026年8月3日之後繼續執行。 但是，如果您停止、複製或重新發佈歷程，則會在更新設定前遭到封鎖。


| 歷程狀態 | 2026年8月3日之後的影響 |
| --- | --- |
| **即時歷程** | 未受影響。 現有的即時歷程會繼續執行。 不會自動停止。 |
| **新歷程** | 在取代批次對象之前，禁止發佈。 |
| **草稿歷程** | 在取代批次對象之前，禁止發佈。 |
| **重複的歷程** | 在取代批次對象之前，禁止發佈。 |


## 移轉指南 {#migration-paths}

如果您在「對象資格」節點中使用批次對象，請在下方識別您的使用案例，並遵循建議的移轉路徑。

### 使用案例1 — 以AJO訊息追蹤事件為基礎的對象 {#use-case-1}

**看起來像這樣：**&#x200B;您的對象資格對象會根據來自Journey Optimizer內部追蹤資料集的電子郵件傳送、開啟或點按，使用條件 — 例如，*「設定檔收到電子郵件」*&#x200B;或&#x200B;*「設定檔開啟電子郵件」*。

>[!NOTE]
>
>自2024年11月起，串流區段不再支援來自Journey Optimizer追蹤資料集的傳送和開啟事件。 現在會在批次模式中評估基於這些事件的對象。 [進一步瞭解對象評估方法](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)

**建議的替代方案：**

* **回應相同歷程中的開啟或點按** — 使用&#x200B;**[回應事件](reaction-events.md)**&#x200B;節點。 其專門建置為回應在同一歷程中傳送之訊息的開啟和點按，而不需要個別受眾。 [檢視使用反應事件的端對端範例](journeys-uc.md#send-multi-channel-messages)

* **跨歷程點選鎖定目標** — 從點選事件建置[串流對象](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)，並改用該串流對象的「對象資格」節點。

* **以跳出為基礎的隱藏** — 使用Journey Optimizer的原生[隱藏清單](../configuration/manage-suppression-list.md)，而非將跳出行為模型化為對象條件。

* **任何剩餘的傳送/開啟邏輯** — 在排定的執行上切換至&#x200B;**[讀取對象](read-audience.md)**&#x200B;歷程，以安全地處理批次對象。


### 使用案例2 — 等待全新批次細分資料的歷程 {#use-case-2}

**看起來像這樣：**&#x200B;您排程在每日細分工作之後執行的歷程，並使用「對象資格」節點來確保歷程只會在最新對象資料可用時引發。

**建議的替代方案：**

使用已啟用批次對象評估&#x200B;**選項的**&#x200B;[&#x200B;讀取對象&#x200B;](read-audience.md)**歷程及**&#x200B;觸發器。 此內建功能會保留歷程執行，直到細分工作完成，然後在有新資料可用時立即開始，而不需要「對象資格」節點。 [瞭解如何設定此選項](read-audience.md#schedule)


### 使用案例3 — 大量定期批次對象啟用 {#use-case-3}

**外觀：**&#x200B;您會定期啟動或重新整理大量對象（可能有數百萬個設定檔），且會一次針對所有新合格的設定檔引發對象資格歷程。

**建議的替代方案：**

使用&#x200B;**[讀取對象](read-audience.md)**&#x200B;歷程。 這是專為大量處理大型受眾所打造，可控制批次處理設定檔，並大規模提供更可預測、更可靠的歷程執行。 [檢視端對端範例](message-to-subscribers-uc.md)

## 如果您的使用案例沒有其他可行方案可依循，該怎麼辦？ {#exceptions}

如果使用上述任何移轉路徑都無法解決您的使用案例，請聯絡您的Adobe代表。 若情況無法使用現有替代方案解決，則會個別審查。

## 相關資源 {#related}

* [對象資格事件](audience-qualification-events.md) — 完整設定指南和護欄
* [讀取對象活動](read-audience.md) — 如何設定已排程的批次對象專案
* [回應事件](reaction-events.md) — 如何回應相同歷程中的開啟和點按
* [對象評估方法](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer) — 說明批次、串流和邊緣細分
* [關於對象](../audience/about-audiences.md) — 對象型別以及如何在Journey Optimizer中建置
* [管理隱藏清單](../configuration/manage-suppression-list.md) — 如何存取和設定退信隱藏
* [歷程護欄和限制](limitations.md)
* [歷程登入與退出條件](entry-exit-criteria-guide.md) — 透過真實世界的範例瞭解即時與批次登入模式
* [傳送多頻道訊息](journeys-uc.md#send-multi-channel-messages) — 結合讀取對象、回應事件、電子郵件和推播的端對端使用案例
* [傳送訊息給訂閱者](message-to-subscribers-uc.md) — 透過「讀取對象」進行大量對象啟用的端對端使用案例
