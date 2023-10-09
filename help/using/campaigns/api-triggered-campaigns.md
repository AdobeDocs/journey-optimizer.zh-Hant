---
solution: Journey Optimizer
product: journey optimizer
title: 利用 API 觸發行銷活動
description: 瞭解如何使用Journey Optimizer API觸發行銷活動
topic: Content Management
role: Developer, Admin
level: Intermediate, Experienced
keywords: 行銷活動， API觸發， REST，最佳化工具，訊息
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 6999f52a3426aa252f31440189ba9d1a7118dd0a
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 1%

---

# 利用 API 觸發行銷活動 {#trigger-campaigns}

## 關於API觸發的行銷活動 {#about}

替換為 [!DNL Journey Optimizer]，您可以建立行銷活動，然後使用根據使用者觸發條件從外部系統叫用它們 [互動式訊息執行REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). 這可讓您涵蓋各種行銷和異動訊息需求，例如密碼重設、OTP權杖等。

若要這麼做，您首先需要在Journey Optimizer中建立API觸發的行銷活動，然後透過API呼叫啟動其執行。

![](../rn/assets/do-not-localize/api-triggered.gif)

API觸發的行銷活動的可用管道包括電子郵件、簡訊和推播訊息。

>[!NOTE]
>
>截至目前，推播通知API觸發的行銷活動不支援快速傳送模式。

## 建立API觸發的行銷活動 {#create}

### 設定並啟用行銷活動 {#create-activate}

若要建立API觸發的行銷活動，請遵循下列步驟。 有關如何建立行銷活動的詳細資訊，請參閱 [本節](create-campaign.md).

1. 使用建立新的行銷活動 **[!UICONTROL API觸發]** 型別。

1. 選擇 **[!UICONTROL 行銷]** 或 **[!UICONTROL 異動]** 類別取決於您要傳送的通訊型別。

1. 選擇其中一個支援的頻道和相關聯的頻道介面，以用於傳送您的訊息，然後按一下 **[!UICONTROL 建立]**.

   ![](assets/api-triggered-type.png)

1. 指定行銷活動的標題和說明，然後按一下 **[!UICONTROL 編輯內容]** 以設定要傳送的訊息。

   >[!NOTE]
   >
   >您可以將其他資料傳遞至API裝載，以便用於個人化您的訊息。 [了解更多](#contextual)
   >
   >在內容中使用大量或繁重的內容相關資料可能會影響效能。

1. 在 **[!UICONTROL 對象]** 區段，指定用於識別個人的名稱空間。

   * 如果您要建立 **異動**-type campaign，必須在API呼叫中定義目標設定檔。 此 **[!UICONTROL 建立新設定檔]** 選項可讓您自動建立資料庫中不存在的設定檔。 [瞭解有關在行銷活動執行時建立設定檔的更多資訊](#profile-creation)

   * 的 **行銷**-type行銷活動，按一下 **[!UICONTROL 對象]** 按鈕以選擇要鎖定的對象。

1. 設定行銷活動的開始和結束日期。

   如果您設定行銷活動的特定開始和/或結束日期，則不會在這些日期以外執行，而如果行銷活動由API觸發，API呼叫將會失敗。

1. 按一下 **[!UICONTROL 檢閱以啟動]** 以檢查您的行銷活動是否已正確設定，然後啟用它。

您現在已準備好從API執行行銷活動。 [了解更多](#execute)

### 執行行銷活動 {#execute}

啟動行銷活動後，您需要擷取產生的範例cURL請求，並將其用於API中以建置您的裝載並觸發行銷活動。

1. 開啟行銷活動，然後從以下位置複製並貼上範例請求： **[!UICONTROL cURL要求]** 區段。

   ![](assets/api-triggered-curl.png)

1. 將此cURL請求用於API以建置您的裝載並觸發行銷活動。 如需詳細資訊，請參閱 [互動式訊息執行API檔案](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).


   API呼叫範例也適用於 [此頁面](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

   >[!NOTE]
   >
   >如果您在建立行銷活動時已設定特定的開始和/或結束日期，則不會在這些日期以外執行，並且API呼叫將會失敗。

## 在API觸發的行銷活動中使用內容屬性 {#contextual}

透過API觸發的行銷活動，您可以在API裝載中傳遞其他資料，並在行銷活動中使用這些資料，以個人化您的訊息。

讓我們舉個例子，客戶想要重設密碼，而您想要傳送第三方工具產生的密碼重設URL。 透過API觸發的行銷活動，您可以將此產生的URL傳遞至API裝載，並運用至行銷活動以將其新增至訊息。

>[!NOTE]
>
>與設定檔啟用的事件不同，在REST API中傳遞的內容資料用於一次性通訊，而不是針對設定檔儲存。 設定檔的建立次數上限為名稱空間詳細資訊（如果找不到的話）。

為了在您的行銷活動中使用這些資料，您需要將這些資料傳遞至API裝載，並使用運算式編輯器新增至您的訊息中。 若要這麼做，請使用 `{{context.<contextualAttribute>}}` 語法，其中 `<contextualAttribute>` 應該符合包含您要傳遞之資料的API裝載中的變數名稱。

此 `{{context.<contextualAttribute>}}` 語法僅對應到String資料型別。

![](assets/api-triggered-context.png)


>[!IMPORTANT]
>
>傳入要求的內容屬性不能超過50kb，且一律視為字串型別。
>
>此 `context.system` 語法限製為僅限Adobe內部使用，並且不應用於傳遞內容屬性。

請注意，目前左側邊欄功能表中沒有可用的內容屬性。 屬性必須直接在個人化運算式中輸入，使用者不執行任何檢查 [!DNL Journey Optimizer].

## 在行銷活動執行時建立設定檔 {#profile-creation}

在某些情況下，您可能需要將交易式訊息傳送至系統中不存在的設定檔。 例如，如果未知的使用者嘗試重設您網站上的密碼。

當資料庫中不存在設定檔時，Journey Optimizer可讓您在執行行銷活動時自動建立該設定檔，以允許傳送訊息至此設定檔。

>[!IMPORTANT]
>
>若是交易式訊息，此功能僅適用於 **建立非常小的體積設定檔** 在大量交易式傳送使用案例中，大量設定檔已存在於平台中。

若要在行銷活動執行時啟用設定檔建立，請切換 **[!UICONTROL 建立新設定檔]** 中的選項 **[!UICONTROL 對象]** 區段。 如果停用此選項，則會拒絕任何傳送的未知設定檔，且API呼叫將失敗。

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>在中建立未知的設定檔 **AJO互動式訊息設定檔資料集** 資料集，分別位於每個傳出頻道（電子郵件、簡訊和推播）的三個預設名稱空間（電子郵件、電話和ECID）中。
