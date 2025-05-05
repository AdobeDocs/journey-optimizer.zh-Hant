---
solution: Journey Optimizer
product: journey optimizer
title: 禁止名單
description: 瞭解如何使用隱藏清單
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 11%

---

# 禁止名單 {#suppression-list}

隱藏清單包含您要從傳送中排除的地址和網域，因為傳送給這些聯絡人可能會損害您的傳送信譽和傳送率。

[!DNL Journey Optimizer]隱藏清單是在您自己的環境層級（亦即針對指定的沙箱）管理。

它會收集在單一使用者端環境中所有郵件中隱藏的電子郵件地址和網域，這表示會特定於與沙箱ID關聯的組織ID。

>[!NOTE]
>
>Adobe會保留已知不良地址的更新清單（這些地址已被證明會損害參與和郵寄信譽），並確保不會將電子郵件傳遞給他們。 此清單在所有 Adobe 客戶通用的全球禁止名單中進行管理。 全球禁止名單中包含的地址和網域名稱都會隱藏起來。 傳遞報告中僅顯示排除的收件者人數。

此外，您也可以利用 Journey Optimizer **Suppression REST API**，使用禁止名單與允許清單控制外寄郵件。 [了解如何使用 Suppression REST API](https://developer.adobe.com/journey-optimizer-apis/references/suppression/){target="_blank"}

## 為什麼要使用隱藏清單？ {#why-suppression-list}

為了控制收件匣擁有者收到的電子郵件訊息，並確保他們僅收到想要的訊息，網際網路服務提供者(ISP)和商業垃圾郵件篩選器會根據其使用的IP位址和傳送網域，使用其專屬演演算法來追蹤電子郵件寄件者的整體信譽。

如果您未將他們的意見反應（例如垃圾訊息申訴、退回等）納入考量，他們會對您的信譽進行評等。 隱藏清單可協助您接受ISP的意見回饋。

抑制其電子郵件地址的收件者會自動從郵件傳遞中排除。 這會加快傳送速度，因為錯誤率對傳送速度有顯著影響。

## 隱藏清單上有什麼？ {#what-s-on-suppression-list}

地址會新增到隱藏清單中，如下所示：

* 所有&#x200B;**硬退信**&#x200B;和&#x200B;**垃圾郵件申訴**&#x200B;都會在單次發生後自動將對應的地址傳送到隱藏清單。 在[本節](#spam-complaints)中進一步瞭解垃圾郵件投訴。

* **軟退信**&#x200B;不會立即傳送位址到隱藏清單，但會增加錯誤計數器。 接著會執行數次[重試](../configuration/retries.md)，當錯誤計數器達到臨界值時，會將地址新增到隱藏清單中。

* 您也可以&#x200B;[**手動**&#x200B;新增地址或網域](../configuration/manage-suppression-list.md#add-addresses-and-domains)至隱藏清單。

在[本節](#delivery-failures)中進一步瞭解硬跳出和軟跳出。

>[!NOTE]
>
>未訂閱的使用者地址無法傳送到隱藏清單，因為他們沒有接收來自[!DNL Journey Optimizer]的電子郵件。 他們的選擇在Experience Platform層級處理。 深入瞭解[選擇退出](../privacy/opt-out.md)。

對於每一個地址，抑制的基本原因和抑制類別（軟、硬等）都會顯示在抑制清單中。 在[本節](../configuration/manage-suppression-list.md)中進一步瞭解存取及管理隱藏清單。

>[!NOTE]
>
>訊息傳送程式會排除狀態為&#x200B;**[!UICONTROL 已隱藏]**&#x200B;的設定檔。 因此，雖然&#x200B;**歷程報告**&#x200B;會顯示這些設定檔已移動歷程（[讀取對象](../building-journeys/read-audience.md)和[訊息活動](../building-journeys/journeys-message.md)），但&#x200B;**電子郵件報告**&#x200B;不會將它們納入&#x200B;**[!UICONTROL 已傳送]**&#x200B;量度中，因為這些設定檔在電子郵件傳送前已篩選掉。
>
>深入瞭解[即時報告](../reports/live-report.md)和[Customer Journey Analytics報告](../reports/report-gs-cja.md)。 若要找出所有排除案例的原因，您可以使用[Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=zh-Hant){target="_blank"}。

### 傳遞失敗 {#delivery-failures}

傳送失敗時有兩種型別的錯誤：

* **硬退信**。 硬跳出表示無效的電子郵件地址（即不存在的電子郵件地址）。 這涉及來自接收電子郵件伺服器的退回訊息，明確指出地址無效。
* **軟退信**。 這是有效的電子郵件地址發生的暫時電子郵件退信。

**硬退信**&#x200B;會自動將電子郵件地址新增至隱藏清單。

發生太多次的&#x200B;**軟退信** <!--or an **ignored** error-->也會在多次重試後將電子郵件地址傳送至隱藏清單。 [進一步瞭解重試](../configuration/retries.md)

如果您繼續傳送至這些地址，可能會影響您的傳送率，因為這會告訴ISP您可能沒有遵循電子郵件地址清單維護最佳實務，因此您可能不是值得信賴的寄件者。

### 垃圾訊息申訴 {#spam-complaints}

隱藏清單會收集將您的郵件標籤為垃圾郵件的電子郵件地址。 例如，如果有人寫信給客戶服務，要求永不再收到您的郵件，您執行個體中將隱藏該人員的電子郵件地址，而您將無法再傳送給該地址。

在收件者提交垃圾郵件投訴後將其傳送給他們，可能會對您的傳送信譽產生巨大影響，因為它會通知ISP您可能會傳送不必要的電子郵件，並且可能不會收聽收件者。

這可能會造成您的IP位址或傳送網域遭到封鎖，若將這些位址列入隱藏清單可避免發生這種情況。

有些ISP會提供回饋迴路(FBL)，當收到電子郵件的使用者選擇將其標示為垃圾訊息時，會自動通知電子郵件寄件者。 [了解更多](deliverability.md#feedback-loops)
