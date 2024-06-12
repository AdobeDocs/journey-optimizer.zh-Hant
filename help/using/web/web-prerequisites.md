---
title: 網路頻道先決條件
description: 若要在Journey Optimizer使用者介面中存取及製作網頁，請遵循此頁面的先決條件
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 9509fd67-6d12-4440-aad8-59690936be97
source-git-commit: 83e93b18a3f5a8e688ad519d3e1c0d70d91dfc9f
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 2%

---

# 先決條件和護欄 {#web-prerequisites}

若要能夠存取及編寫中的網頁 [!DNL Journey Optimizer] 請依照下列必要條件操作使用者介面：

* 若要對網站新增修改，您必須具備特定實施。 [了解更多](#implementation-prerequisites)

* 若要存取 [!DNL Journey Optimizer] 網頁設計工具中，您必須安裝特定的Google Chrome瀏覽器擴充功能。 [了解更多](#visual-authoring-prerequesites)

* 若要正確傳送網頁體驗，請務必詳細定義Adobe Experience Platform設定 [此處](#delivery-prerequisites).

## 警告注意事項 {#caution-notes-web}

* 目前在 [!DNL Journey Optimizer] 您只能在中建立網站體驗 **行銷活動**. [了解更多](../campaigns/create-campaign.md#configure)

* [!DNL Journey Optimizer] 網路行銷活動會定位在其他頻道中之前未參與的新設定檔。 這會增加您的可參與設定檔總數，如果您購買的可參與設定檔數量超過合約數量，可能會影響成本。 每個套件的授權量度都列在 [Journey Optimizer產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} 頁面。


>[!AVAILABILITY]
>
>目前，Web channel不適用於已購買Adobe的組織 **Health Shield** 和 **隱私權與安全防護板** 附加方案。

## 實作必要條件 {#implementation-prerequisites}

目前支援兩種型別的實作，以便能在您的Web屬性上編寫和傳送Web Channel行銷活動：

* 僅限使用者端 — 若要對網站新增修改，您必須實作 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"} 在您網站上的。

  >[!NOTE]
  >
  >請確認您的AEP Web SDK版本為2.16或更高版本。

* 混合模式 — 您可以使用 [AEPEdge Network伺服器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} 以請求個人化伺服器端；回應會提供給Adobe Experience Platform Web SDK，以在使用者端轉譯修改。 在Adobe Experience Platform中瞭解更多 [Edge Network伺服器API檔案](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"}. 您可以進一步瞭解混合模式，並檢視中的部分實作範例 [此部落格](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

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

1. 按一下 **[!UICONTROL 新增至Chrome]** > **[!UICONTROL 新增擴充功能]**.

   >[!NOTE]
   >
   >如果您正在使用Microsoft Edge，這會將擴充功能新增至Edge，即使按鈕標示為 **[!UICONTROL 新增至Chrome]**.

1. 請確定已在瀏覽器的工具列中正確啟用Visual Editing Helper瀏覽器擴充功能。

   ![](assets/web-visual-editing-extension-edge.png)

現在，在中開啟網站時，會自動啟用Adobe Experience Cloud Visual Editing Helper。 [!DNL Journey Optimizer] [網頁設計工具](edit-web-content.md#work-with-web-designer) 以支援撰寫。

擴充功能沒有任何條件設定，且會自動處理所有設定，包括SameSite Cookie設定。

>[!NOTE]
>
>有些網站可能無法可靠地在中開啟 [!DNL Journey Optimizer] 網頁設計工具，原因如下：
>
> * 網站的安全性原則非常嚴格。
> * 網站位於iframe中。
> * 外部無法存取客戶的QA或預備網站（網站為內部網站）。

### 疑難排解網站未載入 {#troubleshooting}

使用Adobe時 [!DNL Journey Optimizer] Web設計工具如果嘗試載入無法載入的網站，會顯示一則訊息，建議您安裝 [Visual Editing Helper瀏覽器擴充功能](#install-visual-editing-helper).

1. 請確定Visual Editing Helper瀏覽器擴充功能已正確安裝。

1. 如果網站仍發生非預期的行為，請確定您的瀏覽器允許第三方Cookie，否則網頁無法在 [!DNL Journey Optimizer] 網頁設計工具。

對於驗證下的頁面，如果登入頁面無法載入，或嘗試登入後您仍未登入：

1. 請嘗試先在新瀏覽器標籤中登入，並導覽至所需頁面，然後複製URL並嘗試在 [!DNL Journey Optimizer] 網頁設計工具。

2. 如果您仍然無法在以下位置載入網站： [!DNL Journey Optimizer] 網頁設計工具請聯絡Adobe客戶服務以回報問題，並確認您指定了失敗的URL。

## 傳遞必要條件 {#delivery-prerequisites}

若要正確傳送Web體驗，必須定義下列設定：

* 在 [Adobe Experience Platform資料彙集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hant){target="_blank"}，確定您有定義的資料流，例如 **[!UICONTROL Adobe Experience Platform]** 您擁有的服務 **[!UICONTROL Adobe Journey Optimizer]** 選項已啟用。

  這可確保Adobe Experience Platform Edge可正確處理Journey Optimizer傳入事件。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* 在 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}，請確定您有一個合併原則， **[!UICONTROL Active-On-Edge合併原則]** 選項已啟用。 若要這麼做，請在 **[!UICONTROL 客戶]** > **[!UICONTROL 設定檔]** > **[!UICONTROL 合併原則]** Experience Platform功能表。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  此合併原則的使用者為 [!DNL Journey Optimizer] 傳入頻道，可在邊緣正確啟用和發佈傳入行銷活動。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hant){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

* 若要針對Journey Optimizer Web體驗的傳送進行疑難排解，您可以使用 **Edge傳遞** 檢視範圍 **Adobe Experience Platform保證**. 此外掛程式可讓您詳細檢查請求呼叫、驗證預期的邊緣呼叫是否如預期發生，以及檢查設定檔資料，包括身分對應、區段會籍和同意設定。 此外，您可以檢閱請求符合資格的活動，並識別未符合資格的活動。

  使用 **Edge傳遞** 外掛程式可協助您取得所需的深入分析，以有效瞭解傳入的實施並疑難排解。

  [深入瞭解邊緣傳遞檢視](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery)

## 內容實驗先決條件 {#experiment-prerequisites}

若要啟用網頁管道的內容實驗，您必須確定 [資料集](../data/get-started-datasets.md) 用於您的Web實作 [資料流](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} 也包含在您的報告設定中。

換言之，在設定實驗報告時，如果您新增的資料集未出現在網頁資料流中，則網頁資料不會顯示在內容實驗報告中。

瞭解如何在中新增內容實驗報告的資料集 [本節](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>資料集是由 [!DNL Journey Optimizer] 報告系統並且不會影響資料收集或資料擷取。

如果您是 **非** 使用以下預先定義的 [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant#field-group){target="_blank"} 針對您的資料集結構： `AEP Web SDK ExperienceEvent` 和 `Consumer Experience Event` (如中的定義 [此頁面](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"})，請務必新增下列欄位群組： `Experience Event - Proposition Interactions`， `Application Details`， `Commerce Details`、和 `Web Details`. 以下專案需要這些選項 [!DNL Journey Optimizer] 內容實驗報告，追蹤每個設定檔參與哪些實驗與處理。

>[!NOTE]
>
>新增這些欄位群組不會影響正常的資料收集。 它僅適用於執行實驗的頁面，而保留所有其他追蹤不變。

## 資產的品牌網域 {#branded-domains-for-assets}

在製作網頁體驗時，如果您新增來自 [Adobe Experience Manager Assets](../content-management/assets.md) 程式庫，您必須設定用於發佈此內容的子網域。 [了解更多](web-delegated-subdomains.md)
