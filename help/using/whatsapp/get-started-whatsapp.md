---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 WhatsApp 訊息
description: 了解如何在 Journey Optimizer 建立及傳送 WhatsApp 訊息
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
TQID: https://experienceleague.adobe.com/uHzRC9X6rB9EXH4gIFiRxFaeNcrTD0-40RrxZkN4XFg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b8df23d2-98a2-4406-86cc-2babe8728d36id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 43066cc40499d87771b251766d5fa6b96afb1bb5
workflow-type: ht
source-wordcount: 707
ht-degree: 100%

---

# 開始使用 WhatsApp 訊息 {#get-started-whatsapp}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解 WhatsApp 管道在 Journey Optimizer 中的運作方式，以及其先決條件和限制，以便您可以決定如何將 WhatsApp 新增至您的歷程與行銷活動。

>[!ENDSHADEBOX]

您目前可以透過 Meta 的[雲端 API](https://developers.facebook.com/docs/whatsapp/cloud-api/)，直接透過 Journey Optimizer 傳送 WhatsApp 訊息。 此功能可將 WhatsApp 緊密整合至歷程和行銷活動，強化和收件者之間的通訊和參與度。

* 在&#x200B;**歷程**&#x200B;中。 建立歷程、新增 **WhatsApp** 活動及定義基本設定，然後瀏覽至&#x200B;**[!UICONTROL 動作：WhatsApp]** 右窗格以建立 WhatsApp 訊息的內容。 請在[此頁面](../building-journeys/journey-gs.md)進一步了解如何建立歷程。

* 在&#x200B;**行銷活動**&#x200B;中。 建立行銷活動，選取 **WhatsApp** 作為您的動作並定義基本設定，然後編輯訊息內容以定義要傳送的 WhatsApp 訊息。 了解如何建立[動作行銷活動](../campaigns/campaign-action.md#action-campaign-action) | [API 觸發的行銷活動](../campaigns/api-triggered-campaigns.md) | [協調的行銷活動](../orchestrated/create-orchestrated-campaign.md#create)

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## 使用案例 {#use-cases}

當您的客群已經使用 WhatsApp，而您想結合豐富內容與真正的雙向對話時，WhatsApp 效果最佳。

| 優點 | 原因 | 使用案例範例 |
| --- | --- | --- |
| 全球參與度高 | 廣泛使用的傳訊平台，在許多地區採用率高 | 觸及已活躍於 WhatsApp 的國際客群 |
| 豐富的互動式訊息 | 支援影像、影片、按鈕和快速回覆 | 產品目錄、含快速回覆選項的預約確認 |
| 雙向對話體驗 | 收件者可以在同一個對話串中回覆 | 客戶支援對話、訂單追蹤問題 |
| 互動式多畫面體驗 | WhatsApp Flow 範本可讓您在聊天中建立引導式多步驟互動 | 問卷調查、潛在客戶擷取表單 |
| 透過官方 API 實現合規性與信任 | 透過 Meta 已驗證的 Cloud API 傳遞，並進行傳送者驗證 | 建立收件者信任的品牌驗證通訊 |
| 與其他管道整合 | 可與其他管道一起納入歷程和行銷活動中 | 將 WhatsApp 作為輔助接觸點的多管道歷程 |

## 不適用情境 {#when-not-to-use}

WhatsApp 仰賴客群採用和明確同意，因此並不適用於所有情境。在下列情況下，建議考慮採用其他管道：

* 您的客群未使用 WhatsApp，因為採用率會因地區和人口統計特徵而大幅不同
* 收件者尚未明確選擇加入，而這是 Meta 傳訊政策的要求
* 訊息很緊急且需要保證送達；鑑於 WhatsApp 的傳遞和範本審查限制，SMS 或推播更能處理此類需求
* 內容冗長或複雜，更適合使用電子郵件，因為電子郵件提供更多空間和更豐富的格式設定
* 您這邊無法提供即時對話支援，因為雙向 WhatsApp 對話串會讓人期待及時回覆

## 先決條件 {#prereq}

將 WhatsApp 與 Journey Optimizer 整合需要下列項目：

* Meta 企業管理員帳戶
* [具有已驗證寄件者名稱與電話號碼的 WhatsApp 企業帳戶](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [使用者授權權杖擁有適當使用權限](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [核准的 Meta 範本](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

在繼續整合之前，您還需要瞭解下列內容：

* [WhatsApp 內容規則](https://www.whatsapp.com/legal/messaging-guidelines)
* [遵守 Meta 原則](https://www.whatsapp.com/legal)
* [24 小時交談限制](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## 限制 {#limitations}

下列限制適用於 WhatsApp 頻道：

* 已經可以在 Adobe Journey Optimizer 中的 WhatsApp 頻道使用 HIPAA，但第三方還未納入 Adobe 的 BAA。 客戶需自行負責法規遵循及供應商驗證。

* 請注意，尚未支援自動化或是預先定義的回答訊息。

* 自 2025 年 4 月起，會針對擁有美國電話號碼 (由 +1 開始撥號的國碼、美國區域碼組成的號碼) 的 WhatsApp 使用者，暫時暫停傳送所有行銷範本訊息。 [可到 Meta 文件中進一步瞭解](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* 原生整合功能不允許整合入第三方企業服務提供者 (BSP)。

## 作法影片 {#video}

以下影片說明如何將 WhatsApp 整合為 Adobe Journey Optimizer 中的原生頻道，以便大規模提供安全、即時、個人化的訊息。

+++ 收看影片

>[!VIDEO](https://video.tv.adobe.com/v/3470244?learn=on)

+++

## 其他學習資源

探索更多有關 WhatsApp 傳訊和設定的教學課程影片。

➡️ [WhatsApp 管道教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/channels/whatsapp/whatsapp-introduction){target="_blank"}

