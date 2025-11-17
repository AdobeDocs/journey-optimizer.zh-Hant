---
title: 開始使用程式碼型體驗
description: 了解 Journey Optimizer 中的程式碼型體驗
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: ht
source-wordcount: '855'
ht-degree: 100%

---

# 開始使用程式碼型頻道 {#get-started-code-based}

[!DNL Journey Optimizer] 可讓您透過所有接觸點 (例如：網頁應用程式、行動應用程式、桌面應用程式、視訊主控台、電視連結裝置、智慧型電視、資訊站、ATM、語音助理、IoT 裝置等)，個人化並測試您要提供給客戶的體驗。

透過&#x200B;**程式碼型體驗**&#x200B;功能，您可以使用簡單且直覺式的非視覺化編輯器來定義傳入體驗。 無論您擁有的應用程式類型為何，都可讓您在應用程式或網頁的個別與更精細位置插入和編輯特定元素，而不是將修改套用至整個內容。

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>有關程式碼型體驗的特定建議，請參閱[此頁面](code-based-prerequisites.md)。


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<!--[Learn how to create a code-based campaign in this video](#video)-->

➡️[本章節](../experience-decisioning/experience-decisioning-uc.md)呈現了一個端到端使用案例，說明如何使用內容實驗來比較決策與程式碼型體驗管道。

## 何時使用程式碼型頻道，而不是其他頻道 {#code-based-vs-other-channels}

### 比較程式碼型與其他頻道

何時應使用程式碼型頻道，而不是其他 [!DNL Journey Optimizer] 頻道？

* 透過網頁瀏覽器或行動應用程式存取數位屬性時，您都可以考慮使用程式碼型體驗，否則最好使用 [!DNL Journey Optimizer] [Web 管道](../web/get-started-web.md){target="_blank"}或[!DNL Journey Optimizer] [應用程式內傳訊](../../rp_landing_pages/in-app-landing-page.md){target="_blank"}管道。

<!--* You can use the code-based channel as an alternative to the [!DNL Journey Optimizer] web channel if your website cannot be loaded into the [web designer](../web/web-visual-editor.md){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} that powers visual authoring for web channel.-->

* 如果您採用 API 型、無頭式或伺服器端實施，就可以使用程式碼型頻道作為 [!DNL Journey Optimizer] 網頁或應用程式內頻道的替代方案。

* 如果您想要修改原生應用程式內內容，而非顯示模式、快顯視窗或覆蓋內容，也可以善用原生行動應用程式上的程式碼型頻道，當成應用程式內頻道的替代方案。

### 程式碼型對比網路頻道 {#code-based-vs-web}

若要執行網路使用案例，您可以使用網路頻道或程式碼型體驗，但具體適合使用哪一種則視您的內容而定。 主要差異如下所列，以便讓您可以針對何時使用哪種體驗，做出明智的決定。

**網頁**

* 使用[網頁設計工具](../web/web-visual-editor.md){target="_blank"}視覺化編輯器，或是網頁[非視覺化編輯器](../web/web-non-visual-editor.md)來編輯您的內容。
* 您需要 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"} — 用戶端實作。
  <!--* You need the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}-->
* 網路頻道可讓您修改頁面上的所有內容，並包含可用來進行變更的預先定義動作清單。 [了解更多](../web/web-visual-editor.md){target="_blank"}
* 設定容易，上手快速。
* 專注於行銷人員人物誌。

**程式碼型體驗**

* 使用[個人化編輯器](create-code-based.md#edit-code)，編輯您的內容。
* 您必須已先安裝 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"} - 用戶端實作，或是 [AEP Edge Network 伺服器 API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=zh-Hant){target="_blank"} - 伺服器端實作。
* 程式碼型體驗需要先在實施中的進行開發工作，以確保您的應用程式可以通過 [!DNL Journey Optimizer] 來解譯和傳遞為這些位置在邊緣上發佈的內容。[了解更多](code-based-surface.md)
* 它需要更多規劃，而且只能變更開發人員指定的內容。 因此，您必須識別應用程式上有哪些元件 (首頁橫幅、網頁橫幅、功能表列等) 需要修改，以便進行個人化或測試，同時與開發團隊合作，即可建立用來處理這類變更所需的實作。
* 它可讓您使用 JSON 程式碼內容。
* 專注於開發人員人物誌。

## 運作方式 {#how-it-works}

>[!CAUTION]
>
>此功能適合開發人員人物誌和/或經驗豐富的使用者。 只要是由開發團隊處理通道設定和初始設定，具備一些程式碼撰寫技能的行銷人員就可以使用此功能。

若要使用 [!DNL Journey Optimizer] 程式碼型體驗功能編輯內容，頁面或應用程式需要檢測。若要這樣做，您必須預先宣告特定的個別位置 (又稱為「[表面](code-based-surface.md)」)，也就是您想要插入或取代內容的位置。

>[!NOTE]
>
>目前與設定相關聯的內容只能使用 HTML 或 JSON 格式。

必須先建立並提交以下程式碼型體驗的重要步驟。

1. 請務必遵循頻道特定先決條件。 [了解更多](code-based-prerequisites.md)

1. 在應用程式實作中定義[表面](code-based-surface.md#surface-definition)，基本上那裡就是您想要新增體驗的位置。

1. 建立參考位置的程式碼型管道設定。 [了解作法](code-based-configuration.md#create-code-based-configuration)

1. 使用此設定在 [!DNL Journey Optimizer] 中建立歷程或行銷活動。[了解作法](create-code-based.md#create-code-based-experience)

1. 使用 [!DNL Journey Optimizer] 個人化編輯器，為所選設定指定內容來編寫體驗。 [了解作法](create-code-based.md#edit-code)

1. 測試程式碼型體驗。 [了解作法](test-code-based.md)

1. 發佈內容。[了解作法](publish-code-based.md)

1. 程式碼型體驗歷程或行銷活動正式上線後，要求必須先準備好表面內容的應用程式，或頁面實作，才能擷取並顯示內容。

   >[!INFO]
   >
   >若想確認，應用程式實施團隊會送出明確 API 或 SDK 呼叫，為程式碼型設定中已定義的表面擷取內容，例如「橫幅文字」或「建議匣 1」，或應用程式中與 UI 無關的決策點，例如「搜尋演算法參數」。 <!--In this case, the implementation team is responsible for rendering or otherwise interpreting and acting on the returned content.--> [了解更多](code-based-implementation-samples.md)

## 其他資源

* **[建立程式碼型體驗](create-code-based.md)** - 了解如何建立及設定自訂實作的程式碼型行銷活動和歷程。
* **[設定程式碼型管道](code-based-configuration.md)** - 使用適當的介面和實作設定來設定程式碼型體驗設定。
* **[程式碼型先決條件](code-based-prerequisites.md)** - 了解實作所需的技術需求和開發人員資源。
* **[測試程式碼型體驗](test-code-based.md)** - 了解如何在發佈之前預覽和測試您的程式碼型體驗。
* **[實作範例](code-based-implementation-samples.md)** - 探索各種使用案例的程式碼範例和實作模式。
* **[程式碼型體驗教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/channels/code-based-experience-channel/create-a-code-based-experience-campaign){target="_blank"}** - 探索有關程式碼型功能和最佳做法的逐步教學課程影片。

