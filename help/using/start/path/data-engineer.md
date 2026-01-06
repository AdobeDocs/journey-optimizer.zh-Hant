---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 資料工程師快速入門
description: 作為資料工程師，深入瞭解如何使用 Journey Optimizer
feature: Get Started
role: Developer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 2d699fe8a3320400dad2d5d962028d6e2a5425f8
workflow-type: ht
source-wordcount: '898'
ht-degree: 100%

---

# 資料工程師快速入門 {#data-engineer}

作為&#x200B;**資料架構者**&#x200B;或&#x200B;**資料工程師**，您可以設定、維護客戶輪廓資料和其他資料來源，以便支援 [!DNL Journey Optimizer] 協調的體驗。 這包括將所有客戶、企業資料，不論是來自網頁、客戶關係管理，或是離線來源，都能一併整合入客戶統一的 360 度視圖中。 您可以將客戶設定檔資料、企業資料模型化為結構描述、設定來源連接器，以便擷取資料，同時確認資料流程順暢無阻，即可啟用即時客戶洞察、參與度。 當[系統管理員](administrator.md)授與您存取權限並準備好您的環境，您就可以開始使用[!DNL Adobe Journey Optimizer]。

>[!NOTE]
>
>若要深入瞭解&#x200B;**資料攝取**&#x200B;相關資訊，請參閱 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hant){target="_blank"}。

## 基本資料設定步驟

請依照下列步驟，為 Journey Optimizer 設定資料奠定良好基礎：

1. **建立身分識別的命名空間**。在 Adobe [!DNL Journey Optimizer]，**身分識別**&#x200B;連結跨裝置和管道的消費者，結果會是身分識別圖表。 連結的身分識別圖，可依據所有企業接觸點的互動，打造個人化體驗。請[在此頁面](../../audience/get-started-identity.md)進一步了解身分識別與身分識別命名空間。

   此外，請設定&#x200B;**補充識別碼**，即可啟用相同設定檔，再根據次要識別碼，例如訂購 ID，或是預訂 ID，輸入多重歷程執行個體。 深入瞭解[補充識別碼](../../building-journeys/supplemental-identifier.md)。

1. **建立結構描述**，再為輪廓啟用結構描述。 結構描述是一組規則，足以代表並驗證資料的結構和格式。 從高層面來說，結構描述會提供真實物件 (例如個人) 等抽象定義，還會概述應加入物件的每個執行個體資料 (例如名字、姓氏、生日等)。

   * 針對標準歷程、行銷活動：使用[XDM 結構描述](../../data/get-started-schemas.md)
   * 針對協調的行銷活動：建立[關聯式結構描述](../../orchestrated/gs-schemas.md)，以便啟用多實體細分

1. **建立資料集**，再啟用輪廓資料集。 資料集是資料集合的儲存和管理結構，通常是包含方案 (欄) 和欄位 (列) 的表格。 資料集也包含中繼資料，可說明其儲存資料的各個層面。 建立資料集後，您可以將資料集對應至現有結構並新增資料。 請[在此頁面](../../data/get-started-datasets.md)深入了解資料集。

   對於進階案例，請準備&#x200B;**個資料集，以便執行階段查詢**，才能使用記錄資料集中的即時資料，擴充歷程執行。 深入瞭解[資料集查詢](../../building-journeys/dataset-lookup.md)。

1. **設定來源連接器**。Adobe Journey Optimizer 讓您可以從外部來源擷取資料，同時可以使用 Platform 服務來建立、加標籤，同時強化傳入資料。您可以從多種來源 (如 Adobe 應用程式、雲端型的儲存空間、資料庫和其他許多來源) 擷取資料。 請[在此頁面](../get-started-sources.md)深入了解來源連接器。

1. **建立測試輪廓**。使用[測試模式](../../building-journeys/testing-the-journey.md)在傳送前於歷程中[預覽和測試訊息](../../content-management/preview-test.md)。 建立測試輪廓的步驟已[在此頁面](../../audience/creating-test-profiles.md)詳細說明。

1. **設定計算屬性**（選填）。 從設定檔資料建立衍生屬性，以便簡化細分、個人化。 計算屬性會自動計算複雜量度，例如「過去 90 天內的總購買次數」或是「平均訂購值」。 深入了解[計算屬性](../../audience/computed-attributes.md)。

此外，若想在歷程中傳送訊息，就必須設定&#x200B;**[!UICONTROL 資料來源]**、**[!UICONTROL 事件]**&#x200B;和&#x200B;**[!UICONTROL 動作]**。請參閱[本節](../../configuration/about-data-sources-events-actions.md)以了解更多資訊。

![](../assets/admin-menu.png)

* **資料來源**&#x200B;設定可讓您定義系統連線，以擷取將用於歷程的其他資訊。[在此章節](../../datasource/about-data-sources.md)深入瞭解資料來源相關內容。

* **事件**&#x200B;可讓您一直觸發歷程，以即時傳送訊息給流入歷程的個人。 在事件設定中，您會設定歷程中預期的事件。 會依照 Adobe Experience Data Model (XDM)，對傳入事件的資料進行標準化。事件來自串流擷取 API，適用於驗證和未驗證的事件 (例如 Adobe Mobile SDK 事件)。[在此章節](../../event/about-events.md)深入瞭解事件相關內容。

* [!DNL Journey Optimizer] 隨附內建訊息功能：您可以在歷程中建立訊息，並設計內容。 如果您使用第三方系統來傳送訊息，例如 Adobe Campaign，請建立&#x200B;**自訂動作**。若要了解更多關於動作的資訊，請參閱[此區段](../../action/action.md)。

## 監視和分析歷程資料

歷程執行後，您可以在資料湖中查詢歷程步驟事件，以監視績效、疑難排解問題並分析客戶行為。使用 SQL 查詢來分析：

* 輪廓進入與退出模式
* 錯誤率和捨棄原因
* 讀取客群匯出工作績效
* 自訂動作績效量度
* 歷程執行個體狀態和瓶頸

探索現成的[歷程分析查詢範例](../../reports/query-examples.md)，以開始進行資料分析和疑難排解。

## 跨角色共同作業

您的資料設定工作對其他團隊至關重要：

>[!BEGINTABS]

>[!TAB 與管理員合作]

與[管理員](administrator.md)共同處理存取權和治理：

* 請求資料管理和結構描述建立的必要權限
* 協調沙箱存取權，以進行開發和測試
* 就資料治理原則和同意管理達成一致
* 討論資料保留原則與儲存需求

>[!TAB 與開發人員合作]

與[開發人員](developer.md)共同處理資料結構和事件：

* 提供實作所需的 XDM 結構描述和事件結構
* 定義需要傳送的事件及其必要的承載格式
* 就資料收集需求和資料品質標準達成一致
* 同時測試事件傳送和資料擷取

>[!TAB 與行銷人員合作]

與[行銷人員](marketer.md)共同處理客群與資料：

* 建立個人化和細分的計算屬性
* 根據其行銷活動和歷程需求建立客群
* 為協調的行銷活動設定關聯式結構描述
* 支援進階使用案例的多實體細分

>[!ENDTABS]
