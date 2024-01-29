---
solution: Journey Optimizer
product: journey optimizer
title: 符合新的DMARC要求
description: 瞭解必須在Journey Optimizer中設定DMARC記錄的原因和時間
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 子網域，網域，郵件， dmarc，記錄
source-git-commit: a153960d083cbeab8beca30733832a9df8af9cbc
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 7%

---

# 符合新的DMARC要求 {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="了解更多有關必要的 DMARC 更新的資訊"
>abstract="作為強制執行業界最佳實務的一部分，Google和Yahoo都將要求您擁有 **DMARC記錄** ，適用於您用來傳送電子郵件給他們的任何網域，從 **2024年2月1日**.<br>因此，請務必確認您在 Journey Optimizer 中委派給 Adobe 的所有子網域已經設定 DMARC 記錄。"

作為強制執行業界最佳實務的一部分，Google和Yahoo都將要求您擁有 **DMARC記錄** 用於傳送電子郵件給他們的任何網域。 此新需求開始於 **2024年2月1日**.

進一步瞭解Google和Yahoo在中提出的要求 [本節](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>若未遵守Gmail和Yahoo的新要求，預期會導致電子郵件進入垃圾郵件資料夾或遭到封鎖。

因此，Adobe強烈建議您務必為您已委派給Adobe的所有子網域設定DMARC記錄 [!DNL Journey Optimizer]. 請依照以下適用於您的案例的步驟操作：

* 如果您有 [已完全委派](delegate-subdomain.md#full-subdomain-delegation) 若要將子網域傳送至Adobe，請遵循下列兩個選項之一：

   * 在您委派之子網域的父項網域上設定DMARC **在您的託管解決方案中**.

   * 在您的委派子網域上設定DMARC **在 [!DNL Journey Optimizer] 管理UI**  — 不需額外處理託管解決方案。 [了解作法](dmarc-record.md#implement-dmarc)

* 如果您已使用設定您的傳送子網域 [CNAME](delegate-subdomain.md#cname-subdomain-delegation)，請遵循下列兩個選項之一：
   * 在您的子網域或子網域的父項網域上設定DMARC **在您的託管解決方案中**.
   * 在您的委派子網域上設定DMARC **在 [!DNL Journey Optimizer] 管理UI**. [了解作法](dmarc-record.md#implement-dmarc)

     不過，若是CNAME委派，也需要在您的託管解決方案中輸入。 因此，請務必與您的IT部門進行協調，以便他們能夠在 [!DNL Journey Optimizer] 功能已推出（1月30日起）。 [了解更多](dmarc-record.md#implement-dmarc)

**更多詳細資訊，請參閱 [!DNL Journey Optimizer] DMARC即將推出的功能適用於 [本節](dmarc-record.md).**

>[!NOTE]
>
>如果您有任何問題或需要支援，請聯絡您的Adobe傳遞顧問或您的Adobe代表。

Google和Yahoo分享的最新時間表如下：

* Google：

   * **2024年2月**  — 會開始提供不合規警告的暫時跳出。 如果您尚未符合合規性，在短暫的延遲後，電子郵件仍會正常傳遞。 如果您完全符合法規要求，則不會有任何暫時跳出，也不會受到影響。

   * **2024年4月**  — 未符合DMARC要求的寄件者將開始封鎖。 一開始只會封鎖一部分不符合規範的電子郵件，而封鎖的百分比會隨著時間而增加。

   * **2024年6月1日**  — 任何未完全合規的寄件者都會遇到封鎖的情況。

* 雅虎尚未提供確切日期，但已表示「執法將從2024年2月開始。 執法將逐步推出」。

>[!NOTE]
>
>進一步瞭解如何在中實施DMARC [傳遞性最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} 以更能瞭解對電子郵件傳遞能力的影響。
