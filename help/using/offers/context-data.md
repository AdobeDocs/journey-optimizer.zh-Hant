---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 開始使用內容資料
description: 瞭解如何在決策管理中運用內容資料。
badge: label="舊版" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 4e736f9d-0f05-4a79-8ebf-ea22517d78a9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/aVm2FFqkJWN-k1qngYsp94FgKIZWaLCMUneFd0rVNpA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 12%

---

# 開始使用內容資料 {#context-data}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！ [了解更多](../experience-decisioning/gs-experience-decisioning.md)

作為決策請求的一部分傳送的資料被視為內容資料。 例如，您可以在決定引擎中運用內容資料，以設計決定規則，要求作出決定請求時目前的天氣為≥80度。

內容資料的定義在&#x200B;**決策**&#x200B;和&#x200B;**Edge決策** API要求之間有所不同。 對於這兩種型別的請求，內容資料可用於適用性規則或排名公式，但只有Edge Decisioning API請求可以使用內容資料來個人化內容。

開始之前，請檢查下列護欄和限制：

* 由於在決策呼叫和Edge決策呼叫之間傳遞上下文的方式不同，上下文型適用規則和排名公式在決策呼叫和Edge決策呼叫之間不可互換。
* 只有使用決策API才能使用`dryrun`引數進行測試。 Edge Decisioning API不提供此功能。 請注意，使用決策API將此引數設為`true`並不會影響上限和主張數量。

有關如何在每個API中使用內容資料的詳細資訊，請參閱下列章節：

* [在Edge Decisioning請求中使用內容資料](context-data-edge.md)
* [在決策請求中使用內容資料](context-data-decisioning.md)
