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
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# DMARC記錄 {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="設定DMARC記錄"
>abstract="設定DMARC記錄以避免ISP發生傳遞問題"

>[!CAUTION]
>
>繼最近的Gmail和Yahoo公告後，Journey Optimizer現在支援DMARC驗證技術。//您必須更新已在執行個體上建立的所有子網域以包含DMARC支援。//

務必在2月1日前完成此作業，近期將推出此檔案

開始日期

您有2個選項：

* 從現在開始，您可以自行操作：隨時與IT部門進行設定

* 在AJO中執行此作業 — 但若是這種情況，您需要等到1月30日

   * 完全委派：您可以在1月30日完成委派（AJO版本）

   * CNAME會與您的IT部門一起進行規劃，這樣就不會太費時，但您需要進行規劃

作為強制執行業界最佳實務的一部分，Google和Yahoo都將要求您擁有用於向其傳送電子郵件的任何網域的DMARC記錄。 此新需求開始於 **2024年2月1日**.

瞭解更多關於Google和Yahoo對DMARC記錄的要求，請參閱 [本節](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

進一步瞭解Google和Yahoo於 [此頁面](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

DMARC，代表 **網域型訊息驗證、報告和符合性**，是一種電子郵件驗證通訊協定，可協助防範電子郵件詐騙、網路釣魚和其他詐騙活動。

* 電子郵件驗證：

   * SPF （寄件者原則架構）： DMARC仰賴SPF驗證傳送的郵件伺服器的身分。 SPF會根據網域的授權IP位址清單，檢查傳送伺服器的IP位址，協助確認電子郵件訊息是否來自授權來源。
   * DKIM (DomainKeys Identified Mail)： DMARC也會使用DKIM在電子郵件新增數位簽名，讓收件者驗證郵件的完整性和真實性。

* DMARC有助於防止惡意行為者傳送看似來自您網域的電子郵件。 透過設定DMARC，您可以指定電子郵件提供者應如何處理驗證檢查失敗的訊息，減少網路釣魚電子郵件送達收件者的可能性。

* DMARC提供明確的原則，讓電子郵件提供者在遇到聲稱來自您網域的訊息時，能遵循這些原則，進而協助改善電子郵件傳遞能力。 這可以降低合法電子郵件被標示為垃圾郵件或拒絕的機會。

* 藉由實作DMARC，您可以確保未經授權的當事人不會濫用您的網域進行網路釣魚或其他惡意活動，進而保護您的品牌聲譽。 對於仰賴與客戶和合作夥伴進行電子郵件通訊的企業和組織而言，這一點尤其重要。

設定DMARC記錄涉及將DNS TXT記錄新增到您網域的DNS設定。 此記錄會指定您的DMARC原則，例如是隔離還是拒絕驗證失敗的訊息。 實作DMARC是強化電子郵件安全性、保護組織和收件者免受電子郵件威脅的主動步驟。

[進一步瞭解DMARC的可遞送性最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=zh-Hant){target="_blank"} 以更能瞭解DMARC對電子郵件傳遞能力的影響。

如果不新增DMARC，您將至少被隔離。

請確定您擁有可以接收郵件的正版收件匣 — 您管理此收件匣(不應該是Adobe收件匣)

建議為24，因為如果低於24，通常會評估您的容量/檢查您的>聊天GPT

Google和Yahoo，以及所有其他主要ISP

對於版本流程中的CNAME，您需要再次下載CSV檔案（不是為了完全委派）

新DMARC記錄

在RN中>放在首位所有子網域都必須更新以支援DMARC



