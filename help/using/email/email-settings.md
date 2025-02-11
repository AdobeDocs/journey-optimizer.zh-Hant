---
solution: Journey Optimizer
product: journey optimizer
title: 設定電子郵件設定
description: 了解如何在通道設定層級進行電子郵件設定
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: 設定、電子郵件、設定
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: a1bdbc741a96325d71562b8f5ce5279096689cf0
workflow-type: tm+mt
source-wordcount: '2834'
ht-degree: 100%

---

# 設定電子郵件設定 {#email-settings}

若要開始建立電子郵件，您必須設定電子郵件頻道設定，定義郵件所需的所有技術參數。[了解如何建立設定](../configuration/channel-surfaces.md)

>[!NOTE]
>
>為了維護您的聲譽並改善您的傳遞能力，在建立電子郵件設定之前，請設定您用於傳送電子郵件的子網域。[了解更多](../configuration/about-subdomain-delegation.md)

在頻道設定的專用區段中定義電子郵件設定，如下所述。

![](assets/surface-email-settings.png){width="50%" align="left"}

電子郵件設定依照下列邏輯傳送通訊：

* 對於批次歷程，不適用於在進行電子郵件表面設定之前已啟動的批次執行。變更將在下次重複或新執行時生效。

* 若是交易型訊息，下次通訊時會立即套用變更（最多延遲五分鐘）。

>[!NOTE]
>
>更新的電子郵件組態設定會在使用該設定的歷程或行銷活動中自動套用。

## 電子郵件類型 {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="定義電子郵件類型"
>abstract="選取使用此設定時將傳送的電子郵件類型：促銷用的行銷型電子郵件 (需使用者同意)，或非商業的交易型電子郵件 (還可在特定情況下傳送至取消訂閱的輪廓)。"

在&#x200B;**電子郵件類型**&#x200B;區段中，選取設定的訊息類型：**[!UICONTROL 行銷]**&#x200B;或&#x200B;**[!UICONTROL 交易型]**。

* 對於促銷電子郵件，請選取&#x200B;**行銷**，例如零售商店的每週促銷活動。這些訊息需要使用者同意。

* 對於非商業電子郵件，請選取&#x200B;**交易型**，例如訂購確認、密碼重設通知或傳遞資訊。這些電子郵件可以傳送給&#x200B;**取消訂閱**&#x200B;行銷通訊的使用者。這些訊息只能在特定情境中傳送。

建立訊息時，您必須選擇符合您為電子郵件選取之類別的有效頻道設定。

## 子網域 {#subdomains}

選取要用來傳送電子郵件的子網域。

>[!NOTE]
>
>為了增加對電子郵件設定的控制，您可以定義動態子網域。[了解更多](../email/surface-personalization.md#dynamic-subdomains)

為了維護您網域的聲譽、加快 IP 暖身過程並改善傳遞能力，請將您的傳送子網域委派給 Adobe。[了解更多](../configuration/about-subdomain-delegation.md)

## IP 集區詳細資料 {#ip-pools}

選取要與設定關聯的 IP 集區。[了解更多](../configuration/ip-pools.md)

![](assets/surface-subdomain-ip-pool.png){width="50%" align="left"}

當選取的 IP 集區處於[版本](../configuration/ip-pools.md#edit-ip-pool)（**[!UICONTROL 處理中]**&#x200B;狀態）且從未與所選子網域關聯時，您無法繼續建立設定。否則，仍會使用 IP 集區/子網域關聯的最舊版本。如果是這種情況，請將設定儲存為草稿，並在 IP 集區具有&#x200B;**[!UICONTROL 成功]**&#x200B;狀態時重試。

>[!NOTE]
>
>對於非生產環境，Adobe 不會建立立即可用的測試子網域，也不會授予共用傳送 IP 集區的存取權。您需要[委派自己的子網域](../configuration/delegate-subdomain.md)，並使用指派至您組織集區的 IP。

選取 IP 集區後，當游標停留在 IP 集區下拉式清單下方顯示的 IP 位址上時，會顯示 PTR 資訊。[進一步了解 PTR 記錄](../configuration/ptr-records.md)

>[!NOTE]
>
>如果未設定 PTR 記錄，請聯絡您的 Adobe 代表。

## 清單取消訂閱{#list-unsubscribe}

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom"
>title="定義如何管理取消訂閱的資料"
>abstract="**Adobe 管理**：同意資料由您在 Adobe 系統內進行管理。<br>**客戶管理**：同意資料由您在外部系統中進行管理，除非由您啟動，否則 Adobe 系統中不會同步更新同意資料。"

<!--Do not modify - Legal Review Done -->

從清單中[選取子網域](#subdomains-and-ip-pools)後，會顯示&#x200B;**[!UICONTROL 啟用清單取消訂閱]**&#x200B;選項。

此選項預設為啟用，以在電子郵件標頭加入一鍵取消訂閱 URL，例如：

![](assets/preset-list-unsubscribe-header.png)

>[!NOTE]
>
>如果停用此選項，一鍵取消訂閱 URL 將不會顯示在電子郵件標頭。

您可以從&#x200B;**[!UICONTROL 同意層級]**&#x200B;下拉式清單之中選取同意層級。它可特定於頻道或設定檔身分。根據此設定，當使用者使用電子郵件標頭的清單取消訂閱 URL時，會在 Adobe Journey Optimizer 中以頻道層級或 ID 層級更新同意。

清單取消訂閱標頭提供兩種功能，除非您取消選取其中一項或兩項功能，否則這兩項功能預設為啟用：

![](assets/surface-list-unsubscribe-mailto.png){width="80%"}

<!--![](assets/surface-list-unsubscribe.png){width="80%"}-->

* **Mailto（取消訂閱）**&#x200B;位址，這是將取消訂閱要求路由至進行自動處理的目標位址。

  在 Journey Optimizer 中，取消訂閱電子郵件地址是根據您[選取的子網域](#subdomains-and-ip-pools)，顯示在頻道設定的預設 **Mailto（取消訂閱）**&#x200B;位址。

* **一鍵取消訂閱 URL**，根據您在頻道組態設定中設定並配置的子網域，預設為一鍵退出 URL 產生的清單取消訂閱標頭。

<!--
    >[!AVAILABILITY]
    >
    >One-click Unsubscribe URL Header will be available in Adobe Journey Optimizer starting June 3, 2024.
    >
-->

**[!UICONTROL Mailto（取消訂閱）]**&#x200B;功能和&#x200B;**[!UICONTROL 一鍵取消訂閱 URL]** 功能是選用功能。

如果您不想使用預設產生的一鍵取消訂閱 URL，可以取消勾選該功能。在&#x200B;**[!UICONTROL 啟用清單取消訂閱]**&#x200B;選項處於開啟狀態且&#x200B;**[!UICONTROL 一鍵取消訂閱 URL]** 功能處於取消勾選的情況下，如果您在使用此設定所建立的訊息中新增[一鍵退出連結](../email/email-opt-out.md#one-click-opt-out)，則清單取消訂閱標頭會獲取您在電子郵件內文插入的一鍵退出連結，並將其用作一鍵取消訂閱 URL 值。

![](assets/preset-list-unsubscribe-opt-out-url.png)

>[!NOTE]
>
>如果您未在訊息內容加入一鍵退出連結，且頻道組態設定中的預設&#x200B;**[!UICONTROL 一鍵取消訂閱 URL]** 已取消勾選，則清單取消訂閱標題的電子郵件標頭不會傳遞任何 URL。

在 [本節](../email/email-opt-out.md#unsubscribe-header)進一步了解管理訊息中取消訂閱功能更多資訊。

<!--![](assets/surface-list-unsubscribe-custom.png){width="80%"}-->

## 標頭參數 {#email-header}

在&#x200B;**[!UICONTROL 標頭參數]**&#x200B;區段中，輸入與該設定所傳送電子郵件類型相關的寄件者名稱和電子郵件地址。

>[!NOTE]
>
>為了增強對電子郵件設定的控制，您可以個人化標頭參數。[了解更多](../email/surface-personalization.md#personalize-header)

* **[!UICONTROL 寄件者姓名]**：寄件者姓名，例如您的品牌名稱。
* **[!UICONTROL 寄件者電子郵件前置詞]**：您想要用於通訊的電子郵件地址。
* **[!UICONTROL 回覆姓名]**：收件者在其電子郵件用戶端軟體中按一下&#x200B;**回覆**&#x200B;按鈕時將使用的名稱。
* **[!UICONTROL 回覆電子郵件]**：收件者在其電子郵件用戶端軟體中按一下&#x200B;**回覆**&#x200B;按鈕時將使用的電子郵件地址。[了解更多](#reply-to-email)
* **[!UICONTROL 錯誤電子郵件前置詞]**：在傳送郵件幾天後，ISP 產生的所有錯誤（非同步退件）都會在此位址接收到。此位址也會接收休假通知及質詢回應。

  如果您想要在未委派給 Adobe 的特定電子郵件地址上接收休假通知和質詢回應，您需要設定[轉寄流程](#forward-email)。在此情況下，請確定您有手動或自動化解決方案來處理傳入此收件匣的電子郵件。

>[!NOTE]
>
>**[!UICONTROL 寄件者電子郵件前置詞]**&#x200B;與&#x200B;**[!UICONTROL 錯誤電子郵件前置詞]**&#x200B;位址使用目前選取的[委派子網域](../configuration/about-subdomain-delegation.md)來傳送電子郵件。例如，如果委派的子網域是 *marketing.luma.com*：
>* 輸入 *contact* 作為&#x200B;**[!UICONTROL 寄件者電子郵件前置詞]** — 寄件者電子郵件為 *contact@marketing.luma.com*。
>* 輸入 *error* 作為&#x200B;**[!UICONTROL 錯誤電子郵件前置詞]** — 錯誤位址為 *error@marketing.luma.com*。


![](assets/preset-header.png){width="80%"}

>[!NOTE]
>
>位址必須以字母 (A-Z) 開頭，並且只能包含英數字元。您也可以使用底線 `_`、點 `.` 和連字號 `-` 字元。

### 回覆電子郵件 {#reply-to-email}

定義&#x200B;**[!UICONTROL 回覆電子郵件]**&#x200B;地址時，只要電子郵件地址是有效、格式正確且不含任何拼寫錯誤，您就可以指定任何電子郵件地址。

用於回覆的收件匣將將收到所有回覆電子郵件，但休假通知和質詢回覆除外，這些郵件將在 **錯誤電子郵件**&#x200B;地址收到。

若要確保正確管理回覆，請遵循下列建議：

* 確保專用收件匣有足夠的接收容量，可接收使用電子郵件設定傳送的所有回覆電子郵件。如果收件匣出現退信，您可能無法收到客戶的一些回覆。

* 處理回覆時必須牢記隱私權與合規義務，因為回覆可能包含個人識別資訊 (PII)。

* 請勿在回覆收件匣中將郵件標示為垃圾訊息，因為這會影響傳送至此地址的所有其他回覆。

此外，在定義&#x200B;**[!UICONTROL 回覆電子郵件]**&#x200B;地址時，請務必使用具有有效 MX 記錄設定的子網域，否則電子郵件設定處理將會失敗。

如果在提交電子郵件設定時發生錯誤，表示您輸入之位址的子網域尚未設定 MX 記錄。請連絡您的管理員以設定對應的 MX 記錄，或使用其他具有有效 MX 記錄設定的位址。

>[!NOTE]
>
>如果您輸入之位址的子網域是[已完全委派](../configuration/delegate-subdomain.md#full-subdomain-delegation)至 Adobe 的網域，請連絡您的 Adobe 帳戶主管。

### 轉寄電子郵件 {#forward-email}

若要將 [!DNL Journey Optimizer] 收到的委派子網域的所有電子郵件轉寄至特定電子郵件地址，請聯絡 Adobe 客戶服務部門。

>[!NOTE]
>
>如果用於&#x200B;**[!UICONTROL 回覆電子郵件]**&#x200B;地址的子網域未委派給 Adobe，則該地址無法進行轉寄。

您需要提供：

* 您選擇的轉寄電子郵件地址。請注意，轉寄電子郵件地址網域無法與委派給 Adobe 的任何子網域相符。
* 您的沙箱名稱。
* 將使用轉寄電子郵件地址的設定名稱或子網域。
  <!--* The current **[!UICONTROL Reply to (email)]** address or **[!UICONTROL Error email]** address set at the channel configuration level.-->

>[!NOTE]
>
>每個子網域只能有一個轉寄電子郵件地址。因此，如果多個設定使用相同的子網域，則必須對所有設定使用相同的轉寄電子郵件地址。

轉寄電子郵件地址由 Adobe 設定。這需要 3 至 4 天的時間。

完成後，**[!UICONTROL 回覆電子郵件]**&#x200B;和&#x200B;**錯誤電子郵件**&#x200B;地址收到的所有郵件，以及傳送至&#x200B;**寄件者電子郵件**&#x200B;地址的所有電子郵件，都會轉寄至您提供的特定電子郵件地址。

>[!NOTE]
>
>根據預設，如果未啟用轉寄，則會捨棄直接傳送至&#x200B;**寄件者**&#x200B;地址的電子郵件。

## 密件副本電子郵件 {#bcc-email}

您可以將 [!DNL Journey Optimizer] 傳送之電子郵件的相同副本（或密件副本）傳送至密件副本收件匣，以儲存這些電子郵件以供合規性或封存。

若要這麼做，請在頻道設定層級啟用&#x200B;**[!UICONTROL 密件副本電子郵件]**&#x200B;選用功能。[了解更多](../configuration/archiving-support.md#bcc-email)

![](assets/preset-bcc.png)

此外，在定義&#x200B;**[!UICONTROL 密件副本電子郵件]**&#x200B;地址時，請務必使用具有有效 MX 記錄設定的子網域，否則電子郵件設定處理將會失敗。

如果在提交電子郵件設定時發生錯誤，表示您輸入之位址的子網域尚未設定 MX 記錄。請連絡您的管理員以設定對應的 MX 記錄，或使用其他具有有效 MX 記錄設定的位址。

## 傳送到禁止的電子郵件地址 {#send-to-suppressed-email-addresses}

>[!CONTEXTUALHELP]
>id="ajo_surface_suppressed_addresses"
>title="覆寫禁止名單優先順序"
>abstract="即使其電子郵件地址因垃圾郵件投訴而位於 Adobe Journey Optimizer 禁止名單中，您也可以決定傳送交易型訊息到輪廓。此選項預設為停用。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/manage-suppression-list.html?lang=zh-Hant" text="管理禁止名單"

>[!IMPORTANT]
>
>只有當您選取&#x200B;**[!UICONTROL 交易型]**&#x200B;電子郵件類型時，才能使用此選項。[了解更多](#email-type)

在 [!DNL Journey Optimizer] 中，所有標示為永久性退信、暫時性退信和垃圾郵件投訴的電子郵件地址都會自動收集到[禁止名單](../configuration/manage-suppression-list.md)之中，不會被納入到歷程或行銷活動的傳送範圍。

不過，您可以決定繼續傳送&#x200B;**交易型**&#x200B;類型的訊息給設定檔，即使其電子郵件地址因使用者投訴垃圾郵件而列入禁止名單中亦然。

事實上，交易型訊息通常包含有用的預期資訊，例如訂購確認或密碼重設通知。因此，即使他們將您的一封行銷訊息舉報為垃圾郵件，大多數情況下您仍希望客戶收到此類非商業電子郵件。

若要將因垃圾郵件投訴而被封鎖的電子郵件地址包含在交易型訊息對象中，請從&#x200B;**[!UICONTROL 傳送至封鎖的電子郵件地址]**&#x200B;區段中選取對應的選項。

![](assets/preset-suppressed-email-addresses.png)

>[!NOTE]
>
>此選項預設為停用。

作為傳遞能力的最佳實務，此選項預設為停用，以確保不會聯絡已選擇退出的客戶。不過，您可以變更此預設選項，然後允許您將交易型訊息傳送給客戶。

一旦啟用此選項，儘管客戶將您的行銷電子郵件標記為垃圾郵件，此類客戶仍可使用目前設定接收您的交易型訊息。請務必根據傳遞能力最佳實務管理選擇退出偏好設定。

## 種子清單 {#seed-list}

>[!CONTEXTUALHELP]
>id="ajo_surface_seed_list"
>title="新增種子清單"
>abstract="選取您所選的種子清單，以自動向您的客群新增特定的內部地址。這些種子地址將在傳遞執行時包含在內，且為了保證目的將收到一份準確的訊息副本。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html#use-seed-list" text="什麼是種子清單?"

[!DNL Journey Optimizer] 內的種子清單，可讓您在您的傳送過程中自動包含特定的電子郵件種子地址。[了解更多](../configuration/seed-lists.md)

>[!CAUTION]
>
>目前該功能僅適用於電子郵件頻道。

在&#x200B;**[!UICONTROL 種子清單]**&#x200B;區段中選取與您相關的清單。在[本節](../configuration/seed-lists.md#create-seed-list)之中了解如何建立種子清單。

![](../configuration/assets/seed-list-surface.png){width="80%"}

>[!NOTE]
>
>一次只能選取一個種子清單。

當行銷活動或歷程中使用目前設定時，在傳送執行時候會包含所選種子清單上的電子郵件地址，這表示他們將會收到傳送的副本以供保證。

在[本節](../configuration/seed-lists.md#use-seed-list)之中了解如何在行銷活動或歷程中使用種子清單。

## 電子郵件重試參數 {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="調整重試時段"
>abstract="當電子郵件由於暫時性的軟退信錯誤而傳遞失敗時，將重試 3.5 天 (84 小時)。您可以調整此預設的重試時段以進一步滿足您的需求。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/retries.html" text="關於重試"

您可以設定&#x200B;**電子郵件重試參數**。

![](assets/preset-retry-parameters.png)

依預設，[重試時段](../configuration/retries.md#retry-duration)設定為 84 小時，但您可以調整此設定以更符合您的需求。

您必須輸入下列範圍內的整數值（小時或分鐘）：

* 若是行銷電子郵件，最小重試時段為 6 小時。
* 若是交易型電子郵件，最小重試時段為 10 分鐘。
* 對於這兩種電子郵件類型，重試時段的上限為 84 小時（或 5040 分鐘）。

欲了解有關重試的更多資訊，請參閱[本節](../configuration/retries.md)。

## URL 追蹤 {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="定義 URL 追蹤參數"
>abstract="使用此區段以將追蹤參數自動附加到電子郵件內容中的 URL。此功能為選用。"

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="預覽 URL 追蹤參數"
>abstract="重新探討要如何將追蹤參數附加到電子郵件內容中出現的 URL。"

您可以使用 **[!UICONTROL URL 追蹤參數]**&#x200B;來測量跨頻道行銷工作的有效性。此功能為選用。

本章節定義的參數將會附加至您的電子郵件內容中所包含的 URL 末尾。接著，您就可以在 Adobe Analytics 或 Google Analytics 等網站分析工具中擷取這些參數，並建立各種效能報告。

您可使用&#x200B;**[!UICONTROL 新增參數]**&#x200B;按鈕，新增最多 10 個追蹤參數。

![](assets/preset-url-tracking.png){width="80%"}

若要設定 URL 追蹤參數，您可以在&#x200B;**[!UICONTROL 名稱]**&#x200B;和&#x200B;**[!UICONTROL 值]**&#x200B;欄位中直接輸入所需的值。

您也可以使用[個人化編輯器](../personalization/personalization-build-expressions.md)來編輯每個&#x200B;**[!UICONTROL 值]**&#x200B;欄位。按一下版本圖示以開啟編輯器。從那裡，您可以選取可用的內容屬性和/或直接編輯文字。

![](assets/preset-url-tracking-editor.png)

下列預先定義的值可透過個人化編輯器取得：

* **來源動作 ID**：新增至歷程或行銷活動電子郵件動作的 ID。

* **來源動作名稱**：新增至歷程或行銷活動電子郵件動作的名稱。

* **來源 ID**：傳送電子郵件歷程或行銷活動的 ID。

* **來源名稱**：傳送電子郵件歷程或行銷活動的名稱。

* **來源版本 ID**：傳送電子郵件歷程或行銷活動版本的 ID。

* **優惠方案 ID**：電子郵件中使用的優惠方案 ID。

>[!NOTE]
>
>您可以結合輸入文字值並使用個人化編輯器中的內容屬性。每個&#x200B;**[!UICONTROL 值]**&#x200B;欄位可包含的字元數最多為 5 KB。

<!--You can drag and drop the parameters to reorder them.-->

以下是 Adobe Analytics 和 Google Analytics 相容 URL 的範例。

* 與 Adobe Analytics 相容的 URL：`www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* 與 Google Analytics 相容的 URL：`www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

您可以動態預覽產生的追蹤 URL。每次新增、編輯或移除參數時，預覽都會自動更新。

![](assets/preset-url-tracking-preview.png)

>[!NOTE]
>
>您也可以將動態個人化追蹤參數新增至電子郵件內容中存在的連結，但無法在設定層級執行此操作。您必須在使用電子郵件設計工具撰寫訊息時執行此操作。[了解更多](message-tracking.md#url-tracking)

## 執行地址 {#execution-address}

>[!CONTEXTUALHELP]
>id="ajo_email_config_execution_address"
>title="覆寫要使用的預設執行地址"
>abstract="當資料庫 (個人、專業等) 中有多個電子郵件地址時，您可以選擇優先傳送哪一個。此主要地址是在沙箱層級定義，但您可以在此處覆寫此特定電子郵件設定的預設設定。"

當您定位設定檔時，資料庫中可能會提供數個電子郵件地址（專業電子郵件地址、個人電子郵件地址等）。

在這種情況下，[!DNL Journey Optimizer] 會在沙箱層級使用&#x200B;**[!UICONTROL 執行欄位]**&#x200B;所指定的位址，以決定優先使用設定檔服務內哪個電子郵件地址。[了解更多](../configuration/primary-email-addresses.md)

>[!NOTE]
>
>若要檢查目前預設使用的欄位，請存取&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL 一般設定]** > **[!UICONTROL 執行欄位]**&#x200B;選單。

不過，您可以在電子郵件頻道設定層級變更此預設執行欄位。然後，您可以將此設定套用至特定行銷活動或歷程。

若要這麼做，請編輯 **[!UICONTROL 傳送地址]**&#x200B;欄位，並從可用的電子郵件類型 XDM 欄位清單中選取項目。

![](assets/email-config-delivery-address.png)

執行欄位會更新，然後作為主要地址使用。它會覆寫沙箱層級的一般設定。
