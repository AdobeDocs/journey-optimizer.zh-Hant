---
solution: Journey Optimizer
product: journey optimizer
title: 廠商整合
description: 搭配任何公開有效API的外部平台使用Adobe Journey Optimizer整合，加上經過工程測試的供應商模式，讓您在設計設定時獲得信賴度。
feature: Integrations
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: 整合，廠商，協力廠商
source-git-commit: 3733c9ab401f85b22e1d6e07dbf4db535ff8a96d
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 1%

---


# 開始使用廠商整合 {#vendor-integration}

>[!BEGINSHADEBOX]

目錄：

* [使用整合](external-sources.md)
* **[開始使用廠商整合](vendor-integration-gs.md)**
* [可用的廠商](vendor-integration.md)
* [常見問題集](vendor-integration-faq.md)

>[!ENDSHADEBOX]

當每個系統公開適合您使用案例的&#x200B;**API端點**，且與整合如何發出要求及使用回應相容時，您可以在Adobe Journey Optimizer中使用&#x200B;**整合**，透過HTTP **呼叫**&#x200B;外部系統。 如需完整的工作流程，請參閱[使用整合](external-sources.md)。

所描述的協力廠商解決方案清單是說明性的，並非詳盡無遺。 在滿足產品需求時，也可以使用其他平台。

## 作業護欄 {#operational-guardrails}

當您在本指南或類似廠商中設定任何整合時，請套用下列內容：

* **回應格式：**&#x200B;整合從&#x200B;**JSON**&#x200B;回應對應欄位。 設計呼叫，讓API傳回適合編寫時對映的JSON。
* **承載與欄位：**&#x200B;僅要求與對應您需要的屬性。 較小的回應可減少延遲，並限制敏感資料的曝光。
* **端點形狀：**&#x200B;當產品預期目標查閱時，偏好使用穩定、**單一資源**&#x200B;擷取（例如一個專案、產品或成員）而非廣泛清單或分頁端點。 請參閱[限制和排除](#limitations-exclusions)和[使用整合](external-sources.md)。
* **磁碟區和可靠性：**&#x200B;遵守廠商的&#x200B;**速率限制**。 為您的管道設定&#x200B;**逾時**、**重試**&#x200B;和&#x200B;**快取**&#x200B;原則（例如批次電子郵件與異動傳送），並在載入下驗證。
* **安全性：**&#x200B;根據您組織的原則儲存和輪換權杖、API金鑰和OAuth認證。 請勿在訊息內容中內嵌秘密。

## 限制和排除 {#limitations-exclusions}

協力廠商解決方案清單是&#x200B;**說明性的**，並非詳盡無遺。 廠商API、主機、速率限制和JSON回應形狀可能會變更。 使用供應商的目前檔案和您的訂閱確認端點、驗證和欄位對應。 這裡的模式假設&#x200B;**讀取導向**&#x200B;呼叫適合個人化。 除非另有註明，否則回寫、批次匯出或非JSON回應可能不在範圍內。

## 快速導覽 {#quick-navigation}

使用這些群組連結來快速跳至相關的廠商模式：

* **內容與CMS：** [內容](#contentful)，[Sitecore](#sitecore)，[Salsify](#salsify)，[內容棧疊](#contentstack)，[Akeneo](#akeneo)，[Magnolia](#magnolia)
* **忠誠度與獎勵：** [Voucherify](#voucherify)，[Talon.One](#talon-one)，[Antavo](#antavo)，[Salesforce忠誠度](#salesforce-loyalty)，[毛細管](#capillary)
* **範本和傳訊：** [Stensul](#stensul)，[Marigold](#marigold)，[Adobe Target建議](#adobe-target-recommendations)
* **資料、天氣和作業：** [AccuWeather](#accuweather)，[ShipStation](#shipstation)，[RevenueCat](#revenuecat)，[Databricks](#databricks)
* **評論、同意和社交：** [Bynder](#bynder)，[Trustpilot](#trustpilot)，[Bazaarvoice](#bazaarvoice)，[OneTrust](#onetrust)，[Meta](#meta)，[Aprimo](#aprimo)，[Epsilon (Epsilon3)](#epsilon)
