---
title: 隱藏清單
description: 了解隱藏清單是什麼、其用途以及其中包含的內容。
source-git-commit: a2eee802f82552e56ced00f93e5e4c8a7b3feb7a
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 4%

---

# 隱藏清單{#suppression-list}

![](assets/do-not-localize/badge.png)

隱藏清單包含您要從傳遞中排除的電子郵件地址，因為向這些聯繫人發送可能會損害您的傳送信譽和傳遞率。

[!DNL Journey Optimizer]隱藏清單是在您自己的環境級別管理的。

它會收集會在單一用戶端環境中隱藏於所有郵件中的電子郵件地址和網域，這表示會專屬於與沙箱ID相關聯的IMS組織ID。

<!--It gathers spam complaints, hard bounces, and soft bounces that occur consistently.-->

## 為什麼要查禁清單？{#why-suppression-list}

為了控制收件匣擁有者收到的電子郵件訊息，並確保只接收他們想要的郵件，網際網路服務提供者(ISP)和商業垃圾郵件篩選器有其專有的演算法，可根據其使用的IP位址和傳送網域來追蹤電子郵件傳送者的整體信譽。

如果您未接受其意見（例如垃圾郵件投訴、退信等） 考慮到這些因素，他們會降低你的聲譽。 隱藏清單可協助您遵守ISP的意見。

會自動從郵件傳送中排除其電子郵件地址遭隱藏的收件者。 這會加快傳送速度，因為錯誤率對傳送速度有顯著影響。

## 隱藏清單上有什麼？{#what-s-on-suppression-list}

隱藏清單中會新增電子郵件地址，如下所示：

* 所有&#x200B;**硬退信**&#x200B;和&#x200B;**垃圾郵件投訴**&#x200B;在發生單一事件後會自動將對應的電子郵件地址傳送至隱藏清單。

* **軟退** 信和臨 **** 時忽略錯誤不會立即將電子郵件地址發送到隱藏清單，但會增加錯誤計數器。然後會執行多次重試，當錯誤計數器達到臨界值時，地址會新增至隱藏清單。 深入了解[重試次數](configuration/retries.md)。

<!--You can also manually add an address to the suppression list. Manual category will be available when ability to manually add an address to the suppression list (via API) is released.-->

>[!NOTE]
>
>未訂閱用戶的地址無法發送到隱藏清單，因為他們沒有收到來自[!DNL Journey Optimizer]的電子郵件。 其選項會在Experience Platform層級處理。 深入了解[選擇退出](../using/consent.md)。
<!--Email addresses of recipients who **unsubscribe** from your sendings are NOT sent to the suppression list. Confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

對於每個地址，隱藏的基本原因和隱藏類別（軟、硬等） 顯示在隱藏清單中。 了解有關[此部分](configuration/manage-suppression-list.md)中訪問和管理隱藏清單的詳細資訊。

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

### 傳送失敗{#delivery-failures}

傳送失敗時有三種錯誤類型：

* **硬跳**。硬退信表示電子郵件地址無效（即不存在的電子郵件地址）。 這包括從接收電子郵件伺服器傳回的退信，該退信明確指出地址無效，例如「未知的使用者」。
* **軟跳出**。這是針對有效電子郵件地址而發生的臨時電子郵件退信。
* **忽略**。這是針對有效電子郵件地址而發生但已知為臨時的電子郵件退信，例如連接嘗試失敗、與垃圾郵件相關的臨時問題（電子郵件信譽）或臨時技術問題。<!--does it exist in CJM?-->

**硬退信**&#x200B;會自動將電子郵件地址新增至隱藏清單。

發生太多次的&#x200B;**軟跳出**&#x200B;或&#x200B;**ignored**&#x200B;錯誤，也會在多次重試後將電子郵件地址傳送至隱藏清單。 [重試時了解更多](configuration/retries.md)

如果您繼續傳送至這些地址，可能會影響您的傳送率，因為它會告訴ISP您可能沒有遵循電子郵件地址清單維護最佳實務，因此可能不是值得信賴的寄件者。

### 垃圾郵件投訴{#spam-complaints}

隱藏清單會收集將訊息標示為垃圾訊息的電子郵件地址。 例如，如果某人寫信給客戶服務部門，要求您不再接收來自您的郵件，則該人的電子郵件地址在您的執行個體中會遭到隱藏，您將無法再傳送至該地址。

在收件者提交垃圾郵件投訴後傳送給收件者，可能會對您的傳送信譽造成重大影響，因為它會通知ISP您可能會傳送不想要的電子郵件，而且可能不會監聽收件者。

這可能會導致您的IP位址或傳送網域遭到封鎖，而這些位址會列在隱藏清單中，即可避免此情形。

<!--### Unsubscriptions {#unsubscriptions}

Every email sent to recipients must include an unsubscribe link. Upon clicking this link, if a recipient confirms [opting out](consent.md), the corresponding email address is immediately sent to the suppression list. This user must not receive communication from your brand until subscribed again.
NOT TRUE > "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

<!--MOVED to Configuration/Retries section

The threshold is set at three errors:
* For the same delivery, at the third attempt, the address is suppressed.
* If there are different deliveries and two errors occur at least 24 hours apart, the error counter is incremented upon each error and the address is also suppressed at the third attempt.
When a delivery is successful after a retry, the error counter of the address is reinitialized.

### Retries {#retries}

If a message fails due to a temporary bounce of the **Ignored** type, retries will be performed for **3.5 days** from the time the message was added to the email queue.

The minimum delay between retries and the maximum number of retries to be performed are ///managed by the Enhanced MTA/// based on how well an IP is performing, both historically and currently at a given domain.

After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->
