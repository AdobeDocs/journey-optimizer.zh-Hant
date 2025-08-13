---
solution: Journey Optimizer
product: Journey Optimizer
title: 委派電子郵件子網域
description: 委派電子郵件子網域
redpen-status: CREATED_||_2025-08-11_21-07-51
source-git-commit: 5a8ef88cba254241933607ca59156d35e0e92926
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 3%

---


# 委派電子郵件子網域{#section-overview}

在Adobe Journey Optimizer中委派電子郵件子網域可讓管理員改善電子郵件傳遞能力、保護網域信譽，並簡化行銷活動管理。 透過設定子網域，您可以隔離不同型別的電子郵件流量，例如行銷和異動訊息，同時確保符合業界標準。 本節會介紹主要設定方法（例如完全委派和CNAME設定），並探討這些方法在工作量和控制方面的差異。 您還將學習如何管理基本DNS記錄(如DMARC和PTR)、透過Google TXT記錄增強Gmail傳遞能力，以及使用IP集區分組IP。 無論您是要最佳化安全性或聲譽，本指南都能讓程式可接近且有效。

## 委派電子郵件子網域

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

開始使用子網域委派

瞭解在Adobe Journey Optimizer中委派子網域的優點、設定方法和考量事項。

[開始委派子網域](../using/configuration/about-subdomain-delegation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

委派子網域

將子網域委派至Adobe的逐步指引，包括完全委派和CNAME設定。

[瞭解如何委派](../using/configuration/delegate-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

設定DMARC記錄

設定DMARC記錄，以增強委派子網域的電子郵件安全性和傳遞能力。

[立即設定DMARC](../using/configuration/dmarc-record.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

新增Google TXT記錄

在Adobe Journey Optimizer中新增Google TXT記錄，驗證Gmail傳遞能力的子網域。

[新增Google TXT記錄](../using/configuration/google-txt.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

存取和編輯PTR記錄

管理委派子網域的PTR記錄，包括編輯和瞭解更新狀態。

[編輯PTR記錄](../using/configuration/ptr-records.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

建立IP集區

群組IP位址可改善電子郵件傳遞能力，並有效管理子網域信譽。

[建立IP集區](../using/configuration/ip-pools.md)
:::

::::
