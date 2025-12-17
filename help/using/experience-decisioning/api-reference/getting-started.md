---
title: 開始使用Decisioning API
description: 瞭解如何開始使用決策API以程式設計方式管理決策專案並提供個人化優惠。
feature: API, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 7a4b5d4e-9c1d-4f3a-b8e9-1d5f6e7a8c3a
version: Journey Orchestration
source-git-commit: e46ab0637a0fa4a2b4b8b6ff3b8ab3eb5d38e0f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 4%

---

# Decisioning API開發人員指南 {#decisioning-api-developer-guide}

決策API可讓您以程式設計方式建立和管理用來向客戶提供個人化優惠的元件。 這些RESTful API針對決策專案、選擇策略、適用性規則和其他決策元件提供完整的CRUD （建立、讀取、更新、刪除）作業。

## Authentication {#authentication}

在使用決策API之前，您必須設定驗證以存取API端點。 如需逐步指示，請參閱[Journey Optimizer驗證指南](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}。

## 可用的API作業 {#available-operations}

決策API為決策元件提供全面的管理功能。 可用的作業類別如下：

* **決定專案** — 建立、讀取、更新、刪除和列出決定專案，這些決定專案代表您想要提供給客戶的優惠或內容。

  ➡️ [瞭解如何管理決定專案](decisions-items/create.md)

* **專案集合** — 將決定專案組織到集合中，以使用適用性規則更輕鬆地進行管理和定位。

  ➡️ [瞭解如何管理專案集合](items-collections/create.md)

* **選擇策略** — 定義當多個專案符合傳送資格時，如何選擇和排名決策專案。

  ➡️ [瞭解如何管理選擇策略](selection-strategies/create.md)

* **適用性規則** — 設定條件，決定哪些設定檔符合接收特定決定專案的資格。

  ➡️ [瞭解如何管理適用性規則](eligibility-rules/create.md)

* **排名公式** — 建立自訂排名邏輯，以決定決策專案的顯示順序。

  ➡️ [瞭解如何管理排名公式](ranking-formulas/create.md)

* **位置** — 定義可在您的體驗中顯示決策專案的位置或內容。

  ➡️ [瞭解如何管理刊登版位](exd-placements/create.md)

## 後續步驟 {#next-steps}

現在您已了解決策API的基本知識，您可以繼續特定操作：

* [建立決定項目](decisions-items/create.md)
* [列出決定專案](decisions-items/decision-items-list.md)
* [建立選擇策略](selection-strategies/create.md)
* [建立適用性規則](eligibility-rules/create.md)

如需有關在行銷活動和歷程中使用決策的詳細資訊，請參閱[決策檔案](../gs-experience-decisioning.md)。
