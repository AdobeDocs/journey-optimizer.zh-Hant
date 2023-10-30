---
title: 開始使用程式碼型體驗
description: 了解 Journey Optimizer 中的程式碼型體驗
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: ht
source-wordcount: '1172'
ht-degree: 100%

---

# 開始使用程式碼型頻道 {#get-sarted-code-based}

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* **[開始使用程式型頻道](get-started-code-based.md)**
* [程式碼型先決條件](code-based-prerequisites.md)
* [程式碼型實施範例](code-based-implementation-samples.md)
* [建立程式碼型體驗](create-code-based.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>程式碼型體驗頻道目前僅作為 Beta 版提供給部分使用者。若要加入 Beta 版計畫，請連絡 Adobe 客戶服務。

[!DNL Journey Optimizer] 可讓您透過所有接觸點 (例如：網頁應用程式、行動應用程式、桌面應用程式、視訊主控台、電視連結裝置、智慧型電視、資訊站、ATM、語音助理、IoT 裝置等)，個人化並測試您要提供給客戶的體驗。

透過&#x200B;**程式碼型體驗**&#x200B;功能，您可以使用簡單且直覺式的非視覺化編輯器來定義傳入體驗。 無論您擁有的應用程式類型為何，都可讓您在應用程式或網頁的個別與更精細位置插入和編輯特定元素，而不是將修改套用至整個內容。

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

當您[建立行銷活動](../campaigns/create-campaign.md#configure)時，請選取&#x200B;**程式碼型體驗 (Beta)** 作為您的動作，並定義基本設定。

>[!NOTE]
>
>如果這是您第一次建立網頁體驗，請務必遵循[本章節](code-based-prerequisites.md)所說明的先決條件。

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
<a href="code-based-prerequisites.md"><strong>先決條件</strong></a>
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
<a href="create-code-based.md#edit-code">
<img alt="驗證" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="create-code-based.md#edit-code"><strong>編輯程式碼</strong></a>
</div>
<p>
</td>
</tr></table>



<!--[Learn how to create a code-based campaign in this video](#video)-->

## 何時使用程式碼型頻道，而不是其他頻道 {#code-based-vs-other-channels}

### 比較程式碼型與其他頻道

何時應使用程式碼型頻道，而不是其他 [!DNL Journey Optimizer] 頻道？

* 透過網頁瀏覽器或行動應用程式存取數位屬性時，您都可以考慮使用程式碼型體驗，否則最好使用[!DNL Journey Optimizer][網路頻道](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"}。

* 如果網站無法載入至可支援網路頻道視覺化製作的[網頁設計工具](../web/edit-web-content.md#work-with-web-designer){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"}，您可以使用程式碼型頻道作為 [!DNL Journey Optimizer] 網路頻道的替代方案。

* 如果您採用 API 型、無頭式或伺服器端實施，您也可以使用程式碼型頻道作為 [!DNL Journey Optimizer] 網頁或應用程式內頻道的替代方案。

### 程式碼型對比網路頻道

若要執行網路使用案例，您可以使用網路頻道或程式碼型體驗，但具體適合使用哪一種則視您的內容而定。 主要差異如下所列，以便您能對何時使用哪種體驗做出明智的決定。

**網路**
* 使用[網頁設計工具](../web/edit-web-content.md#work-with-web-designer){target="_blank"}視覺化編輯器，編輯您的內容。
* 您需要 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}
* 網路頻道可讓您修改頁面上的所有內容，並包含可用來進行變更的預先定義動作清單。 [了解更多](../web/edit-web-content.md#work-with-web-designer){target="_blank"}
* 設定容易，上手快速。
* 專注於行銷人員角色。

**程式碼型體驗**
* 使用[運算式編輯器](create-code-based.md#edit-code)，編輯您的內容。
* 程式碼型體驗需要先在實施中的進行開發工作，以確保您的介面可以通過 [!DNL Journey Optimizer] 來解釋和傳遞為這些介面在邊緣上發佈的內容。[了解更多](#surface-definition)
* 它需要更多規劃，而且只能變更開發人員指定的內容。 因此，務必要識別介面上需要修改以進行個人化或測試的元件 (首頁橫幅、主圖影像、功能表列等)。然後與開發團隊合作，建置處理這些變更所需的實施。
* 它可讓您使用 JSON 程式碼內容。
* 專注於開發人員角色。

## 運作方式 {#how-it-works}

>[!CAUTION]
>
>此功能適合開發人員角色和/或經驗豐富的使用者。 只要是由開發團隊處理表面實作和初始設定，具備一些程式碼撰寫技能的行銷人員就可以使用此功能。

若要使用 [!DNL Journey Optimizer] 程式碼型體驗功能編輯內容，頁面或應用程式需要檢測。 若要這樣做，您必須預先宣告特定的個別位置 (稱為「[表面](#surface-definition)」)，其為您要插入或取代內容的位置<!--HOW??-->。

>[!NOTE]
>
>目前與表面相關聯的內容只能是 HTML 或 JSON。 <!--WILL COME LATER: text, image or another format depending on the application-->

實作程式碼型行銷活動的重要步驟如下。

1. 定義[表面](#surface-definition)，其基本上是您要新增程式碼型體驗的位置，然後使用此表面在 [!DNL Journey Optimizer] 中建立行銷活動。 [了解作法](create-code-based.md#create-code-based-campaign)

1. 使用 [!DNL Journey Optimizer] 運算式編輯器，為所選表面指定內容來編寫體驗。 [了解作法](create-code-based.md#edit-code)

1. 應用程式實施團隊會發出明確 API 或 SDK 呼叫，為已命名的表面擷取內容，例如「橫幅文字」或「建議匣 1」，或應用程式中與 UI 無關的決策點，例如「搜尋演算法參數」。 在此情況下，實作團隊負責轉譯或解譯傳回的內容並採取行動。<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## 什麼是表面？ {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="定義基於程式碼的體驗表面"
>abstract="基於程式碼的表面是為使用者或系統互動而設計的任何實體，由 URI 唯一識別。"

**程式碼型體驗表面**&#x200B;是為使用者或系統互動而設計的任何實體<!--ask Robert to explain further-->，由 **URI** 唯一識別。

換言之，可將表面視為位於任何有實體 (接觸點) 存在之階層層級的容器。<!--good idea to illustrate how it can be seen, but to clarify-->

* 其可以是網頁、行動應用程式、桌面應用程式，或大型實體內的特定內容位置 (例如`div`) 或非標準顯示模式 (例如，資訊站或桌面應用程式橫幅)。<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* 其也可以延伸至內容容器的特定片段，用於非顯示或抽象顯示目的 (例如，傳遞至服務的 JSON Blob)。

* 其也可以是符合各種用戶端介面定義的萬用字元表面 (例如，網站每個頁面上的主圖影像位置可翻譯為表面URI，例如：web://mydomain.com/*#hero_image)。

基本上，表面 URI 由多個區段組成：
1. **類型**：網頁、行動應用程式、服務、資訊站、tvcd 等
1. **屬性**：網域或應用程式套裝
1. **路徑**：頁面/應用程式活動 ± 頁面/應用程式活動上的位置 <!--to clarify-->

下表列出各種裝置的一些表面 URI 定義範例。

| 類型 | URI | 說明 |
| --------- | ----------- | ------- |   
| Web | web://domain.com/path/page.html | 代表網站的個別路徑和頁面。 |
| Web | web://domain.com/path/page.html#element | 代表特定網域的特定頁面中的個別元素。 |
| Web | web://domain.com/*#element | 萬用字元表面 - 代表特定網域下每個頁面中的個別元素。 |
| 桌面 | desktop://com.vendor.bundle | 代表特定的桌面應用程式。 |
| 桌面 | desktop://com.vendor.bundle#element | 代表應用程式中的特定元素，例如按鈕、功能表、主圖橫幅等。 |
| iOS 應用程式 | mobileapp://com.vendor.bundle | 代表單一平台的特定行動應用程式，在此案例中為 iOS 應用程式。 |
| iOS 應用程式 | mobileapp://com.vendor.bundle/activity | 代表行動應用程式中的特定活動 (檢視)。 |
| iOS 應用程式 | mobileapp://com.vendor.bundle/activity#element | 代表活動中的特定元素，例如按鈕或其他檢視元素。 |
| Android 應用程式 | mobileapp://com.vendor.bundle | 代表單一平台的特定行動應用程式，在此案例中為 Android 應用程式。 |
| tvOS 應用程式 | tvos://com.vendor.bundle | 代表特定的 tvOS 應用程式。 |
| 電視應用程式 | tvcd://com.vendor.bundle | 代表特定智慧型電視或電視連結裝置應用程式 - 套裝 ID。 |
| 服務 | service://servicename | 代表伺服器端程序或其他手動實體。 |
| 資訊站 | kiosk://location/screen | 潛在可輕鬆新增的其他表面類型範例。 |
| ATM | atm://location/screen | 潛在可輕鬆新增的其他表面類型範例。 |
