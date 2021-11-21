---
title: 監視消息執行
description: 了解監控和傳遞准則
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: 0184614fb3203a1b5fee7603acd173042f223578
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 1%

---

# 管理傳遞能力 {#manage-deliverability}

傳遞能力是您傳送至收件者收件匣的成功度量。

**電子郵件傳遞** 指一組特性，這些特性決定了郵件通過個人電子郵件地址在短時間內以預期的質量和內容和格式到達目的地的能力。 這些特徵分為四大類：資料質量、訊息和內容、傳送基礎架構和信譽。 它們共同構成了成功電子郵件傳遞計畫的基礎。

此 **傳遞率** 是點擊收件者收件匣的訊息數，與已傳送的訊息數相比。 這取決於許多因素，尤其是：

* 垃圾郵件投訴有限
* 低硬反彈率
* 目標地址的質量
* 訊息內容
* 發件人信譽

最佳化您的 [!DNL Journey Optimizer] 體驗，建議您使用本節所列的最佳實務。 傳遞能力問題通常與網際網路服務提供者(ISP)和郵件伺服器管理員實施的針對垃圾郵件的保護相關。

如需深入了解什麼是傳遞能力，以及深入了解關鍵傳遞能力條款、概念和方法，請參閱 [Adobe傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=zh-Hant){target=&quot;_blank&quot;}。

## 降低投訴率 {#reduce-complaint-rate}

ISP通常會以明顯的方式將收到的郵件報告為垃圾郵件。 這使得能夠識別不可靠的來源。 快速接受選擇退出請求，因此顯示您是可靠的寄件者，可降低投訴率。 [進一步了解選擇退出管理](consent.md#opt-out-management).

一般而言，請勿嘗試讓想要退出的收件者填寫欄位（例如其電子郵件地址或名稱），以此方式來阻礙收件者。 取消訂閱登錄頁面應該只包含一個驗證按鈕。

請求額外確認時，請支付額外護理費：使用者可能有兩個電子郵件地址已重新導向至相同的方塊(例如：firstname.lastname@club.com和firstname.lastname@internet-club.com)。 如果設定檔只能記住第一個地址，而且想透過傳送給另一個地址的訊息取消訂閱，則表單會拒絕此項，因為加密的識別碼與輸入的電子郵件地址不符。

## 利用隱藏清單 {#suppression-lists}

[!DNL Journey Optimizer] 會管理收集垃圾郵件投訴、硬退信及軟退信的隱藏清單，這些內容會持續發生。

為保護您的傳遞能力，預設情況下，隱藏清單上的收件人將被排除在所有將來的傳遞之外，因為向這些聯繫人發送可能會損害您的發送信譽。

[進一步了解隱藏清單](suppression-list.md).

## 使用監控工具 {#monitoring-tools}

使用提供的功能 [!DNL Journey Optimizer] 監視傳遞能力。

此 **[!UICONTROL Executions]** 訊息清單的索引標籤可讓您透過一組即時指標來檢查傳送的執行情形。 此標籤會顯示在其他項目中：
* 成功執行、傳送和傳送的訊息數。
* 已開啟的訊息數，以及已點按的訊息/連結數。

[進一步了解監控訊息執行](message-monitoring.md).

## 調整訊息內容 {#adapt-message-content}

某些消息的內容可以檢測為垃圾郵件，程度較輕。

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

若要改善您的傳遞率，並確保您的電子郵件可送達收件者，在設計訊息內容時，請遵循下列原則：

* **寄件者名稱和地址**:地址必須明確標識發件人。 網域必須屬於寄件者，並註冊給寄件者。 域註冊表不得私有化。

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **取消訂閱連結和登錄頁面**:取消訂閱連結至關重要。 表單必須可見且有效，且必須可運作。

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[深入了解如何設計電子郵件內容](design-emails.md).

<!--
## Establish your reputation as a sender

If you recently moved to another email service provider, IP address, or email domain or subdomain, you need to establish your reputation as a sender. Otherwise, your deliveries might be blocked or moved to the spam folder of the recipients' mailbox.

To warm up your IP, you can gradually ramp up the number of your deliveries. See this [use case](building-journeys/ramp-up-deliveries-uc.md).
-->