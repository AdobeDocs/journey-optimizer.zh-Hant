---
title: 監視消息執行
description: 瞭解監控和交付性指導
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# 管理可交付性 {#manage-deliverability}

送貨能力是您送貨到收件人收件箱的成功度量。

**電子郵件傳送能力** 指一組特徵，這些特徵決定了郵件通過個人電子郵件地址在短時間內到達其目標的能力，並且在內容和格式方面具有預期的質量。 這些特徵分為四大類：資料質量、消息和內容、發送基礎架構和信譽。 它們共同構成了成功電子郵件傳遞計畫的基礎。

的 **可交付率** 是與已傳送的郵件數相比，按收件人收件箱的郵件數。 這取決於諸多因素，尤其是：

* 有限的垃圾郵件投訴
* 低硬反彈率
* 目標地址的質量
* 消息內容
* 發件人信譽

優化您的 [!DNL Journey Optimizer] 經驗，我們建議使用本節中列出的最佳做法。 傳送性問題通常與網際網路服務提供商(ISP)和郵件伺服器管理員實施的針對垃圾郵件的保護相關。

要深入瞭解什麼是可交付性，並瞭解關鍵可交付性術語、概念和方法的更多資訊，請參閱 [Adobe交付能力最佳實踐指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=zh-Hant){target=&quot;_blank&quot;}。

## 降低投訴率 {#reduce-complaint-rate}

ISP通常有一種突出的方法將收到的郵件報告為垃圾郵件。 這使得能夠識別不可靠的來源。 通過快速滿足選擇退出請求並因此表明您是可靠的發件人，您可以降低投訴率。 [瞭解有關退出管理的更多資訊](consent.md#opt-out-management)。

一般來說，不要通過要求收件人填寫電子郵件地址或姓名等欄位來妨礙希望退出的收件人。 取消訂閱登錄頁應只有一個驗證按鈕。

在請求額外確認時，請多加小心：用戶可能有兩個重定向到同一框的電子郵件地址(例如：firstname.lastname@club.com和firstname.lastname@internet-club.com)。 如果配置檔案只能記住第一個地址，並希望通過發送到另一個地址的消息取消訂閱，則表單將拒絕此操作，因為加密的標識符與輸入的電子郵件地址不匹配。

## 利用抑制清單 {#suppression-lists}

[!DNL Journey Optimizer] 管理一個抑制清單，該清單可收集持續發生的垃圾郵件投訴、硬回報和軟回報。

為了保護您的傳送能力，預設情況下，禁止清單中包含地址的收件人將被排除在所有將來的傳送之外，因為發送到這些聯繫人可能會損害您的發送信譽。

[瞭解有關禁止顯示清單的詳細資訊](suppression-list.md)。

## 使用監視工具 {#monitoring-tools}

使用提供的功能 [!DNL Journey Optimizer] 監控你的送貨能力。

的 **[!UICONTROL Executions]** 頁籤，您可以通過一組即時指示器檢查交貨的執行情況。 此頁籤顯示以下內容：
* 成功執行、發送和傳遞的消息數。
* 已開啟的消息數和已按一下的消息/連結數。

[瞭解有關監視消息執行的詳細資訊](message-monitoring.md)。

## 調整消息內容 {#adapt-message-content}

在較小程度上，某些消息的內容可以被檢測為垃圾郵件。

要提高您的可傳送率並確保電子郵件到達收件人，請在設計郵件內容時遵循以下原則：

* **發件人名稱和地址**:地址必須明確標識發件人。 域必須由發件人擁有並註冊。 不能對域註冊進行私有化。

* **取消訂閱連結和登錄頁**:取消訂閱連結至關重要。 它必須可見且有效，並且表單必須有效。

[瞭解有關設計電子郵件內容的詳細資訊](design-emails.md)。

## 建立您作為發件人的信譽

如果您最近轉到了其他電子郵件服務提供商、 IP地址、電子郵件域或子域，則需要建立您作為發件人的信譽。 否則，您的遞送可能會被阻止或移動到收件人郵箱的垃圾郵件資料夾。

要預熱您的IP，您可以逐步增加交貨數量。 查看 [用例](../building-journeys/ramp-up-deliveries-uc.md)。
