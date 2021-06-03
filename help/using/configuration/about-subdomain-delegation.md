---
title: 委派子網域
description: 了解如何委派子網域
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: da995c56b59fb191934788c7aea9048123a2fe6d
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 43%

---


# 開始使用子網域委派

## 隔離您的品牌以保護您的聲譽

子網域是您網域的分區，可用來隔離您的名稱或各類流量（交易訊息、行銷資訊等等）。讓我們以「mybrand.com」網域為例，這是個用來傳送交易和行銷通訊的網域。在此情況下，您可以決定設定兩個子網域：

* 「Info.mybrand.com」子網域用來進行交易通訊（購買確認函、密碼重設等等）；
* 「marketing.mybrand.com」子網域則用來傳送電子郵件給潛在客戶。

您可以藉此維護網域和其他子網域的信譽。舉例來說，如果「marketing.mybrand.com」子網域因傳遞能力不佳，而被網際網路服務提供者新增至封鎖清單，如此就能防止整個「mybrand.com」網域和「info.mybrand.com」子網域被新增至封鎖清單。

## 讓您的資源URL對客戶保持透明

實施解決方案時，對外部元件有以下要求：包括設定要追蹤的連結和網頁、顯示鏡像頁面等。

雖然這些需求是透過Adobe和客戶托管的元件來管理，但其中包含URL，可供電子郵件的收件者看到。 為避免有指出基礎技術解決方案或托管提供者的URL，您可以設定子網域，讓這對電子郵件的收件者透明。 [深入了解網域委派](https://helpx.adobe.com/tw/campaign/kb/domain-name-delegation.html)。

## Journey Optimizer中的子網域委派

Journey Optimizer提供數項功能，可協助您管理子網域：

* [直接從介](delegate-subdomain.md) 面委派子網域，
* [將Google TXT記錄](google-txt.md) 新增至您的子網域，以確保電子郵件能成功傳送至Gmail地址、
* [訪問為子](ptr-records.md) 域生成的PTR記錄，允許通過發送郵件伺服器來驗證這些記錄。
