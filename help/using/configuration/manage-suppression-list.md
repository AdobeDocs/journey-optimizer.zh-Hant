---
title: 管理隱藏清單
description: '了解如何存取及管理Journey Optimizer隱藏清單 '
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: 應用程式設定
topic: 管理
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 1%

---


# 管理隱藏清單 {#manage-suppression-list}

透過[!DNL Journey Optimizer]，您可以監控自動排除而無法在歷程中傳送的所有電子郵件地址，例如：

* 無效（硬跳出）或一致軟跳出的位址，如果您繼續將這些位址納入傳送中，可能會對您的電子郵件信譽造成負面影響。
* 對您的其中一封電子郵件發出某種垃圾郵件投訴的收件人。

<!--Profiles who unsubscribe from your sendings. Learn more on [opting-out](../consent.md). NOT TRUE as confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

此類電子郵件地址會自動收集到Journey Optimizer **隱藏清單**&#x200B;中。 進一步了解[本節](../suppression-list.md)。

## 訪問隱藏清單 {#access-suppression-list}

若要存取排除的電子郵件地址的詳細清單，請開啟「**[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]**」功能表，然後按一下「**[!UICONTROL View suppression lists]**」連結。

![](../assets/suppression-list-link.png)

篩選器可協助您瀏覽清單。

![](../assets/suppression-list-filters.png)

<!--suppression date,  category and reason, but on staging, only creation date filter is available-->

<!--You can also download the list as a CSV file for analysis and reporting purpose. Won't be available.-->

## 隱藏類別和原因 {#suppression-categories-and-reasons}

當訊息無法傳送至電子郵件地址時，Journey Optimizer會判斷傳送失敗的原因，並將其與隱藏類別建立關聯。

隱藏類別如下：

* **硬**:會立即將電子郵件地址發送到隱藏清單。

* **軟**:一旦錯誤計數器達到限制臨界值，軟錯誤就會將地址發送到隱藏清單。[重試時了解更多](retries.md)

* **已忽略**:
   * 當有效電子郵件地址發生錯誤，但已知為暫時錯誤（例如連接嘗試失敗或暫時性技術問題）時，一旦錯誤計數器達到限制閾值，就會將電子郵件地址添加到隱藏清單中。 [深入了解重試次數](retries.md)。
   * 當錯誤是垃圾郵件投訴的結果時，發出投訴的收件人的電子郵件地址將立即發送到隱藏清單。

<!--**Manual**: You can also manually add an email address to the suppression list. => Manual category will be available when manually adding an address to the suppression list (via API)-->

>[!NOTE]
>
>在[傳送失敗類型](../suppression-list.md#delivery-failures)區段中，深入了解軟退信和硬退信。

對於列出的每個電子郵件地址，您也可以檢查&#x200B;**[!UICONTROL Reason]**&#x200B;是否排除它，以及它添加到隱藏清單的日期/時間。

![](../assets/suppression-list-temp.png)
<!--to replace with suppression-list.png when Manual category is available (through API)-->

傳送失敗的可能原因有：

| 原因 | 說明 | 隱藏類別 |
---------|----------|--------- |
| **[!UICONTROL Undetermined]** | 無法識別從收件者網域訊息傳輸代理(MTA)收到的退信原因。 | 已忽略 |
| **[!UICONTROL Invalid Recipient]** | 收件者無效或不存在。 | 硬 |
| **[!UICONTROL Soft Bounce]** | 消息軟退信的原因不是此表中列出的軟錯誤，例如當發送超出ISP建議的允許速率時。 | 軟 |
| **[!UICONTROL DNS Failure]** | 由於DNS失敗而退信。 | 軟 |
| **[!UICONTROL Mailbox Full]** | 由於收件者的信箱已滿而無法接受更多訊息，訊息已退信。 | 軟 |
| **[!UICONTROL Too Large]** | 郵件已退信，因為它對收件者太大。 [](retries.md) 將執行檢索：您可以編輯訊息大小，然後重新插入以供傳送。 | 已忽略 |
| **[!UICONTROL Timeout]** | 訊息逾時，表示其已軟退信，並達到訊息重試限制（3.5天）。 | 已忽略 |
| **[!UICONTROL Admin Failure]** | 根據發送系統管理員配置的策略，消息失敗。<!--For example, if emails are blackholed at the global, domain or binding level using the "blackhole" directive, this bounce code is used.--> | 已忽略 |
| **[!UICONTROL Generic Bounce: No RCPT]** | 無法確定該郵件的收件人。 | 已忽略 |
| **[!UICONTROL Generic Bounce]** | 訊息因未指定原因而失敗。 | 已忽略 |
| **[!UICONTROL Mail Block]** | 接收者已封鎖訊息（即收件者MTA）。 | 已忽略 |
| **[!UICONTROL Spam Block]** | 接收者已封鎖該訊息，因為該訊息來自已知的垃圾訊息來源。 例如，它可能是傳送IP區塊。 | 已忽略 |
| **[!UICONTROL Spam Content]** | 接收者（收件者MTA）將訊息內容封鎖為垃圾訊息。 | 已忽略 |
| **[!UICONTROL Prohibited Attachment]** | 由於郵件包含附件，因此被接收者阻止。 | 已忽略 |
| **[!UICONTROL Relaying Denied]** | 由於不允許中繼，因此接收器阻止了該消息。 | 軟 |
| **[!UICONTROL Auto-Reply]** | 郵件是自動回覆/休假郵件。 | 已忽略 |
| **[!UICONTROL Transient Failure]** | 消息傳輸已暫時延遲。 | 已忽略 |
| **[!UICONTROL Challenge-Response]** | 該消息是挑戰 — 響應探測。 | 軟 |

>[!NOTE]
>
>未訂閱的使用者沒有收到來自[!DNL Journey Optimizer]的電子郵件，因此其電子郵件地址無法傳送至隱藏清單。 其選項會在Experience Platform層級處理。 深入了解[選擇退出](../consent.md)。

<!--
Removed from the table provided by SparkPost/Momentum:
| **[!UICONTROL Subscribe]** | The message is a subscribe request. | Ignored |
| **[!UICONTROL Unsubscribe]** | The message is an unsubscribe request. | Hard |
-->

<!--Note to add eventually: If a user is subscribed and [!DNL Journey Optimizer] fails to send emails to their subscribed email address, they will get added to the suppression list. (not sure it's possible to subscribe through AJO or need to find reference to Experience Platform doc?)-->


