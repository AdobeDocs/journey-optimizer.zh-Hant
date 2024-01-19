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
hide: true
hidefromtoc: true
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# DMARC記錄重要更新{#dmarc-record}


>[!CAUTION]
>
>繼最近的Gmail和Yahoo公告後，Journey Optimizer現在支援DMARC驗證技術。

作為強制執行業界最佳實務的一部分，Google和Yahoo都將要求您擁有用於向其傳送電子郵件的任何網域的DMARC記錄。 此新需求開始於 **2024年2月1日**.

瞭解更多關於Google和Yahoo對DMARC記錄的要求，請參閱 [本節](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

進一步瞭解Google和Yahoo於 [此頁面](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

接下來，您會有一段動作或後續步驟供您使用，其中將說明：

您必須為所有子網域進行設定
* 如果您已將網域完全委派給我們，則您有兩個選項
   * 在您的託管解決方案中，於委派網域的父網域上設定DMARC，或
   * 使用我們即將推出在管理員UI中的功能，在委派網域上設定DMARC，而不需要額外的託管解決方案工作
* 如果您已為傳送網域設定CNAME，則您有兩個選項
   * 在託管解決方案的子網域或子網域的父網域上設定DMARC，或
   * 使用我們即將推出的Admin UI功能設定DMARC。 不過，我們不僅需要UI，還需要主機解決方案中的專案。

即將提供更多有關我們即將推出的功能的詳細資訊。

此外，如果未設定，您可從以下區段複製與DMARC相關的區段（從以上連結複製），以包含影響。 現在，我們要麼只推出與DMARC相關的產品。 或者，您可以在此處說明此公告適用於DMARC且按一下取消訂閱，以下是兩項功能的最新時間表。

自10月最初公告以來，已陸續更新時間表。

最近的時間表看起來像這樣：

Gmail：

* 2024年2月 — 旨在發出不合規警告的暫時彈回將開始。 如果您尚未符合合規性，在短暫的延遲後，電子郵件仍會正常傳遞。 如果您完全符合法規，則不會有暫時的跳出，也不會有任何發現。
* 2024年4月 — 除了List-Unsubscribe 1-Click之外，所有不符合規範的寄件者都將開始封鎖。 一開始只會封鎖一部分不符合規範的電子郵件，隨著時間推移，封鎖的%會增加。
* 2024年6月1日 — 任何未完全合規的寄件者（包括List-Unsubscribe 1-Click）將會遇到封鎖問題。

Yahoo：

尚未提供確切日期，但已表示「執法工作將於2024年2月開始。 執法將逐步推出」。
