---
solution: Journey Optimizer
product: journey optimizer
title: 關於資料集存留時間(TTL)護欄
description: ' [!DNL Adobe Journey Optimizer]中的資料集存留時間護欄'
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 平台、資料湖、建立、湖、資料集、設定檔
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 18%

---

# 資料集存留時間 (TTL) 護欄 {#ttl-guardrail}

自 2025 年 2 月起，將在 **新沙箱和新組織** 中，向 Journey Optimizer 系統產生的資料集，開放使用存留時間 (TTL) 護欄功能，如下所示：

* 輪廓存放區中的資料為 90 天
* 資料湖中的資料為 13 個月

此變更將在後續階段中轉出到&#x200B;**現有的客戶沙箱**。

## 受影響的資料集 {#datasets}

下表列出所有受影響的資料集及其在資料湖和個人資料存放區中的個別存留時間。

| 資料集 | 資料湖TTL | 設定檔存放區TTL |
|------|-----|-----|
| AJO訊息回饋事件資料集 | 13 個月 | 90 天 |
| AJO電子郵件追蹤體驗事件資料集 | 13 個月 | 90 天 |
| AJO推播追蹤體驗事件資料集 | 13 個月 | 90 天 |
| AJO實體資料集 | 13 個月 | 90 天 |
| AJO表面資料集 | 13 個月 | 不適用 |
| AJO傳入活動事件資料集 | 13 個月 | 90 天 |
| AJO分類資料集 | 13 個月 | 不適用 |
| AJO電子郵件密件副本意見事件資料集 | 13 個月 | 不適用 |
| acpEntity事件資料集 | 13 個月 | 不適用 |
| 歷程 | 13 個月 | 不適用 |
| 歷程步驟事件 | 13 個月 | 不適用 |
| 決定物件存放庫 — 個人化優惠 | 13 個月 | 不適用 |
| 決定物件存放庫 — 遞補優惠 | 13 個月 | 不適用 |
| 決定物件存放庫 — 位置 | 13 個月 | 不適用 |
| 決定物件存放庫 — 活動 | 13 個月 | 不適用 |
| Experience Decisioning物件存放庫 — 個人化優惠專案 | 13 個月 | 不適用 |
| ODE DecisionEvents - prod decisioning | 13 個月 | 不適用 |

## 常見問題 {#faq}

以下是有關資料集TLL常見問題的解答清單。

+++此變更只會套用至生產沙箱，還是也會套用至開發沙箱？

此變更將套用至所有沙箱型別。

+++

+++對於設定檔存放區中的90天TTL，設定檔本身是否會受到影響？

90天後，會捨棄設定檔中系統產生的資料集資料，而非設定檔本身。

+++

+++如果系統產生的資料集資料被推送到[!DNL Customer Journey Analytics] (CJA)，CJA中的資料也會受到TTL影響嗎？

[!DNL Customer Journey Analytics]中的資料會與Experience Platform保持同步。 因此，因系統產生的資料集資料的TTL而移除資料，也會影響[!DNL Customer Journey Analytics]中的資料。

+++

+++ 客戶是否可以在設定檔存放區中增加[!DNL Journey Optimizer]系統資料集資料的TTL？ 

目前不支援TTL副檔名。 不過，我們已計畫最佳化TTL流程，以便在2025年下半年開始的某個時候允許這些擴充請求。

>[!NOTE]
>
>儲存在設定檔中的資料受限於「總資料量」權益。 因此，設定檔上因TTL延伸所增加的任何資料儲存都將計入「總資料量」權益。 [深入瞭解](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html){target=_blank}

+++

+++客戶能否為Data Lake中的[!DNL Journey Optimizer]系統資料集增加TTL？ 

目前不支援TTL副檔名。 客戶可以透過目的地匯出資料，以保留更長的資料時間。 [深入瞭解](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html){target=_blank}。 此外，擁有&#x200B;**[!DNL Data Distiller]**&#x200B;權益的客戶可以建立衍生資料集，以便在沒有TTL的情況下將資料儲存在Data Lake中。 [深入瞭解](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=_blank}

+++

+++TTL是否會影響下列功能？ 

* **查詢存放區**：否
* **歷程上限**：否
* **優惠方案上限**：否
* **傳送時間最佳化(STO)**：否
* **訊息頻率上限** （亦即商務規則）：否
* **報告**：否

  >[!NOTE]
  >
  >已在[!DNL Customer Journey Analytics] (CJA)連線上實作TTL，這會將受影響資料集資料的有效回顧期間縮短為13個月。

* **Experience Platform資料來源**：是 — 體驗事件擷取須遵守90天TTL。
* **計算屬性**：是 — 初始回填計算將限製為過去90天的資料；計算屬性將根據後續更新的增量事件進行更新。 後續更新一旦達到回顧期間（最多6個月），TTL基本上就不會再影響運算屬性。 更多詳情。
* **分段和重新目標定位**：是 — 分段取決於設定檔存放區中的資料；因此，受影響資料集資料的回顧時間限製為90天。
* **追蹤**：是 — 將受影響資料集資料的有效回顧期間縮短至90天。 來自受影響資料集的資料會在Data Lake中存留13個月。

+++

+++什麼時間戳記會用於TTL強制執行（例如，用於回填使用案例）？ 

系統會使用事件時間戳記（即並非擷取日期）。

+++
