---
title: 網路頻道先決條件
description: 若要在Journey Optimizer使用者介面中存取及製作網頁，請遵循此頁面的先決條件
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 6cb4f8ab-77ad-44a2-b2bf-a97f87b8f1db
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 12%

---

# 先決條件和護欄 {#web-prerequisites}

若要能夠存取及編寫中的網頁 [!DNL Journey Optimizer] 請依照下列必要條件操作使用者介面：

* 若要對網站新增修改，您必須具備特定實施。 [了解更多](#implementation-prerequisites)

* 若要存取 [!DNL Journey Optimizer] 網頁設計工具中，您必須安裝特定的Google Chrome瀏覽器擴充功能。 [了解更多](#visual-authoring-prerequesites)

* 若要正確傳送網頁體驗，請務必詳細定義Adobe Experience Platform設定 [此處](#delivery-prerequisites).

## 警告注意事項 {#caution-notes-web}

* 目前在 [!DNL Journey Optimizer] 您只能在中建立網站體驗 **行銷活動**. [了解更多](../campaigns/create-campaign.md#configure)

* [!DNL Journey Optimizer] 網路行銷活動會定位在其他頻道中之前未參與的新設定檔。 這會增加您的可參與設定檔總數，如果您購買的可參與設定檔數量超過合約數量，可能會影響成本。 每個套件的授權量度都列在 [Journey Optimizer產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html) 頁面。


>[!AVAILABILITY]
>
>目前，Web channel不適用於已購買AdobeHealthcare Shield附加產品的組織。
>

## 實作必要條件 {#implementation-prerequisites}

目前支援兩種型別的實作，以便能在您的Web屬性上編寫和傳送Web Channel行銷活動：

* 僅限使用者端 — 若要對網站新增修改，您必須實作 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"} 在您網站上的。

* 混合模式 — 您可以使用 [AEP Edge Network伺服器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=zh-Hant){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>目前不支援僅伺服器端實作。

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## 視覺化編寫必要條件 {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

為了能夠可靠地開啟、編寫和預覽您的網頁，在 [!DNL Journey Optimizer] 網頁設計工具，您必須擁有 [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 瀏覽器擴充功能已安裝在您的網頁瀏覽器上。

>[!CAUTION]
>
>Google Chrome和Microsoft Edge是目前唯一支援在中編寫網頁的瀏覽器。 [!DNL Journey Optimizer].

### 安裝Visual Editing Helper擴充功能 {#install-visual-editing-helper}

若要下載並安裝Visual Editing Helper瀏覽器擴充功能，請遵循下列步驟。

1. 在瀏覽器中開啟新索引標籤(Google Chrome或Microsoft Edge)。

1. 前往 [Google Chrome線上應用程式商店](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. 如果您正在使用Microsoft Edge，請選取 **[!UICONTROL 允許來自其他存放區的擴充功能]** 在頂端橫幅上。 這可讓您將擴充功能從Chrome線上應用程式商店新增至Microsoft Edge。

1. 搜尋並導覽至 [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 瀏覽器延伸模組。

1. 按一下「**[!UICONTROL 新增至 Chrome]** > **[!UICONTROL 新增擴充功能]**」。

   >[!NOTE]
   >
   >如果您正在使用Microsoft Edge，這會將擴充功能新增至Edge，即使按鈕標示為 **[!UICONTROL 新增至Chrome]**.

1. 請確定已在瀏覽器的工具列中正確啟用Visual Editing Helper瀏覽器擴充功能。

   ![](assets/web-visual-editing-extension-edge.png)

<!--1. Launch [!DNL Journey Optimizer] in a new tab of your browser with the extension installed.

1. Create a web channel campaign in [!DNL Journey Optimizer]. [Learn how](author-web.md#create-web-campaign)

1. Open the [!DNL Journey Optimizer] web designer to start authoring your web experience. [Learn more](author-web.md)-->

現在，在中開啟網站時，會自動啟用Adobe Experience Cloud Visual Editing Helper。 [!DNL Journey Optimizer] 網頁設計工具以支援撰寫。

擴充功能沒有任何條件設定，且會自動處理所有設定，包括SameSite Cookie設定。

>[!NOTE]
>
>有些網站可能無法可靠地在中開啟 [!DNL Journey Optimizer] 網頁設計工具，原因如下：
>
> * 網站的安全性原則過於嚴格。
> * 網站架設在 iFrame 中。
> * 客戶的 QA 或暫存網站無法供外部世界使用 (網站僅供內部使用)。

### 疑難排解網站未載入 {#troubleshooting}

使用Adobe時 [!DNL Journey Optimizer] Web設計工具如果嘗試載入無法載入的網站，會顯示一則訊息，建議您安裝 [Visual Editing Helper瀏覽器擴充功能](#install-visual-editing-helper).

如果Visual Editing Helper瀏覽器擴充功能已正確安裝，但網站仍然無法載入或發生意外行為，可能的修正措施是在瀏覽器中開啟您的網站並接受Cookie，然後再嘗試將其載入到 [!DNL Journey Optimizer] 網頁設計工具。

對於驗證下的頁面，如果登入頁面無法載入，或嘗試登入後您仍未登入：

* 請嘗試先在新瀏覽器標籤中登入，並導覽至所需頁面，然後複製URL並嘗試在 [!DNL Journey Optimizer] 網頁設計工具。

* 如果您仍然無法在以下位置載入網站： [!DNL Journey Optimizer] 網頁設計工具請聯絡Adobe客戶服務以回報問題，並確認您指定了失敗的URL。

## 傳遞必要條件 {#delivery-prerequisites}

若要正確傳送Web體驗，必須定義下列設定：

* 在 [Adobe Experience Platform資料彙集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hant){target="_blank"}，確定您有定義的資料流，例如 **[!UICONTROL Adobe Experience Platform]** 您擁有的服務 **[!UICONTROL Adobe Journey Optimizer]** 選項已啟用。

  這可確保Adobe Experience Platform Edge可正確處理Journey Optimizer傳入事件。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=zh-Hant){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* 在 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  此合併原則的使用者為 [!DNL Journey Optimizer] 傳入頻道，可在邊緣正確啟用和發佈傳入行銷活動。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hant){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

## 資產的品牌網域 {#branded-domains-for-assets}

在製作網頁體驗時，如果您新增來自 [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) 程式庫，您必須設定用於發佈此內容的子網域。 [了解更多](web-delegated-subdomains.md)
