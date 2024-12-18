---
solution: Journey Optimizer
product: journey optimizer
title: 關於存留時間(TTL)和串流細分變更
description: Adobe Journey Optimizer中的存留時間和串流細分變更
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: platform、資料湖、建立、湖、資料集、輪廓
source-git-commit: f9fdb738210c5450376bdbf86b44d385cd740fd0
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 5%

---


# 存留時間和串流細分變更 {#ttl-guardrail}

## 串流區段更新 {#segmentation-update}

自2024年11月1日起，串流區段將不再支援使用來自Journey Optimizer追蹤和意見反應資料集的傳送和開啟事件。 此變更將套用至所有客戶沙箱和組織。 有關過去不鼓勵此作法的資訊，請參閱[這裡](../audience/about-audiences.md#streaming-segmentation-events-guardrails)。

**常見問題**

+++ 這些變更是否會影響點按或其他追蹤事件的使用？

此變更只會影響傳送和開啟事件的使用；點按次數和其他追蹤事件仍可用於串流區段。

+++

+++ 此變更是否會影響批次細分？

此變更只會影響串流分段；傳送和開啟事件仍可用於批次區段。 如果用於串流區段，則會以批次方式評估。

+++

+++ 此變更是否會影響追蹤資料的收集？

此變更不會影響追蹤資料的收集。 將繼續收集傳送和開啟的事件。

+++


+++ 此變更是否會影響反應事件？

歷程中的反應事件不受此變更的影響。

+++


+++ 此變更只會套用至生產沙箱，還是也會套用至開發沙箱？

此變更將套用至所有沙箱型別。

+++

+++ 傳送事件產生的意見反應事件是否也會受到此變更的影響？

此變更也適用於排除事件和由傳送導致的退回/延遲事件。

+++

## 分階段存留時間(TTL)更新 {#ttl}

從2025年2月開始，存留時間(TTL)護欄將推出至&#x200B;**新沙箱和新組織**&#x200B;中的Journey Optimizer系統產生的資料集，如下所示：

* 輪廓存放區中的資料為 90 天
* 資料湖中的資料為 13 個月

此變更將在後續階段中轉出到&#x200B;**現有的客戶沙箱**。

**常見問題**

+++ 此變更只會套用至生產沙箱，還是也會套用至開發沙箱？

此變更將套用至所有沙箱型別。

+++

+++ 對於設定檔存放區中的90天TTL，設定檔本身是否會受到影響？

90天後，會捨棄設定檔中系統產生的資料集資料，而非設定檔本身。

+++

+++ 如果系統產生的資料集資料被推送到Customer Journey Analytics (CJA)，CJA中的資料也會受到TTL影響嗎？

CJA中的資料會與Experience Platform保持同步。 因此，因系統產生的資料集資料的TTL而移除資料，也會影響CJA中的資料。

+++
