---
product: experience platform
solution: Experience Platform
title: 開始使用內容資料
description: 瞭解如何在決策管理中運用內容資料。
badge: label="舊版" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 4e736f9d-0f05-4a79-8ebf-ea22517d78a9
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 5%

---

# 開始使用內容資料 {#context-data}

作為決策請求的一部分傳送的資料被視為內容資料。 例如，您可以在決定引擎中運用內容資料，以設計決定規則，要求作出決定請求時目前的天氣為≥80度。

內容資料的定義在&#x200B;**決策**&#x200B;和&#x200B;**Edge決策** API要求之間有所不同。 對於這兩種型別的請求，內容資料可用於適用性規則或排名公式，但只有Edge Decisioning API請求可以使用內容資料來個人化內容。

開始之前，請檢查下列護欄和限制：

* 由於在決策呼叫和Edge決策呼叫之間傳遞上下文的方式不同，上下文型適用規則和排名公式在決策呼叫和Edge決策呼叫之間不可互換。
* 只有使用決策API才能使用`dryrun`引數進行測試。 Edge Decisioning API不提供此功能。 請注意，使用決策API將此引數設為`true`並不會影響上限和主張數量。

有關如何在每個API中使用內容資料的詳細資訊，請參閱下列章節：

* [在Edge Decisioning請求中使用內容資料](context-data-edge.md)
* [在決策請求中使用內容資料](context-data-decisioning.md)
