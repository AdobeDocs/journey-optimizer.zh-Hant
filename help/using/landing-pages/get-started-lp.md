---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用登陸頁面
description: 了解 Journey Optimizer 的登陸頁面
feature: Landing Pages, Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: 登陸、登陸頁面、開始、開始
exl-id: 0da96e32-52ad-4cc3-bac4-844b1f39ed16
source-git-commit: d0dd382521aeb2c7e18dc547c2ec55fa1472ab8d
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 14%

---

# 開始使用登陸頁面 {#get-started-lp}

登陸頁面是使用者從電子郵件、網站、廣告或任何其他數位位置按一下後被導向到的獨立網頁。

[!DNL Journey Optimizer]可讓您建立並設計登入頁面，將您的使用者導向線上表單，以便他們可以選擇加入或選擇退出接收您的通訊或特定服務（例如電子報）。

➡️ [透過此影片深入了解設定訂閱和建立登陸頁面](#video)

## 何時使用登入頁面 {#when-to-use}

當您想要執行以下動作時使用登入頁面：

* 讓客戶&#x200B;**透過電子郵件或行銷活動中的連結，選擇加入或選擇退出**&#x200B;行銷通訊或特定服務或電子報，包括目標服務的訂閱清單。 [閱讀全文](lp-use-cases.md#subscription-to-a-service)
* 在傳送通訊前&#x200B;**收集同意**，並在選擇加入或選擇退出時傳送&#x200B;**確認電子郵件**。 [閱讀全文](lp-use-cases.md#send-confirmation-email)
* **使用**&#x200B;資料擷取&#x200B;**[!UICONTROL 登陸頁面上的表單來擷取或更新設定檔資料]**，適用於漸進式設定檔、偏好設定、註冊及類似的情況。 [閱讀全文](#data-capture-lp)
* 將使用者重新導向至&#x200B;**專用網頁表單**，而不需在[!DNL Journey Optimizer]外部建立外部頁面
* 使用&#x200B;**的內容設計功能建置**&#x200B;回應式登陸頁面[!DNL Journey Optimizer]

### 使用登入頁面擷取資料 {#data-capture-lp}

**[!UICONTROL 資料擷取]**&#x200B;登陸頁面可讓您內嵌已發佈的表單，讓訪客透過表單預設集中設定的串流連線，提交寫入您[!DNL Adobe Experience Platform]資料集的屬性。 [瞭解如何在登入頁面中建立和內嵌表單](lp-forms.md)

>[!NOTE]
>
>**已知設定檔** （在[!DNL Adobe Experience Platform]中識別的現有設定檔）支援透過登入頁面表單擷取資料。 登入頁面應從&#x200B;**個人化連結** （例如來自電子郵件促銷活動）開啟，以便在頁面載入時解析設定檔身分。

以下是範例使用案例：

1. **漸進式設定檔擴充** — 透過個人化登陸頁面，從已知客戶收集額外屬性（例如電話號碼、出生日期或地點），以擴充其現有的[!DNL Experience Platform]設定檔，以進行細分和個人化。

2. **偏好設定中心更新** — 允許已知訂閱者透過登陸頁面管理其通訊偏好設定（頻道、主題興趣），變更通常會在大約15分鐘內反映在其[!DNL Experience Platform]設定檔中。

3. **事件或網路研討會註冊** — 從註冊頁面上的已知設定檔擷取事件特定資料，使用註冊屬性更新設定檔，並觸發確認歷程。

4. **忠誠度或方案註冊** — 透過登入頁面提交其他詳細資料，豐富下游目標定位的設定檔，讓現有客戶註冊忠誠度方案或會員等級。

5. **競賽或競賽專案** — 讓已知客戶透過登陸頁面表單進入競賽或抽獎；擷取專案特定的詳細資訊（回答、偏好設定或宣告），並將它們寫入設定檔以支援資格、獲勝者選擇和後續歷程。

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-lp.md">
<img alt="銷售機會" src="../assets/do-not-localize/lp-subscription.jpeg">
</a>
<div><a href="create-lp.md"><strong>建立登陸頁面</strong>
</div>
<p>
</td>
<td>
<a href="subscription-list.md">
<img alt="不頻繁" src="../assets/do-not-localize/lp-list.jpg">
</a>
<div>
<a href="subscription-list.md"><strong>建立訂閱清單</strong></a>
</div>
<p></td>
<td>
<a href="lp-forms.md">
<img alt="Journey Optimizer中登入頁面的Forms清單" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>在您的登入頁面中使用表單</strong></a>
</div>
<p>
</td>
<td>
<a href="../reports/lp-report-live.md">
<img alt="驗證" src="../assets/do-not-localize/lp-reporting.jpg">
</a>
<div>
<a href="../reports/lp-report-live.md"><strong>報告</strong></a>
</div>
<p>
</td>
</tr></table>

## 開始之前 {#prerequisites}

在建立登入頁面之前，請先完成下列設定步驟：

1. **設定子網域** — 設定專用於託管登陸頁面的子網域。 [了解更多](lp-subdomains.md)
1. **建立登陸頁面預設集** — 預設集會定義套用至登陸頁面的子網域和其他設定。 [了解更多](lp-presets.md#lp-create-preset)
1. **建立訂閱清單** （針對訂閱使用案例） — 如果您希望客戶訂閱或取消訂閱特定服務，則此為必要專案。 [了解更多](subscription-list.md)
1. **建立表單** （用於資料擷取使用案例） — 當您想要在&#x200B;**[!UICONTROL 資料擷取]**&#x200B;登陸頁面上內嵌表單並將提交內容傳送到[!DNL Experience Platform]時需要。 [了解更多](lp-forms.md)

## 運作方式 {#how-it-works}

建立及部署登入頁面的順序如下：

1. **建立並設定您的登陸頁面** — 選取預設集、設定主要頁面，然後新增任何必要的子頁面。 [了解更多](create-lp.md#create-landing-page)
1. **設計頁面** — 使用[!DNL Journey Optimizer]的拖放編輯器建置頁面內容和表單。 [了解更多](design-lp.md)
1. **測試並發佈您的登入頁面** — 預覽頁面、測試表單行為，然後發佈使其上線。 [了解更多](create-lp.md#test-landing-page)
1. **訊息或歷程中的連結** — 將登入頁面URL新增至電子郵件、行銷活動或歷程動作，讓客戶可以存取。 [了解更多](../email/message-tracking.md#insert-links)

## 作法影片{#video}

以下影片說明如何建立訂閱清單、設定登入頁面以選擇加入或選擇退出服務、將選擇加入/選擇退出選項整合至訊息並設定相關歷程。

>[!VIDEO](https://video.tv.adobe.com/v/341280?quality=12&learn=on)
