---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用文字訊息 (簡訊/MMS/RCS)
description: 了解如何在 Journey Optimizer 建立及傳送文字訊息
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
source-git-commit: 73a347c104fe28799c264f9a8b6c3e5e12c8d892
workflow-type: ht
source-wordcount: '825'
ht-degree: 100%

---

# 開始使用文字訊息 {#get-started-sms}

使用 [!DNL Journey Optimizer] 在客戶的行動裝置傳送文字訊息 (簡訊/MMS/RCS) 給客戶。您可以從簡訊/MMS/RCS 編輯器建立、個人化及預覽文字格式的訊息。

文字訊息可在歷程或行銷活動中建立和傳送。 對於簡訊、MMS 和 RCS，請使用簡訊動作。

* 在&#x200B;**歷程**&#x200B;中。建立歷程、新增簡訊活動及定義基本設定。然後，瀏覽到右側的「簡訊動作」窗格以建立簡訊、MMS 或 RCS 訊息的內容。[了解如何建立歷程](../building-journeys/journey-gs.md)

* 在&#x200B;**行銷活動**&#x200B;中。建立行銷活動後，請選取 [簡訊] 作為動作並定義基本設定。然後，編輯訊息內容以定義要傳送的簡訊、MMS 或 RCS 訊息。了解如何建立[動作行銷活動](../campaigns/campaign-action.md#action-campaign-action) | [API 觸發的行銷活動](../campaigns/api-triggered-campaigns.md) | [協調的行銷活動](../orchestrated/create-orchestrated-campaign.md#create)

>[!IMPORTANT]
>
>如果這是您第一次建立文字訊息，請確定已設定簡訊管道。[了解更多](sms-configuration.md)

## 文字訊息功能 {#sms-capabilities}

Adobe Journey Optimizer 提供全面的文字訊息功能，可跨多個管道與您的客戶互動：

**簡訊 (短訊息服務)**

傳送最多 160 個字元的純文字訊息。簡訊是所有行動裝置上支援最廣泛的文字訊息格式。

**MMS (多媒體訊息服務)**

透過多媒體內容 (包括影片、影像、音訊片段及 GIF) 增強您的通訊。除了媒體檔案外，MMS 訊息最多可允許 1600 個字元的文字。[深入瞭解 MMS 限制](../start/guardrails.md#sms-guardrails)

**RCS (進階通訊解決方案)**

使用進階功能 (例如輪播、豐富卡片、建議的動作和增強型媒體支援) 傳送品牌互動式訊息。RCS 在支援的裝置上提供更豐富的訊息傳送體驗。

## 主要功能 {#key-features}

**個人化和動態內容**

使用個人化編輯器建立個人化文字訊息。新增輪廓屬性、條件式內容和動態資料，量身打造傳送給個別收件者的訊息。[了解個人化](../personalization/personalize.md)

**多重提供者支援**

Adobe Journey Optimizer 與領先的簡訊服務提供者整合：

* **Sinch** - [設定指南](sms-configuration-sinch.md)
* **Twilio** - [設定指南](sms-configuration-twilio.md)
* **Infobip** - [設定指南](sms-configuration-infobip.md)
* **自訂提供者** - 使用自訂 API 整合來設定任何其他簡訊提供者。[了解更多](sms-configuration-custom.md)

**URL 縮短與追蹤**

在訊息中新增縮短的可追蹤 URL 以監視參與度。需要設定子網域才能使用 URL 縮短功能。[瞭解如何設定簡訊子網域](sms-subdomains.md)

**選擇退出管理**

透過內建的選擇退出管理，確保符合業界標準與法規。Journey Optimizer 會自動處理 Sinch 和 Infobip 提供者的標準選擇退出關鍵字 (停止、結束、取消等)。[瞭解選擇退出管理](sms-opt-out.md)

**預覽與測試**

使用測試輪廓和樣本資料進行傳送前，請先測試您的文字訊息。預覽個人化、內容和格式，以確保您的訊息正確顯示。[瞭解如何傳送訊息](send-sms.md)

**報告與分析**

透過全面的報告功能追蹤簡訊行銷活動和歷程的績效：

* [簡訊行銷活動報告](../reports/campaign-global-report-cja-sms.md)
* [簡訊歷程報告](../reports/journey-global-report-cja-sms.md)

## 設定要求 {#configuration-requirements}

在傳送文字訊息之前，您必須：

1. **選擇簡訊提供者** - 從 Sinch、Twilio、Infobip 中選取，或設定自訂提供者
2. **設定 API 認證** - 將提供者的 API 權杖和服務 ID 與 Journey Optimizer 整合
3. **建立管道設定** - 設定行銷和交易型訊息的簡訊設定
4. **設定子網域 (可選)** - 只有在您打算在訊息中使用 URL 縮短時才需要

這些設定步驟通常由系統管理員執行。[簡訊設定快速入門](sms-configuration.md)

## 快速入門手冊 {#quick-start}

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="sms-configuration.md">
<img alt="驗證" src="../assets/do-not-localize/sms-config.jpg">
</a>
<div>
<a href="sms-configuration.md"><strong>設定簡訊頻道</strong></a>
</div>
<p>設定您的簡訊提供者和管道設定</p>
</td>
<td>
<a href="create-sms.md">
<img alt="銷售機會" src="../assets/do-not-localize/sms-create.jpeg">
</a>
<div><a href="create-sms.md"><strong>建立文字訊息</strong></a>
</div>
<p>設計並個人化您的簡訊、MMS 或 RCS 內容</p>
</td>
<td>
<a href="send-sms.md">
<img alt="不頻繁" src="../assets/do-not-localize/sms-sending.jpg">
</a>
<div>
<a href="send-sms.md"><strong>預覽與傳送</strong></a>
</div>
<p>測試文字訊息並傳送給客群</p>
</td>
<td>
<a href="sms-opt-out.md">
<img alt="驗證" src="../assets/do-not-localize/sms-opt-out.jpg">
</a>
<div>
<a href="sms-opt-out.md"><strong>管理選擇退出</strong></a>
</div>
<p>處理取消訂閱的請求並確保合規性</p>
</td>
</tr></table>

## 其他資源 {#additional-resources}

瀏覽下列主題，深入瞭解 Journey Optimizer 中的文字訊息。

+++設定指南

了解如何設定簡訊環境：

* [簡訊管道設定概觀](sms-configuration.md)
* [建立簡訊管道設定](sms-configuration-surface.md)
* [設定簡訊子網域以縮短 URL](sms-subdomains.md)

+++

+++提供者設定指南

各個簡訊服務提供者的逐步設定：

* [設定 Sinch 提供者](sms-configuration-sinch.md)
* [設定 Twilio 提供者](sms-configuration-twilio.md)
* [設定 Infobip 提供者](sms-configuration-infobip.md)
* [設定自訂簡訊提供者](sms-configuration-custom.md)

+++

+++內容建立與管理

建立、個人化及管理您的文字訊息內容：

* [建立簡訊/MMS 訊息](create-sms.md)
* [預覽、測試和傳送訊息](send-sms.md)
* [文字訊息中的個人化](../personalization/personalize.md)
* [動態內容](../personalization/get-started-dynamic-content.md)

+++

+++合規性與隱私權

確保您的文字訊息符合法規與隱私權標準：

* [選擇退出管理](sms-opt-out.md)
* [隱私權與同意](../privacy/opt-out.md#opt-out-decision-management)

+++

+++績效追蹤

監視和分析您的簡訊行銷活動和歷程績效：

* [簡訊行銷活動報告](../reports/campaign-global-report-cja-sms.md)
* [簡訊歷程報告](../reports/journey-global-report-cja-sms.md)

+++

+++歷程與行銷活動整合

瞭解如何將簡訊整合至您的客戶歷程與行銷活動中：

* [將簡訊新增至歷程](../building-journeys/journeys-message.md)
* [建立簡訊行銷活動](../campaigns/create-campaign.md)

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

**相關主題**

* [在歷程中新增訊息](../building-journeys/journeys-message.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [護欄與限制](../start/guardrails.md#sms-guardrails)
* [簡訊與行動傳訊教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/channels/sms-channel/sms-mms-messages-overview){target="_blank"}
