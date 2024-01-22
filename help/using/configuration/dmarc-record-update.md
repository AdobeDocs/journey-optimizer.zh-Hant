---
solution: Journey Optimizer
product: journey optimizer
title: 強制性DMARC更新
description: 瞭解必須在Journey Optimizer中設定DMARC記錄的原因和時間
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 子網域，網域，郵件， dmarc，記錄
hide: true
hidefromtoc: true
source-git-commit: a93f1c81cceaee4f55cd7555284c4d8016ed4e21
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 強制性DMARC更新 {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="進一步瞭解強制性DMARC更新"
>abstract="作為強制執行業界最佳實務的一部分，Google和Yahoo都將要求您擁有 **DMARC記錄** ，適用於您用來傳送電子郵件給他們的任何網域，從 **2024年2月1日**. <br>因此，您必須確保已針對您已委派給Journey Optimizer中的Adobe的所有子網域設定DMARC記錄。"

作為強制執行業界最佳實務的一部分，Google和Yahoo都將要求您擁有 **DMARC記錄** 用於傳送電子郵件給他們的任何網域。 此新需求開始於 **2024年2月1日**.

進一步瞭解Google和Yahoo在中提出的要求 [本節](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>若未遵守Gmail和Yahoo的新要求，預期會導致電子郵件進入垃圾郵件資料夾或遭到封鎖。

因此，Adobe強烈建議您務必為您已委派給Adobe的所有子網域設定DMARC記錄 [!DNL Journey Optimizer]. 請依照以下適用於您的案例的步驟操作：

<!--
* Set up DMARC on your subdomains, or on the parent domain of your subdomains, **in your hosting solution**. You can do it as of now.

* Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI** - with no extra work on your hosting solution. This feature will be available on January 30, 2024.

    >[!CAUTION]
    >
    >If you have set up [CNAME delegation](delegate-subdomain.md#cname-subdomain-delegation) for your sending subdomains, it will also require some entry into your hosting solution. Make sure you coordinate with your IT department so that they can perform the update as soon as the [!DNL Journey Optimizer] feature is available (on January 30, 2024). (and be ready on February 1st, 2024)

    More details on the [!DNL Journey Optimizer] DMARC upcoming feature will come soon.
-->

* 如果您有 [已完全委派](delegate-subdomain.md#full-subdomain-delegation) 若要將子網域傳送至Adobe，請遵循下列兩個選項之一：

   * 在您委派之子網域的父項網域上設定DMARC **在您的託管解決方案中**.

   * 在您的委派子網域上設定DMARC **使用中即將推出的功能 [!DNL Journey Optimizer] 管理UI**  — 不需額外處理託管解決方案。

* 如果您已設定 [CNAME委派](delegate-subdomain.md#cname-subdomain-delegation) 若要傳送子網域，請遵循下列兩個選項之一：
   * 在您的子網域或子網域的父項網域上設定DMARC **在您的託管解決方案中**.
   * 在您的委派子網域上設定DMARC **使用中即將推出的功能 [!DNL Journey Optimizer] 管理UI**. 不過，您也必須輸入託管解決方案。 因此，請務必與您的IT部門進行協調，以便他們能夠在 [!DNL Journey Optimizer] 功能已推出（1月30日起）。 <!--and be ready on February 1st, 2024-->

**更多詳細資訊，請參閱 [!DNL Journey Optimizer] DMARC即將推出功能。**

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
