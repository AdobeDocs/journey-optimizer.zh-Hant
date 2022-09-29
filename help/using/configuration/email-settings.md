---
title: 設定電子郵件設定
description: 了解如何在通道表面層級配置電子郵件設定
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: 8a8950dbbda9a0a3aa498e304e41294ad343d0be
workflow-type: tm+mt
source-wordcount: '1188'
ht-degree: 2%

---

# 設定電子郵件設定 {#email-settings}

在通道表面的專用區段（即訊息預設集）設定中定義電子郵件設定。 了解如何在 [本節](channel-surfaces.md).

![](assets/preset-email-settings.png)

## 電子郵件類型 {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="定義電子郵件類別"
>abstract="選取使用此表面時要傳送的電子郵件類型：行銷促銷電子郵件，需要使用者同意，或非商業電子郵件的交易式，也可在特定內容中傳送給取消訂閱的設定檔。"

在 **電子郵件類型** 節，選擇將與曲面一起發送的消息類型： **行銷** 或 **交易**.

* 選擇 **行銷** 促銷電子郵件：這些訊息需要使用者同意。

* 選擇 **交易** 例如，非商業電子郵件（例如訂單確認、密碼重設通知或傳送資訊）。

>[!CAUTION]
>
>**交易** 可以傳送電子郵件給從行銷通訊取消訂閱的設定檔。 這些訊息只能在特定內容中傳送。

當 [建立訊息](../messages/get-started-content.md)，您必須選擇符合您為電子郵件選取之類別的有效管道表面。

## 子網域和IP池 {#subdomains-and-ip-pools}

在 **子網域和IP池** 部分，您必須：

1. 選取用來傳送電子郵件的子網域。 [了解更多](about-subdomain-delegation.md)

1. 選擇要與曲面關聯的IP池。 [了解更多](ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

在所選IP池下時，無法繼續建立曲面 [版本](ip-pools.md#edit-ip-pool) (**[!UICONTROL 處理]** 狀態)，且從未與選取的子網域相關聯。 否則，仍將使用最舊版本的IP池/子域關聯。 如果是這種情況，請將曲面另存為草稿，然後在IP池具有 **[!UICONTROL 成功]** 狀態。

>[!NOTE]
>
>對於非生產環境，Adobe不會建立現成可用的測試子網域，也不會授予對共用傳送IP池的存取權。 您需要 [委派您自己的子網域](delegate-subdomain.md) 並使用分配給您組織的池中的IP。

## 清單 — 取消訂閱 {#list-unsubscribe}

上 [選取子網域](#subdomains-and-ip-pools) 從清單中， **[!UICONTROL 啟用清單 — 取消訂閱]** 選項。

![](assets/preset-list-unsubscribe.png)

依預設，會啟用此選項。

如果您保留為啟用，取消訂閱的連結會自動納入電子郵件標題中，例如：

![](assets/preset-list-unsubscribe-header.png)

如果停用此選項，電子郵件標題中將不會顯示取消訂閱連結。

取消訂閱連結包含兩個元素：

* 安 **取消訂閱電子郵件地址**，所有取消訂閱的請求都會傳送至。

   在 [!DNL Journey Optimizer]，則預設會是「取消訂閱電子郵件地址」 **[!UICONTROL Mailto（取消訂閱）]** 顯示於通道表面的地址，根據 [選取的子網域](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* 此 **取消訂閱URL**，即登錄頁面的URL，一旦取消訂閱，系統會將使用者重新導向。

   如果您新增 [一鍵式選擇退出連結](../messages/consent.md#one-click-opt-out) 若要使用此介面建立訊息，取消訂閱URL將為一鍵式選擇退出連結所定義的URL。

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >若您未在訊息內容中新增一鍵式選擇退出連結，則不會向使用者顯示任何登陸頁面。

進一步了解如何在 [本節](../messages/consent.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## 標題參數{#email-header}

在 **[!UICONTROL 標題參數]** 部分，輸入與使用該曲面發送的電子郵件類型相關聯的發件人姓名和電子郵件地址。

>[!CAUTION]
>
>電子郵件地址必須使用目前選取的 [委派子網域](about-subdomain-delegation.md).

* **[!UICONTROL 寄件者名稱]**:寄件者的名稱，例如您的品牌名稱。

* **[!UICONTROL 寄件者電子郵件]**:您要用於通訊的電子郵件地址。 例如，如果委派的子網域為 *marketing.luma.com*，您可以使用 *contact@marketing.luma.com*.

* **[!UICONTROL 答復（姓名）]**:收件者點按 **回覆** 按鈕。

* **[!UICONTROL 回覆（電子郵件）]**:收件者點按 **回覆** 按鈕。 您必須使用在委派子網域上定義的位址(例如 *reply@marketing.luma.com*)，否則會捨棄電子郵件。

* **[!UICONTROL 錯誤電子郵件]**:在傳送數天郵件（非同步退信）後，ISP產生的所有錯誤都會在此位址上接收。

![](assets/preset-header.png)

>[!NOTE]
>
>地址必須以字母(A-Z)開頭，並且只能包含英數字元。 您也可以使用底線 `_`，點`.` 連字型大小 `-` 字元。

### 轉寄電子郵件 {#forward-email}

如果您想要轉送至特定電子郵件地址，則收到的所有電子郵件 [!DNL Journey Optimizer] 如需委派的子網域，請聯絡Adobe客戶服務。 您需要提供：

* 您選擇的轉寄電子郵件地址。 請注意，轉送電子郵件地址網域不能符合委派給Adobe的任何子網域。
* 您的沙箱名稱。
* 要使用轉發電子郵件地址的表面名稱。
* 目前 **[!UICONTROL 回覆（電子郵件）]** 在通道表面層設定的地址。

>[!NOTE]
>
>每個子網域只能有一個轉寄電子郵件地址。 因此，如果多個曲面使用相同的子域，則所有曲面都必須使用相同的轉發電子郵件地址。

轉寄電子郵件地址由Adobe設定。 這可能需要3到4天。

## 密件副本電子郵件 {#bcc-email}

您可以傳送由 [!DNL Journey Optimizer] 到BCC收件箱，在該收件箱中儲存這些郵件，以滿足合規性或歸檔目的。

要執行此操作，請啟用 **[!UICONTROL 密件副本電子郵件]** 通道曲面層的可選特徵。 [了解更多](archiving-support.md#bcc-email)

![](assets/preset-bcc.png)

## 電子郵件重試參數 {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="調整重試時間段"
>abstract="當電子郵件傳送因暫時軟退信錯誤而失敗時，將執行3.5天（84小時）的重試。 您可以調整此預設的重試時間段，以更符合您的需求。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/monitor-reputation/retries.html" text="關於重試"

您可以設定 **電子郵件重試參數**.

![](assets/preset-retry-parameters.png)

依預設， [重試時間段](retries.md#retry-duration) 設為84小時，但您可以調整此設定以更符合您的需求。

您必須在以下範圍內輸入整數值（以小時或分鐘為單位）:

* 若是行銷電子郵件，最低重試時間為6小時。
* 對於交易式電子郵件，最低重試期間為10分鐘。
* 對於這兩種電子郵件類型，最大重試時間為84小時（或5040分鐘）。

深入了解中的重試次數 [本節](retries.md).

## URL追蹤 {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="定義URL追蹤參數"
>abstract="使用本節來自動將追蹤參數附加至您電子郵件內容中出現的URL。 此功能是選取性的。"

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="預覽URL追蹤參數"
>abstract="檢閱如何將追蹤參數附加至電子郵件內容中出現的URL。"

您可以使用 **[!UICONTROL URL追蹤參數]** 來評估跨管道行銷工作的成效。 此功能是選取性的。

本節中定義的參數會附加至電子郵件訊息內容中所包含的URL結尾。 接著，您就可以在網頁分析工具(例如Adobe Analytics或Google Analytics)中擷取這些參數，並建立各種效能報表。

<!--Three URL tracking parameters are auto-populated as an example when you create a channel surface. You can edit these and add up to 10 tracking parameters using the **[!UICONTROL Add new parameter]** button.-->

您可以使用 **[!UICONTROL 新增參數]** 按鈕。

![](assets/preset-url-tracking.png)

若要設定URL追蹤參數，您可以直接在 **[!UICONTROL 名稱]** 和 **[!UICONTROL 值]** 欄位。

<!--You can also choose from a list of predefined values by navigating to the following objects:
* Journey attributes: **Source id**, **Source name**, **Source version id**
* Action attributes: **Action id**, **Action name**
* Offer decisioning attributes: **Offer id**, **Offer name**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>Do not select a folder: make sure to browse to the necessary folder and select a profile attribute to use as a tracking parameter value.-->

您也可以編輯 **[!UICONTROL 值]** 欄位使用 [運算式編輯器](../personalization/personalization-build-expressions.md). 按一下版本圖示以開啟編輯器。 從那裡，您可以選取所選內容屬性及/或直接編輯文字。

![](assets/preset-url-tracking-editor.png)

>[!NOTE]
>
>您可以從運算式編輯器中結合輸入文字值和使用內容屬性。 每個 **[!UICONTROL 值]** 欄位總共可包含最多255個字元。

<!--You can drag and drop the parameters to reorder them.-->

以下是Adobe Analytics和Google Analytics相容URL的範例。

* Adobe Analytics相容URL: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* Google Analytics相容URL: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

您可以動態預覽產生的追蹤URL。 每次添加、編輯或刪除參數時，預覽都會自動更新。

![](assets/preset-url-tracking-preview.png)