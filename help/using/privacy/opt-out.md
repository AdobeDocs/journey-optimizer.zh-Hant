---
solution: Journey Optimizer
product: journey optimizer
title: 管理選擇退出
description: 了解如何管理選擇退出與隱私權
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# 管理選擇退出 {#consent}

## 關於退出管理 {#about}

向收件者提供取消訂閱從品牌接收通訊的能力是一項法律規定。 深入了解 [Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}。

**為什麼這很重要？**

* 未遵守這些法規會為您的品牌帶來法律風險。
* 它可協助您避免傳送未經請求的通訊給收件者，這可能會使他們將您的訊息標示為垃圾訊息，並損害您的名譽。

## Journey Optimizer中的選擇退出管理 {#opt-out-ajo}

從歷程或行銷活動傳送訊息時，您必須一律確保客戶可取消訂閱未來的通訊。 取消訂閱後，設定檔會自動從未來行銷訊息的對象中移除。

同時 **[!DNL Journey Optimizer]** 提供管理電子郵件和簡訊中選擇退出的方式，推播通知不需要您邊上的任何動作，因為收件者可以透過其裝置本身取消訂閱。 例如，在下載或使用您的應用程式時，使用者可以選取停止通知。 同樣地，他們可以透過行動作業系統變更通知設定。

了解如何在以下章節中管理Journey Optimizer電子郵件和SMS訊息中的選擇退出：

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="銷售機會" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;&lt;a href=" ../email/email-opt-out.md"><strong>電子郵件選擇退出管理</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="不頻繁" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;
&lt;a href=" ../sms/sms-opt-out.md"><strong>SMS選擇退出管理</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>在 [!DNL Journey Optimizer]，則同意由Experience Platform處理 [同意結構](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target=&quot;_blank&quot;}。 依預設，同意欄位的值為空白，且視為同意接收您的通訊。 您可以在上線至所列的其中一個可能值時修改此預設值 [此處](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target=&quot;_blank&quot;}。