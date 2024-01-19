---
solution: Journey Optimizer
product: journey optimizer
title: DMARC記錄
description: 瞭解如何在Journey Optimizer中設定DMARC記錄
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 子網域，網域，郵件， dmarc，記錄
source-git-commit: f9d3234a64ad659660c2d2c4ad24ab5c240cb857
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 1%

---

# DMARC記錄 {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="設定DMARC記錄"
>abstract="設定DMARC記錄以避免ISP發生傳遞問題。 作為強制執行業界最佳實務的一部分，Google和Yahoo都要求您擁有用於向其傳送電子郵件的任何網域的DMARC記錄。"

>[!CAUTION]
>
>繼最近的Gmail和Yahoo公告後，Journey Optimizer現在支援DMARC驗證技術。

<!--TO ADD TO AJO HOME PAGE (first tab)

>[!TAB Mandatory DMARC update]

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them, starting on **February 1st, 2024**. Make sure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in Journey Optimizer.

[![image](using/assets/do-not-localize/learn-more-button.svg)](using/configuration/dmarc-record-update.md)
-->

作為強制執行業界最佳實務的一部分，Google和Yahoo都將要求您擁有 **DMARC記錄** 用於傳送電子郵件給他們的任何網域。 此新需求開始於 **2024年2月1日**.

進一步瞭解Google和Yahoo在中提出的要求 [本節](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>若未遵守Gmail和Yahoo的新要求，預期會導致電子郵件進入垃圾郵件資料夾或遭到封鎖。

因此，Adobe強烈建議您務必為您已委派給Adobe的所有子網域設定DMARC記錄 [!DNL Journey Optimizer]. 請遵循下列兩個選項之一：

* 在您的子網域或子網域的父項網域上設定DMARC， **在您的託管解決方案中**.

* 在您的委派子網域上設定DMARC **使用中的新功能 [!DNL Journey Optimizer] 管理UI**  — 不需額外處理託管解決方案。 [了解更多](#implement-dmarc)

  >[!CAUTION]
  >
  >如果您已設定 [CNAME委派](delegate-subdomain.md#cname-subdomain-delegation) 針對您的傳送子網域，也需要在您的託管解決方案中輸入一些內容。 請務必與您的IT部門協調，以便他們能夠在 [!DNL Journey Optimizer] 功能已推出（2024年1月30日）。 <!--and be ready on February 1st, 2024-->

>[!NOTE]
>
>進一步瞭解如何在中實施DMARC [傳遞性最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} 以更能瞭解對電子郵件傳遞能力的影響。

## 什麼是DMARC？

DMARC，代表 **網域型訊息驗證、報告和符合性**，是一種電子郵件驗證通訊協定，可協助防範電子郵件詐騙、網路釣魚和其他詐騙活動。

* 電子郵件驗證：

   * SPF （寄件者原則架構）： DMARC仰賴SPF驗證傳送的郵件伺服器的身分。 SPF會根據網域的授權IP位址清單，檢查傳送伺服器的IP位址，協助確認電子郵件訊息是否來自授權來源。
   * DKIM (DomainKeys Identified Mail)： DMARC也會使用DKIM在電子郵件新增數位簽名，讓收件者驗證郵件的完整性和真實性。

* DMARC有助於防止惡意行為者傳送看似來自您網域的電子郵件。 透過設定DMARC，您可以指定電子郵件提供者應如何處理驗證檢查失敗的訊息，減少網路釣魚電子郵件送達收件者的可能性。

* DMARC提供明確的原則，讓電子郵件提供者在遇到聲稱來自您網域的訊息時，能遵循這些原則，進而協助改善電子郵件傳遞能力。 這可以降低合法電子郵件被標示為垃圾郵件或拒絕的機會。

* 藉由實作DMARC，您可以確保未經授權的當事人不會濫用您的網域進行網路釣魚或其他惡意活動，進而保護您的品牌聲譽。 對於仰賴與客戶和合作夥伴進行電子郵件通訊的企業和組織而言，這一點尤其重要。

設定DMARC記錄涉及將DNS TXT記錄新增到您網域的DNS設定。 此記錄會指定您的DMARC原則，例如是隔離還是拒絕驗證失敗的訊息。 實作DMARC是強化電子郵件安全性、保護組織和收件者免受電子郵件威脅的主動步驟。

## 實施 DMARC {#implement-dmarc}

* 如果不新增DMARC，您將至少被隔離。

* 確保您擁有可以接收郵件的正版收件匣 — 您管理此收件匣(不應該是Adobe收件匣)

建議為24，因為通常這是ISP具有的。
如果低於，請評估您的容量/檢查您的>聊天GPT

如果偵測到DMARC記錄，您可以複製貼上列出的相同值，或視需要變更它們。

如果您不輸入任何值，則會使用預設值。

### 完全委派的子網域

### 使用CNAME委派的子網域

對於版本流程中的CNAME，您需要再次下載CSV檔案（不是為了完全委派）





