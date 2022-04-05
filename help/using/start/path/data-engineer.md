---
title: Journey Optimizer資料工程師入門
description: 作為資料工程師，瞭解如何與Journey Optimizer合作
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 1d0e28583c500d5eddf9f88250f279d188c4784a
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 9%

---

# 資料工程師入門 {#data-engineer}

作為 **Adobe Journey Optimizer資料工程師**、準備和維護客戶配置檔案資料，以推動由 [!DNL Journey Optimizer]、為架構中的客戶和業務資料建模並配置源連接器以接收資料。 你可以開始使用 [!DNL Adobe Journey Optimizer] 一次 [系統管理員](administrator.md) 授予您訪問權限並準備您的環境。


瞭解如何 **標識資料並建立模式和資料集** 將你的資料轉到Adobe Experience Platform。

>[!NOTE]
>
>瞭解有關 **資料攝取** 在 [Adobe Experience Platform文檔](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

以下各節詳細介紹了建立標識命名空間和啟用配置檔案和test配置檔案的資料集的步驟：

1. **建立標識命名空間**。 Adobe [!DNL Journey Optimizer]。 **身份** 將消費者連結到設備和通道，結果是標識圖。 連結的身份圖用於根據您所有業務接觸點之間的交互來個性化體驗。  瞭解有關標識和標識命名空間的詳細資訊 [此頁](../../segment/get-started-identity.md)。

1. **建立架構** 並為配置檔案啟用它。 模式是一組規則，用於表示和驗證資料的結構和格式。 在高級別上，架構提供了真實世界對象（如人）的抽象定義，並概述該對象的每個實例中應包括哪些資料（如名字、姓氏、生日等）。  瞭解有關架構的詳細資訊 [此頁](../get-started-schemas.md)。

1. **建立資料集** 並為配置檔案啟用它。 資料集是資料集合的儲存和管理結構，通常是包含方案 (欄) 和欄 (列) 的表格。 資料集還包含描述其所儲存資料的各個方面的元資料。 建立資料集後，可以將其映射到現有架構並將資料添加到該架構中。 瞭解有關資料集的詳細資訊 [此頁](../get-started-datasets.md)。

1. **配置源連接器**。 AdobeJourney Optimzer允許從外部源接收資料，同時讓您能夠使用平台服務構建、標籤和增強傳入資料。 您可以從多種源(如Adobe應用程式、基於雲的儲存、資料庫和許多其他源)接收資料。 瞭解有關源連接器的詳細資訊 [此頁](../get-started-sources.md)。

1. **建立測試設定檔**. Test配置檔案在使用 [test模式](../../building-journeys/testing-the-journey.md) 在旅途中， [預覽和test您的郵件](../../design/preview.md) 在發送之前。 發現建立test配置檔案的步驟 [此頁](../../segment/creating-test-profiles.md)。


此外，要在行程中發送消息，必須配置 **[!UICONTROL Data Sources]**。 **[!UICONTROL Events]** 和 **[!UICONTROL Actions]**。 請參閱[本節](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* 的 **資料源** 配置允許您定義到系統的連接，以檢索將在您的行程中使用的其他資訊。 瞭解有關資料源的詳細資訊 [此部分](../../datasource/about-data-sources.md)。

* **事件** 允許你觸發整個旅程，即時地向流入旅程的個體發送消息。 在事件配置中，您可以配置行程中預期的事件。 傳入事件的資料按照Adobe體驗資料模型(XDM)進行規範化。 事件來自串流獲取 API，適用於驗證和未驗證的事件（例如 Adobe Mobile SDK 事件）。瞭解有關事件的詳細資訊 [此部分](../../event/about-events.md)。

* [!DNL Journey Optimizer] 內置消息功能：您可以設計內容並發佈消息。 如果您使用第三方系統發送消息，例如，Adobe Campaign，請建立 **自定義操作**。 瞭解有關此操作的詳細資訊 [此部分](../../action/action.md)。
