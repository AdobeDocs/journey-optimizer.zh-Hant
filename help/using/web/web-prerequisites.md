---
title: 網路頻道先決條件
description: 若要能夠訪問和編寫Journey Optimizer用戶介面中的網頁，請遵循本頁的先決條件
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 6cb4f8ab-77ad-44a2-b2bf-a97f87b8f1db
source-git-commit: 65a33d6836c43564ef7c93660a8076677ea5cba8
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 13%

---

# 先決條件和護欄 {#web-prerequisites}

能夠訪問和編寫 [!DNL Journey Optimizer] 用戶介面，遵循以下先決條件：

* 要向網站添加修改，您需要具有特定的實施。 [了解更多](#implementation-prerequisites)

* 訪問 [!DNL Journey Optimizer] web設計器中，必須安裝特定的GoogleChrome瀏覽器擴展。 [了解更多](#visual-authoring-prerequesites)

* 要正確提供Web體驗，請確保定義詳細的Adobe Experience Platform設定 [這裡](#delivery-prerequisites)。

## 警告

目前在 [!DNL Journey Optimizer]，您只能使用&#x200B;**行銷活動**&#x200B;建立網路體驗。[了解更多](../campaigns/create-campaign.md#configure)


[!DNL Journey Optimizer] Web活動針對以前在其他渠道中從未使用過的新配置檔案。 這將增加可接合配置檔案的總數，如果您購買的可接合配置檔案的合同數量超過，則這可能會帶來成本影響。 每個包的許可證度量列在 [Journey Optimizer產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html) 的子菜單。

## 實施先決條件 {#implementation-prerequisites}

目前支援兩種類型的實施，以在Web屬性上啟用Web渠道市場活動的創作和交付：

* 僅限客戶端 — 要向網站添加修改，您需要實施 [Adobe Experience PlatformWeb SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"} 在你的網站上。

* 混合模式 — 您可以使用 [AEP邊緣網路伺服器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=zh-Hant){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}。

>[!NOTE]
>
>當前不支援僅伺服器端實現。

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## 視覺創作先決條件 {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

要能夠可靠地開啟、編寫和預覽網頁，請 [!DNL Journey Optimizer] Web設計器，必須 [Adobe Experience Cloud視覺編輯幫助程式](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 瀏覽器擴展安裝在web瀏覽器上。

>[!CAUTION]
>
>GoogleChrome和MicrosoftEdge目前是支援在 [!DNL Journey Optimizer]。

### 安裝Visual Editing幫助程式擴展 {#install-visual-editing-helper}

要下載和安裝Visual Editing Helper瀏覽器擴展，請執行以下步驟。

1. 在瀏覽器(GoogleChrome或Microsoft邊緣)中開啟新頁籤。

1. 轉到 [GoogleChrome網店](https://chrome.google.com/webstore/category/extensions){target="_blank"}。

1. 如果使用Microsoft邊，請選擇 **[!UICONTROL 允許來自其他儲存的擴展]** 在最上面的橫幅上。 這將允許您將擴展從Chrome Web Store添加到Microsoft邊緣。

1. 搜索並導航至 [Adobe Experience Cloud視覺編輯幫助程式](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 瀏覽器擴展。

1. 按一下「**[!UICONTROL 新增至 Chrome]** > **[!UICONTROL 新增擴充功能]**」。

   >[!NOTE]
   >
   >如果使用「Microsoft邊」(Edge)，則即使按鈕已標籤為「邊」(Edge)，也會將擴展添加到「邊」(Edge) **[!UICONTROL 添加到Chrome]**。

1. 確保在瀏覽器的工具欄中正確啟用了Visual Editing Helper瀏覽器擴展。

   ![](assets/web-visual-editing-extension-edge.png)

<!--1. Launch [!DNL Journey Optimizer] in a new tab of your browser with the extension installed.

1. Create a web channel campaign in [!DNL Journey Optimizer]. [Learn how](author-web.md#create-web-campaign)

1. Open the [!DNL Journey Optimizer] web designer to start authoring your web experience. [Learn more](author-web.md)-->

當在中開啟網站時，Adobe Experience Cloud可視編輯幫助程式現在自動啟用 [!DNL Journey Optimizer] Web設計器即可完成創作。

擴展沒有任何條件設定，並自動處理所有設定，包括SameSite Cookie設定。

>[!NOTE]
>
>某些網站可能無法在 [!DNL Journey Optimizer] Web設計器的原因如下：
>
> * 網站的安全性原則過於嚴格。
> * 網站架設在 iFrame 中。
> * 客戶的 QA 或暫存網站無法供外部世界使用 (網站僅供內部使用)。


### 排除未載入網站的故障 {#troubleshooting}

使用Adobe [!DNL Journey Optimizer] Web設計器，如果嘗試載入未能載入的網站，將顯示一條消息，建議您安裝 [Visual Editing Helper瀏覽器擴展](#install-visual-editing-helper)。

如果正確安裝了Visual Editing Helper瀏覽器擴展，但網站仍無法載入或行為異常，則可能的解決辦法是在瀏覽器中開啟您的網站並接受Cookie，然後再嘗試將其載入到 [!DNL Journey Optimizer] web設計器。

對於正在驗證的頁面，如果登錄頁載入失敗，或者在嘗試登錄後仍未登錄：

* 嘗試先在新瀏覽器頁籤中登錄並導航到所需頁面，然後複製URL，然後嘗試在 [!DNL Journey Optimizer] web設計器。

* 如果仍然無法在 [!DNL Journey Optimizer] Web設計員，聯繫Adobe「客戶服務」報告問題，確保指定失敗的URL。

## 交付先決條件 {#delivery-prerequisites}

要正確提供Web體驗，必須定義以下設定：

* 在 [Adobe Experience Platform資料收集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target="_blank"}，確保您有定義的資料流，如 **[!UICONTROL Adobe Experience Platform]** 服務 **[!UICONTROL 邊緣分割]** 和 **[!UICONTROL Adobe Journey Optimizer]** 選項。

   這確保Journey Optimizer入站事件由Adobe Experience Platform邊緣正確處理。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=zh-Hant){target="_blank"}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL Adobe Journey Optimizer]** 選項僅在 **[!UICONTROL 邊緣分割]** 選項。

* 在 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

   此合併策略由 [!DNL Journey Optimizer] 入站渠道，以正確激活和發佈邊緣上的入站市場活動。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hant){target="_blank"}

   ![](assets/web-aep-merge-policy.png)

## 資產的標籤域 {#branded-domains-for-assets}

創作Web體驗時，如果添加來自 [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) 庫，必須設定將用於發佈此內容的子域。 [了解更多](web-delegated-subdomains.md)
