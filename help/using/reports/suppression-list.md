---
solution: Journey Optimizer
product: journey optimizer
title: 隱藏清單
description: 了解如何使用隱藏清單
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 6014088011c41fd5f673eb3d36fb0609c4a01270
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 3%

---

# 隱藏清單 {#suppression-list}

隱藏清單包含您要從傳送中排除的位址和網域，因為傳送至這些連絡人可能會損害您的傳送信譽和傳送率。

此 [!DNL Journey Optimizer] 隱藏清單是在您自己的環境層級（即針對指定的沙箱）進行管理。

它會收集會在單一用戶端環境中隱藏於所有郵件的電子郵件地址和網域，這表示是專屬於與沙箱ID相關聯的組織ID。

>[!NOTE]
>
>Adobe會保留已知錯誤地址的更新清單，這些地址已被證明對參與和郵件信譽有害，並確保不會向他們發送電子郵件。 此清單會以全域隱藏清單來管理，所有Adobe客戶都會看到這份清單。 全局隱藏清單中包含的地址和域名將被隱藏。 傳送報告中只會指出已排除的收件者數目。

## 為什麼要查禁清單？ {#why-suppression-list}

為了控制收件匣擁有者收到的電子郵件訊息，並確保只接收他們想要的郵件，網際網路服務提供者(ISP)和商業垃圾郵件篩選器有其專有的演算法，可根據其使用的IP位址和傳送網域來追蹤電子郵件傳送者的整體信譽。

如果您未接受其意見（例如垃圾郵件投訴、退信等） 考慮到這些因素，他們會降低你的聲譽。 隱藏清單可協助您遵守ISP的意見。

會自動從郵件傳送中排除其電子郵件地址遭隱藏的收件者。 這會加快傳送速度，因為錯誤率對傳送速度有顯著影響。

## 隱藏清單上有什麼？ {#what-s-on-suppression-list}

地址將按如下方式添加到隱藏清單中：

* 全部 **硬跳出** 和 **垃圾投訴** 在發生單次事件後，自動將相應的地址發送到隱藏清單。

* **軟跳出數** 請勿立即將地址發送到隱藏清單，但它們會增加錯誤計數器。 數個 [重試](../configuration/retries.md) 然後執行，當錯誤計數器達到臨界值時，地址將添加到隱藏清單中。

* 您也可以 [**手動** 添加地址或域](../configuration/manage-suppression-list.md#add-addresses-and-domains) 到隱藏清單。

進一步了解 [本節](#delivery-failures).

>[!NOTE]
>
>未訂閱用戶的地址無法發送到隱藏清單，因為他們沒有收到來自的電子郵件 [!DNL Journey Optimizer]. 其選項會在Experience Platform層級處理。 深入了解 [退出](../privacy/opt-out.md).

對於每個地址，隱藏的基本原因和隱藏類別（軟、硬等） 顯示在隱藏清單中。 了解有關訪問和管理隱藏清單的更多資訊，位於 [本節](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>具有 **[!UICONTROL 隱藏]** 在訊息傳送程式期間會排除狀態。 因此，若 **歷程報表** 會將這些設定檔顯示為已在歷程中移動([讀取區段](../building-journeys/read-segment.md) 和 [訊息活動](../building-journeys/journeys-message.md)), **電子郵件報表** 不會將其納入 **[!UICONTROL 已傳送]** 量度，因為在傳送電子郵件前會先將量度篩選掉。
>
>深入了解 [即時報表](../reports/live-report.md) 和 [全域報表](../reports/global-report.md). 若要找出所有排除案例的原因，您可以使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。

### 傳遞失敗 {#delivery-failures}

傳送失敗時有兩種錯誤：

* **硬跳出**. 硬退信表示電子郵件地址無效（即不存在的電子郵件地址）。 這包括從接收電子郵件伺服器傳回的退信，明確指出地址無效。
* **軟跳出**. 這是針對有效電子郵件地址而發生的臨時電子郵件退信。

A **硬跳出** 自動將電子郵件地址添加到隱藏清單。

A **軟跳出** <!--or an **ignored** error--> 多次發生的情況也會在多次重試後將電子郵件地址傳送至隱藏清單。 [重試時了解更多](../configuration/retries.md)

如果您繼續傳送至這些地址，可能會影響您的傳送率，因為它會告訴ISP您可能沒有遵循電子郵件地址清單維護最佳實務，因此可能不是值得信賴的寄件者。

### 垃圾郵件投訴數 {#spam-complaints}

隱藏清單會收集將訊息標示為垃圾訊息的電子郵件地址。 例如，如果某人寫信給客戶服務部門，要求您不再接收來自您的郵件，則該人的電子郵件地址在您的執行個體中會遭到隱藏，您將無法再傳送至該地址。

在收件者提交垃圾郵件投訴後傳送給收件者，可能會對您的傳送信譽造成重大影響，因為它會通知ISP您可能會傳送不想要的電子郵件，而且可能不會監聽收件者。

這可能會導致您的IP位址或傳送網域遭到封鎖，而這些位址會列在隱藏清單中，即可避免此情形。
