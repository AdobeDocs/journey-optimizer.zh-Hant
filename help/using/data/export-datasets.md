---
solution: Journey Optimizer
product: journey optimizer
title: 將資料集匯出至雲端儲存位置
description: 了解如何使用Adobe Experience Platform雲端儲存目標匯出資料集。
role: User
level: Beginner
keywords: platform，資料湖，建立，湖，資料集，設定檔
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 1%

---


# 將資料集匯出至雲端儲存位置 {#export-datasets}

>[!AVAILABILITY]
>
>資料集匯出功能目前為測試版，可供所有Adobe Journey Optimizer使用者使用。 如果您尚未擁有存取權，請與Adobe代表合作，取得目的地的存取權。

Journey Optimizer可讓您與雲端儲存位置建立即時連線，以匯出資料集的內容。

通過定期導出資料，您可以確保客戶交互的完整和最新記錄、將此資訊用於報告或分析，並保持遵守法律要求。

## 可用的雲端儲存目的地 {#destinations}

您可以將資料集匯出至6個雲端儲存空間目的地，您可從 **[!UICONTROL 目的地]** ，在 **[!UICONTROL 目錄]** 標籤。

![](assets/dataset-export-setup.png)

>[!AVAILABILITY]
>
>這些目的地均可在測試版中提供，且可能會有所變更。

有關每個目的地的詳細資訊，請參閱Adobe Experience Platform檔案：

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure資料湖第2代](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [Data Landing Zone](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Google雲端儲存空間](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## 先決條件 {#prerequisites}

開始匯出資料集前，請先檢查下列必要條件：

* 若要匯出資料集，您需要 **管理目的地**, **檢視目的地**, **啟動目的地**，和 **管理和啟用資料集目的地** [存取控制權限](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions). 閱讀 [存取控制概觀](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html) 或聯絡您的產品管理員以取得所需的權限。

* 此功能僅支援匯出第一代資料，亦即中定義的原始資料 [Real-time Customer Data Platform產品說明](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2c-edition-prime-and-ultimate-packages.html). 請確定您要匯出的資料集不包含第二代資料。

## 匯出資料集的主要步驟 {#main-steps}

將資料集匯出至雲端儲存空間位置的主要步驟如下：

![](assets/dataset-export-process.png)

有關每個步驟的詳細資訊，請參閱Adobe Experience Platform檔案： [將資料集匯出至雲端儲存目的地](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en).

1. **設定雲端儲存目的地**. 如果您尚未這麼做，請從目的地目錄連線至雲端儲存空間目的地。 [了解如何建立新的目的地連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=en#setup)

   <!--![](assets/dataset-export-setup.png)-->

1. **選擇雲儲存目標** 匯出資料集的位置。 在目的地目錄中，按一下 **[!UICONTROL 匯出資料集]** 按鈕，然後選取要使用的連線。

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >如果您使用Adobe Journey Optimizer和即時客戶設定檔，目的地卡會顯示「啟用」按鈕，讓您根據已啟用的權限，匯出資料集和啟用此目的地的區段。

1. **選取資料集** 匯出至所選目的地的資訊。

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **排程匯出** 資料集。 指定匯出的開始時間和發生頻率。

   <!--![](assets/dataset-export-schedule.png)-->

1. **檢閱並確認匯出** 勾選顯示在設定結尾的摘要。

   <!--![](assets/dataset-export-review.png)-->

匯出完成後，資料集的內容會根據您設定的排程儲存在雲端儲存空間位置。 [了解如何驗證資料集匯出是否成功](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify)
