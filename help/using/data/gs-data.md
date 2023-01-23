---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用Journey Optimizer中的資料
description: 了解如何在Journey Optimizer中使用資料
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 資料，管理，平台
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# 開始使用 [!DNL Journey Optimizer] {#about-data}

最終客戶資料的豐富性和覆蓋性決定了任何客戶體驗解決方案的優勢和成功；而且這些資料是神聖的，對任何給定客戶來說都是最有價值的。 技術選擇現在內在內置，對資料管理能力進行嚴格評估。

使用 [!DNL Adobe Journey Optimizer]，您可以輕鬆管理、保留這些資料，並將其匯出至屬於您技術堆疊一部分的平台或系統。

**我的資料、規則** - [!DNL Adobe Journey Optimizer] 除了所有歷程資料和其操作固有的選件資料外，持續（即時）會建立一組豐富的客戶設定檔資料。 從您的資料庫中提取的草稿用戶資料將得到豐富，並轉換為具有覆蓋範圍和深度的高價值資料。 您希望此資料安全無虞，同時無處不在，以便在整個IT生態系統中利用其價值。

總的來說，您希望從資料中獲得的靈活性是：


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="目的地" src="assets/do-not-localize/dest.png" /> 
    <br>其他目的地可用 — 而 [!DNL Adobe Journey Optimizer] 為超個性化的客戶體驗整合和整合資料，您希望此資料在整體技術環境中的其他系統中，同時尋找其他方法來利用此資料。
    <div>
     <a href="../start/ajo-integrations.md">了解更多</a></div>
    </div>
    <br>
  </td>
</tr>
</table>

<!--td>
    <div><img alt="retention" src="assets/do-not-localize/retention.png" />  
    <br>Retained for a stipulated duration – Industry or regional regulations (such as GDPR or CCPA) or internal data governance policies stipulate how long or how short a duration, data needs to be maintained or archived in Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Learn more</a></div>
  </td>
</tr>
<tr style="border: 0;"-->
<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="原則" src="assets/do-not-localize/policy.png" /> 
    <br>根據商定的時間表或您的策略刪除資料 — 資料刪除是資料保護的一個關鍵方面，是所有資料治理過程中的關鍵步驟。 [!DNL Adobe Journey Optimizer] 可能產生的資料多於需要。 此外，您也想在資料集的必要持續時間過後，盡量處理所發生的情況，無論是因為公用程式或法規的緣故。 您需要的控制是在任何指定時間點刪除資料。 <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html">進一步了解Adobe Experience Platform檔案中的資料衛生</a></div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform]，其中 [!DNL Adobe Journey Optimizer] 已建置，可讓您在參與期間以及參與結束期間，對資料有最高層級的控制。 內 [!DNL Journey Optimizer]，您就能完全控制資料(由 [!DNL Journey Optimizer])、覆蓋到該資料的控管，以及該資料傳送至的目的地。

所有資料均視為客戶的屬性，只能根據您的要求進行維護、加密、分發或銷毀。 Adobe是您的受託人，絕對無權存取您的資料。

您可以使用 [!DNL Journey Optimizer]資料的靈活性，可滿足您與資料保留、存檔或刪除相關的特定要求：

* **資料擷取/匯出**:您可以隨時透過資料存取API開始擷取來源資料，不會受到任何懲罰或延遲。 此 [資料存取API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target="_blank"} 為用戶提供RESTful介面，重點在於發現資料集並使其可訪問 [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   請注意，歷程或行銷活動中使用的內容無法透過上述API或目的地方法擷取。

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 30 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **清除和歸檔機制**:資料和存檔的清除可以在 [!DNL Adobe Journey Optimizer] 自動執行資料保留政策。 可以為不同的資料實體定義不同的老化策略。 也可以定義匯出機制，以在清除或封存老化資料前自動匯出。

   Adobe Experience Platform UI中的資料衛生工作區可讓您建立和監控各種資料衛生工作，包括刪除消費者身分和排程資料集有效期。 此工作區隨「安全與隱私保護」和「醫療保健防護」一起提供。 深入了解 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html){target="_blank"}.

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **參與終止/退出時擷取資料**:合約終止時，您的資料會從Adobe的儲存空間中完全移除。 此外，您也可以在終止協定前提取完整的設定檔擷取。 此功能不需額外付費。 您可以隨時執行此作業，而不只是在終止時。

上述方法由合約定義，並在資料處理協定(DPA)中詳細說明，且Adobe在合約開始時與您相互同意。 Adobe應用程式，包括 [!DNL Journey Optimizer]，其設計原則是將每個客戶的資料視為該客戶的專屬資料資產。
