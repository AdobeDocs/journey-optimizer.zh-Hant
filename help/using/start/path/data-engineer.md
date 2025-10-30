---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 資料工程師快速入門
description: 作為資料工程師，深入瞭解如何使用 Journey Optimizer
feature: Get Started
role: Developer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 資料工程師快速入門 {#data-engineer}

作為 **Adobe Journey Optimizer 資料工程師**，準備並維護客戶輪廓資料，以支援 [!DNL Journey Optimizer] 安排的體驗，為結構中的客戶和業務資料建立模型，並設定來源連接器以擷取資料。 當[系統管理員](administrator.md)授與您存取權限並準備好您的環境，您就可以開始使用[!DNL Adobe Journey Optimizer]。


在此頁面中了解如何&#x200B;**識別資料並建立結構和資料集** 以將您的資料傳入 Adobe Experience Platform。

>[!NOTE]
>
>若要深入瞭解&#x200B;**資料攝取**&#x200B;相關資訊，請參閱 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hant){target="_blank"}。

建立身分識別命名空間和為輪廓啟用的資料集，以及測試輪廓的步驟在以下各節中詳細說明：

1. **建立身分識別命名空間**。在 Adobe[!DNL Journey Optimizer]，**身分識別** 連結跨裝置和管道的消費者，結果會是身分識別圖表。 連結的身分識別圖表可依據您所有業務接觸點的互動，來個人化體驗。  請[在此頁面](../../audience/get-started-identity.md)進一步了解身分識別與身分識別命名空間。

1. **建立結構**&#x200B;並為輪廓啟用它。 結構描述是一組規則，足以代表並驗證資料的結構和格式。 從高層面來說，結構提供了真實對象 (如人) 的抽象定義，並概述應包含在該對象的每個執行個體中的資料 (如名字、姓氏、生日等)。  請[在此頁面](../../data/get-started-schemas.md)深入了解結構描述。

1. **建立資料集**&#x200B;並為輪廓啟用它。 資料集是資料集合的儲存和管理結構，通常是包含方案 (欄) 和欄位 (列) 的表格。 資料集也包含中繼資料，可說明其儲存資料的各個層面。 建立資料集後，您可以將資料集對應至現有結構並新增資料。 請[在此頁面](../../data/get-started-datasets.md)深入了解資料集。

1. **設定來源連接器**。Adobe Journey Optimizer 讓您可以從外部來源擷取資料，同時可以使用 Platform 服務來建立、加標籤，同時強化傳入資料。您可以從多種來源 (如 Adobe 應用程式、雲端型的儲存空間、資料庫和其他許多來源) 擷取資料。 請[在此頁面](../get-started-sources.md)深入了解來源連接器。

1. **建立測試輪廓**。使用[測試模式](../../building-journeys/testing-the-journey.md)在傳送前於歷程中[預覽和測試訊息](../../content-management/preview-test.md)。 建立測試輪廓的步驟已[在此頁面](../../audience/creating-test-profiles.md)詳細說明。


此外，若要在歷程中傳送訊息，您必須設定&#x200B;**[!UICONTROL 資料來源]**、**[!UICONTROL 事件]**&#x200B;和&#x200B;**[!UICONTROL 動作]**。請參閱[本節](../../configuration/about-data-sources-events-actions.md)以了解更多資訊。

![](../assets/admin-menu.png)

* **資料來源**&#x200B;設定可讓您定義系統連線，以擷取將用於歷程的其他資訊。[在此章節](../../datasource/about-data-sources.md)深入瞭解資料來源相關內容。

* **事件**&#x200B;可讓您一直觸發歷程，以即時傳送訊息給流入歷程的個人。 在事件設定中，您會設定歷程中預期的事件。 會依照 Adobe Experience Data Model (XDM)，對傳入事件的資料進行標準化。事件來自串流擷取 API，適用於驗證和未驗證的事件 (例如 Adobe Mobile SDK 事件)。[在此章節](../../event/about-events.md)深入瞭解事件相關內容。

* [!DNL Journey Optimizer] 隨附內建訊息功能：您可以在歷程中建立訊息，並設計內容。 如果您使用第三方系統來傳送訊息，例如 Adobe Campaign，請建立&#x200B;**自訂動作**。[在本節](../../action/action.md)中進一步了解動作。
