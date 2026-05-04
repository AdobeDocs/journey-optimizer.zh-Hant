---
solution: Journey Optimizer
product: journey optimizer
title: 廠商整合
description: 搭配任何公開有效API的外部平台使用Adobe Journey Optimizer整合，加上經過工程測試的供應商模式，讓您在設計設定時獲得信賴度。
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: 整合，廠商，協力廠商
source-git-commit: 4cc3c959fe08c1d574a5d041bf7721441bc96f97
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---


# 廠商整合 {#vendor-integration}

當每個系統公開適合您使用案例的&#x200B;**API端點**，且與整合如何發出要求及使用回應相容時，您可以在Adobe Journey Optimizer中使用&#x200B;**整合**，透過HTTP **呼叫**&#x200B;外部系統。 如需完整的工作流程，請參閱[使用整合](integrations.md)。

所描述的協力廠商解決方案清單是說明性的，並非詳盡無遺。 在滿足產品需求時，也可以使用其他平台。

## 作業護欄 {#operational-guardrails}

當您在本指南或類似廠商中設定任何整合時，請套用下列內容：

* **回應格式：**&#x200B;整合對應來自&#x200B;**JSON**&#x200B;或&#x200B;**HTML**&#x200B;回應的欄位。 設計呼叫，讓API傳回JSON或HTML （適合在編寫時對應）。
* **承載與欄位：**&#x200B;僅要求與對應您需要的屬性。 較小的回應可減少延遲，並限制敏感資料的曝光。
* **端點形狀：**&#x200B;當產品預期目標查閱時，偏好使用穩定、**單一資源**&#x200B;擷取（例如一個專案、產品或成員）而非廣泛清單或分頁端點。 請參閱[限制和排除](#limitations-exclusions)和[使用整合](integrations.md)。
* **磁碟區和可靠性：**&#x200B;遵守廠商的&#x200B;**速率限制**。 為您的管道設定&#x200B;**逾時**、**重試**&#x200B;和&#x200B;**快取**&#x200B;原則（例如批次電子郵件與異動傳送），並在載入下驗證。
* **安全性：**&#x200B;根據您組織的原則儲存和輪換權杖、API金鑰和OAuth認證。 請勿在訊息內容中內嵌秘密。


## 限制和排除 {#limitations-exclusions}

協力廠商解決方案清單是&#x200B;**說明性的**，並非詳盡無遺。 廠商API、主機、速率限制，以及JSON或HTML回應形狀可能會有所變更。 使用供應商的目前檔案和您的訂閱確認端點、驗證和欄位對應。 這裡的模式假設&#x200B;**讀取導向**&#x200B;呼叫適合個人化。 整合僅支援來自&#x200B;**JSON**&#x200B;和&#x200B;**HTML**&#x200B;回應的對應。 不支援&#x200B;**回寫**、**批次匯出**&#x200B;以及任何其他格式的回應。

## 快速導覽 {#quick-navigation}

使用這些群組連結來快速跳至相關的廠商模式：

* **內容管理系統：** [內容](vendor-integration.md#contentful)，[Sitecore](vendor-integration.md#sitecore)，[Salsify](vendor-integration.md#salsify)，[內容棧疊](vendor-integration.md#contentstack)，[Akeneo](vendor-integration.md#akeneo)，[Magnolia](vendor-integration.md#magnolia)
* **忠誠度與獎勵：** [Voucherify](vendor-integration.md#voucherify)，[Talon.One](vendor-integration.md#talon-one)，[Antavo](vendor-integration.md#antavo)，[Salesforce忠誠度](vendor-integration.md#salesforce-loyalty)，[毛細管](vendor-integration.md#capillary)
* **範本、個人化和建議：** [Stensul](vendor-integration.md#stensul)，[Marigold](vendor-integration.md#marigold)，[Adobe Target建議](vendor-integration.md#adobe-target-recommendations)
* **資料、天氣和作業：** [AccuWeather](vendor-integration.md#accuweather)，[ShipStation](vendor-integration.md#shipstation)，[RevenueCat](vendor-integration.md#revenuecat)，[Databricks](vendor-integration.md#databricks)
* **評論、同意和社交：** [Bynder](vendor-integration.md#bynder)，[Trustpilot](vendor-integration.md#trustpilot)，[Bazaarvoice](vendor-integration.md#bazaarvoice)，[OneTrust](vendor-integration.md#onetrust)，[Meta](vendor-integration.md#meta)，[Aprimo](vendor-integration.md#aprimo)，[Epsilon (Epsilon3)](vendor-integration.md#epsilon)
