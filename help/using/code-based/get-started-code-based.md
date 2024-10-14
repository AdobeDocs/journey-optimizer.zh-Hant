---
title: 開始使用程式碼型體驗
description: 了解 Journey Optimizer 中的程式碼型體驗
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: 83c8417d4aee278eba33e4adf6ccd033bcc6be1a
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 83%

---

# 開始使用程式碼型頻道 {#get-sarted-code-based}

[!DNL Journey Optimizer] 可讓您透過所有接觸點 (例如：網頁應用程式、行動應用程式、桌面應用程式、視訊主控台、電視連結裝置、智慧型電視、資訊站、ATM、語音助理、IoT 裝置等)，個人化並測試您要提供給客戶的體驗。

透過&#x200B;**程式碼型體驗**&#x200B;功能，您可以使用簡單且直覺式的非視覺化編輯器來定義傳入體驗。 無論您擁有的應用程式類型為何，都可讓您在應用程式或網頁的個別與更精細位置插入和編輯特定元素，而不是將修改套用至整個內容。

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>有關程式碼型體驗的特定護欄和建議，請參閱[此頁面](code-based-prerequisites.md)。


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="#how-it-works">
<img alt="銷售機會" src="../assets/do-not-localize/privacy-audit.jpeg">
</a>
<div><a href="#how-it-works"><strong>運作方式</strong>
</div>
<p>
</td>
<td>
<a href="code-based-prerequisites.md">
<img alt="驗證" src="../assets/do-not-localize/web-prerequisites.jpg">
</a>
<div>
<a href="code-based-prerequisites.md"><strong>護欄和限制</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="不頻繁" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>建立程式碼型體驗</strong></a>
</div>
<p></td>
<td>
<a href="code-based-implementation-samples.md">
<img alt="驗證" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong>實施範例</strong></a>
</div>
<p>
</td>
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

## 何時使用程式碼型頻道，而不是其他頻道 {#code-based-vs-other-channels}

### 比較程式碼型與其他頻道

何時應使用程式碼型頻道，而不是其他 [!DNL Journey Optimizer] 頻道？

* 透過網頁瀏覽器或行動應用程式存取數位屬性時，您都可以考慮使用程式碼型體驗，否則最好使用 [!DNL Journey Optimizer] [Web 管道](../web/get-started-web.md){target="_blank"}或[!DNL Journey Optimizer] [應用程式內傳訊](../in-app/get-started-in-app.md){target="_blank"}管道。

* 如果網站無法載入至[網頁設計工具](../web/edit-web-content.md#work-with-web-designer){target="_blank"}視覺編輯器，或您無法使用可支援 Web 管道視覺化製作的[瀏覽器擴充功能](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"}，您可以使用程式碼型管道作為 [!DNL Journey Optimizer] Web 管道的替代方案。

* 如果您採用 API 型、無頭式或伺服器端實施，您也可以使用程式碼型頻道作為 [!DNL Journey Optimizer] 網頁或應用程式內頻道的替代方案。

### 程式碼型對比網路頻道 {#code-based-vs-web}

若要執行網路使用案例，您可以使用網路頻道或程式碼型體驗，但具體適合使用哪一種則視您的內容而定。 主要差異如下所列，以便您能對何時使用哪種體驗做出明智的決定。

**網路**

* 使用[網頁設計工具](../web/edit-web-content.md#work-with-web-designer){target="_blank"}視覺化編輯器，編輯您的內容。
* 您需要已在網頁瀏覽器上安裝 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"} 實作與 [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 擴充功能。 [深入暸解](../web/web-prerequisites.md){target="_blank"}
* 網路頻道可讓您修改頁面上的所有內容，並包含可用來進行變更的預先定義動作清單。 [了解更多](../web/edit-web-content.md#work-with-web-designer){target="_blank"}
* 設定容易，上手快速。
* 專注於行銷人員角色。

**程式碼型體驗**

* 使用[個人化編輯器](create-code-based.md#edit-code)，編輯您的內容。
* 程式碼型體驗需要先在實施中的進行開發工作，以確保您的應用程式可以通過 [!DNL Journey Optimizer] 來解譯和傳遞為這些位置在邊緣上發佈的內容。[了解更多](code-based-configuration.md#surface-definition)
* 它需要更多規劃，而且只能變更開發人員指定的內容。 因此，務必要識別介面上需要修改以進行個人化或測試的元件 (首頁橫幅、主圖影像、功能表列等)。然後與開發團隊合作，建置處理這些變更所需的實施。
* 它可讓您使用 JSON 程式碼內容。
* 專注於開發人員角色。

## 運作方式 {#how-it-works}

>[!CAUTION]
>
>此功能適合開發人員角色和/或經驗豐富的使用者。 只要您的開發團隊處理頻道設定和初始設定，具備某些程式碼撰寫技能的行銷人員就可以使用此功能。

若要使用 [!DNL Journey Optimizer] 程式碼型體驗功能編輯內容，頁面或應用程式需要檢測。 若要這麼做，您必須先宣告您要插入或取代內容的特定個別位置（稱為&quot;[曲面](code-based-configuration.md#surface-definition)&quot;）。

>[!NOTE]
>
>目前，與設定相關聯的內容只能是HTML或JSON。

實作程式碼型行銷活動的重要步驟如下。

1. 在您的應用程式實作中定義[surface](code-based-configuration.md#surface-definition)，這基本上是您要新增程式碼型體驗的位置，並建立參照該位置的程式碼型體驗通道設定。 [了解作法](code-based-configuration.md#create-code-based-configuration)

1. 使用此設定在[!DNL Journey Optimizer]中建立歷程或行銷活動。 [了解作法](create-code-based.md#create-code-based-campaign)

1. 使用 [!DNL Journey Optimizer] 個人化編輯器，為所選設定指定內容來編寫體驗。 [了解作法](create-code-based.md#edit-code)

1. 應用程式實施團隊會發出明確 API 或 SDK 呼叫，為已命名的表面擷取內容，例如「橫幅文字」或「建議匣 1」，或應用程式中與 UI 無關的決策點，例如「搜尋演算法參數」。 在此情況下，實作團隊負責轉譯或解譯傳回的內容並採取行動。 [了解更多](code-based-implementation-samples.md)
