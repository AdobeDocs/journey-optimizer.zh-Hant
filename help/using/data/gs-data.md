---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 [!DNL Journey Optimizer]
description: 了解如何在 [!DNL Journey Optimizer]
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 2dcfcc8d7006c92e046152db5ac1288bdde8b063
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 3%

---

# 開始使用 [!DNL Journey Optimizer] {#about-data}

最終客戶資料的豐富性和覆蓋性決定了任何客戶體驗解決方案的優勢和成功；而且，這些資料是神聖的，對任何給定客戶來說都是最有價值的。 技術選擇現在內在內置，對資料管理能力進行嚴格評估。

透過 Adobe Journey Optimizer，您可以輕鬆管理、保留這些資料，並將其匯出至屬於您技術堆疊一部分的平台或系統。 

**我的資料、規則** - Journey Optimizer除了其作業固有的所有歷程資料和選件資料外，還會持續（即時）建立一組豐富的客戶設定檔資料。 從您的資料庫中提取的草稿用戶資料將得到豐富，並轉換為具有覆蓋範圍和深度的高價值資料。 您希望此資料安全無虞，同時無處不在，以便在整個IT生態系統中利用其價值。

總的來說，您希望從資料中獲得的靈活性是三倍：


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="目的地" src="assets/do-not-localize/dest.png" /> 
    <br>其他目的地皆可使用 — 雖然Journey Optimizer可協同化及整合資料，以提供超個人化的客戶體驗，但您仍希望將這些資料整合至整體技術版圖中的其他系統，同時尋找其他運用這些資料的方式。
    <div>
     <a href="../start/ajo-integrations.md">了解更多</a></div>
    </div>
    <br>
  </td>
</tr>
  <td>
    <div><img alt="保留" src="assets/do-not-localize/retention.png" />  
    <br>保留的時間符合規定 — 產業或地區法規（例如GDPR或CCPA）或內部資料控管政策規定在Adobe Experience Platform Data Lake中需要維護或封存資料的時間長度或時間短。 <a href="../privacy/get-started-privacy.md">了解更多</a></div>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <div><img alt="原則" src="assets/do-not-localize/policy.png" /> 
    <br>根據商定的時間表或您的策略刪除資料 — 資料刪除是資料保護的一個關鍵方面，是所有資料治理過程中的關鍵步驟。 Journey Optimizer可能產生的資料多於需求。 此外，您也想在資料集的必要持續時間過後，盡量處理所發生的情況，無論是因為公用程式或法規的緣故。 您需要的控制是在任何指定時間點刪除資料。 <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html">進一步了解Adobe Experience Platform檔案中的資料衛生</a></div>
  </td>
</tr>
</table>

Adobe Experience Platform是Journey Optimizer的建置基礎，可讓您在參與期間以及參與結束期間，獲得最高層級的資料控制。 在Journey Optimizer中，您可以完全控制資料(由Journey Optimizer匯入或產生)、覆蓋在該資料上的控管，以及該資料傳送至的目的地。

所有資料均視為客戶的屬性，只能根據您的要求進行維護、加密、分發或銷毀。 Adobe是您的受託人，絕對無權存取您的資料。

您可以使用Journey Optimizer的資料靈活性，滿足與資料保留、存檔或刪除相關的特定需求：

* **資料擷取/匯出**:您可以隨時透過資料存取API開始擷取來源資料，不會受到任何懲罰或延遲。 此 [資料存取API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target=&quot;_blank&quot;}為使用者提供RESTful介面，著重於Experience Platform內所擷取資料集的可探索性和可存取性。 <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   請注意，歷程或行銷活動中使用的內容無法透過上述API或目的地方法擷取。

* **設定檔服務資料保留**:對於附加至任何設定檔的行為和時間系列資料，您可以選擇使用Journey Optimizer的預設設定，從新增至設定檔之日，或直到您選取的替代時段為止，將此資料保留最多30天。 Adobe保留這些資料的時間因合約而異，具體列於組織的資料保留政策中。

   進一步了解中的體驗事件過期時間 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target=&quot;_blank&quot;}。

* **清除和歸檔機制**:在Journey Optimizer中，資料和封存的清除可以自由定義並自動化，以自動執行資料保留政策。 可以為不同的資料實體定義不同的老化策略。 也可以定義匯出機制，以在清除或封存老化資料前自動匯出。

   Adobe Experience Platform UI中的資料衛生工作區可讓您建立和監控各種資料衛生工作，包括刪除消費者身分和排程資料集有效期。 此工作區隨「安全與隱私保護」和「醫療保健防護」一起提供。 深入了解 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html){target=&quot;_blank&quot;}。

* **資料湖和刪除**:儲存在Data Lake中的客戶資料可由Journey Optimizer保留：

   * 為期7天，以便將客戶資料帶入設定檔服務，之後可能會永久刪除，或
   * 直到被您刪除


* **參與終止/退出時擷取資料**:合約終止時，您的資料會從Adobe的儲存空間中完全移除。 此外，您也可以在終止協定前提取完整的設定檔擷取。 此功能不需額外付費。 您可以隨時執行此作業，而不只是在終止時。

上述方法由合約定義，並在資料處理協定(DPA)中詳細說明，且Adobe在合約開始時與您相互同意。 Adobe應用程式(包括Journey Optimizer)的設計原則是將每個客戶的資料視為該客戶的專有資料資產。
