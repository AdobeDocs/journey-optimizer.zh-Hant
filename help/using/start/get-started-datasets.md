---
title: 開始使用資料集
description: 了解如何在Adobe Journey Optimizer中使用Adobe Experience Platform資料集
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 4cf9a45ee9cc7169d060799de7d1ea128caa140f
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 7%

---

# 開始使用資料集 {#datasets-gs}

所有擷取至Adobe Experience Platform的資料都會以資料集形式保存在Data Lake中。 資料集是資料集合的儲存和管理結構，通常是包含方案 (欄) 和欄 (列) 的表格。 

## 存取資料集{#access-datasets}

此 **資料集** 工作區 [!DNL Adobe Journey Optimizer] 使用者介面可讓您探索資料並建立資料集。

選擇 **資料集** 在左側導覽中，開啟「資料集」控制面板。

![](assets/datasets-home.png)

新增資料至 [!DNL Adobe Experience Platform] 是建立設定檔的基礎。 之後，您就能在 [!DNL Adobe Journey Optimizer]. 首先定義結構，使用ETL工具準備和標準化資料，然後根據您的結構建立資料集。

選取 **瀏覽** 索引標籤，顯示貴組織所有可用資料集的清單。 系統會顯示每個列出資料集的詳細資訊，包括其名稱、資料集所遵守的結構，以及最新擷取執行的狀態。

依預設，只會顯示您已擷取的資料集。 如果要查看系統產生的資料集，請啟用 **顯示系統資料集** 在篩選器中切換。

![](assets/ajo-system-datasets.png)

選取資料集名稱，以存取其「資料集」活動畫面，並查看您選取之資料集的詳細資訊。 活動索引標籤包含將所使用訊息的比率視覺化的圖形，以及成功和失敗批次的清單。

可用的不同資料集如下：

**報告**

* _報表 — 訊息意見事件資料集_:訊息傳送記錄檔。 關於從Journey Optimizer傳送所有訊息以用於報表和區段建立用途的資訊。 此資料集也會記錄來自退信之電子郵件ISP的意見。
* _報表 — 電子郵件追蹤體驗事件資料集_:用於報表和區段建立目的之電子郵件通道的互動記錄。 儲存的資訊會通知使用者在電子郵件（開啟、點按等）上執行的動作。
* _報表 — 推播追蹤體驗事件資料集_:用於報表和區段建立用途的「推播」管道互動記錄。 儲存的資訊會通知使用者在推播通知上執行的動作。
* _報告 — 歷程步驟事件_:擷取從Journey Optimizer產生的所有歷程步驟體驗事件，供報表之類的服務使用。 對於在Customer Journey Analytics中建立YoY分析報表也很重要。 系結至歷程中繼資料。
* _報告 — 歷程_:包含歷程中每個步驟資訊的中繼資料資料集。
* _報告 — 密件副本_:意見事件資料集，用於儲存BCC電子郵件的傳送記錄。 以用於報告用途。

**同意**

* _同意服務資料集_:儲存設定檔的同意資訊。

**Intelligent Services**

* _傳送時間最佳化分數/參與分數_:輸出Journey AI的分數。

## 預覽資料集{#preview-datasets}

在「資料集活動」畫面中，選取 **預覽資料集** 在畫面的右上角附近，預覽此資料集中最新成功的批次資料。 資料集空白時，預覽連結會停用。

![](assets/dataset-preview.png)

## 建立資料集{#create-datasets}

若要建立新資料集，請先選取 **建立資料集** 在「資料集」控制面板中。

您可以：

* 從結構建立資料集。 [深入了解本檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;}
* 從CSV檔案建立資料集。 [深入了解本檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=zh-Hant){target=&quot;_blank&quot;}

觀看此影片，了解如何建立資料集、將資料對應至結構、新增資料，以及確認資料已內嵌。

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)

## 資料治理

在資料集中，瀏覽 **資料控管** 標籤來檢查資料集和欄位層級的標籤。 資料控管會根據套用的原則類型來分類資料。

其核心功能之一 [!DNL Adobe Experience Platform] 是將來自多個企業系統的資料匯整在一起，讓行銷人員更能識別、了解並吸引客戶。 此資料可能受貴組織或法律法規所定義的使用限制所限制。 因此，務必確保您的資料操作符合資料使用策略。

[!DNL Adobe Experience Platform Data Governance] 可讓您管理客戶資料，並確保符合適用於資料使用的法規、限制和政策。 它在Experience Platform內的各個層級（包括編目、資料處理、資料使用標籤、資料使用策略）發揮關鍵作用，並控制資料在營銷操作中的使用。

進一步了解資料控管和資料使用標籤，位於 [資料控管檔案](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/user-guide.html){target=&quot;_blank&quot;}

## 範例和使用案例{#uc-datasets}

了解如何建立結構、資料集和內嵌資料，以在Adobe Journey Optimizer中新增測試設定檔，位於 [此端對端範例](../segment/creating-test-profiles.md)

進一步了解在 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh-Hant){target=&quot;_blank&quot;}。

了解如何在 [資料擷取概述檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

提供查詢範例的使用案例清單 [此處](../start/datasets-query-examples.md).

**另請參閱**

* [串流獲取概觀](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hant){target=&quot;_blank&quot;}
* [將資料內嵌至Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html){target=&quot;_blank&quot;}
