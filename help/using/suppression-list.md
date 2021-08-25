---
title: 隱藏清單
description: 了解隱藏清單是什麼、其用途以及其中包含的內容。
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 2%

---

# 隱藏清單 {#suppression-list}

隱藏清單包含您要從傳遞中排除的電子郵件地址，因為向這些聯繫人發送可能會損害您的傳送信譽和傳遞率。

[!DNL Journey Optimizer]隱藏清單是在您自己的環境級別管理的。

它會收集會在單一用戶端環境中隱藏於所有郵件中的電子郵件地址和網域，這表示會專屬於與沙箱ID相關聯的IMS組織ID。

<!--It gathers spam complaints, hard bounces, and soft bounces that occur consistently.-->

## 為什麼要查禁清單？ {#why-suppression-list}

為了控制收件匣擁有者收到的電子郵件訊息，並確保只接收他們想要的郵件，網際網路服務提供者(ISP)和商業垃圾郵件篩選器有其專有的演算法，可根據其使用的IP位址和傳送網域來追蹤電子郵件傳送者的整體信譽。

如果您未接受其意見（例如垃圾郵件投訴、退信等） 考慮到這些因素，他們會降低你的聲譽。 隱藏清單可協助您遵守ISP的意見。

會自動從郵件傳送中排除其電子郵件地址遭隱藏的收件者。 這會加快傳送速度，因為錯誤率對傳送速度有顯著影響。

## 隱藏清單上有什麼？ {#what-s-on-suppression-list}

隱藏清單中會新增電子郵件地址，如下所示：

* 所有&#x200B;**硬退信**&#x200B;和&#x200B;**垃圾郵件投訴**&#x200B;在發生單一事件後會自動將對應的電子郵件地址傳送至隱藏清單。

* **軟退** <!--and temporary **ignored** errors--> 信不會立即將電子郵件地址傳送至隱藏清單，但會增加錯誤計數器。然後會執行數次[重試](configuration/retries.md)，當錯誤計數器達到臨界值時，地址會新增至隱藏清單。

* 您也可以手動&#x200B;[****&#x200B;將地址或域](configuration/manage-suppression-list.md#add-addresses-and-domains)添加到隱藏清單中。

進一步了解[此區段](#delivery-failures)中的硬跳出和軟跳出。

>[!NOTE]
>
>未訂閱用戶的地址無法發送到隱藏清單，因為他們沒有收到來自[!DNL Journey Optimizer]的電子郵件。 其選項會在Experience Platform層級處理。 深入了解[選擇退出](../using/consent.md)。
<!--Email addresses of recipients who **unsubscribe** from your sendings are NOT sent to the suppression list. Confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

對於每個地址，隱藏的基本原因和隱藏類別（軟、硬等） 顯示在隱藏清單中。 了解有關[此部分](configuration/manage-suppression-list.md)中訪問和管理隱藏清單的詳細資訊。

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

>[!NOTE]
>
>狀態為&#x200B;**[!UICONTROL Suppressed]**&#x200B;的設定檔會在訊息傳送程式期間排除。 因此，雖然&#x200B;**歷程報表**&#x200B;會將這些設定檔顯示為已在歷程（[讀取區段](building-journeys/read-segment.md)和[訊息](building-journeys/journeys-message.md)活動）中移動，但&#x200B;**電子郵件報表**&#x200B;不會在電子郵件傳送前篩選掉的&#x200B;**[!UICONTROL Sent]**&#x200B;量度中納入這些設定檔。
>
>進一步了解[即時報表](reports/live-report.md)和[全域報表](reports/global-report.md)。 若要找出所有排除案例的原因，您可以使用[Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。

### 傳送失敗 {#delivery-failures}

傳送失敗時有兩種錯誤：

* **硬跳**。硬退信表示電子郵件地址無效（即不存在的電子郵件地址）。 這包括從接收電子郵件伺服器傳回的退信，明確指出地址無效。
* **軟跳出**。這是針對有效電子郵件地址而發生的臨時電子郵件退信。
<!--* **Ignored**. This is an email bounce that occurred for a valid email address but is known to be temporary, such as a failed connection attempt, a temporary Spam-related issue (email reputation), or a temporary technical issue.-->

**硬退信**&#x200B;會自動將電子郵件地址新增至隱藏清單。

發生太多次的&#x200B;**軟跳出** <!--or an **ignored** error-->也會在多次重試後將電子郵件地址傳送至隱藏清單。 [重試時了解更多](configuration/retries.md)

如果您繼續傳送至這些地址，可能會影響您的傳送率，因為它會告訴ISP您可能沒有遵循電子郵件地址清單維護最佳實務，因此可能不是值得信賴的寄件者。

### 垃圾郵件投訴 {#spam-complaints}

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
