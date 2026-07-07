---
solution: Journey Optimizer
product: journey optimizer
title: CNIL對電子郵件追蹤畫素的指引
description: 瞭解CNIL關於電子郵件追蹤畫素的更新指引，以及可支援您合規努力的Adobe Journey Optimizer控制項。
feature: Privacy, Consent Management
topic: Content Management
role: User
level: Intermediate
keywords: CNIL，追蹤，畫素，電子郵件，同意，選擇退出，隱私權
source-git-commit: b55af0fe5510f37049713fe8d0b7a2ac73516323
workflow-type: tm+mt
source-wordcount: '1466'
ht-degree: 1%

---


# 瞭解CNIL更新的電子郵件追蹤畫素指南 {#cnil-pixel-tracking}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解CNIL在2026年4月關於電子郵件追蹤畫素的建議，並探索Adobe Journey Optimizer控制項 — 開啟追蹤切換、連結層級追蹤、同意管理、選擇退出機制和隱藏 — 可以支援您的合規工作。

>[!ENDSHADEBOX]

此頁面僅供參考。 這不是法律建議，也不保證您遵守適用法律。 底下所述的Adobe Journey Optimizer產品功能是建置區塊，若妥善設定和運作，可支援相容的實作。 每位客戶都有責任決定及遵守其適用法律所規範的義務。

## 概觀 {#overview}

在2026年4月14日，法國資料保護機構&#x200B;*Commission National de l&#39;Informatique et des Libertés* (CNIL)發佈了一項關於在電子郵件中使用追蹤畫素的[建議](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf)。 此指引澄清何時需要同意，並強調正確同意實務對於電子郵件畫素追蹤的重要性。 此政策可能會影響任何實體傳送電子郵件給法國訂閱者的傳送實務。

CNIL從建議之日起提供三個月的時間，讓公司通知其電子郵件收件者（「使用者」）追蹤畫素的存在、其目的和使用者選擇退出的權利。 在此轉換期間，客戶應通知使用者畫素追蹤的相關資訊，並視需要提供選擇退出。 **CNIL預計在2026年7月14日之後開始執行活動。**

由於CNIL和其他監管機構會釐清追蹤畫素和相關問題的指引，Adobe將繼續監控更新，並通知客戶支援Adobe Journey Optimizer等電子郵件行銷的Adobe產品的技術功能。

Adobe Journey Optimizer提供的控制項可協助客戶管理傳送層級的開啟追蹤。 根據適用的CNIL指引和其他法律，客戶有責任決定自己的合規義務，但這些功能可能會支援客戶合規工作。

### 什麼是電子郵件追蹤畫素 {#tracking-pixel}

電子郵件追蹤畫素是內嵌在電子郵件HTML中的1x1透明影像。 收件者的電子郵件使用者端載入該影像時，畫素會偵測伺服器並記錄時間戳記、裝置型別、電子郵件使用者端等資料，有時還會偵測大致位置的IP位址。 然後，該記錄會繫結至收件者的記錄，讓行銷人員檢視電子郵件是否已開啟。

### 客戶支援 {#support}

尋求協助實作上述變更的客戶可與其現有的Adobe生態系統互動。 如有關於所引用Adobe功能的技術問題，請聯絡您的客戶成功經理或技術客戶經理。

## 與電子郵件追蹤相關的Adobe Journey Optimizer功能 {#ajo-functionality}

Adobe Journey Optimizer提供數種原生控制項，協助客戶處理CNIL指引的內容。 以下各節將說明相關的產品功能。

### 電子郵件型別分類 {#email-type}

在Adobe Journey Optimizer中，每個電子郵件通道設定都會分類為行銷或異動。 此分類會決定是否需要在傳送前取得訂閱者同意。

* **行銷電子郵件**：傳送給選擇加入的訂閱者的促銷通訊。 需要使用者同意。 這些電子郵件會自動遵循隱藏和選擇退出偏好設定。
* **異動電子郵件**：非商業通訊（例如，訂單確認、密碼重設）。 根據適用法律，這些資料可以傳送給已取消訂閱行銷通訊的設定檔。

電子郵件型別設定在[頻道設定](../email/email-settings.md#email-type)層級。 在歷程或行銷活動中製作電子郵件時，作者必須選取電子郵件型別符合通訊性質的管道設定。 此分類會通知在傳遞前套用哪些同意檢查。

### 開啟追蹤控制項 {#open-tracking}

Adobe Journey Optimizer可讓行銷人員控制個別訊息層級的開啟追蹤（即1x1畫素）。 在歷程或行銷活動中建立電子郵件時，訊息屬性面板中有兩個追蹤選項可用：

* **[!UICONTROL 電子郵件開啟次數]**：控制電子郵件中是否包含開啟追蹤畫素。 依預設，會啟用此選項。
* **[!UICONTROL 點按電子郵件]**：控制是否追蹤連結點按。 此選項也依預設為啟用。

若要停用特定電子郵件的開啟追蹤，請在建立您的郵件時取消勾選&#x200B;**[!UICONTROL 電子郵件開啟次數]**&#x200B;選項。 停用時，選項會防止收集該傳送的開啟追蹤資料。 對於傳送給法國訂閱者的組織，請在執行日期之前檢閱所有作用中歷程和行銷活動的開啟追蹤設定。

<!--
EDITORIAL NOTE – ENGINEERING CONFIRMATION NEEDED before publish:
Clarify whether unchecking "Email opens" fully removes the 1x1 tracking pixel from the delivered HTML, or whether the pixel is still present in the HTML but open data is suppressed at the data processing layer only. The current wording ("prevents open tracking data from being collected") is intentionally neutral. If the pixel is removed: update to state this explicitly. If the pixel remains but data is not processed: reword to make that distinction clear, to avoid misleading customers seeking CNIL compliance.
-->

[瞭解如何追蹤訊息](../email/message-tracking.md)

### 連結層級追蹤管理 {#link-tracking}

除了每則訊息的開啟追蹤切換外，Adobe Journey Optimizer的電子郵件Designer提供精細的控制功能，讓您掌控要追蹤的URL。 使用電子郵件Designer中的&#x200B;**[!UICONTROL 連結]**&#x200B;面板，作者可以檢視訊息中的所有追蹤URL，並個別設定每個連結的追蹤模式。

每個連結的可用追蹤模式包括：

* **已追蹤**：啟動追蹤此 URL。
* **選擇退出**：將此URL指定為選擇退出或取消訂閱URL。
* **映象頁面**：將此URL指定為映象頁面連結。
* **從不**：無論訊息層級的設定為何，都不會為此URL啟用追蹤。

設定特定連結至&#x200B;**永不**&#x200B;有助於確保即使啟用訊息層級追蹤，仍不會追蹤某些URL。

[瞭解如何在電子郵件Designer中管理追蹤](../email/message-tracking.md#manage-tracking)

### 同意擷取和管理 {#consent-management}

Adobe Journey Optimizer透過Adobe Experience Platform (AEP) [同意和偏好設定結構描述](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=zh-Hant){target="_blank"}處理同意。 同意偏好設定會儲存在設定檔層級，並在歷程和行銷活動執行期間自動強制執行。

與電子郵件追蹤相關的主要同意屬性包括：

* **`consents.marketing.email.val`**：主要電子郵件行銷同意欄位。 值`y`表示選擇加入；`n`表示選擇退出。 預設會將空白值視為同意（此預設可在上線時變更）。

### 選擇退出與撤銷機制 {#opt-out}

Adobe Journey Optimizer為訂閱者提供多種選擇退出通訊和管理其偏好設定的機制，所有這些都可在Adobe Experience Platform中更新設定檔的同意屬性。

**按一下取消訂閱（電子郵件標題）**

在電子郵件通道設定中開啟&#x200B;**[!UICONTROL 啟用List-Unsubscribe]**&#x200B;選項時，一鍵取消訂閱URL和mailto位址會自動新增至電子郵件標題。 收件者可直接選擇退出其電子郵件使用者端，而不需按一下電子郵件內文。 新通道設定預設會啟用此選項。

[瞭解如何設定清單取消訂閱](../email/list-unsubscribe.md)

**一鍵選擇退出（電子郵件內文）**

作者可以使用電子郵件Designer，直接在電子郵件內容中插入一鍵退出連結。 收件者按一下此連結時，就會立即更新其偏好設定。 選擇退出的適用範圍為以下其中一項：

* **頻道層級**：將設定檔退出所有未來跨頻道的電子郵件通訊。
* **身分層級**：僅選擇退出目前郵件中使用的特定電子郵件地址。

[瞭解如何新增一鍵退出連結](../email/email-opt-out.md#one-click-opt-out)

透過登陸頁面&#x200B;**偏好設定中心**

Adobe Journey Optimizer的原生登陸頁面功能可讓組織建立偏好設定中心，讓訂閱者可管理其通訊和追蹤偏好設定。 當訂閱者提交偏好設定中心表單時，他們的選擇會寫回到「同意和偏好設定」欄位群組中的其AEP設定檔屬性。

對於CNIL法規遵循情況，偏好設定中心登陸頁面可以從電子郵件頁尾連結（不同於取消訂閱連結），因此收件者可以管理其追蹤偏好設定，而不受其訂閱狀態的影響。

[瞭解如何管理客戶的偏好設定](../action/preference-center.md)

### 同意處理與強制執行 {#consent-enforcement}

收件者透過上述任何機制選擇退出時，會發生下列情況：

* 設定檔的同意屬性(`consents.marketing.email.val`)在Adobe Experience Platform中更新為`n`。
* 設定檔會立即從歷程和行銷活動中的未來行銷電子郵件傳送中排除。
* 退出資訊會儲存在AEP同意服務資料集中。
* Journey Optimizer會在每次傳送前在管道層級執行同意檢查，確保退出的設定檔不會接收行銷通訊。

[進一步瞭解選擇退出管理](opt-out.md)

### 同意原則 {#consent-policies}

組織可以在Adobe Journey Optimizer中建立並強制執行同意原則，以確保只有符合特定同意條件的設定檔才會接收通訊。 同意原則可透過行銷動作與管道設定相關聯。

[瞭解如何使用同意政策](../action/consent.md)

### 隱藏清單與重新請求 {#suppression}

Adobe Journey Optimizer會自動管理隱藏清單，其中包含導致硬退信、軟退信或垃圾郵件投訴的電子郵件地址。 隱藏清單上的設定檔會從未來的行銷傳送中排除。

Journey Optimizer隱藏REST API提供對傳出訊息的額外程式化控制，可讓組織透過API管理隱藏和允許清單行為。

[瞭解如何管理隱藏清單](../configuration/manage-suppression-list.md)

<!--
EDITORIAL NOTE – ENGINEERING CONFIRMATION NEEDED before publish:
AJO has no native equivalent of Campaign v8's "lastPixelRefusalDate" field or re-solicitation typology rule. If re-solicitation governance for pixel consent refusal is required, customers would likely need to: (a) create a custom XDM date field to capture the pixel refusal date, and (b) build an AEP audience that filters out profiles where that date falls within the last six months, then use that audience as a suppression filter in campaigns/journeys. Confirm with Engineering: (1) whether this guidance should be included in this article, and (2) whether any native AJO improvements are planned in this area.
-->

### 報表 {#reporting}

Adobe Journey Optimizer的電子郵件報告透過[即時報告](../reports/live-report.md)和[Customer Journey Analytics報告](../reports/report-gs-cja.md)提供開啟和點按量度。 當針對郵件停用&#x200B;**[!UICONTROL 電子郵件開啟]**&#x200B;追蹤時，將不會收集該傳遞的開啟資料；報告只會反映點按次數和其他參與訊號。

