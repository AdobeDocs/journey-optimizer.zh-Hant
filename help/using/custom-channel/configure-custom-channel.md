---
title: 設定自訂頻道 — 概觀
description: 瞭解管理員在Adobe Journey Optimizer中設定自訂頻道時必須完成的步驟，從建立頻道到設定頻道設定。
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="有限可用性" type="Informative"
source-git-commit: 4556e8b50fe71cf9d703d034a3c5772b8fea9d33
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 9%

---


# 設定自訂頻道 {#custom-channel-configuration}

>[!AVAILABILITY]
>
>此功能為有限可用性。 請聯絡您的 Adobe 代表以取得存取權。

設定自訂頻道是管理員工作，每個頻道發生一次。 設定頻道後，行銷人員可以立即在行銷活動、歷程和協調行銷活動中選取它，就像任何原生[!DNL Journey Optimizer]頻道一樣。

設定程式包含四個步驟：定義管道本身（端點、驗證、裝載）、管理用於驗證請求的API認證、選擇性地委派子網域以進行連結追蹤，以及最終建立行銷人員將在編寫時選取的管道設定。

>[!NOTE]
>
>開始之前，請檢閱自訂通道的先決條件和護欄，包括所需的許可權和支援的驗證方法。

## 設定步驟 {#steps}

自訂頻道的設定程式包含四個步驟。 以下連結的文章會詳細說明每個步驟。

| 步驟 | 您所做的工作 | 為何這項能力很重要 | 連結 |
| --- | --- | --- | --- |
| **1. 建立自訂頻道** | 在Channel Builder中定義端點URL、標頭、節流原則、驗證型別和訊息裝載結構。 | 這是管道的核心定義。 它會告訴[!DNL Journey Optimizer]如何傳送訊息以及該訊息的外觀。 | [了解更多](create-custom-channel.md) |
| **2. 管理API認證** | 建立並管理用來驗證端點之要求的認證集。 | 透過多個認證集，您可在不同品牌或環境中重複使用相同的管道定義，且不會複製管道。 | [了解更多](custom-channel-api-credentials.md) |
| **3. 委派子網域** *（選擇性）* | 委派專為您自訂頻道使用的子網域。 | 只有在您的訊息裝載包含可追蹤連結時才需要。 如果沒有委派的子網域，此管道將無法使用連結追蹤。 | [了解更多](custom-channel-subdomains.md) |
| **4. 建立頻道設定** | 建立具名預設集，將自訂頻道連結至特定憑證、子網域和選用裝載預設值。 | 建立行銷活動或歷程時，行銷人員會選取自訂管道和相關聯的管道設定。 您可以為相同管道建立多個設定（例如，每個品牌或地區一個設定）。 | [了解更多](custom-channel-configuration.md) |

<!--
## Get started {#get-started}

1. [Create the custom channel](create-custom-channel.md) by defining its endpoint, authentication method, and message payload structure in the Channel Builder.
1. [Set up API credentials](custom-channel-api-credentials.md) to authenticate requests sent to your endpoint — required for all authentication types other than **None**.
1. [Delegate a subdomain](custom-channel-subdomains.md) if your message payload includes trackable links and you want them served from a branded domain.
1. [Create a channel configuration](custom-channel-configuration.md) to produce the named preset that marketers will select when building campaigns and journeys.


-->