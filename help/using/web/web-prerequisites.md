---
title: 網路通道必要條件
description: 若要在Journey Optimizer使用者介面中存取及撰寫網頁，請遵循本頁面的必要條件
feature: Web Channel
topic: Content Management
role: User
level: Beginner
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 11%

---

# 網路通道必要條件 {#web-prerequisites}

若要存取及編寫 [!DNL Journey Optimizer] 使用者介面，請遵循下列必要條件：

* 若要新增修改至您的網站，您必須有特定實作。 [了解更多](#implementation-prerequisites)

* 若要存取 [!DNL Journey Optimizer] 網頁設計工具中，您必須安裝特定的Google Chrome瀏覽器擴充功能。 [了解更多](#visual-authoring-prerequesites)

* 若要正確傳送網頁體驗，請務必詳細定義Adobe Experience Platform設定 [此處](#delivery-prerequisites).

## 實作必要條件 {#implementation-prerequisites}

目前支援兩種實作類型，以在您的Web屬性上啟用網頁頻道行銷活動的製作和傳送：

* 僅限用戶端 — 若要將修改新增至您的網站，您必須實作 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"} 在您的網站上。

* 混合模式 — 您可以使用 [AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=zh-Hant){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>目前不支援僅限伺服器端實作。

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## 視覺化製作必要條件 {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

若要以可靠的方式開啟、撰寫和預覽您的網頁，請進入 [!DNL Journey Optimizer] 網頁設計人員，您必須 [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 瀏覽器擴充功能安裝在您的網頁瀏覽器上。

>[!CAUTION]
>
>Google Chrome和Microsoft Edge目前是唯一支援在 [!DNL Journey Optimizer].

### 安裝Visual Editing Helper擴充功能 {#install-visual-editing-helper}

要下載和安裝Visual Editing Helper瀏覽器擴展，請執行以下步驟。

1. 在瀏覽器中開啟新標籤(Google Chrome或Microsoft Edge)。

1. 前往 [Google Chrome線上商店](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. 如果您使用Microsoft Edge，請選取 **[!UICONTROL 允許來自其他商店的擴充功能]** 在頂部橫幅上。 這可讓您將擴充功能從Chrome線上應用程式商店新增至Microsoft Edge。

1. 搜尋並導覽至 [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 瀏覽器擴充功能。

1. 按一下「**[!UICONTROL 新增至 Chrome]** > **[!UICONTROL 新增擴充功能]**」。

   >[!NOTE]
   >
   >如果您使用Microsoft Edge，即使按鈕已標示，擴充功能仍會新增至Edge **[!UICONTROL 新增至Chrome]**.

1. 請確定瀏覽器工具列中的Visual Editing Helper瀏覽器擴充功能已正確啟用。

   ![](assets/web-visual-editing-extension-edge.png)

<!--1. Launch [!DNL Journey Optimizer] in a new tab of your browser with the extension installed.

1. Create a web channel campaign in [!DNL Journey Optimizer]. [Learn how](author-web.md#create-web-campaign)

1. Open the [!DNL Journey Optimizer] web designer to start authoring your web experience. [Learn more](author-web.md)-->

Adobe Experience Cloud Visual Editing Helper現在會在 [!DNL Journey Optimizer] 網頁設計工具來強化製作功能。

擴充功能沒有任何條件式設定，且會自動處理所有設定，包括SameSite Cookie設定。

>[!NOTE]
>
>某些網站可能無法可靠地在 [!DNL Journey Optimizer] Web設計器，原因如下：
>
> * 網站的安全性原則過於嚴格。
> * 網站架設在 iFrame 中。
> * 客戶的 QA 或暫存網站無法供外部世界使用 (網站僅供內部使用)。


### 疑難排解網站未載入 {#troubleshooting}

使用Adobe時 [!DNL Journey Optimizer] 網頁設計工具，如果您嘗試載入無法載入的網站，會顯示訊息建議您安裝 [Visual Editing Helper瀏覽器擴充功能](#install-visual-editing-helper).

如果正確安裝了Visual Editing Helper瀏覽器擴充功能，但網站仍無法載入或意外運作，可能的修正是先在瀏覽器中開啟您的網站並接受Cookie，然後再嘗試將其載入 [!DNL Journey Optimizer] 網頁設計工具。

若為驗證下的頁面，如果登入頁面無法載入，或嘗試登入後，您仍未登入：

* 請嘗試先在新的瀏覽器標籤中登入，並導覽至所需的頁面，然後複製URL，並嘗試在中開啟它 [!DNL Journey Optimizer] 網頁設計工具。

* 如果您仍無法在 [!DNL Journey Optimizer] 網頁設計人員請聯絡Adobe客戶服務以報告問題，並確定您指定失敗的URL。

## 傳送必要條件 {#delivery-prerequisites}

為了正確傳送網頁體驗，必須定義下列設定：

* 在 [Adobe Experience Platform資料收集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target="_blank"}，請確定您有定義的資料流，例如在 **[!UICONTROL Adobe Experience Platform]** 服務 **[!UICONTROL 邊緣分割]** 和 **[!UICONTROL Adobe Journey Optimizer]** 選項。

   這可確保Journey Optimizer入站事件由Adobe Experience Platform Edge正確處理。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=zh-Hant){target="_blank"}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL Adobe Journey Optimizer]** 選項僅可在 **[!UICONTROL 邊緣分割]** 選項。

* 在 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

   此合併策略由 [!DNL Journey Optimizer] 傳入頻道，在邊緣上正確啟用和發佈傳入促銷活動。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target="_blank"}

   ![](assets/web-aep-merge-policy.png)

<!--
Branded domains for assets

When authoring web experiences, if you add content coming from the [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) library, you  must set up the subdomain that will be used to publish this content. [Learn more](web-delegated-subdomains.md)-->



