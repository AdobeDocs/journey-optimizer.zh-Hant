---
title: 預覽消息和發送校樣
description: 瞭解如何預覽和test郵件
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: f2c2a360-a4b2-4416-bbd0-e27dd014e4ac
source-git-commit: 3f41545f41f258eede2167aa9ab45db51e91cacf
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 2%

---

# 預覽和test郵件{#preview-and-proof}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_simulation_test_profile"
>title="添加test配置檔案"
>abstract="可以通過選擇標識命名空間和相應的標識值來添加test配置檔案。"

定義消息內容後，可以使用test配置檔案預覽和test它。 如果插入 [個性化內容](../personalization/personalize.md)，您將能夠利用test配置檔案資料檢查此內容在消息中的顯示方式。

要檢測電子郵件內容或個性化設定中可能的錯誤，請將校樣發送到test配置檔案。 每次更改時都應發送證明，以驗證最新內容。

>[!CAUTION]
>
>您需要有test配置檔案才能預覽郵件和發送校樣。
>
>瞭解如何在中建立test配置檔案 [此頁](../segment/creating-test-profiles.md)。

要test郵件內容，您需要：

* [選擇test配置檔案](#select-test-profiles)
* [檢查消息預覽](#preview-your-messages)

然後你就能 [發送校樣](#send-proofs) 到您的test檔案。

另外，利用 **斜石** 帳戶 [!DNL Journey Optimizer] 立即預覽 **電子郵件呈現** 常用電子郵件客戶端。 然後，您可以確保電子郵件內容看起來非常出色，並且在每個收件箱中都能正常工作。 瞭解如何在中解鎖Litmus電子郵件預覽 [此部分](#email-rendering)

>[!CAUTION]
>
>預覽消息或發送校樣時，只顯示配置檔案個性化資料。 基於上下文資料（例如事件資訊）的個性化只能在旅程的上下文中測試。 瞭解如何test個性化 [此使用案例](../personalization/personalization-use-case.md)。

➡️ [瞭解如何在此視頻中預覽、校樣和發佈電子郵件](#video-preview)

## 選擇test配置檔案{#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="預覽和test郵件"
>abstract="定義消息內容後，可以使用test配置檔案預覽和test它。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/validate/preview.html?lang=en#email-rendering" text="電子郵件轉譯"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/validate/preview.html?lang=en#preview-your-messages" text="預覽"

使用 [Test配置檔案](../segment/creating-test-profiles.md) 目標與定義的目標條件不匹配的其他收件人。

要選擇test配置檔案，請執行以下步驟：

1. 在消息介面或電子郵件設計器中，按一下 **[!UICONTROL Show preview]** 按鈕，來查看test配置檔案選擇。

   ![](assets/email-preview-button.png)

1. 通過按一下以下命令選擇用於標識test配置檔案的命名空間 **[!UICONTROL Identity namespace]** 的子菜單。

   ![](assets/previewselect-namespace.png)

   瞭解有關Adobe Experience Platform標識命名空間的詳細資訊 [此部分](../segment/get-started-identity.md)。

   在下面的示例中，我們將使用 **電子郵件** 命名空間。

1. 使用搜索欄位查找命名空間，選擇它並按一下 **[!UICONTROL Select]**

   ![](assets/preview-email-namespace.png)

1. 輸入標識test配置檔案的值，然後按一下 **[!UICONTROL Find test profile]**。

   ![](assets/preview-identity-value.png)

1. 如果在郵件中添加了個性化設定，請添加其他配置檔案，以便根據配置檔案資料test郵件的不同變型。 添加後，配置檔案將列在選擇欄位下。

   ![](assets/preview-profile-list.png)

   根據消息個性化元素，此清單顯示相關列中每個test配置檔案的資料。

## 預覽消息{#preview-your-messages}

一次 [test配置檔案](#select-test-profiles) 選項，您可以預覽消息並檢查內容。

1. 按一下 **[!UICONTROL Preview]** 頁籤test消息。

1. 選擇test配置檔案。 可以檢查列中的可用值。 使用右/左箭頭瀏覽資料。

   ![](assets/preview-tab-select-profile.png)

1. 按一下 **[!UICONTROL Select data]** 表徵圖，以添加或刪除列。

   ![](assets/preview-select-data.png)

   您可以在清單末尾看到特定於當前消息的個性化欄位。 在本示例中，配置檔案城市、名和姓。 選擇這些欄位，並確保這些值填充到您的test配置檔案中。

1. 在消息預覽中，個性化元素被所選test配置檔案資料替換。

   例如，對於此郵件，電子郵件內容和電子郵件主題都是個性化的：

   ![](assets/preview-test-profile.png)

1. 選擇其他test配置檔案，以預覽郵件的每個變體的電子郵件呈現。

對於推送通知預覽：

1. 切換到 **[!UICONTROL Push]** 頻道 **[!UICONTROL Channels]** 右上角的下拉清單 **[!UICONTROL Preview]** 的上界。

   ![](assets/preview-select-channel.png)

1. 應用上述相同步驟以選擇test配置檔案，並選擇要預覽內容的設備類型： **[!UICONTROL iOS]** 或 **[!UICONTROL Android]**。

   ![](assets/preview-iOS.png)

1. 在推式預覽中，test配置檔案資料被用於消息內容。

   例如，對於此推送通知，標題和正文都是個性化的：

   ![](assets/preview-android.png)

## 傳送校樣{#send-proofs}

證明是一條特定的消息，允許您在將消息發送到主受眾之前test該消息。 證明的接收者負責批准郵件：呈現、內容、個性化設定、配置。

一次 [test配置檔案](#select-test-profiles) 的子菜單。

1. 在 **[!UICONTROL Preview]** 螢幕，按一下 **[!UICONTROL Send proof]** 按鈕

   ![](assets/send-proof-button.png)

1. 從 **[!UICONTROL Send proof]** 鍵入收件人的電子郵件，然後按一下 **[!UICONTROL Add]** 把證據寄給你自己或你的組織成員。

   請注意，您最多可以為憑證交付添加10個收件人。

   ![](assets/send-proof-button_2.png)

1. 然後，選擇 **Test配置檔案** 用於個性化消息內容。

   證明的每個接收者將接收與所選test配置檔案數量相同的郵件。 例如，如果您添加了五封收件人電子郵件並選擇了十封test配置檔案，則您將發送五十封證明郵件，而每個收件人將收到十封。

1. 如果需要，可以在證明的主題行中添加前置詞。 只有字母數字字元和特殊字元，如。- _() [ ]，可作為主題行的前置詞。

1. 按一下「**[!UICONTROL Send proof]**」。

   ![](assets/send-proof-select.png)

1. 回到  **[!UICONTROL Preview]** 螢幕，按一下  **[!UICONTROL View proofs]** 按鈕

   ![](assets/send-proof-view.png)

建議在每次修改消息內容後發送校樣。

>[!NOTE]
>
>在發送到test配置檔案的校樣中，指向鏡像頁的連結不處於活動狀態。 僅在最後消息中激活。

## 電子郵件轉譯{#email-rendering}

您可以利用 **斜石** 帳戶 [!DNL Journey Optimizer] 立即預覽 **電子郵件呈現** 常用電子郵件客戶端。

要訪問電子郵件呈現功能，您需要：

* 擁有Litmus帳戶
* [選擇test配置檔案](#select-test-profiles)

然後，執行以下步驟：

1. 在電子郵件設計器中，按一下 **[!UICONTROL Preview]** 按鈕 **[!UICONTROL Email rendering]** 頁籤。

1. 按一下 **連接你的Litmus帳戶** 右上角。

   ![](assets/email-rendering-litmus.png)

1. 輸入您的憑據並登錄。

   ![](assets/email-rendering-credentials.png)

1. 按一下 **運行test** 按鈕以生成電子郵件預覽。

1. 在流行的案頭、移動和基於Web的客戶端中檢查您的電子郵件內容。

   ![](assets/email-rendering-previews.png)

>[!CAUTION]
>
>連接時 **斜石** 帳戶 [!DNL Journey Optimizer]，您同意將test消息發送到Litmus :一旦發送，這些電子郵件將不再由Adobe管理。 因此， Litmus資料保留電子郵件策略適用於這些電子郵件，包括可能包含在這些test郵件中的個性化資料。

## How-to視頻{#video-preview}

瞭解如何測試各收件匣間的電子郵件呈現、如何根據測試設定檔預覽您的個人化電子郵件、傳送校樣及發佈您的電子郵件。

>[!VIDEO](https://video.tv.adobe.com/v/334239?quality=12)
