---
solution: Journey Optimizer
product: Journey Optimizer
title: 委派電子郵件子網域
description: 委派電子郵件子網域
redpen-status: CREATED_||_2025-08-11_21-07-51
exl-id: 7df9b8e2-136a-4ffc-9243-53c7be026d81
source-git-commit: bb50d06e86f9399dfd295b8091aa637abcaea4a8
workflow-type: ht
source-wordcount: '390'
ht-degree: 100%

---

# 委派電子郵件子網域{#section-overview}

委派電子郵件子網域是[管道設定](../using/configuration/get-started-configuration.md)的核心步驟，您必須先完成，才能從 Journey Optimizer 傳送電子郵件。子網域可讓您隔離流量類型 (例如行銷與交易型)、保護主網域的聲譽，並加快 [IP 暖身](../using/configuration/ip-warmup-gs.md)的速度。它們可與[電子郵件管道設定](../using/email/get-started-email-config.md)和[傳遞能力監視](../using/reports/deliverability.md)搭配使用，以確保訊息可送達收件匣。

您可以從數個設定方法中選擇：**完整委派** (Adobe 管理 DNS)、**CNAME 設定**&#x200B;或&#x200B;**自訂委派** (您擁有憑證和 DNS)。如果您從 CNAME 開始，您可以稍後[移轉至自訂委派](../using/configuration/custom-subdomain-migration.md)，以實現更嚴格的安全性。本節也涵蓋 DMARC 和 PTR 記錄、Gmail 的 Google TXT 記錄以及 IP 集區。如需更廣泛的傳遞能力指引，請參閱[開始使用傳遞能力](../using/reports/deliverability.md)和[監視電子郵件地址](monitor-reputation-landing-page.md)。

## 委派電子郵件子網域

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

開始使用子網域委派

了解在 Adobe Journey Optimizer 中委派子網域的優點、設定方法和考量事項。

[開始委派子網域](../using/configuration/about-subdomain-delegation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

委派子網域

將子網域委派至 Adobe 的逐步指引，包括完全委派和 CNAME 設定。

[了解如何委派](../using/configuration/delegate-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/screwdriver-wrench.svg)

設定自訂子網域

透過自訂委派取得子網域的完整所有權，上傳您自己的 SSL 憑證並保持對網域設定的完整控制。

[設定自訂子網域](../using/configuration/delegate-custom-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

從 CNAME 移轉至自訂委派

將現有的 CNAME 設定子網域移轉至自訂委派，以符合安全性原則並獲得憑證的完整控制權。

[移轉您的子網域](../using/configuration/custom-subdomain-migration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

設定 DMARC 記錄

設定 DMARC 記錄，以增強委派子網域的電子郵件安全性和傳遞能力。

[立即設定 DMARC](../using/configuration/dmarc-record.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

新增 Google TXT 記錄

在 Adobe Journey Optimizer 中新增 Google TXT 記錄，驗證 Gmail 傳遞能力的子網域。

[新增 Google TXT 記錄](../using/configuration/google-txt.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

存取和編輯 PTR 記錄

管理委派子網域的 PTR 記錄，包括編輯和了解更新狀態。

[編輯 PTR 記錄](../using/configuration/ptr-records.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

建立 IP 集區

群組 IP 位址可改善電子郵件傳遞能力，並有效管理子網域信譽。

[建立 IP 集區](../using/configuration/ip-pools.md)
:::

::::

## 其他資源

- **[設定登陸頁面子網域](../using/landing-pages/lp-subdomains.md)** - 設定登陸頁面和訂閱表單的子網域。
- **[設定網頁子網域](../using/web/web-delegated-subdomains.md)** - 為網頁體驗和追蹤委派子網域。
- **[開始使用管道設定](../using/configuration/get-started-configuration.md)** - 所有管道設定步驟的概觀，包括子網域委派。
