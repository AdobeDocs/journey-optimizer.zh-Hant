---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用資料集
description: 了解如何在 Adobe Journey Optimizer 使用 Adobe Experience Platform 資料集
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 平台、資料湖、建立、湖、資料集、設定檔
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 7fb853a898a84ff31c7a24b48f963f06c4d10b6f
workflow-type: ht
source-wordcount: '873'
ht-degree: 100%

---

# 開始使用資料集 {#datasets-gs}

所有擷取至 Adobe Experience Platform 的資料都會以資料集的形式保留在資料湖。資料集是資料集合的儲存和管理結構，通常是包含方案 (欄) 和欄位 (列) 的表格。 

## 存取資料集{#access-datasets}

[!DNL Adobe Journey Optimizer] 使用者介面中的&#x200B;**資料集**&#x200B;工作區可讓您探索資料和建立資料集。

在左側導覽選取&#x200B;**資料集**，開啟資料集儀表板。

![](assets/datasets-home.png)

將資料新增至 [!DNL Adobe Experience Platform] 是建立輪廓的基礎。 然後，您將能夠善用 [!DNL Adobe Journey Optimizer] 的輪廓。首先定義結構描述，使用 ETL 工具準備和標準化資料，然後根據您的結構描述建立資料集。

選取&#x200B;**瀏覽**&#x200B;索引標籤，顯示貴組織所有可用資料集的清單。 系統會顯示每個列出資料集的詳細資訊，包括其名稱、資料集所遵守的結構描述，以及最新擷取執行的狀態。

預設情況下，只會顯示您已擷取的資料集。如果要查看系統產生的資料集，請從篩選器啟用&#x200B;**顯示系統資料集**&#x200B;切換。

![](assets/ajo-system-datasets.png)

>[!NOTE]
>
>自 2024 年 11 月 1 日起，串流分段已不再支援來自 [!DNL Journey Optimizer] 追蹤、回饋資料集的傳送、開啟事件。針對實作頻率上限或疲勞管理部分，請改用企業規則。 您可在[本章節](../conflict-prioritization/rule-sets.md)中找到更多詳細資料，包括[此處](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510){target="_blank"}每日上限的使用案例說明。
>
>此外，自 2025 年 2 月起，存留時間 (TTL) 護欄正推廣至 Journey Optimizer 系統產生的資料集。 [了解更多](datasets-ttl.md)

選取資料集名稱，以存取其「資料集」活動畫面，並查看所選取資料集的詳細資訊。 活動索引標籤包含將所使用訊息的比率視覺化的圖形，以及成功和失敗批次的清單。

Adobe Journey Optimizer 的系統資料集如下所列。

>[!CAUTION]
>
> 系統資料集&#x200B;**不得修改**。 每次產品更新都會自動回復任何變更。

**報告**

* _報告 - 訊息意見事件資料集_：訊息傳遞記錄檔。 有關用於報告與客群建立目的，而從 Journey Optimizer 傳遞之所有訊息的資訊。 電子郵件 ISP 對退回郵件的意見也會記錄在此資料集。
* _報告 - 電子郵件追蹤體驗事件資料集_：用於報告與客群建立目的使用之電子郵件頻道的互動記錄。 儲存的資訊會通知終端使用者在電子郵件執行的動作 (開啟、按一下等)。
* _報告 - 推播追蹤體驗事件資料集_：用於報告與客群建立目的使用之推播通知頻道的互動記錄。 儲存的資訊會通知終端使用者在推播通知執行的動作。
* _報告 - 歷程步驟事件_：擷取從 Journey Optimizer 產生的所有歷程步驟體驗事件，供報告等服務使用。對於在 Customer Journey Analytics 建立 YoY 分析也很重要。繫結至歷程中繼資料。
* _報告 - 歷程_：包含歷程每個步驟資訊的中繼資料資料集。
* _報告 - 密件副本_：用於儲存密件副本電子郵件的傳遞記錄意見事件資料集。 用於報告用途。

**同意**

* _同意服務資料集_：儲存輪廓的同意資訊。

**Intelligent Services**

* _傳送時間最佳化分數 / 參與分數_：輸出 Journey AI 的分數。

若要檢視每個結構描述的欄位與屬性完整清單，請參閱 [Journey Optimizer 結構描述字典](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=zh-Hant){target="_blank"}。

## 預覽資料集{#preview-datasets}

在「資料集活動」畫面，選取畫面右上角附近的&#x200B;**預覽資料集**，預覽此資料集最新成功的批次資料。 當資料集空白時，預覽連結會停用。

![](assets/dataset-preview.png)

## 建立資料集{#create-datasets}

若要建立新資料集，請先在「資料集」儀表板先選取&#x200B;**建立資料集**。

您可以：

* 從結構建立資料集。[在本文件中進一步瞭解](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=zh-Hant#schema){target="_blank"}
* 從 CSV 檔案建立資料集。[在本文件中進一步瞭解](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=zh-Hant){target="_blank"}

觀看此影片，了解如何建立資料集、將資料對應至結構描述、新增資料，以及確認資料已擷取。

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)

## 資料治理

在資料集中，瀏覽&#x200B;**資料控管**&#x200B;索引標籤來檢查資料集和欄位層級的標籤。 資料控管會根據套用的原則類型來分類資料。

[!DNL Adobe Experience Platform] 的核心功能之一是將來自多個企業系統的資料彙整在一起，讓行銷人員更能識別、了解並吸引客戶。 此資料可能受貴組織或法律法規所定義的使用限制所約束。 因此，務必確保您的資料操作符合資料使用原則。

[!DNL Adobe Experience Platform Data Governance] 可讓您管理客戶資料，並確保符合適用於資料使用的法規、限制與原則。它在 Experience Platform 的各個層面發揮關鍵作用，包括編目、資料譜系、資料使用標籤、資料使用原則和控制資料在行銷活動的使用。

深入了解資料控管及資料使用標籤，請參閱[資料治理文件](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/user-guide.html?lang=zh-Hant){target="_blank"}

## 範例和使用案例{#uc-datasets}

了解如何建立結構、資料集和擷取資料，以在 Adobe Journey Optimizer 新增測試輪廓，請參閱[此端對端範例](../audience/creating-test-profiles.md)

請參閱 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh-Hant){target="_blank"}，深入了解資料集建立。

請參閱[資料攝取概觀文件](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hant){target="_blank"}，了解如何使用資料集 UI。

[此處](../data/datasets-query-examples.md)提供查詢範例的使用案例清單。

>[!MORELIKETHIS]
>
>* [串流擷取概觀](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hant){target="_blank"}
>* [將資料收錄至 Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=zh-Hant){target="_blank"}
