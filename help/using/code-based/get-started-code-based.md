---
title: 開始使用程式碼型體驗
description: 瞭解Journey Optimizer中的程式碼型體驗
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
source-git-commit: 4aea5c1434caa07aad26445c49a3d5c6274502ec
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 7%

---

# 開始使用程式碼型管道 {#get-sarted-code-based}

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* **[開始使用程式碼型管道](get-started-code-based.md)**
* [程式碼型必要條件](code-based-prerequisites.md)
* [程式碼型實施範例](code-based-implementation-samples.md)
* [建立程式碼型體驗](create-code-based.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>程式碼型體驗管道目前僅供特定使用者使用，可作為測試版使用。 若要加入測試版計畫，請連絡 Adobe 客戶服務。

[!DNL Journey Optimizer] 可讓您透過所有接觸點（例如網頁應用程式、行動應用程式、案頭應用程式、視訊主控台、電視連線裝置、智慧型電視、資訊站、ATM、語音助理、物聯網裝置等），個人化並測試您要提供給客戶的體驗。

使用 **程式碼型體驗** 功能，您可以使用簡單且直覺式的非視覺編輯器來定義傳入體驗。 無論您擁有的應用程式型別為何，都可讓您在應用程式或網頁的個別與更精細位置插入及編輯特定元素，而非將修改套用至整個內容。

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

當您 [建立行銷活動](../campaigns/create-campaign.md#configure)，選取 **程式碼型體驗(Beta)** 作為您的動作，並定義基本設定。

>[!NOTE]
>
>如果這是您第一次建立網頁體驗，請務必遵循[本章節](code-based-prerequisites.md)所說明的必要條件。

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
<a href="create-code-based.md#edit-code"><strong>編輯您的程式碼</strong></a>
</div>
<p>
</td>
</tr></table>



<!--[Learn how to create a code-based campaign in this video](#video)-->

## 何時使用程式碼式與其他通道 {#code-based-vs-other-channels}

### 程式碼型與其他管道的比較

何時應使用程式碼型通道，而非其他通道 [!DNL Journey Optimizer] 頻道？

* 若您的數位屬性並未透過網頁瀏覽器或行動應用程式進行存取，您可以隨時考慮使用程式碼型體驗，在這樣的情況下，您可能可以更好地使用 [!DNL Journey Optimizer] [Web channel](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"} 頻道。

* 您可以使用程式碼型管道做為 [!DNL Journey Optimizer] 如果網站無法載入到web channel [網頁視覺化編輯器](../web/author-web.md){target="_blank"} or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} 可支援Web Channel的視覺化撰寫。

* 您也可以使用程式碼型管道做為 [!DNL Journey Optimizer] 網頁或應用程式內頻道，以備您採用API型、Headless或伺服器端實作時使用。

### 程式碼型與Web Channel

若要執行Web使用案例，您可以使用Web Channel或程式碼型體驗，但根據您的內容，一種可能比另一種更適合。 主要差異如下所列，以便您能夠針對何時使用做出明智的決策。

**Web**
* 使用編輯您的內容 [視覺化編輯器](../web/author-web.md){target="_blank"}.
* 您需要 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}
* Web Channel可讓您修改頁面上的所有內容，並具備可用來變更的預先定義動作清單。 [了解更多](../web/author-web.md){target="_blank"}
* 設定容易，快速上線。
* 更專注於行銷人員角色。

**程式碼型體驗**
* 使用編輯您的內容 [程式碼編輯器](create-code-based.md#edit-code).
* 程式碼型體驗需要您先前在實作中的開發工作，以確保您的介面可透過以下方式解譯及傳遞發佈在邊緣的內容 [!DNL Journey Optimizer] 用於這些曲面。 [了解更多](#surface-definition)
* 它需要更多規劃，而且只能變更開發人員指定的專案。 因此，必須識別元件（首頁橫幅、主圖影像、功能表列等） ，然後與您的開發團隊合作，建置處理這些變更所需的實作。
* 它可讓您使用JSON程式碼內容。
* 以開發人員為重點。

## 運作方式 {#how-it-works}

>[!CAUTION]
>
>此功能適用於開發人員角色和/或經驗豐富的使用者。 只要您的開發團隊處理表面實作和初始設定，具備某些程式碼撰寫技能的行銷人員就可以使用此功能。

若要使用編輯內容 [!DNL Journey Optimizer] 程式碼型體驗功能，您的頁面或應用程式需要檢測。 若要這麼做，您必須預先宣告特定的個別位置(稱為&quot;[曲面](#surface-definition)&quot;)要插入或取代內容的位置<!--HOW??-->.

>[!NOTE]
>
>目前與表面相關的內容只能是HTML或JSON。 <!--WILL COME LATER: text, image or another format depending on the application-->

實施程式碼型行銷活動的主要步驟如下。

1. 定義 [表面](#surface-definition)，這是您新增程式碼型體驗並在中建立行銷活動的位置 [!DNL Journey Optimizer] 使用此曲面。 [了解作法](create-code-based.md#create-code-based-campaign)

1. 使用為所選曲面指定內容來撰寫體驗 [!DNL Journey Optimizer] 程式碼編輯器。 [了解作法](create-code-based.md#edit-code)

1. 您的應用程式實作團隊會發出明確API或SDK呼叫，為已命名的表面擷取內容，例如「橫幅文字」或「Recommendations系統匣1」，或應用程式中與UI無關的決策點，例如「搜尋演演算法引數」。 在此情況下，實作團隊負責轉譯或解譯傳回的內容並採取行動。<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## 什麼是表面？ {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="定義程式碼型體驗介面"
>abstract="程式碼型介面是指任何專為使用者或系統互動而設計的實體，可由URI唯一識別。"

A **程式碼型體驗介面** 是專為使用者或系統互動設計的任何實體<!--ask Robert to explain further-->，此資訊會由 **URI**.

換言之，若有任何階層層級具有實體（接觸點）存在，則可將表面視為容器。<!--good idea to illustrate how it can be seen, but to clarify-->

* 可以是網頁、行動應用程式、案頭應用程式，或大型實體內的特定內容位置(例如 `div`)或非標準顯示模式（例如資訊站或案頭應用程式橫幅）。<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* 它也可以延伸至內容容器的特定片段，用於非顯示或抽象顯示目的（例如，傳送至服務的JSON Blob）。

* 它也可以是符合各種使用者端介面定義的萬用字元介面(例如，網站每個頁面上的主圖影像位置可以翻譯為介面URI，例如：web://mydomain.com/*#hero_image)。

表面URI基本上由多個區段組成：
1. **型別**：網頁、行動應用程式、服務、資訊站、tvcd等。
1. **屬性**：網域或應用程式套件組合
1. **路徑**：頁面/應用程式活動±頁面/應用程式活動上的位置 <!--to clarify-->

下表列出各種裝置的一些表面URI定義範例。

| 類型 | URI | 說明 |
| --------- | ----------- | ------- |   
| Web | web://domain.com/path/page.html | 代表網站的個別路徑和頁面。 |
| Web | web://domain.com/path/page.html#element | 代表特定網域之特定頁面中的個別元素。 |
| Web | web://domain.com/*#element | 萬用字元表面 — 代表特定網域下每個頁面中的個別元素。 |
| 桌面 | desktop://com.vendor.bundle | 代表特定的案頭應用程式。 |
| 桌面 | desktop://com.vendor.bundle#element | 代表應用程式中的特定元素，例如按鈕、功能表、主圖橫幅等。 |
| iOS 應用程式 | ios://com.vendor.bundle | 代表單一平台的特定行動應用程式 — 在此案例中為iOS應用程式。 |
| iOS 應用程式 | ios://com.vendor.bundle/activity | 代表行動應用程式中的特定活動（檢視）。 |
| iOS 應用程式 | ios://com.vendor.bundle/activity#element | 代表活動內的特定元素，例如按鈕或其他檢視元素。 |
| Android應用程式 | android://com.vendor.bundle | 代表單一平台的特定行動應用程式 — 在此案例中為Android應用程式。 |
| tvOS應用程式 | tvos://com.vendor.bundle | 代表特定的tvOS應用程式。 |
| 電視應用程式 | tvcd://com.vendor.bundle | 代表特定的智慧型電視或電視連線裝置應用程式 — 套件組合ID。 |
| 服務 | service://servicename | 代表伺服器端程式或其他手動實體。 |
| 資訊站 | kiosk://location/screen | 可輕鬆新增的潛在其他曲面型別範例。 |
| ATM | atm://location/screen | 可輕鬆新增的潛在其他曲面型別範例。 |