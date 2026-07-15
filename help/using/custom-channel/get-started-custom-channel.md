---
title: 開始使用自訂頻道
description: 瞭解如何使用 [!DNL Journey Optimizer]'s Channel Builder to bring any outbound messaging channel into [!DNL Journey Optimizer] 並將其用於行銷活動、歷程及協調的行銷活動。
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
badge: label="有限可用性" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---


# 開始使用自訂頻道 {#get-started-custom-channel}

>[!AVAILABILITY]
>
>此功能為有限可用性。 請聯絡您的 Adobe 代表以取得存取權。

<!--Multilingual support, business rules enforcement, and [!DNL Adobe Experience Decisioning] integration are planned for a future release.-->

[!DNL Journey Optimizer]的&#x200B;**自訂管道**&#x200B;功能可讓您將任何傳出管道匯入[!DNL Journey Optimizer]，以便用於行銷活動、歷程及協調的行銷活動，就像任何原生管道一樣。 使用&#x200B;**頻道產生器**，管理員可以建立及設定新的頻道，而不需要工程部門的介入，行銷人員可以立即開始使用這些頻道與客戶通訊。

## 它可解決什麼問題？ {#why-custom-channels}

[!DNL Journey Optimizer]原生支援電子郵件、簡訊、推播通知、WhatsApp、LINE和其他頻道。 不過，許多組織使用的傳訊平台並非原生整合（例如WeChat、Kakao Talk、Messenger或外部提供者），且想要在[!DNL Journey Optimizer]中使用這些平台進行協調與行銷活動建立，同時仍由自己的供應商提供。

<!--TBC: Another use case is when organizations have a legacy messaging gateway that exposes an HTTP endpoint, and they want to use it in [!DNL Journey Optimizer] without having to build a custom integration.-->

自訂通道填補此空白：可讓您使用任何輸出HTTP端點作為完整[!DNL Journey Optimizer]通道，解除鎖定：

* **完整通道功能** — 最佳化（內容實驗和鎖定）、OOTB報告和監控、同意和治理執行，以及運算式片段。<!--Multilingual and business rules are planned for a future release.-->
* **整合式協調流程** — 在單一位置管理您的所有傳訊通道，無論基礎的傳遞提供者為何。
* **無程式碼設定** — 管理員透過Channel Builder UI設定頻道；不需要自訂程式碼或工程作業。

## 自訂管道與自訂動作 {#custom-channel-vs-custom-action}

如果您之前在[!DNL Journey Optimizer]歷程中使用過[自訂動作](../action/action.md)，自訂管道會處理一組不同的使用案例。

**當您需要透過[!DNL Journey Optimizer]未原生支援的平台（例如WeChat、Kakao Talk或自訂訊息閘道）傳送訊息給使用者時**，請使用自訂頻道。 行銷活動、歷程及協調的行銷活動皆提供自訂頻道，以及支援：

* 透過個人化編輯器完全個人化，類似於原生傳出頻道
* 視覺/表單裝載編輯器、預覽和校訂
* 內容實驗與定位
* OOTB報告與監控
* 多個API認證和通道設定
* RBAC/ABAC

自訂管道支援POST作為唯一的HTTP方法。

**當您需要從外部系統（例如客服中心、記錄平台或離線資料庫）擷取資料或推送資訊至外部系統（例如客服中心、記錄平台或離線資料庫）時，請使用自訂動作，作為歷程中的步驟。**&#x200B;自訂動作僅在歷程中可用，並支援GET、PUT和POST方法。

<!--
| | Custom Action | Custom Channel |
| --- | --- | --- |
| **Primary use case** | Retrieve data from or send information to external systems (call centers, offline systems, logging) | Send messages to end users through channels not natively supported in [!DNL Journey Optimizer] |
| **Available in** | Journeys only | Campaigns, journeys, and orchestrated campaigns |
| **Supported HTTP methods** | GET, PUT, POST | POST only |
| **Full personalization (PE)** | No | Yes, through the personalization editor, similar to native outbound channels |
| **Visual/form editor** | No | Yes |
| **Preview and proof** | No | Yes |
| **Content experimentation** | No | Yes |
| **Targeting** | No | Yes |
| **OOTB Reporting** | Yes | Yes |
| **Multiple API credentials and channel configurations** | No | Yes |
| **RBAC/ABAC** | No | Yes |
-->

>[!TIP]
>
>一般建議是使用自訂通道，在傳送訊息給使用者的通道使用案例中。 對於歷程中所需的其他聯結器類使用案例（例如擷取資料或觸發外部系統），您可以繼續使用自訂動作。

## 使用案例 {#use-cases}

自訂管道適用於以下情況：

* **不支援的訊息平台** — 沒有原生[!DNL Journey Optimizer]管道的WeChat、Kakao Talk、Messenger、Telegram或地區訊息服務等管道。
* **自訂傳遞提供者** — 已投資外部提供者的組織，他們想要繼續使用傳送訊息的郵件，但偏好利用[!DNL Journey Optimizer]進行協調、個人化和行銷活動管理。
* **舊版管道** — 公開HTTP端點的專有或舊版傳訊閘道。
* **特定產業管道** — 醫療保健、銀行警示系統或政府通知服務的安全訊息。

## 運作方式 {#how-it-works}

設定和使用自訂管道會遵循以下主要階段：

1. **設定** （管理員） — 管理員會在&#x200B;**頻道產生器**&#x200B;中建立自訂頻道，定義端點、驗證、節流原則及訊息裝載結構。 接著會建立管道設定並連結至自訂管道。 [了解更多](configure-custom-channel.md)
1. **建立** （行銷人員） — 行銷人員將自訂管道新增至歷程、行銷活動或精心安排的行銷活動，選取管道設定，並使用[!DNL Journey Optimizer]的個人化編輯器編寫訊息裝載。 [了解更多](create-custom-experience.md)
1. **傳送** — 當設定檔符合資格時，[!DNL Journey Optimizer]會將個人化裝載傳送至設定的端點。 外部系統處理呼叫並傳遞訊息。
1. **監視** （管理員/行銷人員） — 管理員和行銷人員可以透過[!DNL Journey Optimizer]的報告和監視儀表板來監視自訂頻道的效能和可靠性。 [了解更多](monitor-custom-channel.md)

<!--
## Next steps {#next-steps}

* Review the prerequisites and permissions before setting up your first custom channel. [Learn more](custom-channel-prerequisites.md)
* Configure your first custom channel using the Channel Builder. [Learn more](custom-channel-configuration.md)
* Create a custom channel experience in a journey or campaign. [Learn more](create-custom-experience.md)
-->
