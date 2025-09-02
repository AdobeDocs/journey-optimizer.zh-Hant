---
solution: Journey Optimizer
product: journey optimizer
title: 切換至深色模式
description: 瞭解如何在電子郵件Designer中使用深色模式
badge: label="Beta" type="Informative"
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 深色模式，電子郵件，顏色，編輯器
hide: true
hidefromtoc: true
exl-id: 27442cb0-5027-4d9c-9d3c-9ec33af7c9ff
source-git-commit: 95e50386d4190d0b967d133a327c25ab1681b5c1
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 13%

---

# 管理深色模式內容 {#dark-mode}

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode"
>title="切換至深色模式"
>abstract="切換至深色模式，您可以預覽其呈現方式並定義特定的自訂設定。<br>警告：最終呈現結果取決於收件者的電子郵件用戶端。並非所有電子郵件用戶端都支援自訂深色模式。"

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode_image"
>title="將特定影像用於深色模式"
>abstract="您可以選取另一張影像，以在深色模式開啟時顯示。<br>警告：為深色模式新增特定影像並不能保證它將在所有電子郵件用戶端中正確呈現。並非所有電子郵件用戶端都支援自訂深色模式。"

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode_preview"
>title="切換至深色模式"
>abstract="切換至深色模式，以預覽它在支援的電子郵件用戶端上的呈現方式。<br>警告：最終呈現結果取決於收件者的電子郵件用戶端。並非所有電子郵件用戶端都支援自訂深色模式。"

>[!AVAILABILITY]
>
>此功能目前為 Beta 版本，僅供 Beta 版客戶使用。若要加入 Beta 版計畫，請聯絡 Adobe 代表。

設計電子郵件時，[!DNL Journey Optimizer] [電子郵件Designer](get-started-email-design.md)可讓您切換至&#x200B;**[!UICONTROL 深色模式]**，您可在此定義特定的自訂設定。 當深色模式開啟時，支援的電子郵件使用者端會顯示您為此模式定義的設定。

>[!WARNING]
>
>深色模式的最終呈現取決於收件者的電子郵件使用者端。
>
>並非所有電子郵件用戶端都支援自訂深色模式。<!--[See the list](#non-supporting-email-clients)-->此外，某些電子郵件使用者端只會對收到的所有電子郵件套用自己的預設深色模式。 在此情況下，您無法轉譯您在電子郵件Designer中定義的自訂設定。

[此區段](#supporting-email-clients)中會顯示支援深色模式的電子郵件使用者端清單。

## 什麼是深色模式？ {#what-is-dark-mode}

深色模式可讓支援的電子郵件使用者端和應用程式針對文字、按鈕和其他UI元素，顯示背景較暗且顏色較淺的電子郵件。 它可減輕眼睛疲勞、節省電池壽命，並改善低光環境的可讀性，提供更舒適的觀賞體驗。

<!--Dark Mode uses a dark color palette with light text and UI elements to reduce eye strain, save battery life, and improve readability in low-light environments.-->

隨著主要作業系統和應用程式(Apple Mail、Gmail、Outlook、Twitter、Slack)的發展，確保內容清晰易懂，並吸引所有使用者觀看已成為現代電子郵件設計的重要考量。

不過，無法保證您的電子郵件在所有裝置上的深色模式中看起來完全相同。 電子郵件應用程式或裝置覆寫原始設計，也可能會導致某些視覺上的變更。

事實上，電子郵件使用者端套用深色模式的方式可能有所不同，如下所示<!--between different devices and apps-->：

* 並非所有電子郵件使用者端都支援此功能。

  >[!NOTE]
  >
  >[此區段](#non-supporting-email-clients)中會顯示不支援深色模式的電子郵件使用者端清單。

* 有些電子郵件使用者端會自動調整顏色、背景和影像。 在此情況下，如果您在電子郵件Designer中定義自訂設定，這些設定可能不會呈現。

* 其他電子郵件使用者端提供呈現自訂深色模式的選項（例如使用`@media (prefers-color-scheme: dark)`方法）。 在此情況下，應顯示您在電子郵件Designer中定義的特定設定。 在[本節](#define-custom-dark-mode)中瞭解如何在電子郵件Designer中定義自訂深色模式設定。

## 電子郵件設計工具中的深色模式 {#dark-mode-email-designer}

在電子郵件Designer中，若要使用深色模式，必須考量兩個方面：

* 您可以預覽預設深色模式在大多數支援的電子郵件使用者端中的呈現方式。 [了解更多](#preview-dark-mode)

<!--
    >[!CAUTION]
    >
    >The final rendering may vary according to the recipient's email client. To see the exact rendering for each email client, use the [Email rendering](../content-management/rendering.md) option.-->

* 如果您想要覆寫支援電子郵件使用者端的預設設定，可以定義套用至正在編輯之電子郵件的自訂深色模式設定。 [了解更多](#define-custom-dark-mode)

<!--
    >[!WARNING]
    >
    >Not all email clients support custom dark mode. Some email clients only apply their own default dark mode for all emails that are received. In this case, the custom settings that you defined in the Email Designer cannot be rendered. [Learn more](#guardrails)-->

### 預覽預設深色模式 {#preview-dark-mode}

若要存取電子郵件Designer中的深色模式，並取得預設深色模式設定的預覽，請遵循下列步驟。

1. 從電子郵件Designer首頁，選取&#x200B;**[!UICONTROL 從草稿開始設計]**&#x200B;選項。 [了解更多](content-from-scratch.md)

<!--Should work with templates and themes, NOT for LP and fragments - but TBC with eng.
    >[!NOTE]
    >
    >Currently you may not be able to switch to dark mode if you select an [email template](use-email-templates.md) or if you apply a [theme](apply-email-themes.md).-->

1. 將[結構](content-from-scratch.md)和[內容元件](content-components.md)新增至您的內容。

1. 在中央畫布的右上方，切換至&#x200B;**[!UICONTROL 深色模式]**。

   ![](assets/light-mode-toggle.png)

1. 預設深色模式預覽隨即顯示。

   ![](assets/dark-mode-default.png)

依預設，電子郵件Designer深色模式預覽會將「全色反轉」色彩配置套用至影像和圖示以外的所有元素。

這表示它會偵測含有明暗元素的區域，並加以反轉，讓淺色背景變成深色，深色文字變成淺色，而深色背景變成淺色，淺色文字變成深色。

>[!CAUTION]
>
>最終呈現內容可能會因收件者的電子郵件使用者端而異。 若要檢視儘可能接近每個電子郵件使用者端最終結果的模擬，請使用[電子郵件呈現](../content-management/rendering.md)選項。

<!--This is custom dark mode:

  ![](assets/dark-mode-custom.png)

Here you can see that we have applied a different background, defined another image and change the color of the text and button.-->

### 定義自訂深色模式 {#define-custom-dark-mode}

切換至&#x200B;**[!UICONTROL 深色模式]**&#x200B;後，您可以選擇編輯內容的特定樣式元素，這些樣式元素只有在收件者的電子郵件使用者端中啟用深色模式時才會顯示，前提是它支援該功能。

>[!WARNING]
>
>並非所有電子郵件使用者端都支援深色模式。 此外，某些電子郵件用戶端只會對收到的所有電子郵件套用自己的預設深色模式。在這兩種情況下，系統無法呈現您在電子郵件設計工具中定義的自訂設定。

若要運用Email Designer自訂深色模式樣式，Journey Optimizer會使用<!-- `@media (prefers-color-scheme: dark)` method--> `@media (prefers-color-scheme: dark)` CSS查詢，會偵測使用者的電子郵件使用者端是否已設為深色模式，並套用您電子郵件中定義的深色主題設計。

若要定義自訂深色模式設定，請遵循下列步驟。

1. 請務必在電子郵件Designer中切換至&#x200B;**[!UICONTROL 深色模式]**&#x200B;預覽。 [了解作法](#preview-dark-mode)

1. 編輯任何樣式色彩屬性，例如文字、背景、按鈕等。

1. 您無法變更影像和圖示的顏色，但只能為深色模式定義特定資產。 若要這麼做，請選取任何影像。 使用&#x200B;**[!UICONTROL 設定]**&#x200B;窗格中的專用切換開關切換至&#x200B;**[!UICONTROL 深色模式]**&#x200B;並選取其他資產。

   ![](assets/dark-mode-image.png)

   <!--![](assets/dark-mode-custom.png)-->

1. 您隨時可以&#x200B;**[!UICONTROL 切換到即時檢視]**，以檢查您的內容在各種裝置大小上可能會如何呈現。 從這個檢視中，選取畫面頂端的「深色模式」切換按鈕，即可預覽不同裝置上的深色模式內容版本。

   ![](assets/dark-mode-live-view.png){width="80%" align="center"}

   >[!CAUTION]
   >
   >即時檢視是通用的預覽，用來比較各種裝置大小下的轉譯效果。 最終呈現內容可能會因收件者的電子郵件使用者端而異。

1. 在您滿意深色模式的變更後，請按一下&#x200B;**[!UICONTROL 模擬內容]**。

   ![](assets/dark-mode-simulate.png)

1. 選取&#x200B;**[!UICONTROL 轉譯電子郵件]**&#x200B;並連線至您的Litmus帳戶。 您可以看到各種電子郵件使用者端的最終深色模式演算。 深入瞭解[電子郵件呈現](../content-management/rendering.md)。

   >[!WARNING]
   >
   >雖然模擬非常接近電子郵件在深色模式下的顯示方式，但由於電子郵件服務提供者或裝置層級設定的差異，實際呈現可能會有所不同。

## 最佳做法 {#best-practices}

隨著主要電子郵件使用者端採用深色模式的人數增加，您必須考量您的電子郵件在明暗環境中呈現的方式，不論您是否使用[自訂深色模式](#define-custom-dark-mode)。

深色模式可以改變顏色、背景和影像 — 有時會覆寫設計選擇。 為確保視覺一致性、協助工具及品牌完整性，請遵循下列最佳實務。

**最佳化您的影像和標誌**

* 避免使用硬式編碼白色或淺色背景的影像。

* 將圖志和圖示儲存為具有透明背景的PNG，以避免在深色模式中看到白色方塊。

* 如果無法使用透明度，請在設計中將影像置於純色背景上，以防止發生尷尬的顏色倒轉。

**觀看您的背景**

* 確保文字和背景顏色之間有足夠的對比，以便在淺色和深色模式中都能閱讀。

* 避免僅依賴背景顏色處理重要內容。 有些使用者端會以深色模式覆寫背景顏色，因此請確定關鍵資訊仍然可見。

**在深色模式中設計可存取的內容**

<!--KEEP dark mode accessibility best practices IN ONE SINGLE LOCATION - for now listed on this page.
If needed, it can be moved to the Design accessible content page:
The best practices for designing accesible content in dark mode are listed in [this section](accessible-content.md#dark-mode).-->

* 使用顏色組合，可輕鬆區別色盲人士。

* 使用中間調調色盤，確保與淺色和深色背景的對比。

* 使用具有高對比度的無障礙色彩組合，以改善可讀性，並符合網頁內容可及性指引(WCAG)標準。 使用WebAIM的「對比檢查器」等工具，驗證色彩對比。

* 避免使用精簡字型，因為這會影響可讀性。 如果您的品牌需要細字型，請在深色模式中將其粗體。

* 略過純黑色的純白色，因為它可能會導致眼睛疲勞，並且可能會由某些電子郵件使用者端自動反轉。

* 如果深色模式不受支援，請提供可存取的遞補樣式。

**在深色模式環境中測試您的電子郵件**

* 使用電子郵件Designer的[深色模式預覽](#preview-dark-mode)，它使用反轉的色彩配置來提早發現問題。

* 使用[電子郵件呈現](../content-management/rendering.md)選項，利用Litmus在主要電子郵件使用者端(Apple Mail、Gmail、Outlook)間模擬您的設計，並瞭解色彩和影像在深色模式下的行為。

<!--**Inline critical styles**

Inline CSS helps maintain more control over styling, as some clients strip external styles in dark mode.-->

## 支援深色模式的電子郵件使用者端 {#supporting-email-clients}

以下是支援深色模式的主要電子郵件使用者端清單。

>[!NOTE]
>
>這些電子郵件使用者端的某些版本不支援深色模式，因此為了清楚起見，也會顯示在此表格中。

| 支援深色模式的電子郵件使用者端 | 相容版本 | *不支援的版本* |
|---------|----------|---------|
| Apple Mail macOS | 12.4， 16.0 | *10.3* |
| Apple Mail iOS | 13.0， 16.1 | *12.2* |
| Outlook macOS | 2019， 16.70， 16.80 | 不適用 |
| Outlook.com | 2019-07， 2022-12 | 不適用 |
| Outlook iOS | 2020-01， 2022-12 | 不適用 |
| Outlook Android | 2023-03 | *2020-01， 2022-12* |
| Samsung電子郵件(Android) | 6.1 | *6.0* |
| Mozilla Thunderbird (macOS) | 68.4 | *60.8， 78.5， 91.13* |
| Fastmail （案頭網路郵件） | 2022-12 | *2021-07* |
| HEY （案頭網路郵件） | 2020-06 | *2022-12* |
| 橙色案頭網路郵件 | 2019-08、2021-03、2022-12、2024-04 | 不適用 |
| 橙色iOS | 2022-12， 2024-04 | *2020-01* |
| 橙色Android | 2024-04 | *2020-01， 2022-12* |
| LaPoste.net | 2021-08， 2022-12 | 不適用 |
| SFR案頭網路郵件 | 2019-08， 2022-12 | 不適用 |
| GMX (iOs和Android) | 2022-06 | 不適用 |
| 1&amp;1 (案頭網路郵件和Android) | 2022-06 | 不適用 |
| WEB.DE (iOs和Android) | 2022-06 | 不適用 |
| Free.fr | 2022-12 | 不適用 |

>[!WARNING]
>
>深色模式的最終呈現取決於每個電子郵件使用者端，因此結果可能因人而異。

<!--
* Check out the list of [email clients supporting dark mode](https://www.caniemail.com/search/?s=dark){target="_blank"}

* Learn more on Dark mode in this [Litmus blog post](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers){target="_blank"}
-->

## 電子郵件使用者端不支援深色模式 {#non-supporting-email-clients}

有些電子郵件使用者端允許使用者將其介面切換至深色模式，但此設定不會影響HTML電子郵件的顯示方式。 無論介面處於淺色還是深色模式，您的電子郵件都會呈現相同的內容。 以下是這些使用者端的清單：

| 電子郵件使用者端不支援深色模式 |
|---------|
| Gmail (案頭網頁郵件、iOS、Android、行動網頁郵件) |
| Outlook Windows |
| Outlook Windows Mail |
| Yahoo！Mail |
| AOL |
| 質子郵件 |
| SFR IOS |
| SFR ANDROID |
| GMX案頭網路郵件 |
| Mail.ru |
| WEB.DE案頭網頁郵件 |
| T-online.de |
