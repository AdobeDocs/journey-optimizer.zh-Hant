---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer資料工程師快速入門
description: 身為資料工程師，深入了解如何使用Journey Optimizer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# 資料工程師快速入門 {#data-engineer}

作為 **Adobe Journey Optimizer資料工程師**，準備並維護客戶設定檔資料，以支援 [!DNL Journey Optimizer]，為結構中的客戶和業務資料建立模型，並設定來源連接器以擷取資料。 您可以開始使用 [!DNL Adobe Journey Optimizer] once [系統管理員](administrator.md) 授予您存取權並準備您的環境。


了解如何 **識別資料並建立結構和資料集** 若要將您的資料匯入本頁的Adobe Experience Platform。

>[!NOTE]
>
>深入了解 **資料擷取** in [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html){target=&quot;_blank&quot;}。

建立身分命名空間和為設定檔啟用的資料集，以及測試設定檔的步驟在以下各節中詳細說明：

1. **建立身分命名空間**. 在Adobe [!DNL Journey Optimizer], **身分** 連結跨裝置和管道的消費者，結果會是身分圖表。 連結的身分圖表可依據您所有業務接觸點的互動，來個人化體驗。  進一步了解身分識別與身分識別命名空間 [在本頁](../../segment/get-started-identity.md).

1. **建立結構** 並為設定檔啟用它。 結構是一組規則，可代表及驗證資料的結構和格式。 從高層面來說，結構提供了真實對象（如人）的抽象定義，並概述應包含在該對象的每個實例中的資料（如名字、姓氏、生日等）。  進一步了解綱要 [在本頁](../../data/get-started-schemas.md).

1. **建立資料集** 並為設定檔啟用它。 資料集是資料集合（通常為表格）的儲存和管理結構，其中包含結構（欄）和欄位（列）。 資料集也包含中繼資料，可說明其儲存資料的各個層面。 建立資料集後，您可以將資料集對應至現有結構並新增資料。 深入了解資料集 [在本頁](../../data/get-started-datasets.md).

1. **配置源連接器**. Adobe Journey Optimizer可讓您從外部來源擷取資料，同時使用Platform服務來建構、加標籤及增強傳入資料。 您可以內嵌來自各種來源的資料，例如Adobe應用程式、雲端儲存、資料庫等。 深入了解來源連接器 [在本頁](../get-started-sources.md).

1. **建立測試設定檔**. 使用 [測試模式](../../building-journeys/testing-the-journey.md) 在歷程中 [預覽和測試訊息](../../email/preview.md) 傳送前。 建立測試設定檔的步驟已詳細說明 [在本頁](../../segment/creating-test-profiles.md).


此外，若要在歷程中傳送訊息，您必須設定 **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** 和 **[!UICONTROL Actions]**. 深入了解 [在本節](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* 此 **資料來源** 設定可讓您定義系統的連線，以擷取將用於歷程的其他資訊。 深入了解資料來源 [在本節](../../datasource/about-data-sources.md).

* **事件** 可讓您一直觸發歷程，即時傳送訊息給流入歷程的個人。 在事件設定中，您會設定歷程中預期的事件。 會依照Adobe Experience Data Model(XDM)，對傳入事件的資料進行標準化。 事件來自串流獲取API，適用於已驗證和未驗證的事件（例如Adobe Mobile SDK事件）。 深入了解事件 [在本節](../../event/about-events.md).

* [!DNL Journey Optimizer] 隨附內建訊息功能：您可以在歷程中建立訊息，並設計內容。 如果您使用協力廠商系統來傳送訊息（例如Adobe Campaign），請建立 **自訂動作**. 進一步了解中的動作 [在本節](../../action/action.md).
