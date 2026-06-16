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
TQID: https://experienceleague.adobe.com/wr4XGNostKoN8jZ50VRAQPoGg9tsNhMOyJGEt1mASso
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: b19d9237-76be-466d-a869-aacf2d72205fid: fb9a80eb-bebc-492f-a0e9-584595621ebbid: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2956c3df01f4b2e753111ecf54163ec4084fecf2
workflow-type: tm+mt
source-wordcount: 781
ht-degree: 94%

---

# 開始使用登陸頁面 {#get-started-lp}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;登陸頁面將電子郵件、廣告或行銷活動的點按轉換為專用的網頁目的地，客戶可在此選擇加入或退出、管理其偏好設定，以及共用設定檔資料，協助您發展同意的受眾，並擷取推動個人化的第一方資料。

>[!ENDSHADEBOX]

登陸頁面是使用者從電子郵件、網站、廣告或任何其他數位位置按一下後被導向到的獨立網頁。

[!DNL Journey Optimizer] 可讓您建立和設計登陸頁面，將使用者引導至線上表單，讓他們可以選擇加入或選擇退出接收通訊或電子報等特定服務。

➡️ [透過此影片深入了解設定訂閱和建立登陸頁面](#video)

## 何時使用登陸頁面 {#when-to-use}

當您想要執行以下動作時使用登陸頁面：

* 讓客戶透過電子郵件或行銷活動中的連結，**選擇加入或選擇退出**&#x200B;行銷通訊或特定服務或電子報，包括目標服務的訂閱清單。 [閱讀全文](lp-use-cases.md#subscription-to-a-service)
* 選擇加入或選擇退出時，請在傳送通訊前&#x200B;**收集同意**&#x200B;並傳送&#x200B;**確認電子郵件**。 [閱讀全文](lp-use-cases.md#send-confirmation-email)
* 使用&#x200B;**[!UICONTROL 資料擷取]**&#x200B;登陸頁面上的表單來&#x200B;**擷取或更新輪廓資料**，適用於漸進式輪廓分析、偏好設定、註冊及類似的情況。 [閱讀全文](#data-capture-lp)
* 將使用者重新導向至&#x200B;**專用網頁表單**，而無需在 [!DNL Journey Optimizer] 外部建立外部頁面
* 使用 [!DNL Journey Optimizer] 的內容設計功能建立&#x200B;**回應式登陸頁面**

### 使用登陸頁面擷取資料 {#data-capture-lp}

**[!UICONTROL 資料擷取]**&#x200B;登陸頁面可讓您嵌入已發佈的表單，讓訪客透過表單預設集中設定的串流連線，提交寫入 [!DNL Adobe Experience Platform] 資料集的屬性。 [瞭解如何在登陸頁面中建立和嵌入表單](lp-forms.md)

>[!NOTE]
>
>**已知輪廓** (在 [!DNL Adobe Experience Platform] 中識別的現有輪廓) 支援透過登陸頁面表單擷取資料。 登陸頁面應從&#x200B;**個人化連結** (例如來自電子郵件行銷活動) 開啟，以便在頁面載入時解析輪廓身分。

以下是範例使用案例：

1. **漸進式輪廓擴充** — 透過個人化登陸頁面，從已知客戶收集額外屬性 (例如電話號碼、出生日期或地點)，以擴充其現有的 [!DNL Experience Platform] 輪廓，以進行細分和個人化。

2. **偏好設定中心更新** — 允許已知訂閱者透過登陸頁面管理其通訊偏好設定 (管道、主題興趣)，變更通常會在大約 15 分鐘內反映在其 [!DNL Experience Platform] 輪廓中。

3. **事件或網路研討會註冊** — 從註冊頁面上的已知輪廓擷取事件特定資料，使用註冊屬性更新輪廓，並觸發確認歷程。

4. **忠誠度或方案註冊** — 透過登陸頁面提交其他詳細資料，擴充輪廓以進行下游目標定位，從而讓現有客戶註冊忠誠度方案或會員等級。

5. **競爭或競賽參與** — 讓已知客戶透過登陸頁面表單參與競賽或抽獎；擷取參與特定的詳細資料 (回答、偏好設定或宣告)，並將它們寫入輪廓以支援資格、獲勝者選擇和後續歷程。

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
<img alt="不常使用" src="../assets/do-not-localize/lp-list.jpg">
</a>
<div>
<a href="subscription-list.md"><strong>建立訂閱清單</strong></a>
</div>
<p></td>
<td>
<a href="lp-forms.md">
<img alt="Journey Optimizer 中登陸頁面的表單清單" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>在您的登陸頁面中使用表單</strong></a>
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

在建立登陸頁面之前，請先完成下列設定步驟：

1. **設定子網域** — 設定專用於託管登陸頁面的子網域。 [了解更多](lp-subdomains.md)
1. **建立登陸頁面預設集** — 預設集會定義套用至登陸頁面的子網域和其他設定。 [了解更多](lp-presets.md#lp-create-preset)
1. **建立訂閱清單** (針對訂閱使用案例) — 如果您希望客戶訂閱或取消訂閱特定服務，則此為必要步驟。 [了解更多](subscription-list.md)
1. **建立表單** (針對資料擷取使用案例) — 如果您想要在&#x200B;**[!UICONTROL 資料擷取]**&#x200B;登陸頁面上嵌入表單並將提交內容傳送到 [!DNL Experience Platform]，則此為必要步驟。 [了解更多](lp-forms.md)

## 運作方式 {#how-it-works}

建立及部署登陸頁面的步驟順序如下：

1. **建立並設定您的登陸頁面** — 選取預設集、設定主要頁面，然後新增任何必要的子頁面。 [了解更多](create-lp.md#create-landing-page)
1. **設計頁面** — 使用 [!DNL Journey Optimizer] 的拖放編輯器建立頁面內容和表單。 [了解更多](design-lp.md)
1. **測試並發佈您的登陸頁面** — 預覽頁面、測試表單行為，然後發佈以使其上線。 [了解更多](create-lp.md#test-landing-page)
1. **訊息或歷程中的連結** — 將登陸頁面 URL 新增至電子郵件、行銷活動或歷程動作，以方便客戶存取。 [了解更多](../email/message-tracking.md#insert-links)

## 作法影片{#video}

以下影片說明如何建立訂閱清單、設定登陸頁面以選擇加入或選擇退出服務、將選擇加入/選擇退出選項整合至訊息以及設定相關歷程。

>[!VIDEO](https://video.tv.adobe.com/v/341280?quality=12&learn=on)

➡️ **在實作中檢視：**&#x200B;探索[登陸頁面使用案例](lp-use-cases.md)，以取得涵蓋訂閱管理、確認電子郵件及資料擷取案例的逐步範例。
