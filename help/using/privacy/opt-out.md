---
solution: Journey Optimizer
product: journey optimizer
title: 管理選擇退出
description: 瞭解如何管理選擇退出與隱私權
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 8b459f71852d031dc650b77725bdc693325cdb1d
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 100%

---

# 管理選擇退出 {#consent}

向接收者提供取消訂閱接收來自品牌通訊的功能是一項法律要求，同時確保此選擇獲得遵守。 進一步瞭解 [Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=zh-Hant#regulations)的適用法規。{target="_blank"}

**為什麼這很重要？**

* 若未遵守這些法規，您的品牌將面臨法律風險。
* 它可協助您避免傳送未經請求的通訊給您的收件者，這可能會使他們將您的訊息標示為垃圾訊息，並損害您的聲譽。

## 管理歷程和行銷活動中的取消訂閱 {#opt-out-ajo}

從歷程或行銷活動傳送訊息時，您必須一律確保客戶可取消訂閱未來的通訊。 取消訂閱後，個人資料將自動從未來行銷訊息的對象中移除。

**[!DNL Journey Optimizer]** 提供管理電子郵件和簡訊訊息中選擇退出的方式，而推播通知不需要由您執行任何動作，因為收件者可以透過其裝置自行取消訂閱。 例如，在下載或使用您的應用程式時，他們可以選擇停止通知。 同樣地，他們也可以透過行動裝置作業系統變更通知設定。

在以下章節中了解如何管理 Journey Optimizer 電子郵件和簡訊訊息中的選擇退出：

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="銷售機會" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%">
</a>
<div><a href="../email/email-opt-out.md"><strong>電子郵件選擇退出管理</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="不頻繁" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%">
</a>
<div>
<a href="../sms/sms-opt-out.md"><strong>簡訊選擇退出管理</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>在 [!DNL Journey Optimizer]，同意由 Experience Platform [同意綱要](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=zh-Hant)處理{target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=zh-Hant#choice-values){target="_blank"}。

## 實施個人化同意 {#opt-out-personalization}

您的客戶也可以選擇退出提供的個人化內容。 設定檔從個人化選擇退出後，您需要確保其資料不會用於個人化，且您必須使用遞補變體取代任何個人化內容。

### 在決策管理中

運用優惠方案時，個人化偏好設定不會自動於使用來自[決策](../offers/api-reference/offer-delivery-api/decisioning-api.md) API 請求或 [邊緣決策](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md) API 請求的[決定範圍](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)實施。 在這種情況下，您需要手動強制執行個人化同意。 若要執行此操作，請遵循下列步驟。

>[!NOTE]
>
>[!DNL Journey Optimizer]發起管道中使用的決定範圍符合其所屬歷程或行銷活動的這項要求。



1. 建立 [Adobe Experience Platform 區段](../segment/about-segments.md)，使用設定檔屬性，例如：*「同意個人化= True」*，將目標鎖定在同意個人化的使用者。 

1. 建立[決定](../offers/offer-activities/create-offer-activities.md)時，新增決定範圍，並根據此區段為包含個人化優惠的每個評估條件集合定義適用性限制。

1. 建立不包括個人化內容的[遞補優惠](../offers/offer-library/creating-fallback-offers.md)。

1. 將非個人化遞補優惠[指派](../offers/offer-activities/create-offer-activities.md#add-fallback)至決定。

1. [檢閱並儲存](../offers/offer-activities/create-offer-activities.md#review)決定。

如果使用者：

* 同意個人化，決定範圍將決定該設定檔的最佳優惠。

* 未同意個人化，對應的設定檔將不符合評估條件中的任何優惠方案資格，因此將收到非個人化的遞補優惠方案。

>[!NOTE]
>
>尚未支援 [!DNL Journey Optimizer] 中將設定檔資料用於[資料模式](../offers/ranking/ai-models.md)的同意。

