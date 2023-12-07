---
title: 開始使用 Experience Decisioning
description: 進一步瞭解體驗決策
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 7%

---

# 開始使用 Experience Decisioning {#get-started-experience-decisioning}

>[!BEGINSHADEBOX 「本檔案指南提供哪些內容」]

* **[開始使用體驗決策](gs-experience-decisioning.md)**
* 管理您的決定專案： [設定專案目錄](catalogs.md) - [建立決定專案](items.md) - [管理專案集合](collections.md)
* 設定專案的選取範圍： [建立決定規則](rules.md) - [建立排名方法](ranking.md)
* [建立選擇策略](selection-strategies.md)
* [建立決定原則](create-decision.md)

>[!ENDSHADEBOX]

## 什麼是Experience Decisioning {#about}

>[!AVAILABILITY]
>
>體驗決策功能目前僅供特定使用者測試版。 若要加入 Beta 版計畫，請連絡 Adobe 客戶服務。

Experience Decisioning透過提供稱為「決策專案」的行銷優惠集中目錄和複雜的決策引擎，簡化了個人化。 此引擎運用規則和排名條件來選取最相關的決定專案，並將之呈現給每個人。

這些決策專案透過新的程式碼型體驗管道(現在可在Journey Optimizer促銷活動中存取)無縫整合到廣泛的傳入介面。

**限制：**

* 決定原則僅適用於程式碼型體驗行銷活動。
* 目前，Experience Decisioning不提供頻率上限。

## 體驗決策關鍵步驟 {#steps}

使用Experience Decisioning的主要步驟如下：

1. **設定自訂屬性**：將自訂屬性設定至目錄的結構描述中，以根據您的特定需求量身打造決定專案的目錄。

1. **建立決定專案** 以向您的目標對象顯示。

1. **使用集合組織**：使用集合根據屬性型規則將決策專案分類。 將集合併入您的選擇策略，以決定應考慮的決定專案集合。

1. **建立決定規則**：決定規則用於決定專案和/或選擇策略中，以決定可向誰顯示決定專案。

1. **實作排名方法**：建立排名方法並在決定策略中套用，以決定選取決定專案的優先順序。

1. **建立選取策略**：建立選擇策略，運用集合、決定規則和排名方法，以識別適合顯示給設定檔的決定專案。

1. **將決定原則內嵌至程式碼型行銷活動中**：決定原則會結合多個選取策略，以決定要向預期對象顯示的合格決定專案。
