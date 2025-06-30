---
title: 決策護欄與限制
description: 進一步瞭解Decisioning護欄和限制。
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 18%

---

# 決策護欄與限制 {#decisioning-guardrails}

為確保最佳化使用決策，請謹記以下護欄和限制。

[!DNL Journey Optimizer]護欄與限制的完整清單可在[此區段](../start/guardrails.md)中取得。

## 決定請求 {#decision-requests}

| 護欄 | 限制 |
| ------- | ------- |
| 使用Edge細分的具有決策原則的程式碼型體驗API請求 | 1500 |
| 具有不使用Edge細分之決策原則的程式碼型體驗API請求 | 5000 |

## 專案集合 {#item-collections}

| 護欄 | 限制 |
| ------- | ------- |
| 項目集合 | 10K |
| 每個專案集合的優惠方案專案總數 | 500 |

## 決策原則 {#decision-policy}

| 護欄 | 限制 |
| ------- | ------- |
| 每個決定原則的選擇策略和手動專案數量 | 10 |
| 每個決定原則傳回的最大優惠專案數 | 30 |

## 適用性規則 {#eligibility-rules}

| 護欄 | 限制 |
| ------- | ------- |
| 決策規則和排名公式總數 | 10,000合併 |
| 每個規則的設定檔屬性數量上限 | 25 |
| 每個規則的最大內容資料屬性數量 | 30 |
| pql規則的大小上限 | 15K (UTF-8) |
| 最大巢狀層級數 | 30 |

## 排名公式 {#ranking-formulas}

| 護欄 | 限制 |
| ------- | ------- |
| 排名公式PQL的大小上限 | 8K (UTF-8) |
| 設定檔屬性數量上限 | 25 |
| 內容資料屬性的最大數量 | 30 |
| 最大巢狀層級數 | 30 |

## 其他 {#others}

| 護欄 | 限制 |
| ------- | ------- |
| 每個優惠方案目錄結構描述的自訂屬性數量 | 100 |
| 選件專案總數 | 10K |
| 總版位 | 1K |
| AI排名模型 | 5 |
| 頻率規則 — 每個選件的上限規則數量上限 | 10 |
