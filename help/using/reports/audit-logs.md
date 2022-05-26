---
title: 對Journey Optimizer資源的審計行動
description: 瞭解如何跟蹤在Journey Optimizer資源上執行的操作。
feature: Monitoring
role: User
level: Intermediate
source-git-commit: 336a2a4d28ce1738cc664861291fdc1f39b3ab29
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 1%

---

# 對Journey Optimizer資源的審計行動 {#track-changes}

## 關於審核日誌 {#audit-logs}

使用Journey Optimizer，您可以識別系統中的用戶對各種服務和功能（如旅程、消息、登錄頁等）執行的操作。

這使您能夠提高系統中所執行活動的可見性，解決問題，並幫助您的企業遵守法規和公司資料管理策略。

每項行動都記錄在可在Adobe Experience Platform訪問的&quot;審計日誌&quot;中的元資料。 有關審核日誌的詳細資訊，包括如何在UI或API中查看和管理這些日誌，請參閱 [Adobe體驗平台文檔](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html)。

![](assets/audit-logs.png)

## 由審核日誌捕獲的事件類型 {#events}

下表概述了審計日誌記錄Journey Optimizer資源的行動。

>[!NOTE]
>
>在「審核」日誌中捕獲的操作的完整清單可在 [Adobe體驗平台文檔](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html#category)。

| 資源 | 動作 |
|-----------|------------------|
| 欄位組 | 建立/刪除/更新 |
| AJO子域 | 建立/刪除/更新 |
| CJM禁止清單 | 建立/刪除/下載CSV |
| AJO消息預設 | 建立/刪除/更新 |
| AJO PTR記錄 | 建立/刪除/更新 |
| 排名策略 | 建立/刪除/更新 |
| 行程自定義操作 | 建立/刪除/更新 |
| AJO登錄頁HTML模板 | 建立/刪除/更新 |
| AJO IP池 | 建立/刪除/更新 |
| AJO登錄頁子域 | 建立/刪除/更新 |
| AJO SMS API憑據 | 建立/刪除/更新 |
| AJO登錄頁預設 | 建立/刪除/更新 |
| 旅程資料源 | 建立/刪除/更新 |
| 旅程事件 | 建立/刪除/更新 |
| AJO保存的表達式模板 | 建立/刪除/更新 |
| 消息頻率規則 | 建立/刪除/更新 |
| AJO登錄頁 | 建立/刪除/更新/發佈/取消發佈 |
| 歷程 | 建立/刪除/更新/停止/發佈 |
| AJO消息 | 建立/刪除/更新/發佈 |
| AJO頻道常規設定 | 建立/刪除/更新 |
