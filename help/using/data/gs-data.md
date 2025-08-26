---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 Journey Optimizer 的資料管理
description: 了解如何在 Journey Optimizer 使用資料
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 資料，管理，平台
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 96%

---

# 開始使用資料管理 {#about-data}

終端客戶資料的豐富性和涵蓋範圍，是任何客戶體驗解決方案的優勢和成功的關鍵；這項資料是神聖的，對於任何特定客戶而言，都具有最高價值。 技術選擇現在內建了對資料管理功能的嚴格評估。

透過 [!DNL Adobe Journey Optimizer]，您可以輕鬆管理、保留這些資料，並將其匯出至屬於您技術堆疊一部分的平台或系統。 

**我的資料，我的規則** - [!DNL Adobe Journey Optimizer] 除了所有歷程資料及營運固有的產品建議資料外，還會持續 (並即時) 建立一組豐富的客戶輪廓。 從您的資料庫擷取的 Strawman 版本使用者資料，會透過涵蓋範圍和深度而擴充轉換為高價值的資料。 您希望資料安全無虞且無處不在，以便可以在整體 IT 生態系統中發揮其價值。

整體而言，您希望資料具有的彈性是：


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="目的地" src="assets/do-not-localize/dest.png" /> 
    <br>可在其他目的地使用 — 同時 [!DNL Adobe Journey Optimizer] 針對超個人化的客戶體驗同步並整合資料，您希望這些資料出現在整體技術環境的其他系統中，同時尋找其他方法善用這些資料。
    <div>
     <a href="../integrations/ajo-integrations.md">了解更多</a></div>
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
    <br>依據已同意的時間表或您的原則進行刪除 — 資料刪除是資料保護的關鍵方面，也是所有資料治理流程中的關鍵步驟。 [!DNL Adobe Journey Optimizer] 可能會產生比所需更多的資料。 此外，無論資料集是因公用程式或法規所限，您都需要極度注意資料集所需期間之後的情形。 您需要的控制是在任何指定時間點刪除資料。 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">了解更多</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform]，[!DNL Adobe Journey Optimizer] 以此為基礎，在參與期間以及參與結束時為您提供最高級別的資料控制。 在 [!DNL Journey Optimizer]內，您可完整控制資料 (被傳入或產生，[!DNL Journey Optimizer])、該資料覆蓋的控管以及該資料傳送到的目的地。

所有資料都視為客戶財產，只能根據您的請求進行維護、加密、發布或銷毀。 Adobe 充當您的受託人，對您的資料絕對沒有任何權利。

您可以使用 [!DNL Journey Optimizer] 的資料彈性，來滿足與資料保留、封存或刪除相關的特定需求：

* **資料擷取/匯出**：您可以隨時透過資料存取 API 啟動來源資料的擷取，不受任何處罰或時間延遲。 [資料存取API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=zh-Hant){target="_blank"}為使用者提供RESTful介面，著重於[!DNL Adobe Experience Platform]內擷取資料集的可發現性和可存取性。<!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

  請注意，無法透過上述 API 或目標方法擷取歷程或行銷活動使用的內容。

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer's default setting of retaining this data for up to 91 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization's data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **清除與封存機制**：資料清除和封存可自由定義，並可在 [!DNL Adobe Journey Optimizer] 自動化， 以自動化資料保留原則。 您可以為不同的資料實體定義不同的老化策略。 也可以定義匯出機制，在清除或封存過時資料之前自動匯出資料。

  資料生命週期工作區可讓您建立及監控各種資料生命週期工作，包括刪除消費者身分識別和排程資料集期限。 此工作區可與安全和隱私保護以及醫療保健一起使用。 請在[此頁面](../privacy/data-hygiene.md)了解更多。

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **參與終止/結束時的資料擷取**：合約終止時，您的資料會從 Adobe 的儲存空間完全移除。 此外，您可以在終止協定之前提取完整的輪廓。 此功能無需額外付費。您可以隨時執行此作業，而不只在合約終止時完成。

上述方法皆以合約形式定義，並在 Adobe 合約開始時與您共同同意的資料處理合約 (DPA) 中詳細說明。 包括 [!DNL Journey Optimizer] 在內的 Adobe 應用程式，其設計原則是根據每個使用者端的資料都被視為該使用者端專有資料資產的原則。
