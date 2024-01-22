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
source-git-commit: 7d5a2a9b80110505688b5bfda2e286c7a6432441
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

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

因此，Adobe強烈建議您務必為您已委派給Adobe的所有子網域設定DMARC記錄 [!DNL Journey Optimizer]. 請依照以下適用於您的案例的步驟操作：

* 如果您有 [已完全委派](delegate-subdomain.md#full-subdomain-delegation) 若要將子網域傳送至Adobe，請遵循下列兩個選項之一：

   * 在您委派之子網域的父項網域上設定DMARC **在您的託管解決方案中**.

   * 在您的委派子網域上設定DMARC **使用中即將推出的功能 [!DNL Journey Optimizer] 管理UI**  — 不需額外處理託管解決方案。

* 如果您已設定 [CNAME委派](delegate-subdomain.md#cname-subdomain-delegation) 若要傳送子網域，請遵循下列兩個選項之一：

   * 在您的子網域或子網域的父項網域上設定DMARC **在您的託管解決方案中**.

   * 在您的委派子網域上設定DMARC **使用中即將推出的功能 [!DNL Journey Optimizer] 管理UI**. 不過，您也必須輸入託管解決方案。 因此，請務必與您的IT部門進行協調，以便他們能夠在 [!DNL Journey Optimizer] 功能已推出（1月30日起）。 <!--and be ready on February 1st, 2024-->

**更多詳細資訊，請參閱 [!DNL Journey Optimizer] DMARC即將推出功能。**

>[!NOTE]
>
>進一步瞭解如何在中實施DMARC [傳遞性最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} 以更能瞭解對電子郵件傳遞能力的影響。

## 什麼是DMARC？

DMARC，代表 **網域型訊息驗證、報告和符合性**，是一種電子郵件驗證方法/通訊協定，可讓網域擁有者保護其網域免受未經授權的使用。

它提供一種驗證傳送者網域的方式，有助於防止惡意行為者傳送看似來自您網域的電子郵件。

DMARC也提供電子郵件驗證狀態的意見回饋，並允許寄件者控制驗證失敗的電子郵件會發生什麼情況。 這包括監視、隔離或拒絕郵件的選項，具體取決於已實施的DMARC原則。

<!--Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.-->

DMARC有三個原則選項：

* 監視(p=none)：指示信箱提供者/ISP執行通常對郵件執行的動作。
* 隔離（p=隔離）：指示信箱提供者/ISP傳送不會將DMARC傳遞給收件者的垃圾郵件或垃圾郵件資料夾的郵件。
* 拒絕(p=reject)：指示信箱提供者/ISP封鎖未傳遞DMARC的郵件，進而導致退信。

## DMARC如何運作？

SPF和DKIM都可用來將電子郵件與網域建立關聯，並共同驗證電子郵件。 DMARC更進一步地進行，並透過比對DKIM和SPF檢查的網域來協助防止詐騙。 若要傳遞DMARC，訊息必須傳遞SPF或DKIM。 如果這兩項驗證都失敗，DMARC將會失敗，而且電子郵件將會根據您選取的DMARC原則傳送。

* SPF （寄件者原則架構）： DMARC仰賴SPF驗證傳送的郵件伺服器的身分。 SPF會根據網域的授權IP位址清單，檢查傳送伺服器的IP位址，協助確認電子郵件訊息是否來自授權來源。
* DKIM (DomainKeys Identified Mail)： DMARC也會使用DKIM在電子郵件新增數位簽名，讓收件者驗證郵件的完整性和真實性。

>[!NOTE]
>
>DMARC需要在&#39;From&#39;和&#39;Return-Path&#39;位址之間對齊。


<!--

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

-->


## 實施 DMARC {#implement-dmarc}

若要實作DMARC，請遵循適用於您案例的下列步驟。

* 如果不新增DMARC，您將至少被隔離。

### 完全委派的子網域

設定在DMARC失敗時收件者伺服器將執行的動作。

DMARC有三個原則選項：

* 監視(p=none)：指示信箱提供者/ISP執行通常對郵件執行的動作。 這是預設值。
* 隔離（p=隔離）：指示信箱提供者/ISP傳送不會將DMARC傳遞給收件者的垃圾郵件或垃圾郵件資料夾的郵件。
* 拒絕(p=reject)：指示信箱提供者/ISP封鎖未傳遞DMARC的郵件，進而導致退信。

接收彙總DMARC報告和鑑證DMARC失敗報告的電子郵件：您最多可以新增5個地址。

* 確保您擁有可以接收郵件的正版收件匣 — 您管理此收件匣(不應該是Adobe收件匣)

要套用DMARC的電子郵件適用百分比：

報告間隔：建議為24，因為通常這是ISP具有的值。
如果低於，請評估您的容量/檢查您的>聊天GPT

如果偵測到DMARC記錄，您可以複製貼上列出的相同值，或視需要變更它們。

如果您不輸入任何值，則會使用預設值。

### 使用CNAME委派的子網域

對於版本流程中的CNAME，您需要再次下載CSV檔案（不是為了完全委派）





