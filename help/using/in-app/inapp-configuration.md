---
title: 應用程式內設定
description: 了解如何設定您的環境，以使用Journey Optimizer傳送應用程式內訊息
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 9%

---

# 設定應用程式內頻道 {#inapp-configuration}

傳送應用程式內訊息之前，您需先在 [!DNL Adobe Experience Platform Data Collection].

1. 從 [!DNL Adobe Experience Platform Data Collection] 帳戶，存取 **[!UICONTROL 資料流]** 按一下 **[!UICONTROL 新資料流]**. 如需資料流建立的詳細資訊，請參閱 [本頁](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. 選取 [!DNL Adobe Experience Platform] 服務。

   [!DNL Edge Segmentation], [!DNL Offer Decisioning] 和 [!DNL Adobe Journey Optimizer] 中指定的URL。

   ![](assets/inapp_config_6.png)

1. 接著，存取 **[!UICONTROL 應用程式曲面]** ，然後按一下 **[!UICONTROL 建立應用程式曲面]**.

   ![](assets/inapp_config_1.png)

1. 將名稱新增至 **[!UICONTROL 應用程式表面]**.

1. 從Apple iOS下拉式清單中，輸入 **iOS套件ID**. 請參閱 [Apple檔案](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) 如需詳細資訊，請參閱 **套件ID**.

   ![](assets/inapp_config_2.png)

1. 從Android下拉式清單中，輸入 **Android封裝名稱**. 請參閱 [Android檔案](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) 如需詳細資訊，請參閱 **套件名稱**.

1. 按一下 **[!UICONTROL 儲存]** 完成 **[!UICONTROL 應用程式表面]**.

   ![](assets/inapp_config_3.png)

   您的 **[!UICONTROL 應用程式表面]** 現在當您使用應用程式內訊息建立新促銷活動時，即可使用。 [了解更多](create-in-app.md)

1. 建立應用程式表面後，您現在需要建立行動屬性。

   請參閱 [本頁](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) 詳細程式。

   ![](assets/inapp_config_4.png)

1. 從新建立屬性的「擴充功能」功能表，安裝下列擴充功能：

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP保證
   * 同意
   * 識別
   * 行動核心
   * 設定檔

   請參閱 [本頁](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en#add-a-new-extension) 詳細程式。

   ![](assets/inapp_config_5.png)

應用程式內通道現在已設定完畢。 您可以開始傳送應用程式內訊息給使用者。

**相關主題：**

* [建立應用程式內訊息](create-in-app.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [設計應用程式內訊息](design-in-app.md)
* [應用程式內報告](inapp-report.md)
