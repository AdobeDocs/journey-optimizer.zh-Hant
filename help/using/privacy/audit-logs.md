---
solution: Journey Optimizer
product: journey optimizer
title: 稽核Journey Optimizer資源上的動作
description: 了解如何追蹤在Journey Optimizer資源上執行的動作。
feature: Monitoring
role: User
level: Intermediate
exl-id: 759b014a-c834-4331-bffd-5bc159ec555d
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# 稽核Journey Optimizer資源上的動作 {#track-changes}

## 關於稽核記錄 {#audit-logs}

透過Journey Optimizer，您可以識別系統中的使用者在各種服務和功能（例如歷程、訊息、登錄頁面等）上執行的動作。

這可讓您提高系統中所執行活動的可見度、疑難排解問題，並協助您的企業遵守法規和公司資料管理政策。

每個動作都會以「稽核記錄」（可在Adobe Experience Platform中存取）中的中繼資料記錄。 如需稽核記錄的詳細資訊，包括如何在UI或API中檢視和管理稽核記錄，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html).

![](assets/audit-logs.png)

## 由審核日誌捕獲的事件類型 {#events}

下表概述稽核記錄檔記錄Journey Optimizer資源的動作。

>[!NOTE]
>
>稽核記錄中擷取的動作完整清單可在 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html#category).

| 資源 | 動作 |
|-----------|------------------|
| AJO行銷活動 | 建立/刪除/更新/啟動/停止 |
| AJO頻道一般設定 | 建立/刪除/更新 |
| AJO IP池 | 建立/刪除/更新 |
| AJO登錄頁面 | 建立/刪除/更新/發佈/取消發佈 |
| AJO登錄頁面HTML範本 | 建立/刪除/更新 |
| AJO登錄頁面預設集 | 建立/刪除/更新 |
| AJO登錄頁面子網域 | 建立/刪除/更新 |
| AJO訊息 | 建立/刪除/更新/發佈 |
| AJO訊息預設集 | 建立/刪除/更新 |
| AJO PTR記錄 | 建立/刪除/更新 |
| AJO儲存的運算式範本 | 建立/刪除/更新 |
| AJO SMS API憑證 | 建立/刪除/更新 |
| AJO子網域 | 建立/刪除/更新 |
| AJO隱藏清單 | 建立/刪除/下載CSV |
| 欄位組 | 建立/刪除/更新 |
| 歷程 | 建立/刪除/更新/停止/發佈 |
| 歷程自訂動作 | 建立/刪除/更新 |
| 歷程資料來源 | 建立/刪除/更新 |
| 歷程事件 | 建立/刪除/更新 |
| 消息頻率規則 | 建立/刪除/更新 |
| 排名策略 | 建立/刪除/更新 |
