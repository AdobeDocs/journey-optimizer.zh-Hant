---
title: 應用程式內頻道必要條件和設定
description: 瞭解如何設定您的環境，以使用Journey Optimizer傳送應用程式內訊息
role: Admin
feature: In App
level: Intermediate
keywords: 應用程式內、訊息、設定、平台
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 9%

---

# 先決條件與設定 {#inapp-configuration}

## 設定步驟 {#inapp-steps}

若要使用[!DNL Journey Optimizer]在歷程與行銷活動中傳送應用程式內訊息，您必須完成下列設定步驟。

1. 開始之前，請確定您對 Journey Optimizer 行銷活動擁有正確的權限，即使您計劃在歷程中僅使用應用程式內訊息也是如此。 仍需要行銷活動權限。 [深入瞭解](../campaigns/get-started-with-campaigns.md#campaign-prerequisites)。
必須授予特定許可權，才能存取Adobe Experience Platform資料收集中的**應用程式介面**&#x200B;功能表。 在[此影片](#video)中瞭解更多。
1. 在Adobe Experience Platform資料收集資料串流中啟用Adobe Journey Optimizer，並檢查Adobe Experience Platform中的預設合併原則，如以下[傳遞先決條件](#delivery-prerequisites)所述。
1. 在Adobe Experience Platform Data Collection中建立和設定應用程式表面，如[本節](#channel-prerequisites)所詳述。
1. 如果您使用內容實驗，請務必遵循[本節](#experiment-prerequisite)中列出的要求。

完成後，您可以建立、設定和傳送您的第一個應用程式內訊息。 在[本節](create-in-app.md)中了解如何達成此目的。

## 傳遞必要條件 {#delivery-prerequisites}

為了正確傳遞應用程式內訊息，必須定義下列設定：

* 在[Adobe Experience Platform Data Collection](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hant){target="_blank"}中，確定您已定義資料串流，例如在&#x200B;**[!UICONTROL Adobe Experience Platform]**&#x200B;服務下，您已啟用Adobe Experience Platform Edge和&#x200B;**[!UICONTROL Adobe Journey Optimizer]**&#x200B;選項。

  這可確保Adobe Experience Platform Edge正確處理Journey Optimizer傳入事件。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/inapp_config_6.png)

* 在[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}中，確定您已啟用預設合併原則&#x200B;**[!UICONTROL Edge上主動式合併原則]**&#x200B;選項。 若要這麼做，請在&#x200B;**[!UICONTROL 客戶]** > **[!UICONTROL 設定檔]** > **[!UICONTROL 合併原則]** Experience Platform功能表下選取原則。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  此合併原則由[!DNL Journey Optimizer]個傳入頻道使用，以便在邊緣正確啟用和發佈傳入行銷活動。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hant){target="_blank"}

  >[!NOTE]
  >
  >使用自訂&#x200B;**[!UICONTROL 資料集偏好設定]**&#x200B;合併原則時，請確定在指定的合併原則中新增&#x200B;**[!UICONTROL 歷程輸入]**&#x200B;資料集。

  ![](assets/inapp_config_8.png)

* 若要針對Journey Optimizer行動體驗的傳遞進行疑難排解，您可以在&#x200B;**Edge Delivery保證**&#x200B;中使用&#x200B;**Adobe Experience Platform**&#x200B;檢視。 此外掛程式可讓您詳細檢查請求呼叫、驗證預期的邊緣呼叫是否如預期發生，以及檢查設定檔資料，包括身分對應、區段會籍和同意設定。 此外，您可以檢閱請求符合資格的活動，並識別未符合資格的活動。

  使用&#x200B;**Edge Delivery**&#x200B;外掛程式可協助您取得所需的深入分析，以有效瞭解並疑難排解傳入的實作。

  [進一步瞭解Edge Delivery檢視](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/assurance/view/edge-delivery)

## 通道設定先決條件 {#channel-prerequisites}

1. 存取&#x200B;**[!UICONTROL 應用程式表面]**&#x200B;功能表並按一下&#x200B;**[!UICONTROL 建立應用程式表面]**。

1. 新增名稱至您的&#x200B;**[!UICONTROL 應用程式表面]**。

   ![](assets/inapp_config_2b.png)

1. 從&#x200B;**[!UICONTROL Apple iOS]**&#x200B;下拉式清單中，為Apple iOS設定您的行動應用程式。

+++ 更多詳情

   1. 輸入您的&#x200B;**[!UICONTROL iOS套件組合識別碼]**。 請參閱[Apple檔案](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids)，以取得有關&#x200B;**套件ID**&#x200B;的詳細資訊。

   1. （選擇性）選擇要從中傳送推播通知的&#x200B;**[!UICONTROL 沙箱]**。 請注意，選擇特定沙箱需要必要的存取許可權。

      如需沙箱管理的詳細資訊，請參閱[此頁面](../administration/sandboxes.md#assign-sandboxes)。

   1. 啟用&#x200B;**[!UICONTROL 推送認證]**&#x200B;選項，以便視需要拖放您的.p8驗證金鑰檔案。

      您也可以啟用&#x200B;**[!UICONTROL 手動輸入推送認證]**&#x200B;選項，以直接複製並貼上您的APN驗證金鑰。

   1. 輸入您的&#x200B;**[!UICONTROL 金鑰識別碼]**&#x200B;和&#x200B;**[!UICONTROL 團隊識別碼]**。

      ![](assets/inapp_config_2.png)

+++

1. 從&#x200B;**[!UICONTROL Android]**&#x200B;下拉式清單中，設定Android的行動應用程式。

+++ 更多詳情

   1. 輸入您的&#x200B;**[!UICONTROL Android封裝名稱]**。 如需&#x200B;**封裝名稱**&#x200B;的詳細資訊，請參閱[Android檔案](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores)。

   1. （選擇性）選擇要從中傳送推播通知的&#x200B;**[!UICONTROL 沙箱]**。 請注意，選擇特定沙箱需要必要的存取許可權。

      如需沙箱管理的詳細資訊，請參閱[此頁面](../administration/sandboxes.md#assign-sandboxes)。

   1. 啟用&#x200B;**[!UICONTROL 推送認證]**&#x200B;選項，視需要拖放您的.json私密金鑰檔案。

      您也可以啟用&#x200B;**[!UICONTROL 手動輸入推送認證]**&#x200B;選項，以直接複製並貼上FCM私密金鑰。

      ![](assets/inapp_config_7.png)

1. 完成&#x200B;**[!UICONTROL 應用程式表面]**&#x200B;的設定時，請按一下&#x200B;**[!UICONTROL 儲存]**。

   ![](assets/inapp_config_3.png)

   使用應用程式內訊息建立新行銷活動時，現在可以使用您的&#x200B;**[!UICONTROL 應用程式表面]**。 [了解更多](create-in-app.md)

1. 建立應用程式表面後，您現在需要建立行動屬性。

   如需詳細程式，請參閱[此頁面](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile)。

   ![](assets/inapp_config_4.png)

1. 從新建立屬性的「擴充功能」功能表中，安裝下列擴充功能：

   * Adobe Experience PlatformEdge Network
   * Adobe Journey Optimizer
   * AEP保證
   * 同意
   * 身分
   * 行動核心
   * 設定檔

   如需詳細程式，請參閱[此頁面](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension)。

   ![](assets/inapp_config_5.png)

應用程式內頻道現已設定。 您可以開始傳送應用程式內訊息給使用者。

## 內容實驗先決條件 {#experiment-prerequisites}

若要啟用應用程式內管道的內容實驗，您必須確定應用程式內實作[資料流](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"}中使用的[資料集](../data/get-started-datasets.md)也包含在報告設定中。

換言之，在設定實驗報告時，如果您新增的資料集未出現在網頁資料流中，則網頁資料不會顯示在內容實驗報告中。

瞭解如何在[本節](../content-management/reporting-configuration.md#add-datasets)中為內容實驗報告新增資料集。

>[!NOTE]
>
>資料集由[!DNL Journey Optimizer]報告系統以唯讀方式使用，不會影響資料收集或資料擷取。

如果您&#x200B;**不**&#x200B;使用下列資料集結構描述的預先定義[欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant#field-group){target="_blank"}： `AEP Web SDK ExperienceEvent`和`Consumer Experience Event` （如[此頁面](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}中所定義），請務必新增下列欄位群組： `Experience Event - Proposition Interactions`、`Application Details`、`Commerce Details`和`Web Details`。 [!DNL Journey Optimizer]內容實驗報告需要這些專案，因為它們正在追蹤每個設定檔參與哪些實驗和處理方式。

>[!NOTE]
>
>新增這些欄位群組不會影響正常的資料收集。 它僅適用於執行實驗的頁面，而保留所有其他追蹤不變。

## 操作說明影片{#video}

以下影片說明如何指派&#x200B;**管理應用程式組態**&#x200B;存取應用程式表面功能表的許可權。

>[!VIDEO](https://video.tv.adobe.com/v/3421607)


**相關主題：**

* [建立應用程式內訊息](create-in-app.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [設計應用程式內訊息](design-in-app.md)
* [應用程式內報告](../reports/campaign-global-report.md#inapp-report)

