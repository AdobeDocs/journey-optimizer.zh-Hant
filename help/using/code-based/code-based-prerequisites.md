---
title: 程式碼型體驗護欄和先決條件
description: 若要使用Journey Optimizer程式碼型功能編輯應用程式和網頁，請遵循本頁面的先決條件
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 2%

---

# 護欄和限制 {#web-prerequisites}

若要能夠在中使用程式碼型體驗動作 [!DNL Journey Optimizer] 並傳遞應用程式可使用的程式碼內容裝載，請遵循下列先決條件：

* 若要在應用程式中新增修改，您必須有特定的實施。 [了解更多](#implementation-prerequisites)

* 為了正確提供程式碼型體驗，請務必詳細說明您定義Adobe Experience Platform設定 [此處](#delivery-prerequisites).

>[!CAUTION]
>
>* 已購買Adobe的組織無法使用程式碼型體驗管道 **Health Shield** 和 **隱私權與安全防護板** 附加方案。
>
>* 您只能在中建立程式碼型體驗 **行銷活動**. [了解更多](../campaigns/create-campaign.md#configure)。

## 實作必要條件 {#implementation-prerequisites}

程式碼型體驗支援任何型別的客戶實施，如下列選項所示。 您可以針對屬性使用使用者端、伺服器端或混合實作方法：

* 僅限使用者端 — 若要對您的網頁或行動應用程式新增修改，您必須實作 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"} 在您的網站上或 [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} 在您行動應用程式上。

* 混合模式 — 您可以使用 [AEPEdge Network伺服器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} 以請求個人化伺服器端；回應會提供給Adobe Experience Platform Web SDK，以在使用者端轉譯修改。 在Adobe Experience Platform中瞭解更多 [Edge Network伺服器API檔案](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"}. 您可以進一步瞭解混合模式，並檢視中的部分實作範例 [此部落格](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* 伺服器端 — 您可以使用 [AEPEdge Network伺服器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} 以請求個人化伺服器端。 您的開發團隊必須處理回應，並在應用程式實作中在使用者端轉譯修改。

您可以在中找到上述每種實作方法的範例 [本節](code-based-implementation-samples.md).

## 傳遞必要條件 {#delivery-prerequisites}

為了正確提供程式碼型體驗，必須定義下列設定：

* 在 [Adobe Experience Platform資料彙集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hant){target="_blank"}，確定您有定義的資料流，例如 **[!UICONTROL Adobe Experience Platform]** 您擁有的服務 **[!UICONTROL Adobe Journey Optimizer]** 選項已啟用。

  這可確保Adobe Experience Platform Edge可正確處理Journey Optimizer傳入事件。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* 在 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}，請確定您有一個合併原則， **[!UICONTROL Active-On-Edge合併原則]** 選項已啟用。 若要這麼做，請在 **[!UICONTROL 客戶]** > **[!UICONTROL 設定檔]** > **[!UICONTROL 合併原則]** Experience Platform功能表。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  此合併原則的使用者為 [!DNL Journey Optimizer] 傳入頻道，可在邊緣正確啟用和發佈傳入行銷活動。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hant){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

* 若要針對Journey Optimizer Web體驗的傳送進行疑難排解，您可使用 **Edge傳遞** 檢視範圍 **Adobe Experience Platform保證**. 此外掛程式可讓您詳細檢查請求呼叫、驗證預期的邊緣呼叫是否如預期發生，以及檢查設定檔資料，包括身分對應、區段會籍和同意設定。 此外，您可以檢閱請求符合資格的活動，並識別未符合資格的活動。

  使用 **Edge傳遞** 外掛程式可協助您取得所需的深入分析，以有效瞭解傳入的實施並疑難排解。

  [深入瞭解邊緣傳遞檢視](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery)

## 內容實驗先決條件 {#experiment-prerequisites}

若要啟用程式碼型管道的內容實驗，您必須確定 [資料集](../data/get-started-datasets.md) 用於您的應用程式實作 [資料流](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} 也包含在您的報告設定中。

換言之，在設定實驗報告時，如果您新增的應用程式資料流中不存在的資料集，應用程式資料將不會顯示在內容實驗報告中。

瞭解如何在中新增內容實驗報告的資料集 [本節](../content-management/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>資料集是由 [!DNL Journey Optimizer] 報告系統並且不會影響資料收集或資料擷取。
