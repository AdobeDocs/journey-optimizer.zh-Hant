---
solution: Journey Optimizer
product: journey optimizer
title: 遵守新的 DMARC 要求
description: 了解必須在 Journey Optimizer 中設定 DMARC 記錄的原因和時機
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: 子網域, 網域, 郵件, dmarc, 記錄
source-git-commit: 745474d6232f01ee959db8d706110477ed0220e2
workflow-type: ht
source-wordcount: '561'
ht-degree: 100%

---

# 遵守新的 DMARC 要求 {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="了解更多有關必要的 DMARC 更新的資訊"
>abstract="為了執行產業最佳實務，Google 和 Yahoo 都要求您對傳送電子郵件所使用的任何網域留有 **DMARC 記錄** (從 **2024 年 2 月 1 日**&#x200B;開始)。<br>因此，請務必確認您在 Journey Optimizer 中委派給 Adobe 的所有子網域已經設定 DMARC 記錄。"

網域型訊息驗證、報告和符合性 (DMARC) 是一種電子郵件驗證方法，可讓網域擁有者保護其網域免受未經授權的使用。向電子郵件提供者/ISP 提供明確的原則，有助於防止惡意行為者傳送聲稱來自您網域的電子郵件。實作 DMARC 可降低合法電子郵件遭標示為垃圾郵件或遭拒絕的風險，並改善電子郵件傳遞能力。

作為強制執行業界最佳實務的一部分，Google 和 Yahoo! 都會對用於向其傳送電子郵件的任何網域，要求提供 **DMARC 記錄**。這項新要求於 **2024 年 2 月 1 日**&#x200B;起生效。

>[!CAUTION]
>
>未能遵循 Gmail 和 Yahoo! 的這項新要求可能導致電子郵件進入垃圾郵件資料夾或遭到封鎖。

因此，Adobe 強烈建議您，務必為在 [!DNL Journey Optimizer] 中委派給 Adobe 的所有子網域設定 DMARC 記錄。請依照下列適用於您情況的步驟進行：

* 如果您已將傳送子網域[完全委派](delegate-subdomain.md#full-subdomain-delegation) 給 Adobe，請依照下列其中一個選項進行：

   * **在託管解決方案中**，於您所委派子網域的上層網域設定 DMARC。
或
   * **在[!DNL Journey Optimizer]** 設定使用者介面中，於委派的子網域設定 DMARC，無需對託管解決方案進行額外工作。 [了解作法](dmarc-record.md#implement-dmarc)

* 如果您已使用 [CNAME](delegate-subdomain.md#cname-subdomain-delegation) 設定傳送子網域，請依照下列其中一個選項進行：

   * **在託管解決方案中**，於子網域或於子網域的上層網域設定 DMARC。
或
   * **在[!DNL Journey Optimizer]** 設定使用者介面中，於委派的子網域設定 DMARC。[了解作法](dmarc-record.md#implement-dmarc)

  >[!IMPORTANT]
  >
  >但是，CNAME 設定還需於裝載解決方案新增部分額外項目。因此，請務必與 IT 部門進行協調，以便他們能夠執行[本節](dmarc-record.md#implement-dmarc)中詳細說明的更新。

Google 和 Yahoo! 分享的最新時間表如下所述：

* Google：

   * **2024 年 2 月** – 暫時退回，其設計目的為開始對不符規範的情況提供警告。如果您尚未能符合規範，電子郵件仍會在短暫的延遲後正常傳遞。如果您完全符合規範，則不會發生暫時退回，也不會受到影響。

   * **2024 年 4 月** – 開始封鎖不符合 DMARC 要求的寄件者。一開始只會封鎖一部分不符合規範的電子郵件，而封鎖的百分比會隨著時間而增加。

   * **2024 年 6 月 1 日** – 任何未完全符合規範的寄件者都會遇到封鎖的情況。

* Yahoo! 尚未提供確切日期，但已表示「將自 2024 年 2 月開始強制進行。以逐步方式強制進行」。

>[!NOTE]
>
>如果您有任何問題或需要支援，請聯絡 Adobe 傳遞能力顧問或 Adobe 代表。

**實用連結**

* 於[傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=zh-Hant#about){target="_blank"}了解更多有關 DMARC 的資訊
* 詳閱 [Google Gmail 公告](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* 詳閱 [Yahoo!公告](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
