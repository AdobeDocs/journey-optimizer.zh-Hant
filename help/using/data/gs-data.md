---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用Journey Optimizer的資料
description: 瞭解如何在Journey Optimizer處理資料
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 資料，管理，平台
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: ef34cb0207d3011eca6d76ad6568f3edc00e13a3
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 1%

---

# 開始管理資料 [!DNL Journey Optimizer] {#about-data}

最終客戶資料的豐富性和覆蓋範圍決定了任何客戶體驗解決方案的強大性和成功；而且此資料是神聖的，對任何給定客戶來說都具有最高價值。 技術選擇現在天生就內置了嚴格評估資料管理能力。

與 [!DNL Adobe Journey Optimizer]，您可以輕鬆管理、保留此資料並將其導出到技術堆棧中的平台或系統。

**我的資料，我的規則** - [!DNL Adobe Journey Optimizer] 連續（並即時）建立一組豐富的客戶概要資料，以及所有行程資料，並提供其運營固有的資料。 從資料庫中攝取的用戶資料的草案版本將得到豐富，並轉換為具有覆蓋範圍和深度的高價值資料。 您希望此資料安全且同時無所不在，以便您能夠在整個IT生態系統中利用其價值。

總的來說，您希望從資料中獲得的靈活性是：


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="目的地" src="assets/do-not-localize/dest.png" /> 
    <br>在其他目標中可用 — 同時 [!DNL Adobe Journey Optimizer] 協同並整合資料以獲得超個性化的客戶體驗，您希望此資料在您整個技術環境中的其他系統中出現，同時您還要尋找其他方法來利用此資料。
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
    <div><img alt="政策" src="assets/do-not-localize/policy.png" /> 
    <br>已刪除協定的時間表或您的策略 — 資料刪除是資料保護的一個關鍵方面，是所有資料治理流程中的關鍵步驟。 [!DNL Adobe Journey Optimizer] 可能會生成超出要求的資料。 此外，您還希望在資料集所需的持續時間之後，盡量關注發生的情況 — 無論是因為實用性或法規。 您需要的控制是在任何給定時間點刪除資料。 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">了解更多</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform], [!DNL Adobe Journey Optimizer] 構建，為您提供最高級別的資料控制 — 在項目期間以及項目結束時。 在 [!DNL Journey Optimizer]，您完全控制資料(即， [!DNL Journey Optimizer])，管理覆蓋到資料和資料發送目的地。

所有資料都被視為客戶的屬性，只能根據您的請求進行維護、加密、分發或銷毀。 Adobe是您的受託人，絕對無權訪問您的資料。

您可以使用 [!DNL Journey Optimizer]滿足您在資料保留、存檔或刪除方面的特定要求的資料靈活性：

* **資料提取/導出**:您可以隨時通過資料存取API啟動源資料提取，而不會受到任何懲罰或延遲。 的 [資料存取API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target="_blank"} 為用戶提供了REST風格的介面，重點關注在其中攝取的資料集的可發現性和可訪問性 [!DNL Adobe Experience Platform]。 <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   請注意，不能通過上述API或目標方法提取行程或市場活動中使用的內容。

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 30 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **清除和存檔機制**:資料和存檔的清除可以在 [!DNL Adobe Journey Optimizer] 自動化資料保留策略。 可以為不同的資料實體定義不同的老化策略。 還可以定義導出機制，以便在清除或存檔老化資料之前自動導出老化資料。

   資料衛生工作區允許您建立和監視各種資料衛生任務，包括刪除消費者身份和安排資料集過期時間。 此工作區可隨Security &amp; Privacy Shield和Healthcare Shield一起使用。 在[本頁](../privacy/data-hygiene.md)中瞭解更多。

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **在項目終止/退出時提取資料**:當合同終止時，您的資料將完全從Adobe的儲存空間中刪除。 此外，在終止協定之前，還可以提取完整的配置檔案提取。 此功能無需額外成本。 這可以在任何時候進行，而不只是在終止時。

以上方法是合同定義的，並在資料處理協定(DPA)中詳細列出，Adobe在項目開始時與您相互同意。 Adobe應用程式，包括 [!DNL Journey Optimizer]，其設計原則是將每個客戶的資料視為該客戶的專有資料資產。
