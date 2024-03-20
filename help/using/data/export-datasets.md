---
solution: Journey Optimizer
product: journey optimizer
title: 將資料集匯出至雲端儲存空間位置
description: 瞭解如何使用Adobe Experience Platform雲端儲存空間目的地匯出資料集。
feature: Datasets
role: User
level: Beginner
keywords: platform、資料湖、建立、湖、資料集、設定檔
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: 83751eae9f703a89a57cb337492377ff2478d4a0
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 9%

---

# 將資料集匯出至雲端儲存空間位置 {#export-datasets}

Journey Optimizer可讓您與雲端儲存位置建立即時連線，以匯出資料集的內容。

透過定期匯出資料，您可以確保擁有完整且最新的客戶互動記錄，以便隨時用於報告、封存或資料分析目的。

## 可用的雲端儲存空間目的地 {#destinations}

您可以將資料集匯出至6個雲端儲存空間目標，您可從以下位置存取： **[!UICONTROL 目的地]** 功能表，在 **[!UICONTROL 目錄]** 標籤。

![](assets/dataset-export-setup.png)


Adobe Experience Platform檔案中提供每個目的地的詳細資訊：

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [資料登陸區域](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Google雲端儲存空間](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## 可供匯出的可用資料集 {#datasets}

從下表瞭解您可以匯出哪些Journey Optimizer資料集。

| 資料集 | 說明 |
| ------- | ------- | 
| AJO密件副本意見事件資料集 | AJO密件副本意見事件資料集 |
| AJO分類資料集 | 用於從Journey Optimizer擷取電子郵件和推播應用程式意見回饋事件的資料集。 透過SDK建立。 |
| AJO同意服務資料集 | 儲存設定檔的同意資訊。 |
| AJO 電子郵件追蹤體驗事件資料集 | 用於報告和建立受眾的電子郵件頻道的互動記錄。  |
| AJO 實體資料集 | 用於儲存傳送給一般使用者之訊息的實體中繼資料的資料集。  |
| AJO傳入活動事件資料集 | Journey Optimizer網路和應用程式內頻道傳遞與互動事件的資料集。 |
| AJO互動式訊息設定檔資料集 | 儲存為支援API觸發的行銷活動而建立的設定檔 |
| AJO 訊息意見回饋事件資料集 | 訊息傳遞記錄。 有關用於報告與對象建立目的，而從 Journey Optimizer 傳遞之所有訊息的資訊。 電子郵件 ISP 對退回郵件的意見也會記錄在此資料集。 |
| AJO設定檔計數器擴充功能 | 儲存包含counter_value和expiryDate的物件地圖，並以counter_id作為索引鍵 |
| AJO推播設定檔資料集 | 儲存設定檔的推播權杖。 |
| AJO 推播追蹤體驗事件資料集 | 推播頻道的互動記錄，用於報表和建立受眾。  |
| AJO表面資料集 | 與Journey Optimizer傳入表面結構描述相關的空白資料集 |
| AOOutputForUPSDatset | 包含要回寫至UPS的所有AO對象會籍 |
| Audience Orchestration設定檔資料集 | 由對象構成對象的對象構成產生。 包含所有對象構成對象、其屬性和擴充資料 |
| 決定物件存放庫 — 活動 | 也稱為使用者介面中的決策。 但是這些是使用者建立的物件，會將所有建置區塊放在一起，包括決策邏輯。 例如，針對特定位置（位置），應考量哪些優惠（優惠收藏），以及要對這些優惠方案使用哪個排名方法。 |
| 決定物件存放庫 — 遞補優惠 | 這是使用者建立之其他型別優惠方案的存放庫。 具體來說，如果他們沒有資格檢視個人化優惠且需要檢視某些內容，他們至少會看到遞補優惠。 此資料集包含此型別選件的屬性 |
| 決定物件存放庫 — 個人化優惠 | 這是使用者建立之優惠方案型別的存放庫。 因此，此資料集包含此類選件的相關屬性 | Ultimate |
| 決定物件存放庫 — 位置 | 這是物件的存放庫，會定義需要顯示優惠的位置。 |
| 歷程步驟事件 | 擷取從Journey Optimizer產生並供Reporting等服務使用的所有歷程步驟體驗事件。 |
| 歷程 | 中繼資料資料集存放歷程中每個步驟的資訊 |
| ODE DecisionEvents - prod decisioning | 每當我們根據請求做出決定時，就會將其計為決定事件 |

## 先決條件 {#prerequisites}

若要匯出資料集，您需要 [存取控制許可權](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions){target="_blank"} listed below. Read the [access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html){target="_blank"} 或聯絡您的產品管理員以取得必要許可權。

| 類別 | 權限 |
|--|--|
| 目的地 | 管理和啟用資料集目的地 |
| 資料管理 | 檢視資料集 |
| 目的地 | 檢視目的地 |

## 匯出資料集的關鍵步驟 {#main-steps}

將資料集匯出至雲端儲存位置的主要步驟如下：

![](assets/dataset-export-process.png)

有關每個步驟的詳細資訊，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html){target="_blank"}.

1. **設定您的雲端儲存空間目的地**. 如果您尚未這麼做，請從目的地目錄連線至雲端儲存空間目的地。 瞭解如何在中建立新的目的地連線 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html#setup){target="_blank"}.

   <!--![](assets/dataset-export-setup.png)-->

1. **選取雲端儲存空間目的地** 匯出資料集的位置。 在目的地目錄中，按一下 **[!UICONTROL 匯出資料集]** 按鈕，並選取要使用的連線。

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >如果您搭配使用Adobe Journey Optimizer以及即時客戶設定檔，目的地卡片將會顯示 **啟動** 按鈕，可讓您根據您啟用的許可權，匯出資料集及為此目的地啟用對象。

1. **選取資料集** 要匯出至所選目的地的檔案。 [進一步瞭解可用於匯出的Journey Optimizer資料集](#datasets)

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **排程匯出** 您的資料集的。 指定匯出應該何時開始，以及應該發生的頻率。

   <!--![](assets/dataset-export-schedule.png)-->

1. **檢閱並確認匯出** 檢查組態結束時顯示的摘要。

   <!--![](assets/dataset-export-review.png)-->

匯出完成後，資料集的內容會根據您設定的排程儲存在雲端儲存位置。 [瞭解如何驗證成功的資料集匯出](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify){target="_blank"}.
