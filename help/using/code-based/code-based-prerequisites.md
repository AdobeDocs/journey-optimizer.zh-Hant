---
title: 程式碼型體驗必要條件
description: 若要使用Journey Optimizer程式碼型功能編輯應用程式和網頁，請遵循本頁面的先決條件
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: 1b6158132e5df1912d9658805fa8b1344c6f938f
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 2%

---

# 程式碼型體驗必要條件 {#code-based-prerequisites}

若要能夠在[!DNL Journey Optimizer]中使用程式碼型體驗動作，並傳遞您的應用程式可以使用的程式碼內容裝載，請遵循下列先決條件：

* 若要在應用程式中新增修改，您必須有特定的實施。 [了解更多](#implementation-prerequisites)

* 為了正確傳遞程式碼型體驗，請務必在[這裡](#delivery-prerequisites)定義詳細的Adobe Experience Platform設定。

* 若要讓資料顯示在程式碼型體驗報表中，請務必遵循下列[報告必要條件](#reporting-prerequisites)。

* 建立[程式碼型體驗通道組態](code-based-configuration.md)時，請務必輸入符合您自己的實作中宣告的字串/路徑或表面URI。 這可確保內容會傳送至指定應用程式或頁面內的所需位置。 否則，將無法傳送變更。 [閱讀全文](code-based-surface.md)

>[!CAUTION]
>
>以您的程式碼型體驗定位假名設定檔（未驗證的訪客）時，請考慮設定自動刪除設定檔的存留時間(TTL)，以管理可參與的設定檔計數和相關成本。 [了解更多](../start/guardrails.md#profile-management-inbound)

## 實作必要條件 {#implementation-prerequisites}

程式碼型體驗支援任何型別的客戶實施，如下列選項所示。 您可以針對屬性使用使用者端、伺服器端或混合實作方法：

* 僅限使用者端 — 若要對您的網頁或行動應用程式新增修改，您必須在您的網站上實作[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"}，或在您的行動應用程式上實作[Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"}。

* 混合模式 — 您可以使用[AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=zh-Hant){target="_blank"}來要求個人化伺服器端；回應會提供給Adobe Experience Platform Web SDK，以轉譯修改內容的使用者端。 在Adobe Experience Platform [Edge Network Server API檔案](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"}中進一步瞭解。 您可以在[此部落格](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}中找到更多有關混合模式的資訊，並檢視一些實作範例。

* 伺服器端 — 您可以使用[AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=zh-Hant){target="_blank"}來要求個人化伺服器端。 您的開發團隊必須處理回應，並在應用程式實作中在使用者端轉譯修改。

您可以在[此區段](code-based-implementation-samples.md)中找到上述每個實作方法的範例。

## 傳遞必要條件 {#delivery-prerequisites}

為了正確提供程式碼型體驗，必須定義下列設定：

* 在[Adobe Experience Platform Data Collection](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hant){target="_blank"}中，確定您已定義資料串流，例如在&#x200B;**[!UICONTROL Adobe Experience Platform]**&#x200B;服務下您已啟用&#x200B;**[!UICONTROL Adobe Journey Optimizer]**&#x200B;選項。

  這可確保Adobe Experience Platform Edge正確處理Journey Optimizer傳入事件。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* 在[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}中，確定您有一個啟用&#x200B;**[!UICONTROL Edge上主動式合併原則]**&#x200B;選項的合併原則。 若要這麼做，請在&#x200B;**[!UICONTROL 客戶]** > **[!UICONTROL 設定檔]** > **[!UICONTROL 合併原則]** Experience Platform功能表下選取原則。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  此合併原則由[!DNL Journey Optimizer]個傳入頻道使用，以便在邊緣正確啟用和發佈傳入行銷活動。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hant){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

* 若要針對Journey Optimizer網頁體驗的傳遞進行疑難排解，您可以在&#x200B;**Edge Delivery**&#x200B;中使用&#x200B;**Adobe Experience Platform Assurance**&#x200B;檢視。 此外掛程式可讓您詳細檢查請求呼叫、驗證預期的邊緣呼叫是否如預期發生，以及檢查設定檔資料，包括身分對應、區段會籍和同意設定。 此外，您可以檢閱請求符合資格的活動，並識別未符合資格的活動。

  使用&#x200B;**Edge Delivery**&#x200B;外掛程式可協助您取得所需的深入分析，以有效瞭解並疑難排解傳入的實作。

  [進一步瞭解Edge Delivery檢視](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

## 報表必要條件 {#reporting-prerequisites}

若要啟用程式碼型管道的報告，您必須確定應用程式實作[資料流](../data/get-started-datasets.md)中使用的[資料集](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"}也包含在報告設定中。

換言之，在設定報表時，如果您新增的應用程式資料流中不存在的資料集，應用程式資料將不會顯示在報表中。

瞭解如何在[本節](../reports/reporting-configuration.md#add-datasets)中新增資料集以進行報告。

>[!NOTE]
>
>資料集由[!DNL Journey Optimizer]報告系統以唯讀方式使用，不會影響資料收集或資料擷取。

