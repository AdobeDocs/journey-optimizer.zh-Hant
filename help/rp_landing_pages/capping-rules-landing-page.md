---
solution: Journey Optimizer
product: Journey Optimizer
title: 設定訊息和歷程上限規則
description: 設定訊息和歷程上限規則
redpen-status: CREATED_||_2025-08-11_20-28-34
exl-id: 630e252a-aab2-4a27-ad46-d4dbfbc3f3a4
source-git-commit: 9e23162373564e7866af115ee2cd706527336e4a
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 38%

---

# 設定訊息和歷程上限規則{#section-overview}

上限規則是[衝突管理與優先順序](../using/conflict-prioritization/gs-conflict-prioritization.md)的一部分 — 它們有助於確保客戶獲得適當的通訊量，而不會感到不知所措。 在套用規則之前，請使用[衝突偵測工具](../using/conflict-prioritization/conflicts.md)來識別重疊的歷程與行銷活動。 當多個通訊符合約一個設定檔的資格時，[優先順序分數](../using/conflict-prioritization/priority-scores.md)會決定哪個訊息會先傳遞。

您可以設定傳送訊息的頻率（頻率上限）、設定檔可以進入的歷程數（歷程上限）以及訊息封鎖的時間（無訊息時數）限制。 規則會分組到&#x200B;**規則集**&#x200B;並套用至行銷活動或歷程。 如需外部系統的程式化控制，請參閱[上限API](../using/configuration/capping.md)。

## 設定訊息和歷程上限規則

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

使用規則集

了解如何建立、管理和啟用規則集，以控制 Adobe Journey Optimizer 中的訊息頻率和歷程進入規則。

[探索規則集](../using/conflict-prioritization/rule-sets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

歷程上限與仲裁

了解如何設定歷程進入和並行上限、排定歷程的優先順序，以及監視排除項目以防止通訊過載。

[了解歷程上限](../using/conflict-prioritization/journey-capping.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

依據管道的頻率限定

了解如何建立並套用管道專屬頻率上限規則，以最佳化訊息傳送並避免過度通訊。

[設定頻率限定](../using/conflict-prioritization/channel-capping.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg)

設定無訊息時數

定義以時間為基礎的電子郵件、簡訊、推播和WhatsApp排除專案，以便在特定期間不會傳送任何訊息，考量客戶偏好和法規遵循。

[設定勿打擾時間](../using/conflict-prioritization/quiet-hours.md)
:::

::::

## 其他資源

- **[開始衝突管理與優先順序](../using/conflict-prioritization/gs-conflict-prioritization.md)** — 衝突偵測、優先順序分數和規則集概觀。
- **[識別潛在衝突](../using/conflict-prioritization/conflicts.md)** — 在套用上限規則之前偵測重疊的歷程和行銷活動。
- **[指派優先順序分數](../using/conflict-prioritization/priority-scores.md)** — 控制當設定檔符合多個通訊的資格時，哪個歷程或行銷活動優先。
