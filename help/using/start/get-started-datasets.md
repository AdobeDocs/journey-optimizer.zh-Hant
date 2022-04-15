---
title: 開始使用資料集
description: 瞭解如何在Adobe Journey Optimizer使用Adobe Experience Platform資料集
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 9ebcfd6c41c17fe3be0423822209443fc55244a7
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 11%

---

# 開始使用資料集 {#datasets-gs}

所有被攝入Adobe Experience Platform的資料都作為資料集保留在資料湖中。 資料集是資料集合的儲存和管理結構，通常是包含方案 (欄) 和欄 (列) 的表格。 

## 訪問資料集{#access-datasets}

的 **資料集** 工作區 [!DNL Adobe Journey Optimizer] 用戶介面允許您瀏覽資料和建立資料集。

選擇 **資料集** 的子菜單。

![](assets/datasets-home.png)

向Adobe Experience Platform添加資料是構建配置檔案的基礎。 然後，您將能夠在 [!DNL Adobe Journey Optimizer]。 首先定義方案，使用ETL工具準備和標準化資料，然後根據您的方案建立資料集。

選擇 **瀏覽** 頁籤，顯示組織的所有可用資料集的清單。 將顯示每個列出的資料集的詳細資訊，包括其名稱、資料集所遵循的架構以及最近接收運行的狀態。

預設情況下，僅顯示您已攝取的資料集。 如果要查看系統生成的資料集，請啟用 **顯示系統資料集** 從篩選器切換。

![](assets/ajo-system-datasets.png)

選擇資料集的名稱以訪問其「資料集」活動螢幕，並查看所選資料集的詳細資訊。 「活動」(Activity)頁籤包含圖形，以可視化正在使用的消息的速率以及成功和失敗批的清單。

## 建立資料集{#create-datasets}

要建立新資料集，請首先選擇 **建立資料集** 資料集儀表板中。

您可以：

* 從架構建立資料集。 [瞭解本文檔中的詳細資訊](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;
* 從CSV檔案建立資料集。 [瞭解本文檔中的詳細資訊](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=zh-Hant){target=&quot;_blank&quot;


觀看此視頻以瞭解如何建立資料集、將其映射到架構、向其添加資料以及確認已接收資料。

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)


瞭解如何在Adobe Journey Optimizer建立模式、資料集和接收資料以添加Test配置檔案 [這個端到端的樣本](../segment/creating-test-profiles.md)

瞭解有關在中建立資料集的詳細資訊 [Adobe Experience Platform文檔](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}。

瞭解如何在 [資料接收概述文檔](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。


**另請參閱**

* [建立模式、資料集和接收資料以添加Journey Optimizer的Test配置檔案](../segment/creating-test-profiles.md)
* [流攝入概述](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hant){target=&quot;_blank&quot;
* [將資料導入Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html){target=&quot;_blank&quot;
