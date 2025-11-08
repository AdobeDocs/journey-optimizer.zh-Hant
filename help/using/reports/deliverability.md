---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用傳遞能力
description: 瞭解傳遞能力准則
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '1138'
ht-degree: 7%

---

# 開始使用傳遞能力 {#manage-deliverability}

傳遞能力是衡量傳遞至收件者收件匣的成功程度。

>[!NOTE]
>
>對於授權Healthcare Shield的客戶，Adobe會使用傳輸層安全性(TLS) 1.2來保護使用者的系統（收件者）與Journey Optimizer（傳送者）之間的資料交換。 如果接收郵件伺服器不支援TLS 1.2，客戶將會遇到傳遞能力問題，包括電子郵件退回給原始寄件者。

**電子郵件傳遞能力**&#x200B;是指一組特性，這些特性決定訊息能否在短時間內透過個人電子郵件地址到達其目的地，而且內容和格式符合預期品質。 這些特性主要分為四個類別：資料品質、訊息和內容、傳送基礎結構和信譽。 這些共同構成了成功電子郵件傳遞計畫的基礎。

**傳遞率**&#x200B;是點選收件者收件匣的訊息數目，與已傳遞的訊息數目比較。 這取決於許多因素，特別是：

* 垃圾郵件投訴數量有限
* 低硬跳出率
* 目標地址的品質
* 訊息內容
* 寄件者信譽

若要最佳化您[!DNL Journey Optimizer]體驗的傳遞能力，我們建議您使用本節所列的最佳實務。 傳遞能力問題通常與網際網路服務提供者(ISP)和郵件伺服器管理員實施的垃圾郵件防護相關聯。

如需深入瞭解什麼是傳遞能力，並深入瞭解傳遞能力的重要術語、概念和方法，請參閱[Adobe傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=zh-Hant){target="_blank"}。

## 降低投訴率 {#reduce-complaint-rate}

ISP通常具有將收到的訊息報告為垃圾訊息的顯著方法。 這樣就可以識別不可靠的來源。 透過快速接受選擇退出請求並顯示您是可靠的寄件者，您可以降低投訴率。 [進一步瞭解選擇退出管理](../privacy/opt-out.md#opt-out-decision-management)

一般而言，請勿透過要求收件者填寫電子郵件地址或名稱等欄位，來妨礙想要選擇退出的收件者。 取消訂閱登入頁面應只有一個驗證按鈕。

請求其他確認時請格外小心：使用者可能有兩個電子郵件地址會重新導向至同一個方塊(例如：firstname.lastname@club.com和firstname.lastname@internet-club.com)。 如果設定檔只能記住第一個地址，並希望透過傳送給另一個的訊息取消訂閱，則表單將拒絕此操作，因為加密的識別碼和輸入的電子郵件地址不匹配。

## 利用隱藏清單 {#suppression-lists}

[!DNL Journey Optimizer]管理隱藏清單，該清單會收集持續發生的垃圾郵件投訴、硬跳出和軟跳出。

為了保護您的傳遞能力，根據預設，地址在隱藏清單中的收件者將會從所有未來的傳遞中排除，因為傳送給這些聯絡人可能會損害您的傳送信譽。

[進一步瞭解隱藏清單](suppression-list.md)

## 使用監控工具 {#monitoring-tools}

使用[!DNL Journey Optimizer]提供的報告功能來監視您的傳遞能力。

行銷活動和歷程報告可讓您透過一組即時指標檢查傳遞的執行方式。 其中會顯示下列專案：

* 成功執行、傳送及傳遞的訊息數。
* 已開啟的訊息數以及已點按的訊息/連結數。

深入瞭解[即時報告](../reports/live-report.md)和[所有時間報告](../reports/report-gs-cja.md)

## 調整訊息內容 {#adapt-message-content}

在較小程度上，某些訊息的內容可能會被偵測為垃圾訊息。

若要改善您的傳遞率並確保您的電子郵件可送達您的收件者，請在設計您的訊息內容時遵循下列原則：

* **寄件者名稱和地址**：地址必須明確識別寄件者。 網域必須由寄件者擁有並註冊給寄件者。 網域登入不可為私用。

* **取消訂閱連結和登陸頁面**：取消訂閱連結是必要的。 它必須可見且有效，而且表單必須有效。

[進一步瞭解設計電子郵件內容](../email/get-started-email-design.md)

## 建立您作為寄件者的信譽 {#reputation}

如果您最近移至其他電子郵件服務提供者、IP位址或電子郵件網域或子網域，您必須建立您作為寄件者的信譽。 否則，您的傳遞可能會遭到封鎖或移至收件者信箱的垃圾郵件資料夾。

在全新的網址傳送電子郵件時，您現在可以直接從使用者介面輕鬆執行IP熱身工作流程。

Adobe Journey Optimizer 提供標準化和有效率的方式，讓您的 IP 位址按照最佳實務來暖身，以實現最佳傳遞能力。

[深入瞭解IP熱身計畫](../configuration/ip-warmup-gs.md)

<!--To warm up your IP, you can gradually ramp up the number of your deliveries. Learn more in this [use case](../building-journeys/ramp-up-deliveries-uc.md).-->

## 實施 DMARC {#dmarc}

為了協助您降低合法電子郵件被標籤為垃圾郵件或拒絕的風險，並防止傳遞問題，[!DNL Journey Optimizer]可讓您為您委派給Adobe的所有子網域設定DMARC記錄。

網域型訊息驗證、報告和符合性(DMARC)是一種電子郵件驗證方法，可讓網域擁有者保護其網域免受惡意行動者的未經授權使用。

[進一步瞭解DMARC記錄](../configuration/dmarc-record.md)

## 了解意見回饋循環 {#feedback-loops}

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="某些子網域可能不可用"
>abstract="由於待處理意見回饋循環註冊，某些子網域目前無法選取。此程序可能需要長達 10 個工作天。完成後，您可以從所有可用子網域進行選擇。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation" text="開始使用子網域委派"

回饋迴路(FBL)是部分ISP提供的服務，當收到電子郵件的使用者選擇將其標示為垃圾郵件（也稱為「投訴」）時，可自動通知電子郵件寄件者。

一般使用者提出由ISP傳回Adobe的投訴後，電子郵件地址會自動新增至[隱藏清單](../reports/suppression-list.md)並從未來的傳遞中排除。 事實上，傳送電子郵件給標籤為垃圾訊息的使用者會對寄件者信譽產生負面影響，並可能導致傳遞問題。 [進一步瞭解垃圾訊息申訴](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>並非所有ISP都提供傳統FBL，例如Gmail。 Gmail不提供個人層級的意見回饋，並且無法用於追蹤個別收件者的垃圾郵件投訴，而是專注於其Google Postmaster工具中的彙總層級報告。 [了解更多](https://support.google.com/a/answer/6254652?hl=en){target="_blank"}

所有Adobe客戶都會自動註冊下列ISP的傳統FBL：

* 1&amp;1

* AOL

* 藍領帶

* Comcast

* Fastmail

* 甘地

* 義大利線上

* 拉波斯特

* Liberty Global (Chello、UPC、Unity Media)

* Locaweb

* Mail.RU

* Microsoft

* OpenRS

* Rackspace

* SEZNM

* SFR

* Silversky

* Swisscom

* Synacor

* 義大利電信

* Telenet

* Telenor

* Telstra

* Terra

* UOL

* 維珍媒體

* Yahoo

* Ziggo

Adobe會定期稽核這些FBL，以確保新增最新的可用FBL。

## 使用SMTP轉送 {#smtp-relay}

[!DNL Journey Optimizer]使用Adobe擁有的郵件傳輸代理程式(MTA)和IP，將您的電子郵件傳送給網際網路服務提供者(ISP)。 但是，在某些情況下，您可能會想要透過自己的MTA和IP來路由傳送最終電子郵件，或者在傳送電子郵件給收件者之前，對電子郵件執行最終驗證。

在這種情況下，您可以選擇將電子郵件中繼至您的組織託管的SMTP伺服器，而非直接從Journey Optimizer傳送至ISP。

>[!AVAILABILITY]
>
>SMTP轉送容量可依需求提供 — 請聯絡您的Adobe代表。
