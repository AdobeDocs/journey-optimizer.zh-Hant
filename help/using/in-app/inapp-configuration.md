---
title: 應用內配置
description: 瞭解如何配置環境以向Journey Optimizer發送應用內消息
role: Admin
level: Intermediate
keywords: 應用內、消息、配置、平台
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: e35aeba17f45145cc7712740cbcf1f0e169760fc
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 11%

---

# 設定應用程式內頻道 {#inapp-configuration}

在發送應用內消息之前，您需要在 [!DNL Adobe Experience Platform Data Collection]。

1. 從 [!DNL Adobe Experience Platform Data Collection] 帳戶，訪問 **[!UICONTROL 資料流]** 的 **[!UICONTROL 新資料流]**。 有關資料流建立的詳細資訊，請參閱 [此頁](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams)。

1. 選擇 [!DNL Adobe Experience Platform] 服務。

   [!DNL Edge Segmentation] 和 [!DNL Adobe Journey Optimizer] 。

   ![](assets/inapp_config_6.png)

1. 然後，訪問 **[!UICONTROL 應用曲面]** 菜單，然後按一下 **[!UICONTROL 建立應用程式曲面]**。

   ![](assets/inapp_config_1.png)

1. 將名稱添加到 **[!UICONTROL 應用表面]**。

1. 從Apple·iOS下拉，輸入 **iOS捆綁ID**。 請參閱 [Apple文檔](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) 的 **捆綁ID**。

   ![](assets/inapp_config_2.png)

1. 從Android下拉清單中，輸入 **Android程式包名稱**。 請參閱 [Android文檔](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) 的 **包名稱**。

1. 按一下 **[!UICONTROL 保存]** 完成配置時 **[!UICONTROL 應用表面]**。

   ![](assets/inapp_config_3.png)

   您 **[!UICONTROL 應用表面]** 現在，在建立帶有In-app消息的新市場活動時將可用。 [了解更多](create-in-app.md)

1. 建立應用程式曲面後，現在需要建立移動屬性。

   請參閱 [此頁](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) 的上界。

   ![](assets/inapp_config_4.png)

1. 從新建立的屬性的「擴展」菜單中，安裝以下擴展：

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP保證
   * 同意
   * 識別
   * 移動核心
   * 設定檔

   請參閱 [此頁](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en#add-a-new-extension) 的上界。

   ![](assets/inapp_config_5.png)

現在已配置In-app通道。 您可以開始向用戶發送應用內消息。

**相關主題：**

* [建立應用程式內訊息](create-in-app.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [設計應用內消息](design-in-app.md)
* [應用程式內報告](../reports/campaign-global-report.md#inapp-report)
