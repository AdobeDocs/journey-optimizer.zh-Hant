---
title: 內容卡設定
description: 內容卡片頻道先決條件
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="限量開放使用" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 8a902298bbbac5689b4f84266dd9c9027e45fad5
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 7%

---

# 內容卡片先決條件 {#content-card-configuration-prereq}

>[!BEGINSHADEBOX]

**目錄**

* [開始使用內容卡](get-started-content-card.md)
* **內容卡先決條件**
* [在Journey Optimizer中設定內容卡片頻道](content-card-configuration.md)
* [建立內容卡片](create-content-card.md)
* [設計內容卡片](design-content-card.md)
* [內容卡片報表](content-card-report.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>內容卡目前僅可用於一組組織（可用性限制）。 如需存取權，請和您的 Adobe 代表聯絡。

若要讓Adobe Journey Optimizer正確顯示內容卡，您必須設定下列Adobe Experience Platform設定：

* **Adobe Experience Platform資料彙集**

  [建立資料流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)並[新增Experience Platform服務](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#aep)。 啟用&#x200B;**[!UICONTROL Edge分段]**&#x200B;和&#x200B;**[!UICONTROL Adobe Journey Optimizer]**&#x200B;選項。 這可確保Journey Optimizer事件由Adobe Experience PlatformEdge Network處理。 如需如何設定資料串流的詳細資訊，請參閱[資料串流檔案](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)。

* **Adobe Experience Platform**

  確定預設合併原則已在&#x200B;**[!UICONTROL 客戶]** > **[!UICONTROL 設定檔]** > **[!UICONTROL 合併原則]** Experience Platform功能表下啟用&#x200B;**Edge上作用中合併原則**。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  >[!NOTE]
  >
  >使用自訂&#x200B;**[!UICONTROL 資料集偏好設定]**&#x200B;合併原則時，請確定在指定的合併原則中新增&#x200B;**[!UICONTROL 歷程輸入]**&#x200B;資料集。

* **Adobe Experience Platform Mobile或Platform Web SDK**

  若是行動與網頁應用程式，若要新增修改至您的網頁或行動應用程式，您必須在您的網站上實作[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/zh-hant/docs/platform-learn/implement-web-sdk/overview)，或在行動應用程式上實作[Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/)。

* **Journey Optimizer**

  建立[內容卡組態](#content-card-configuration)。

* **疑難排解**

  在&#x200B;**Edge Delivery保證**&#x200B;中使用&#x200B;**Adobe Experience Platform**&#x200B;檢視來疑難排解行動體驗。 它可以檢查請求、驗證Edge呼叫及檢查設定檔資料。 [了解更多](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/assurance/view/edge-delivery)

* **內容實驗**

  確認應用程式的[資料流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview#_blank)中使用的資料集也包含在內容實驗報告設定中。 如果資料集不符，應用程式資料不會顯示在報表中。

  瞭解如何在[本節](../content-management/reporting-configuration.md)中為內容實驗報告新增資料集。