---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用行動訊息
description: 瞭解如何在Journey Optimizer中建立和傳送行動訊息
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
TQID: https://experienceleague.adobe.com/Ev0xJ86fpweQxgf-VjGUEl4ebk6BdzhVof2BgiMR9EM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c13ff12d-60f1-49cd-833a-d43359628223id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1006
ht-degree: 24%

---

# 開始使用行動訊息 {#get-started-sms}

>[!IMPORTANT]
>
>如果您是第一次建立行動訊息，請確定行動訊息通道已設定。 [了解更多](mobile-configuration.md)

使用[!DNL Journey Optimizer]透過單一SMS/MMS/RCS編輯器，透過三個通道（**SMS**、**MMS**&#x200B;和&#x200B;**RCS**）將行動訊息傳送給您的客戶，您可以在其中建立、個人化和預覽您的內容。

* **SMS （短訊息服務）**：傳送最多160個字元的純文字訊息，所有行動裝置均支援。
* **MMS （多媒體訊息服務）**：使用影像、視訊、音訊片段和GIF，加上最多1,600個字元的文字，豐富您的訊息。 [深入瞭解 MMS 限制](../start/guardrails.md#sms-guardrails)
* **RCS （豐富通訊服務）**:Deliver&#x200B;品牌化的互動式內容，直接在客戶的原生訊息應用程式中，不需要額外下載應用程式。

行動訊息可在歷程或行銷活動中使用行動訊息動作來建立和傳送：

* 在&#x200B;**歷程**&#x200B;中：新增行動訊息動作至您的歷程，定義基本設定，然後在右側的「行動訊息動作」窗格中撰寫您的內容。 [了解如何建立歷程](../building-journeys/journey-gs.md)

* 在&#x200B;**行銷活動**:Create&#x200B;行銷活動中，選取行動訊息作為您的動作，定義基本設定，然後編輯訊息內容。 了解如何建立[動作行銷活動](../campaigns/campaign-action.md#action-campaign-action) | [API 觸發的行銷活動](../campaigns/api-triggered-campaigns.md) | [協調的行銷活動](../orchestrated/create-orchestrated-campaign.md#create)


## 主要功能 {#key-features}

| 功能 | 說明 |
|---|---|
| **個人化** | 使用個人化編輯器，以設定檔屬性、條件式內容和動態資料量身打造訊息。 [了解更多](../personalization/personalize.md) |
| **提供者支援** | 透過API整合與[Sinch](mobile-configuration-sinch.md)、[Twilio](mobile-configuration-twilio.md)、[Infobip](mobile-configuration-infobip.md)或任何[自訂提供者](mobile-configuration-custom.md)連線。 |
| **URL縮短時間** | 新增可追蹤的縮短URL以監控參與度。 需要子網域設定。 [了解更多](mobile-subdomains.md) |
| **選擇退出管理** | 內建處理標準選擇退出關鍵字（STOP、QUIT、CANCEL等） 適用於Sinch和Infobip。 [了解更多](mobile-opt-out.md) |
| **預覽和測試** | 在傳送之前，使用測試設定檔和範例資料驗證內容。 [了解更多](send-mobile-message.md) |
| **報告** | 使用專用的[行銷活動報告](../reports/campaign-global-report-cja-sms.md)和[歷程報告](../reports/journey-global-report-cja-sms.md)追蹤行銷活動和歷程績效。 |

## 設定要求 {#configuration-requirements}

在傳送行動裝置訊息之前，您必須：

1. **選擇簡訊提供者**：從Sinch、Twilio、Infobip中選取，或設定自訂提供者
2. **設定API認證**：將您提供者的API權杖和服務ID與Journey Optimizer整合
3. **建立頻道設定**：設定行銷和異動訊息的SMS設定
4. **設定子網域（選擇性）**：只有在您打算在郵件中使用URL縮短時才需要

這些設定步驟通常由系統管理員執行。 [簡訊設定快速入門](mobile-configuration.md)

### RCS的需求 {#requirement-rcs}

在Journey Optimizer中使用RCS需要下列先決條件：

* **Sinch RCS API認證**：管理員必須設定Sinch RCS廠商的API認證（專案識別碼、應用程式識別碼和API權杖）。 [了解更多](mobile-configuration-sinch.md)
* **行動訊息通道設定**：管理員必須建立通道設定，並選取啟用RCS的認證，因此訊息會以RCS傳遞，而非SMS。 [了解更多](mobile-configuration.md)
* **遞補簡訊**：強烈建議。 裝置不支援RCS的收件者將不會收到訊息，除非SMS備援可用。 沒有現有SMS流量的客戶應購買SMS和短程式碼。 [了解更多](design-mobile.md#rcs-content)
* **支援的廠商**：原生RCS編寫需要Sinch RCS （Adobe轉售或直接）。 Twilio、Infobip和其他提供者必須使用自訂提供者整合。
* **裝置支援**： Android和iOS裝置支援RCS傳遞。 電信業者和地區可用性不盡相同，RCS無法在全球範圍內普遍使用。

## 其他資源 {#additional-resources}

瀏覽下列主題，進一步瞭解Journey Optimizer中的行動裝置傳訊。

+++設定指南

了解如何設定簡訊環境：

* [簡訊管道設定概觀](mobile-configuration.md)
* [建立簡訊管道設定](mobile-configuration-surface.md)
* [設定簡訊子網域以縮短 URL](mobile-subdomains.md)

+++

+++提供者設定指南

各個簡訊服務提供者的逐步設定：

* [設定 Sinch 提供者](mobile-configuration-sinch.md)
* [設定 Twilio 提供者](mobile-configuration-twilio.md)
* [設定 Infobip 提供者](mobile-configuration-infobip.md)
* [設定自訂簡訊提供者](mobile-configuration-custom.md)

+++

+++內容建立與管理

建立、個人化及管理您的行動訊息內容：

* [建立SMS/RCS/MMS訊息](create-mobile-message.md)
* [預覽、測試和傳送訊息](send-mobile-message.md)
* [行動訊息中的Personalization](../personalization/personalize.md)
* [動態內容](../personalization/get-started-dynamic-content.md)
* [使用 AI 助理產生簡訊內容](../content-management/generative-text.md)

+++

+++合規性與隱私權

確保您的行動通訊符合法規與隱私權標準：

* [選擇退出管理](mobile-opt-out.md)
* [隱私權與同意](../privacy/opt-out.md#opt-out-decision-management)

+++

+++績效追蹤

監視和分析您的簡訊行銷活動和歷程績效：

* [簡訊行銷活動報告](../reports/campaign-global-report-cja-sms.md)
* [簡訊歷程報告](../reports/journey-global-report-cja-sms.md)

+++

+++歷程與行銷活動整合

瞭解如何將簡訊整合至您的客戶歷程與行銷活動中：

* [將簡訊新增至歷程](../building-journeys/journey-action.md)
* [建立簡訊行銷活動](../campaigns/create-campaign.md)

+++

+++RCS常見問題

**Twilio或Infobip是否提供原生RCS訊息？**

不會。 使用協力廠商SMS提供者（例如Twilio或Infobip）時，無法使用Journey Optimizer中的原生RCS設計工具。 不過，RCS訊息可以透過[自訂提供者整合](mobile-configuration-custom.md)傳送。

**為何要與RCS一起購買簡訊？**

應購買SMS音量和短程式碼以啟用SMS遞補，這是建議的路徑。 如果未設定SMS，其裝置或電信業者不支援RCS的設定檔將不會收到訊息。

**Sinch直接客戶是否可以使用原生RCS訊息？**

可以。 使用Sinch的Conversational API的客戶可以存取原生RCS編寫，包括Adobe轉售和Sinch直接客戶。

**RCS是否隨處可用？**

不會。 全球電信業者的採用率持續增長，但RCS並非在所有電信業者和地區都受到普遍支援。 規劃RCS行銷活動時，應研究地區可用性與電信業者支援。

**RCS訊息在裝置上的顯示位置？**

RCS訊息會出現在與標準SMS訊息相同的位置 — 在裝置的原生訊息應用程式中。 他們從品牌化、經過驗證的寄件者送達，給予收件者信任訊號，以瞭解訊息是否合法。

**RCS訊息的字元限製為何？**

多媒體（單一）訊息型別支援最多3,072個字元，遠遠超過標準SMS的160個字元限制。 基本RCS訊息型別限製為160個字元，符合標準SMS限制。

+++

## 作法影片 {#videos}

**設定並傳送簡訊**

瞭解如何設定、編寫並將簡訊納入您的客戶歷程中。

+++收看影片

>[!VIDEO](https://video.tv.adobe.com/v/3420509?learn=on)

+++

**探索行動傳訊功能**

探索 Adobe Journey Optimizer 為行銷人員提供的全方位行動傳訊功能。

+++收看影片

>[!VIDEO](https://video.tv.adobe.com/v/3426021?quality=12&learn=on)

+++

**傳送品牌 RCS 訊息**

了解如何使用自訂簡訊提供者在 Adobe Journey Optimizer 中設定並傳送品牌化互動式 RCS 訊息。

+++收看影片

>[!VIDEO](https://video.tv.adobe.com/v/3464755)

+++
