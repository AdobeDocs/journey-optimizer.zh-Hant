---
title: 最佳化AI收件匣的電子郵件文字
description: 調整Journey Optimizer中電子郵件的純文字層，以便在使用AI最佳化的電子郵件Designer中，AI輔助收件匣使用者端可在摘要郵件或擷取意圖時，使用您的優惠方案和CTA。
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
exl-id: 0c2f95ce-28a0-480c-9829-b7e4975b6340
source-git-commit: 88f47d375f01eff40a0f96e9cf0353b7914a0f89
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 1%

---

# 最佳化AI收件匣的電子郵件文字 {#email-text-optimizer}

[!DNL Adobe Journey Optimizer]隨附電子郵件通道功能，可協助您建構訊息的特定版本，以改善AI輔助收件匣體驗，例如[!DNL Apple Intelligence]中的[!DNL Google Gemini]和[!DNL Gmail]，讓他們能更準確地回答問題，並根據您的內容摘要郵件，獲得更好的結果。

您可以使用此功能來調整訊息的專屬文字版本，這樣AI輔助收件匣體驗就更有可能呈現您想要的選件、行動號召和詳細資訊，而不是精簡自動產生的文字或不相關內容。

## 運作方式 {#how-it-works}

收件者在AI輔助收件匣體驗中可能會詢問的常見問題是&#x200B;*此電子郵件是關於什麼的？*&#x200B;或&#x200B;*這些選件是什麼？*。

* 這些AI助理提供的答案可能是簡短摘要（例如，訊息為促銷、提及VIP早期存取和銷售，並包括產品類別的連結），但仍會省略行銷人員關心的目標，因為助理從他們有效看到的任何文字中推斷出來 — 不一定是您打算的完整故事。

* 此外，助理可能會主動搜尋與品牌相關的折扣或優惠券，並將這些內容摺疊成答案，因此使用者不再只檢視您實際承諾的訊息。 此行為對一般使用者很有用，但若行銷人員需要回答來追蹤傳送中的真實辭彙，此行為會稀釋他們的控制權。

為避免這些問題，[!DNL Journey Optimizer]會建立您訊息的額外文字版本，好讓優惠券、折扣範圍、行動號召以及其他優先順序以清晰的線性副本顯示在最前面。

>[!NOTE]
>
>此專屬文字版本與訊息的預設或自訂純文字版本不同。 [了解更多](text-version-email.md)

目標是讓收件匣AI將您定義的優惠方案和動作中的摘要和問答置於基礎位置，而非依賴較薄的預設文字部分或不相關的網頁結果。

>[!IMPORTANT]
>
>確切的AI助理行為取決於收件匣提供者和模型版本。 傳送電子郵件後，外部AI使用者端提供的回答和摘要可能會不正確、不完整或混淆網頁結果。
>
>「為AI收件匣最佳化電子郵件文字」功能只會在Journey Optimizer中產生專屬文字版本，無法保證第三方助理將如何解譯或顯示訊息。 深入瞭解第三方收件匣AI[的](#inbox-ai-risks)限制和風險。

## 建議的使用案例 {#use-cases}

<!--
* **Critical details only in images** — Offers, promo codes, or deadlines shown in banners or graphics are invisible in plain text. Use the optimizer (and manual edits) so the same facts appear as text, improving extraction by AI summaries and text-only clients.
-->

* **密集或零碎的自動產生文字** — 當預設純文字很難掃描時，最佳化可以透過明確的選件和連結產生更清晰的線性敘述。

* **控制收件匣問答** — 如果您希望收件者詢問助理&#x200B;*電子郵件內容*&#x200B;或&#x200B;*選件內容*，強大的人工智慧收件匣版本可減少部分摘要，並避免依賴未與已核准副本關聯的網頁輔助答案。

## 針對AI收件匣體驗最佳化 {#optimize-with-ai}

>[!IMPORTANT]
>
>使用此功能之前，請先閱讀相關的[風險和限制](#inbox-ai-risks)。
>
>若要存取此功能，您必須同意使用者合約，該合約會在您第一次在[!DNL Journey Optimizer]中使用Generative AI時顯示。 如需詳細資訊，請閱讀[Adobe Experience Cloud Generative AI使用者指南](https://www.adobe.com/tw/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}。

若要最佳化含有[!DNL Journey Optimizer]之AI收件匣的電子郵件純文字版本，請遵循下列步驟。

1. 在[電子郵件Designer](content-from-scratch.md)中開啟您的電子郵件（來自行銷活動、歷程或範本，視您的工作流程而定）。

1. 按一下&#x200B;**[!UICONTROL 「針對AI收件匣最佳化」]**&#x200B;按鈕，以產生改良版本，其中強調重要資訊，以供AI輔助閱讀和摘要之用。

   電子郵件Designer中的![最佳化AI收件匣按鈕](assets/optimize-for-ai-button.png){zoomable="yes" width="80%"}

1. 如果這是您第一次在[!DNL Journey Optimizer]中使用Generative AI，將會要求您同意使用者合約。 若要深入瞭解，請參閱[Adobe Generative AI使用者指南](https://www.adobe.com/tw/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}。

   ![Journey Optimizer中的Generative AI使用者合約對話方塊](assets/optimize-ai-inbox-agreement.png){width=50%}

   按一下&#x200B;**[!UICONTROL 同意]**&#x200B;以繼續。

1. 隨即顯示產生的版本。

   ![已針對AI收件匣最佳化的產生版本](assets/optimize-ai-inbox-output.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >**最佳化AI收件匣的電子郵件文字**&#x200B;不會變更您的HTML設計、配置或影像。

1. 若要對自動產生的內容進行變更，請選取&#x200B;**[!UICONTROL 啟用編輯]**&#x200B;切換按鈕，並視需要手動編輯內容。

1. 一旦對您的版本滿意，請按一下&#x200B;**[!UICONTROL 最佳化電子郵件]**&#x200B;按鈕以進行確認。

1. 您的電子郵件現在已成功針對AI收件匣最佳化。

1. 若要存取或編輯最佳化版本，請按一下&#x200B;**[!UICONTROL [已針對AI收件匣最佳化]]**&#x200B;按鈕。

   電子郵件Designer中的![重新最佳化按鈕](assets/optimize-ai-inbox-optimized-button.png){zoomable="yes" width="80%"}

1. 最佳化版本隨即顯示。 您可以&#x200B;**[!UICONTROL 移除最佳化]**，或按一下&#x200B;**[!UICONTROL 重新最佳化]**&#x200B;以產生新版本。

   ![電子郵件Designer中先前最佳化的版本](assets/optimize-ai-inbox-optimized-version.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >如果您變更原始HTML內容，您需要重新最佳化AI收件匣版本。

## 第三方收件匣AI的風險和限制 {#inbox-ai-risks}

「針對AI收件匣最佳化電子郵件」功能可協助您準備電子郵件的版本，以瞭解信箱提供者可能會處理您[!DNL Journey Optimizer]傳送的方式。 它不會控制這些提供者的產品。 一旦傳遞郵件，[!DNL Gmail]、[!DNL Apple]郵件、[!DNL Outlook]或其他使用者端的任何AI功能都會根據其條款、模型和原則運作，而不是Adobe的。

* **無法預測的簡報** — 摘要、通知模糊和對話式回答可能會省略優惠、錯誤陳述價格或日期、將內容與不相關的網頁結果合併，或是以不再符合您核准副本的方式轉述。 當供應商更新模型或UI而不另行通知時，行為會改變。

* **無法保證與HTML的同等性** — 依賴預覽或助理答案的收件者，可能永遠無法看到完整的HTML設計、影像或法律頁尾。 他們認為，訊息「說」的內容可能只來自AI產生的簡短摘要。

* **隱私權、法規遵循及資料使用** — 收件匣AI可能會根據提供者基礎建設的隱私權政策、保留及地區規則，處理該提供者基礎建設的郵件內容。 受規管行業的組織應評估收件者使用這類功能是否會影響其義務，而不論電子郵件在[!DNL Journey Optimizer]中的撰寫方式為何。

* **品牌與法律曝光度** — 不正確或不完整的AI摘要仍可能會導致客戶對促銷活動、條款或選擇退出語言產生混淆或爭議。 **針對AI收件匣最佳化電子郵件**&#x200B;無法確保協力廠商的模型會忠實地重製您電子郵件的最佳化版本。

* **[!UICONTROL 針對]**&#x200B;中的AI收件匣最佳化[!DNL Journey Optimizer] — 電子郵件Designer中的製作時間控制項與一般使用者收件匣助理不同。 傳送前，請務必檢閱產生的純文字。

## 相關主題 {#related-topics}

* [開始使用電子郵件設計](get-started-email-design.md)
* 如需更廣泛的Adobe產生功能，請參閱[開始使用AI助理來建立內容](../content-management/gs-generative.md)。
