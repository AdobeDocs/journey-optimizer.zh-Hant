---
title: 程式碼型表面
description: 瞭解什麼是程式碼型體驗介面
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 07ec74fb-7fbc-48c6-a8fc-f58f24a60723
source-git-commit: d3f15c09194a50b95107fb84d680606a468f8644
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 50%

---

# 程式碼型體驗表面 {#code-based-surface}

## 什麼是表面？ {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="新增元件的表面 URI"
>abstract="如果您的實作不是針對 Web、iOS 或 Android，或如果您需要以特定 URI 為目標，請輸入表面 URI，它是唯一識別碼，指向您想要提供體驗的實體。確保您輸入的表面 URI 符合您自己的實作中使用的 URI。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-configuration#other" text="為其他平台建立基於程式碼的體驗設定"

程式碼型體驗&#x200B;**surface**&#x200B;是任何專為使用者或系統互動而設計的實體，由[URI](#surface-uri)唯一識別。 介面是在[應用程式實作](code-based-prerequisites.md#implementation-prerequisites)中指定，且必須符合您在[程式碼型體驗通道設定](code-based-configuration.md)中參考的介面。

在任何階層層級中，只要有實體（接觸點）存在，即可將表面視為容器。

* 其可以是網頁、行動應用程式、桌面應用程式，或大型實體內的特定內容位置 (例如`div`) 或非標準顯示模式 (例如，資訊站或桌面應用程式橫幅)。<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* 其也可以延伸至內容容器的特定片段，用於非顯示或抽象顯示目的 (例如，傳遞至服務的 JSON Blob)。

* 其也可以是符合各種用戶端介面定義的萬用字元表面 (例如，網站每個頁面上的主圖影像位置可翻譯為表面URI，例如：web://mydomain.com/*#hero_image)。

>[!NOTE]
>
>當您在同一個表面上執行多個程式碼型體驗動作時，如果使用者符合多個動作的資格，促銷活動或歷程的&#x200B;**[!UICONTROL 優先順序分數]**&#x200B;會決定要傳遞給他們的專案。 [進一步瞭解優先順序分數](../conflict-prioritization/priority-scores.md)

## 表面識別碼 {#surface-uri}

**表面URI**&#x200B;是直接導向應用程式內不同使用者介面元素或元件的精確識別碼。 表面URI基本上由多個區段組成：

1. **類型**：網頁、行動應用程式、ATM、資訊站、tvcd、服務等
1. **屬性**：頁面 URL 或應用程式套裝
1. **容器**：頁面/應用程式活動上的位置

下表列出各種裝置的一些表面 URI 定義範例。

**網頁與行動裝置**

| 類型 | URI | 說明 |
| --------- | ----------- | ------- | 
| 網頁 | `web://domain.com/path/page.html#element` | 代表特定網域之特定頁面中的個別元素，其中元素可以是標籤，如下列範例中的標籤：hero_banner、top_nav、menu、footer 等。 |
| iOS 應用程式 | `mobileapp://com.vendor.bundle/activity#element` | 代表原生應用程式活動中的特定元素，例如按鈕或其他檢視元素。 |
| Android 應用程式 | `mobileapp://com.vendor.bundle/#element` | 代表原生應用程式中的特定元素。 |

**其他裝置型別**

| 類型 | URI | 說明 |
| --------- | ----------- | ------- | 
| 桌面 | `desktop://com.vendor.bundle/#element` | 代表應用程式中的特定元素，例如按鈕、功能表、主圖橫幅等。 |
| 電視應用程式 | `tvcd://com.vendor.bundle/#element` | 代表智慧型電視或電視連結裝置應用程式的特定元素 - 套裝 ID。 |
| 服務 | `service://servicename/#element` | 代表伺服器端程序或其他手動實體。 |
| 資訊站 | `kiosk://location/screen#element` | 潛在可輕鬆新增的其他表面類型範例。 |
| ATM | `atm://location/screen#element` | 潛在可輕鬆新增的其他表面類型範例。 |

**萬用字元表面**

| 類型 | URI | 說明 |
| --------- | ----------- | ------- | 
| 萬用字元網頁 | `wildcard:web://domain.com/*#element` | 萬用字元表面 - 代表特定網域下每個頁面中的個別元素。 |
| 萬用字元網頁 | `wildcard:web://*domain.com/*#element` | 萬用字元表面 - 代表所有以「domain.com」結尾的網域下每個頁面中的個別元素。 |

## URI構成 {#uri-composition}

在[!DNL Journey Optimizer]中，程式碼型Experience Channel支援兩種客戶實作：

* 根據您網站的[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"}，或行動應用程式的[Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"}；
* 使用[AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=zh-Hant){target="_blank"}的伺服器端或混合式。

>[!NOTE]
>
>在[本節](code-based-prerequisites.md#implementation-prerequisites)中進一步瞭解實作必要條件。

使用程式碼型體驗，您可以在精細位置<!--(such as a specific location on a page, or inside a mobile native app)-->上修改內容，這些位置由[!DNL Journey Optimizer]使用[表面URI](#surface-uri)唯一識別。

這些表面URI的構成和處理取決於實作方法：

* **網頁/行動SDK**：您的網頁/行動開發人員需要將這些精細的位置定義為簡單的字串，因為網頁/行動SDK能根據目前的URL/應用程式ID和位置字串自動撰寫表面URI。

* **Edge Network API**：應用程式/頁面開發人員必須定義包含完整路徑和使用內容位置的完整表面URI，因為此型別的實作需要完整URI。

這就是建立[程式碼型體驗通道組態](code-based-configuration.md)時，您有兩種方式可根據選取的平台指定介面：

* 針對&#x200B;**[!UICONTROL Web]**、**[!UICONTROL iOS]**&#x200B;和&#x200B;**[!UICONTROL Android]**&#x200B;平台，您必須輸入&#x200B;**URL/應用程式ID**&#x200B;和&#x200B;**位置或路徑**&#x200B;來構成介面。 深入瞭解如何為[網頁](code-based-configuration.md#web)和[行動裝置](code-based-configuration.md#mobile)平台設定程式碼型體驗

* 如果平台是&#x200B;**[!UICONTROL Other]**，您必須輸入完整的&#x200B;**表面URI**，如上述範例[所示](#surface-uri)。 深入瞭解如何為[其他](code-based-configuration.md#other)平台設定程式碼型體驗
