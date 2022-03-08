---
title: 隱藏清單
description: 瞭解禁止清單是什麼、其目的以及其中包含的內容。
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 2%

---

# 隱藏清單 {#suppression-list}

抑制清單包含您要從交貨中排除的電子郵件地址，因為向這些聯繫人發送可能會損害您的發送信譽和交貨率。

的 [!DNL Journey Optimizer] 隱藏清單由您自己的環境級別管理。

它收集在單個客戶端環境中所有郵件中隱藏的電子郵件地址和域，這意味著特定於與沙盒ID關聯的IMS組織ID。

## 為什麼要列禁令？ {#why-suppression-list}

為了控制收件箱所有者接收的電子郵件並確保他們只接收他們想要的郵件，網際網路服務提供商(ISP)和商業垃圾郵件過濾器使用其專有算法根據他們使用的IP地址和發送域來跟蹤電子郵件發送者的總體信譽。

如果您不聽取他們的反饋（如垃圾郵件投訴、回復等） 考慮到這點，他們會降低你的聲譽。 禁止清單可幫助您遵守ISP的反饋。

電子郵件地址被禁止的收件人將自動排除在郵件傳遞之外。 這會加快傳送速度，因為錯誤率對傳送速度有顯著影響。

## 禁止令上有什麼？ {#what-s-on-suppression-list}

電子郵件地址將按如下方式添加到禁止使用清單中：

* 全部 **硬邊界** 和 **垃圾郵件** 在發生一次事件後自動將相應的電子郵件地址發送到禁止清單。

* **軟邊界** 不要立即將電子郵件地址發送到禁止使用清單，但是它們會增加錯誤計數器。 幾個 [重試](../configuration/retries.md) 然後，執行，並且當錯誤計數器達到閾值時，地址被添加到禁止清單。

* 您也可以 [**手動** 添加地址或域](../configuration/manage-suppression-list.md#add-addresses-and-domains) 到禁止清單。

瞭解有關中的硬邊界和軟邊界的更多資訊 [此部分](#delivery-failures)。

>[!NOTE]
>
>無法將未訂閱用戶的地址發送到禁止使用清單，因為他們沒有接收來自 [!DNL Journey Optimizer]。 他們的選擇在Experience Platform級別處理。 瞭解更多 [跳出](consent.md)。

對於每個地址，抑制的基本原因和抑制類別（軟、硬等） 的下界。 瞭解有關訪問和管理中的禁止顯示清單的詳細資訊 [此部分](../configuration/manage-suppression-list.md)。

>[!NOTE]
>
>配置檔案 **[!UICONTROL Suppressed]** 在消息發送過程中，狀態被排除。 因此，當 **行程報告** 將顯示這些配置檔案在旅途中移動([讀取段](../building-journeys/read-segment.md) 和 [消息](../building-journeys/journeys-message.md) 活動), **電子郵件報告** 不會把它們包括在 **[!UICONTROL Sent]** 在發送電子郵件之前過濾掉度量。
>
>瞭解 [即時報告](../reports/live-report.md) 和 [全局報告](../reports/global-report.md)。 要查找所有排除案例的原因，可使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。

### 傳遞失敗 {#delivery-failures}

傳遞失敗時有兩種錯誤：

* **硬彈**。 硬彈出表示電子郵件地址無效（即電子郵件地址不存在）。 這涉及從接收電子郵件伺服器返回的消息，該消息明確地指出地址無效。
* **軟彈跳**。 這是為有效電子郵件地址發生的臨時電子郵件彈出。

A **硬彈** 自動將電子郵件地址添加到禁止顯示清單。

A **軟彈** <!--or an **ignored** error--> 在多次重試後，也會將電子郵件地址發送到隱藏清單。 [重試時瞭解更多資訊](../configuration/retries.md)

如果您繼續發送到這些地址，可能會影響您的交付率，因為它會告訴ISP您可能沒有遵循電子郵件地址清單維護最佳實踐，因此可能不是可信賴的發件人。

### 垃圾郵件投訴 {#spam-complaints}

禁止顯示清單收集將郵件標籤為垃圾郵件的電子郵件地址。 例如，如果某人向客戶服務部門寫信要求您不再接收您寄來的郵件，則該人的電子郵件地址將在您的整個實例中被禁止，您將無法再將其發送給該地址。

在收件人提交垃圾郵件投訴後向其發送可能會對您的發送聲譽產生巨大影響，因為它會通知ISP您可能會發送不想要的電子郵件，並且可能不會聽取收件人的資訊。

這可能導致IP地址或發送域被阻止，這在這些地址位於禁止清單中時可以避免。
