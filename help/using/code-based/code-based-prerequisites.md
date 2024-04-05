---
title: 程式碼型體驗護欄和先決條件
description: 若要使用Journey Optimizer程式碼型功能編輯應用程式和網頁，請遵循本頁面的先決條件
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: c4444b67313cda81fda9ad16b7ee59226fd7c88a
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 4%

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

* 僅限使用者端 — 若要對您的網頁或行動應用程式新增修改，您必須實作 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"} on your website or [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} 在您行動應用程式上。

* 混合模式 — 您可以使用 [AEP Edge Network伺服器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=zh-Hant){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* 伺服器端 — 您可以使用 [AEP Edge Network伺服器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} 以請求個人化伺服器端。 您的開發團隊必須處理回應，並在應用程式實作中在使用者端轉譯修改。

您可以在中找到上述每種實作方法的範例 [本節](code-based-implementation-samples.md).

## 傳遞必要條件 {#delivery-prerequisites}

為了正確提供程式碼型體驗，必須定義下列設定：

* 在 [Adobe Experience Platform資料彙集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hant){target="_blank"}，確定您有定義的資料流，例如 **[!UICONTROL Adobe Experience Platform]** 您擁有的服務 **[!UICONTROL Adobe Journey Optimizer]** 選項已啟用。

  這可確保Adobe Experience Platform Edge可正確處理Journey Optimizer傳入事件。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=zh-Hant){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* 在 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  此合併原則的使用者為 [!DNL Journey Optimizer] 傳入頻道，可在邊緣正確啟用和發佈傳入行銷活動。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hant){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

## 內容實驗先決條件 {#experiment-prerequisites}

若要啟用程式碼型管道的內容實驗，您必須確定 [資料集](../data/get-started-datasets.md) 用於您的應用程式實作 [資料流](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} 也包含在您的報告設定中。

換言之，在設定實驗報告時，如果您新增的應用程式資料流中不存在的資料集，應用程式資料將不會顯示在內容實驗報告中。

瞭解如何在中新增內容實驗報告的資料集 [本節](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>資料集是由 [!DNL Journey Optimizer] 報告系統並且不會影響資料收集或資料擷取。
