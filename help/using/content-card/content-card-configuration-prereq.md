---
title: 內容卡設定
description: 內容卡片頻道先決條件
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: 598be5d2c5aca0262063c61e80e6b36020983131
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 5%

---

# 內容卡的先決條件 {#content-card-configuration-prereq}

若要讓Adobe Journey Optimizer正確顯示內容卡，您必須設定下列Adobe Experience Platform設定：

* **Adobe Experience Platform資料彙集**

  [建立資料流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure){target="_blank"}並[新增Experience Platform服務](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#aep){target="_blank"}。 啟用&#x200B;**[!UICONTROL Edge分段]**&#x200B;和&#x200B;**[!UICONTROL Adobe Journey Optimizer]**選項。 這可確保Journey Optimizer事件由Adobe Experience Platform Edge Network處理。
將**體驗事件 — 主張互動**&#x200B;欄位群組新增至您的資料集，以將此資料納入您的報表。 [進一步瞭解資料串流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure){target="_blank"}

* **Adobe Experience Platform**

  確定預設合併原則已在&#x200B;**客戶** > **[!UICONTROL 設定檔]** > **[!UICONTROL 合併原則]** Experience Platform功能表底下啟用&#x200B;**[!UICONTROL Edge上作用中合併原則]**。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  >[!NOTE]
  >
  >使用自訂&#x200B;**[!UICONTROL 資料集偏好設定]**&#x200B;合併原則時，請確定在指定的合併原則中新增&#x200B;**[!UICONTROL 歷程輸入]**&#x200B;資料集。

* **Adobe Experience Platform Mobile或Platform Web SDK**

  若要使用行動與網頁應用程式，將修改新增至您的網頁或行動應用程式，您必須在您的網站上實施[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/zh-hant/docs/platform-learn/implement-web-sdk/overview){target="_blank"}，或在行動應用程式上實施[Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/){target="_blank"}。

* **Journey Optimizer**

  建立[內容卡組態](#content-card-configuration)。

* **疑難排解**

  在&#x200B;**Adobe Experience Platform Assurance**&#x200B;中使用&#x200B;**Edge Delivery**&#x200B;檢視來疑難排解行動體驗。 它可以檢查請求、驗證Edge呼叫及檢查設定檔資料。 [了解更多](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

* **內容實驗**

  確認應用程式的[資料流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview#_blank){target="_blank"}中使用的資料集也包含在內容實驗報告設定中。 如果資料集不符，應用程式資料不會顯示在報表中。

  瞭解如何在[本節](../reports/reporting-configuration.md)中為內容實驗報告新增資料集。
