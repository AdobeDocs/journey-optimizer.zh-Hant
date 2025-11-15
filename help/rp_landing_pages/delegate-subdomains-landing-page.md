---
solution: Journey Optimizer
product: Journey Optimizer
title: 委派電子郵件子網域
description: 委派電子郵件子網域
redpen-status: CREATED_||_2025-08-11_21-07-51
exl-id: 7df9b8e2-136a-4ffc-9243-53c7be026d81
source-git-commit: 2b907a3be8b11ac6308d0b563e122c88478d1d37
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 100%

---

# 委派電子郵件子網域{#section-overview}

在 Adobe Journey Optimizer 中委派電子郵件子網域可讓管理員改善電子郵件傳遞能力、保護網域信譽，並簡化行銷活動管理。透過設定子網域，您可以隔離不同類型的電子郵件流量，例如行銷和交易型訊息，同時確保符合業界標準。本節會介紹主要設定方法 (例如完全委派和 CNAME 設定)，並探討這些方法在工作量和控制方面的差異。您還將學習如何管理基本 DNS 記錄 (如 DMARC 和 PTR)、透過 Google TXT 記錄增強 Gmail 傳遞能力，以及使用 IP 集區將 IP 分組。無論您是要最佳化安全性還是聲譽，本指南都能讓流程方便使用且有效。

## 委派電子郵件子網域

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hant)

開始使用子網域委派

了解在 Adobe Journey Optimizer 中委派子網域的優點、設定方法和考量事項。

[開始委派子網域](../using/configuration/about-subdomain-delegation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hant)

委派子網域

將子網域委派至 Adobe 的逐步指引，包括完全委派和 CNAME 設定。

[了解如何委派](../using/configuration/delegate-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=zh-Hant)

設定 DMARC 記錄

設定 DMARC 記錄，以增強委派子網域的電子郵件安全性和傳遞能力。

[立即設定 DMARC](../using/configuration/dmarc-record.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hant)

新增 Google TXT 記錄

在 Adobe Journey Optimizer 中新增 Google TXT 記錄，驗證 Gmail 傳遞能力的子網域。

[新增 Google TXT 記錄](../using/configuration/google-txt.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hant)

存取和編輯 PTR 記錄

管理委派子網域的 PTR 記錄，包括編輯和了解更新狀態。

[編輯 PTR 記錄](../using/configuration/ptr-records.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=zh-Hant)

建立 IP 集區

群組 IP 位址可改善電子郵件傳遞能力，並有效管理子網域信譽。

[建立 IP 集區](../using/configuration/ip-pools.md)
:::

::::
