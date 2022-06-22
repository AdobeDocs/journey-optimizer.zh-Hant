---
title: 開始使用資料集
description: 瞭解如何在Adobe Journey Optimizer使用Adobe Experience Platform資料集
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 1de18fa479a54c09751324a67793ce50e5657ce3
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 8%

---

# 開始使用資料集 {#datasets-gs}

所有被攝入Adobe Experience Platform的資料都作為資料集保留在資料湖中。 資料集是資料集合的儲存和管理結構，通常是包含方案 (欄) 和欄 (列) 的表格。 

## 訪問資料集{#access-datasets}

的 **資料集** 工作區 [!DNL Adobe Journey Optimizer] 用戶介面允許您瀏覽資料和建立資料集。

選擇 **資料集** 的子菜單。

![](assets/datasets-home.png)

向添加資料 [!DNL Adobe Experience Platform] 是構建配置檔案的基礎。 然後，您將能夠在 [!DNL Adobe Journey Optimizer]。 首先定義方案，使用ETL工具準備和標準化資料，然後根據您的方案建立資料集。

選擇 **瀏覽** 頁籤，顯示組織的所有可用資料集的清單。 將顯示每個列出的資料集的詳細資訊，包括其名稱、資料集所遵循的架構以及最近接收運行的狀態。

預設情況下，僅顯示您已攝取的資料集。 如果要查看系統生成的資料集，請啟用 **顯示系統資料集** 從篩選器切換。

![](assets/ajo-system-datasets.png)

選擇資料集的名稱以訪問其「資料集」活動螢幕，並查看所選資料集的詳細資訊。 「活動」(Activity)頁籤包含圖形，以可視化正在使用的消息的速率以及成功和失敗批的清單。

## 預覽資料集{#preview-datasets}

在「資料集」活動螢幕中，選擇 **預覽資料集** 靠近螢幕右上角，預覽此資料集中最近成功的批處理。 當資料集為空時，將停用預覽連結。

![](assets/dataset-preview.png)


## 建立資料集{#create-datasets}

要建立新資料集，請首先選擇 **建立資料集** 資料集儀表板中。

您可以：

* 從架構建立資料集。 [瞭解本文檔中的詳細資訊](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;
* 從CSV檔案建立資料集。 [瞭解本文檔中的詳細資訊](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=zh-Hant){target=&quot;_blank&quot;

觀看此視頻以瞭解如何建立資料集、將其映射到架構、向其添加資料以及確認已接收資料。

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)

## 資料治理

在資料集中，瀏覽 **資料治理** 頁籤，以檢查資料集和欄位級別上的標籤。 資料治理根據應用的策略類型對資料進行分類。

其核心功能之一 [!DNL Adobe Experience Platform] 就是將多個企業系統中的資料整合在一起，以便讓營銷人員能夠識別、理解和吸引客戶。 此資料可能受您的組織或法律法規定義的使用限制的限制。 因此，必須確保資料操作符合資料使用策略。

[!DNL Adobe Experience Platform Data Governance] 允許您管理客戶資料並確保遵守適用於資料使用的法規、限制和策略。 它在Experience Platform的不同級別中起著關鍵作用，包括編目、資料沿襲、資料使用標籤、資料使用策略以及控制資料在市場營銷操作中的使用。

瞭解有關中的「資料治理」和資料使用標籤的詳細資訊 [資料治理文檔](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/user-guide.html){target=&quot;_blank&quot;

## 示例和使用案例{#uc-datasets}

瞭解如何在Adobe Journey Optimizer建立模式、資料集和接收資料以添加Test配置檔案 [這個端到端的樣本](../segment/creating-test-profiles.md)

瞭解有關在中建立資料集的詳細資訊 [Adobe Experience Platform文檔](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}。

瞭解如何在 [資料接收概述文檔](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

提供了包含查詢示例的使用案例清單 [這裡](../start/datasets-query-examples.md)。

**另請參閱**

* [流攝入概述](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hant){target=&quot;_blank&quot;
* [將資料導入Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html){target=&quot;_blank&quot;
