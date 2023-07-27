---
title: 應用程式內設定
description: 瞭解如何設定您的環境，以使用Journey Optimizer傳送應用程式內訊息
role: Admin
level: Intermediate
keywords: 應用程式內、訊息、設定、平台
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 11%

---

# 設定應用程式內頻道 {#inapp-configuration}

在傳送應用程式內訊息之前，您必須在中設定應用程式內頻道 [!DNL Adobe Experience Platform Data Collection].

1. 從您的 [!DNL Adobe Experience Platform Data Collection] 帳戶，存取 **[!UICONTROL 資料流]** 功能表並按一下 **[!UICONTROL 新增資料串流]**. 有關建立資料流的詳細資訊，請參閱 [此頁面](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=zh-Hant).

1. 選取 [!DNL Adobe Experience Platform] 服務。

   [!DNL Edge Segmentation] 和 [!DNL Adobe Journey Optimizer] 必須選取。

   ![](assets/inapp_config_6.png)

1. 然後，存取 **[!UICONTROL 應用程式表面]** 功能表，然後按一下 **[!UICONTROL 建立應用程式表面]**.

   >[!NOTE]
   >
   > 您需要 **管理應用程式設定** 存取的許可權 **[!UICONTROL 應用程式表面]** 功能表。 如需詳細資訊，請參閱 [此影片](#video).

   ![](assets/inapp_config_1.png)

1. 將名稱新增至 **[!UICONTROL 應用程式表面]**.


1. 從Apple iOS下拉式清單中，輸入 **iOS套件組合ID**. 請參閱 [Apple檔案](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) 如需詳細資訊，請參閱 **套件ID**.

   ![](assets/inapp_config_2.png)

1. 從Android下拉式清單，輸入 **Android套件名稱**. 請參閱 [Android檔案](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) 如需詳細資訊，請參閱 **封裝名稱**.

1. 按一下 **[!UICONTROL 儲存]** 當您完成設定 **[!UICONTROL 應用程式表面]**.

   ![](assets/inapp_config_3.png)

   您的 **[!UICONTROL 應用程式表面]** 現在起，使用應用程式內訊息建立新行銷活動時，即可使用。 [了解更多](create-in-app.md)

1. 建立應用程式表面後，您現在需要建立行動屬性。

   請參閱 [此頁面](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) 以取得詳細程式。

   ![](assets/inapp_config_4.png)

1. 從新建立屬性的「擴充功能」功能表中，安裝下列擴充功能：

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP保證
   * 同意
   * 身分
   * 行動核心
   * 設定檔

   請參閱 [此頁面](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension) 以取得詳細程式。

   ![](assets/inapp_config_5.png)

應用程式內頻道現已設定。 您可以開始傳送應用程式內訊息給使用者。

**相關主題：**

* [建立應用程式內訊息](create-in-app.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [設計應用程式內訊息](design-in-app.md)
* [應用程式內報告](../reports/campaign-global-report.md#inapp-report)


## 作法影片{#video}

* 以下影片說明如何指派 **管理應用程式設定** 存取應用程式表面功能表的許可權。

  +++請觀看影片
  >[!VIDEO](https://video.tv.adobe.com/v/3421607)
+++
