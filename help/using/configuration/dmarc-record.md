---
solution: Journey Optimizer
product: journey optimizer
title: DMARC 記錄
description: 瞭解如何在Journey Optimizer中設定DMARC記錄
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: 子網域, 網域, 郵件, dmarc, 記錄
exl-id: f9e217f8-5aa8-4d3a-96fc-65defcb5d340
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 12%

---

# DMARC 記錄 {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="設定 DMARC 記錄"
>abstract="DMARC 是一種電子郵件驗證方法，可讓網域擁有者保護其網域免遭未經授權的使用，並避免信箱提供者的傳遞問題。<br>為了執行產業最佳實務，Google 和 Yahoo! 都要求您對傳送電子郵件所使用的任何網域留有 DMARC 記錄。"

## 什麼是DMARC？ {#what-is-dmarc}

網域型訊息驗證、報告和符合性 (DMARC) 是一種電子郵件驗證方法，可讓網域擁有者保護其網域免受未經授權的使用。透過向電子郵件提供者和網際網路服務提供者(ISP)提供明確的原則，這有助於防止惡意行為者傳送聲稱來自您網域的電子郵件。 實作 DMARC 可降低合法電子郵件遭標示為垃圾郵件或遭拒絕的風險，並改善電子郵件傳遞能力。

DMARC還提供驗證失敗的訊息報告，以及對於未通過DMARC驗證的電子郵件處理的控制。 取決於實作的 [DMARC原則](#dmarc-policies)，則可監視、隔離或拒絕這些電子郵件。 這些功能可讓您採取動作來減少和解決潛在的錯誤。

為了協助您防止傳遞問題，同時控制驗證失敗的郵件， [!DNL Journey Optimizer] 現在直接在其管理介面中支援DMARC技術。 [了解更多](#implement-dmarc)

### DMARC如何運作？ {#how-dmarc-works}

SPF和DKIM都可用來將電子郵件與網域建立關聯，並共同驗證電子郵件。 DMARC更進一步地進行，並透過比對DKIM和SPF檢查的網域來協助防止詐騙。

>[!NOTE]
>
>在Journey Optimizer中，已為您設定SPF和DKIM。

若要傳遞DMARC，訊息必須傳遞SPF或DKIM：

* SPF (Sender Policy Framework)會根據網域的授權IP位址清單，檢查傳送伺服器的IP位址，以協助確認電子郵件訊息是否來自授權來源。
* DKIM (DomainKeys Identified Mail)在電子郵件訊息中新增數位簽名，讓收件者可驗證訊息的完整性和真實性。

如果兩者或兩者皆未通過驗證，DMARC將會失敗，而電子郵件將會根據您選取的DMARC原則傳送。

<!--DMARC requires alignment between the 'From" and 'Return-Path' address.-->

### DMARC原則 {#dmarc-policies}

如果電子郵件無法通過DMARC驗證，您可以決定要對該郵件套用哪個動作。 DMARC有三個原則選項：

* 監視(p=none)：指示信箱提供者/ISP執行通常對郵件執行的動作。
* 隔離（p=隔離）：指示信箱提供者/ISP傳送不會將DMARC傳遞給收件者的垃圾郵件或垃圾郵件資料夾的郵件。
* 拒絕(p=reject)：指示信箱提供者/ISP封鎖未傳遞DMARC的郵件，進而導致退信。

>[!NOTE]
>
>瞭解如何使用設定DMARC原則 [!DNL Journey Optimizer] 在 [本節](#set-up-dmarc).

## DMARC需求更新 {#dmarc-update}

作為強制執行業界最佳實務的一部分，Google 和 Yahoo! 都要求您擁有 **DMARC記錄** 用於傳送電子郵件給他們的任何網域。 這項新要求於 **2024 年 2 月 1 日**&#x200B;起生效。

>[!CAUTION]
>
>未能遵循 Gmail 和 Yahoo! 的這項新要求可能導致電子郵件進入垃圾郵件資料夾或遭到封鎖。

因此，Adobe強烈建議您採取下列動作：

* 確定具有 **DMARC記錄** 設定 **您已委派的所有子網域** Adobe於 [!DNL Journey Optimizer]. [了解作法](#check-subdomains-for-dmarc)

* 時間 **委派任何新子網域** 若要Adobe，您可以 **設定DMARC** 直接 **在 [!DNL Journey Optimizer] 管理介面**. [了解作法](#implement-dmarc)

## 在中實作DMARC [!DNL Journey Optimizer] {#implement-dmarc}

此 [!DNL Journey Optimizer] 管理介面可讓您為已委派或正在委派給Adobe的所有子網域設定DMARC記錄。 詳細步驟如下所述。

### 檢查您現有的子網域以取得DMARC {#check-subdomains-for-dmarc}

確保您已為委派的所有子網域設定DMARC記錄 [!DNL Journey Optimizer]，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL 子網域]** 功能表，然後按一下 **[!UICONTROL 設定子網域]**.

1. 對於每個委派的子網域，請檢查 **[!UICONTROL DMARC記錄]** 欄。 如果指定的子網域找不到記錄，則會顯示警示。

   ![](assets/dmarc-record-alert.png)

   >[!CAUTION]
   >
   >為符合Gmail和Yahoo！的新要求，並避免頂級ISP出現傳遞問題，建議為所有委派的子網域設定DMARC記錄。 [了解更多](dmarc-record-update.md)

1. 選取沒有DMARC記錄關聯的子網域，並填入 **[!UICONTROL DMARC記錄]** 區段來依您組織的需求而定。 有關填入DMARC記錄欄位的詳細步驟，請參見 [本節](#implement-dmarc).

1. 請考量下列兩個選項：

   * 如果您編輯的子網域設定有 [CNAME](delegate-subdomain.md#cname-subdomain-delegation)，您必須將DMARC的DNS記錄複製到您的託管解決方案中，以產生相符的DNS記錄。

     ![](assets/dmarc-record-edit-cname.png)

     請確定DNS記錄已產生至您的網域託管解決方案，並勾選「我確認……」方塊。

   * 如果您正在編輯子網域 [已完全委派](delegate-subdomain.md#full-subdomain-delegation) 若要Adobe，只需填寫 **[!UICONTROL DMARC記錄]** 欄位詳見 [本節](#implement-dmarc). 不需要進一步動作。

     ![](assets/dmarc-record-edit-full.png)

1. 儲存您的變更。

### 為新子網域設定DMARC {#set-up-dmarc}

委派新子網域以在中進行Adobe時 [!DNL Journey Optimizer]，即會在您網域的DNS中建立DMARC記錄。 請依照下列步驟實作DMARC。

>[!CAUTION]
>
>為符合Gmail和Yahoo！的新要求，並避免頂級ISP出現傳遞問題，建議為所有委派的子網域設定DMARC記錄。 [了解更多](dmarc-record-update.md)

<!--If you fail to comply with the new requirement from Gmail and Yahoo! to have DMARC record for all sending domains, your emails are expected to land into the spam folder or to get blocked.-->

1. 設定新的子網域。 [了解作法](delegate-subdomain.md)

1. 前往 **[!UICONTROL DMARC記錄]** 區段。

   如果子網域有現有的DMARC記錄，而且它是由擷取的 [!DNL Journey Optimizer]，您可以使用介面中醒目提示的相同值，或視需要加以變更。

   ![](assets/dmarc-record-found.png)

   >[!NOTE]
   >
   >如果您未新增任何值，則會使用預先填入的預設值。

1. 定義在DMARC失敗時收件者伺服器將執行的動作。 依據 [DMARC原則](#dmarc-policies) 若要套用，請選取下列三個選項之一：

   * **[!UICONTROL 無]** （預設值）：告知接收者不要對未通過DMARC驗證的訊息執行任何動作，但仍會傳送電子郵件報告給寄件者。
   * **[!UICONTROL 隔離]**：通知接收電子郵件伺服器隔離未通過DMARC驗證的電子郵件 — 這通常意味著將這些郵件放在收件者的垃圾郵件或垃圾郵件資料夾中。
   * **[!UICONTROL 拒絕]**：告訴接收者完全拒絕（退回）驗證失敗之網域的任何電子郵件。 啟用此原則後，只有經過網域驗證為100%驗證的電子郵件才有機會放置收件匣。

   >[!NOTE]
   >
   >作為最佳實務，建議您將DMARC政策從提升到緩慢推出DMARC實施 **無**，至 **隔離**，至 **拒絕** 當您瞭解DMARC的潛在影響時。

1. 您可以選擇新增一或多個您選擇的電子郵件地址，以指出位置 **DMARC報表** 在電子郵件上，該 [驗證失敗](#how-dmarc-works) 應該屬於您的組織。 您最多可以為每個報表新增5個地址。

   >[!NOTE]
   >
   >請確定您的控制中有正版收件匣(非Adobe)可接收這些報告。

   ISP會產生兩種不同的報告，傳送者可透過其DMARC原則中的RUA/RUF標籤接收這些報告：

   * **彙總報表** (RUA)：未包含任何可能區分大小寫GDPR的PII （個人識別資訊）。
   * **鑑證失敗報告** (RUF)：其中包含對GDPR敏感的電子郵件地址。 在使用之前，請在內部檢查如何處理需要符合GDPR的資訊。

   >[!NOTE]
   >
   >這些高度技術性的報告提供企圖詐騙的電子郵件概觀。 最好透過協力廠商工具加以消化。

1. 選取 **適用百分比** DMARC電子郵件數量。

   此百分比取決於您對電子郵件基礎結構的信心以及對誤判（標籤為欺詐的合法電子郵件）的容忍度。 組織通常從DMARC原則設定為開始 **無**，逐漸增加DMARC政策百分比，並密切監視對合法電子郵件傳送的影響。

   >[!NOTE]
   >
   >隨著您對電子郵件驗證實務更有信心，請與您的電子郵件管理員和IT團隊合作，逐步提高此百分比。

   作為最佳實務，請以高DMARC相容率為目標，最好接近100%，以便在最大限度提高安全性的同時，將誤報風險降到最低。

1. 選取 **報告間隔** 24到168小時之間。 它可讓網域擁有者定期接收電子郵件驗證結果的更新，並採取必要動作來改善電子郵件安全性。

   <!--The DMARC reporting interval is specified in the DMARC policy published in the DNS (Domain Name System) records for a domain. The reporting interval can be set to daily, weekly, or another specified frequency, depending on the domain owner's preferences.

    The default value (24 hours) is generally the email providers' expectation.-->


<!--

Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.

DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

## What are the benefits of DMARC? {#dmarc-benefits}

The key benefits or DMARC are as folllows:

* DMARC allows email receivers to easily identify the authentication of emails, which could potentially improve delivery.

* It offers reporting on which messages fail SPF and/or DKIM, enabling senders to gain visibility.

* This increased visibility allows for steps to be taken to mitigate further errors. It gives senders a degree of control over what happens with mail that does not pass either of these authentication methods.

-->
