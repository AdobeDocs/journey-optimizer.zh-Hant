---
title: 監視消息執行
description: 瞭解監控與傳遞能力指南
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# 管理傳遞能力{#manage-deliverability}

![](assets/do-not-localize/badge.png)

傳遞能力是您傳送給收件者收件箱的成功度量。

**電子** 郵件傳遞能力是指一組特性，這些特性決定了郵件通過個人電子郵件地址在短時間內到達其目的地的能力，並且在內容和格式方面具有預期的質量。這些特徵可分為四大類：資料品質、訊息和內容、傳送基礎架構和聲譽。 它們共同構成了成功的電子郵件傳遞能力計畫的基礎。

**可傳遞性率**&#x200B;是點擊收件者收件箱的消息數，與傳送的消息數相比。 這取決於許多因素，尤其是：

* 垃圾郵件投訴有限
* 低硬反彈率
* 目標地址的質量
* 訊息內容
* 發件人信譽

若要最佳化[!DNL Journey Optimizer]體驗的傳遞能力，建議使用本節所列的最佳實務。 傳遞能力問題通常與網際網路服務提供商(ISP)和郵件伺服器管理員實施的垃圾郵件防護有關。

## 降低投訴率{#reduce-complaint-rate}

ISP通常會以明顯的方式將收到的訊息報告為垃圾訊息。 這使得識別不可靠源成為可能。 快速接受退出請求，因此顯示您是可靠的寄件者，可降低投訴率。 [進一步瞭解退出管理](consent.md#opt-out-management)。

一般而言，請勿嘗試透過要求收件者填寫電子郵件地址或姓名等欄位，來妨礙想要退出的收件者。 取消訂閱的登陸頁面應僅包含一個驗證按鈕。

在要求額外確認時，請格外小心：使用者可能有兩個電子郵件地址被重新導向至相同方塊(例如：firstname.lastname@club.com和firstname.lastname@internet-club.com)。 如果描述檔僅能記住第一個位址，並希望透過傳送至另一個位址的訊息取消訂閱，表單將拒絕此項訂閱，因為加密的識別碼與輸入的電子郵件地址不符。

## 利用抑制清單{#suppression-lists}

[!DNL Journey Optimizer] 管理收集垃圾郵件投訴、硬性反彈和軟性彈回的抑制清單，這些都會持續發生。

為了保護傳送能力，隱藏清單中地址的收件者預設會從所有未來傳送中排除，因為傳送給這些連絡人可能會傷害您的傳送信譽。

[進一步瞭解隱藏清單](suppression-lists.md)。

## 使用監控工具{#monitoring-tools}

使用[!DNL Journey Optimizer]提供的功能來監控您的傳遞能力。

訊息清單的&#x200B;**[!UICONTROL Executions]**&#x200B;標籤可讓您透過一組即時指標來檢查傳送的效能。 此標籤還顯示：
* 成功執行、發送和傳送的消息數。
* 已開啟的消息數和已按一下的消息／連結數。

[進一步瞭解監控消息執行](message-monitoring.md)。

## 調整消息內容{#adapt-message-content}

在較小程度上，某些消息的內容可被檢測為垃圾郵件。

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

若要改善您的傳送率，並確保您的電子郵件送達收件人，請在設計訊息內容時遵循下列原則：

* **發件人姓名和地址**:地址必須明確識別發件人。網域必須由傳送者擁有並註冊。 域註冊不得私有化。

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **取消訂閱連結和登陸頁面**:取消訂閱連結是必備的。它必須可見且有效，而且表單必須正常運作。

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[進一步瞭解如何設計電子郵件內容](design-emails.md)。
