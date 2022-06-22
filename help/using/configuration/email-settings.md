---
title: 設定電子郵件設定
description: 瞭解如何在郵件預設級別配置電子郵件設定
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: 8f089e885098917d2ebf455b807ac5e6da020190
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 2%

---

# 設定電子郵件設定 {#email-settings}

在郵件預設配置的專用部分定義電子郵件設定。 瞭解如何在中建立消息預設 [此部分](message-presets.md)。

![](assets/preset-email.png)

## 電子郵件類型 {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="定義電子郵件類別"
>abstract="選擇使用此預設時將發送的消息類型：需要用戶同意的促銷消息的市場營銷，或非商業消息的事務性，這些消息也可以在特定上下文中發送到未訂閱的配置檔案。"

在 **電子郵件類型** 部分，選擇將使用預設發送的消息類型： **營銷** 或 **事務性**。

* 選擇 **營銷** 對於促銷消息：這些消息需要用戶同意。

* 選擇 **事務性** 非商業消息（例如，訂單確認、密碼重置通知或傳遞資訊）。

>[!CAUTION]
>
>**事務性** 消息可以發送到從營銷通信中取消訂閱的配置檔案。 這些消息只能在特定上下文中發送。

當 [建立消息](../messages/get-started-content.md#create-new-message)，必須選擇與您為消息選擇的類別匹配的有效消息預設。

## 子域和IP池 {#subdomains-and-ip-pools}

在 **子域和IP池詳細資訊** ，您必須：

1. 選擇要用於發送電子郵件的子域。 [了解更多](about-subdomain-delegation.md)

1. 選擇要與預設關聯的IP池。 [了解更多](ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

當所選IP池位於以下位置時，無法繼續建立預設 [版本](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** 狀態)，且從未與所選子域關聯。 否則，仍將使用IP池/子域關聯的最舊版本。 如果是這種情況，請將預設另存為草稿，並在IP池具有 **[!UICONTROL Success]** 狀態。

>[!NOTE]
>
>對於非生產環境，Adobe不建立現成的test子域，也不授予對共用發送IP池的訪問權限。 你需要 [委派自己的子域](delegate-subdomain.md) 並使用分配給您組織的池中的IP。

## 清單 — 取消訂閱 {#list-unsubscribe}

在 [選擇子域](#subdomains-and-ip-pools) 清單中， **[!UICONTROL Enable List-Unsubscribe]** 按鈕。

![](assets/preset-list-unsubscribe.png)

依預設，會啟用此選項。

如果保持啟用狀態，則取消訂閱連結將自動包含在電子郵件標題中，例如：

![](assets/preset-list-unsubscribe-header.png)

如果禁用此選項，則電子郵件標題中不會顯示取消訂閱連結。

取消訂閱連結包含兩個元素：

* 安 **取消訂閱電子郵件地址**，所有取消訂閱請求都發送到。

   在 [!DNL Journey Optimizer]，取消訂閱電子郵件地址是 **[!UICONTROL Mailto (unsubscribe)]** 在消息預設中顯示的地址，基於 [選定子域](#subdomains-and-ip-pools)。

   ![](assets/preset-list-unsubscribe-mailto.png)

* 的 **取消訂閱URL**，即登錄頁的URL，在取消訂閱後將重定向用戶。

   如果添加 [按一下選擇退出連結](../messages/consent.md#one-click-opt-out) 對於使用此預設建立的消息，取消訂閱URL將是為一次按一下選擇退出連結定義的URL。

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >如果您不在消息內容中添加一鍵退出選項連結，則不會向用戶顯示登錄頁。

瞭解有關將標題取消訂閱連結添加到郵件的詳細資訊 [此部分](../messages/consent.md#unsubscribe-header)。

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## 標題參數{#email-header}

在 **[!UICONTROL HEADER PARAMETERS]** 部分，輸入與使用該預設發送的郵件類型關聯的發件人姓名和電子郵件地址。

>[!CAUTION]
>
>電子郵件地址必須使用當前選定的 [委託子域](about-subdomain-delegation.md)。

* **[!UICONTROL Sender name]**:發件人的名稱，如您的品牌名稱。

* **[!UICONTROL Sender email]**:要用於通信的電子郵件地址。 例如，如果委派的子域是 *營銷.luma.com*，您可以使用 *contact@marketing.luma.com*。

* **[!UICONTROL Reply to (name)]**:收件人按一下 **答復** 按鈕。

* **[!UICONTROL Reply to (email)]**:收件人按一下 **答復** 按鈕。 必須使用在委派子域上定義的地址(例如， *reply@marketing.luma.com*)，否則將刪除電子郵件。

* **[!UICONTROL Error email]**:ISP在發送數天郵件（非同步綁定）後生成的所有錯誤都會在此地址上接收。

![](assets/preset-header.png)

>[!NOTE]
>
>地址必須以字母(A-Z)開頭，並且只能包含字母數字字元。 您還可以使用下划線 `_`，點`.` 連字元 `-` 字元。

### 轉發電子郵件 {#forward-email}

如果要轉發到特定電子郵件地址，則所有收到的電子郵件 [!DNL Journey Optimizer] 對於委派的子域，請與Adobe客戶服務部門聯繫。 您需要提供：

* 您選擇的轉發電子郵件地址。 請注意，轉發電子郵件地址域與委託給Adobe的任何子域不匹配。
* 沙盒名稱。
* 使用轉發電子郵件地址的預設名稱。
* 當前 **[!UICONTROL Reply to (email)]** 地址設定在預設級別。

>[!NOTE]
>
>每個子域只能有一個轉發電子郵件地址。 因此，如果多個預設使用相同的子域，則所有預設都必須使用相同的轉發電子郵件地址。

轉發電子郵件地址將通過Adobe設定。 這可能需要3到4天。

## 密件抄送電子郵件 {#bcc-email}

您可以發送由 [!DNL Journey Optimizer] 發送到密件抄送收件箱，在該收件箱中，這些郵件將儲存為符合性或存檔目的。

為此，請啟用 **[!UICONTROL BCC email]** 可選功能。 [了解更多](bcc-email.md)

![](assets/preset-bcc.png)

## 電子郵件重試參數 {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="調整重試時間段"
>abstract="當電子郵件由於臨時軟彈回錯誤而失敗時，將執行3.5天（84小時）的重試。 您可以調整此預設重試時間段，以更好地滿足您的需要。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/monitor-reputation/retries.html" text="關於重試"

您可以配置 **電子郵件重試參數**。

![](assets/preset-retry-parameters.png)

預設情況下， [重試時間](retries.md#retry-duration) 設定為84小時，但您可以調整此設定以更好地滿足您的需要。

必須在以下範圍內輸入整數值（以小時或分鐘為單位）:

* 對於市場營銷電子郵件，最短重試時間為6小時。
* 對於事務性電子郵件，最短重試時間為10分鐘。
* 對於這兩種電子郵件類型，最大重試時間為84小時（或5040分鐘）。

在中重試時瞭解更多資訊 [此部分](retries.md)。

## URL跟蹤 {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="定義URL跟蹤參數"
>abstract="使用此部分可自動將跟蹤參數附加到電子郵件內容中存在的URL。 此功能是選取性的。"

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="預覽URL跟蹤參數"
>abstract="查看跟蹤參數將如何附加到電子郵件內容中存在的URL。"

您可以使用 **[!UICONTROL URL tracking parameters]** 以衡量您跨渠道的營銷工作的成效。 此功能是選取性的。

本節中定義的參數將附加到電子郵件內容中包含的URL的末尾。 然後，您可以在Web分析工具(如Adobe Analytics或Google Analytics)中捕獲這些參數，並建立各種效能報告。

![](assets/preset-url-tracking.png)

建立消息預設時，會自動填充三個URL跟蹤參數。 您可以使用 **[!UICONTROL Add new parameter]** 按鈕

要配置URL跟蹤參數，可以直接在 **[!UICONTROL Name]** 和 **[!UICONTROL Value]** 的子菜單。

也可以通過導航到以下對象從預定義值清單中進行選擇：
* 行程屬性： **源ID**。 **源名稱**。 **源版本ID**
* 操作屬性： **操作ID**。 **操作名稱**
* Offer decisioning屬性： **服務ID**。 **優惠名稱**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>不選擇資料夾：確保瀏覽到必要的資料夾，並選擇一個配置檔案屬性作為跟蹤參數值。

<!--or edit it using the Expression Editor. Learn more on [personalization](../../personalization/personalize.md#use-expression-editor). Select the contextual attribute of your choice.

You can drag and drop the parameters to reorder them.-->

以下是與Adobe Analytics和Google Analytics相容的URL的示例。

* Adobe Analytics相容URL: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* Google Analytics相容URL: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

>[!NOTE]
>
>可以將鍵入的文本值與選擇預定義的值合併。 每個 **[!UICONTROL Value]** 欄位總共最多可包含255個字元。

可動態預覽結果的跟蹤URL。 每次添加、編輯或刪除參數時，預覽都會自動更新。

![](assets/preset-url-tracking-preview.png)