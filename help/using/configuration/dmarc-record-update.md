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
exl-id: 15b10a61-6ecd-4ffa-b1c2-21e862263f6d
TQID: https://experienceleague.adobe.com/B-gnzjRpmhxELBiXRZxkBvE2yNNgozy-Hed5-k1oaIQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 493
ht-degree: 93%

---

# 遵守新的 DMARC 要求 {#dmarc-record-update}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解您必須在Adobe Journey Optimizer中為委派給Adobe的子網域設定DMARC記錄，以符合Google和Yahoo寄件者要求的原因和時間。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="了解更多有關必要的 DMARC 更新的資訊"
>abstract="Google 和 Yahoo 為執行產業最佳做法，要求您對於傳送電子郵件所使用的任何網域留有 **DMARC 記錄** (自 **2024 年 2 月 1 日**&#x200B;開始)。<br>因此，請務必確認您在 Journey Optimizer 中委派給 Adobe 的所有子網域已經設定 DMARC 記錄。"

網域型訊息驗證、報告和符合性 (DMARC) 是一種電子郵件驗證方法，可讓網域擁有者保護其網域免受未經授權的使用。 向電子郵件提供者/ISP 提供明確的原則，有助於防止惡意行為者傳送聲稱來自您網域的電子郵件。 實作 DMARC 可降低合法電子郵件遭標示為垃圾郵件或遭拒絕的風險，並改善電子郵件傳遞能力。

作為強制執行業界最佳實務的一部分，Google 和 Yahoo! 都會對用於向其傳送電子郵件的任何網域，要求提供 **DMARC 記錄**。 這項新要求於 **2024 年 2 月 1 日**&#x200B;起生效。

>[!CAUTION]
>
>未能遵循 Gmail 和 Yahoo! 的這項新要求 可能導致電子郵件進入垃圾郵件資料夾或遭到封鎖。

因此，Adobe 強烈建議您，務必為在 [!DNL Journey Optimizer] 中委派給 Adobe 的所有子網域設定 DMARC 記錄。 請依照下列適用於您情況的步驟進行：

* 如果您已將傳送子網域[完全委派](delegate-subdomain.md#set-up-subdomain) 給 Adobe，請依照下列其中一個選項進行：

   * **在託管解決方案中**，於您所委派子網域的上層網域設定 DMARC。
或
   * **在[!DNL Journey Optimizer]** 設定使用者介面中，於委派的子網域設定 DMARC，無需對託管解決方案進行額外工作。 [了解作法](dmarc-record.md#implement-dmarc)

* 如果您已使用 [CNAME](delegate-subdomain.md#cname-subdomain-setup) 設定傳送子網域，請依照下列其中一個選項進行：

   * **在託管解決方案中**，於子網域或於子網域的上層網域設定 DMARC。
或
   * **在[!DNL Journey Optimizer]** 設定使用者介面中，於委派的子網域設定 DMARC。 [了解作法](dmarc-record.md#implement-dmarc)

  但是，CNAME 設定還需於裝載解決方案新增部分額外項目。 因此，請務必與 IT 部門進行協調，以便他們能夠執行[本節](dmarc-record.md#implement-dmarc)中詳細說明的更新。

<!--
The most recent timelines shared by Google and Yahoo! are as follows:

* Google:

    * **February 2024** – Temporary bounces designed to provide warning of non-compliance will begin. Emails will still be delivered as normal after a short delay if you are not yet in compliance. If you are fully in compliance there will be no temporary bounces and you will not be affected.

    * **April 2024** – Blocks will begin for senders who are not in compliance with DMARC requirement. Only a portion of non-compliant email will be blocked at first, with the percentage blocked increasing over time.

    * **June 1st, 2024** – Any sender not in full compliance will experience blocking.

* Yahoo! has not provided exact dates, but has said "the rollout of enforcement will begin in February 2024. Enforcement will be gradually rolled out".
-->

>[!NOTE]
>
>如果您有任何問題或需要支援，請聯絡 Adobe 傳遞能力顧問或 Adobe 代表。

**實用連結**

* 於[傳遞能力最佳做法指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=zh-Hant#about){target="_blank"}中瞭解更多有關 DMARC 的資訊
* 詳閱 [Google Gmail 公告](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* 詳閱 [Yahoo! 公告](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
