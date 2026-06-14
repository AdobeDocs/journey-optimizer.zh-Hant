---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 Journey Optimizer 的輪廓
description: 了解如何在 Adobe Journey Optimizer 建立並管理輪廓
feature: Profiles
role: User
level: Beginner
exl-id: be3936e4-8185-4031-9daf-95eea58077d0
TQID: https://experienceleague.adobe.com/QpLGV-y5qbtmksC-99GU5PtaV-mUA-imew8JDj7-weA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3id: b32bb433-f8c6-4931-8e52-e657230a3bf2id: e95b6013-acbe-46e9-a3b5-b80e14088d7did: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: a51edc00631334874d111d8350ee7b0eb8e81aa5
workflow-type: tm+mt
source-wordcount: 527
ht-degree: 36%

---

# 開始使用輪廓 {#profiles-gs}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解Adobe Journey Optimizer中的即時客戶設定檔如何將線上、離線和協力廠商來源的客戶資料整合為單一檢視，以及如何存取設定檔儀表板。

>[!ENDSHADEBOX]

## 關於輪廓

善用 [!DNL Adobe Journey Optimizer] 的即時客戶輪廓，透過合併來自多個管道 (包括線上、離線、CRM 和協力廠商) 的資料，全面瞭解每個客戶。 **輪廓**&#x200B;可讓您將客戶資料合併成統一的檢視畫面，針對每個客戶互動提供可採取行動且附有時間戳記的說明。

➡️ [在影片中探索此功能](#video)

**即時客戶設定檔{&#x200B;1} — 將來自線上、離線和假名的客戶屬性和事件整合到單一整合的設定檔中。使&#x200B;用設定檔在多個接觸點之間提供個人化的即時體驗，藉此吸引客戶。&#x200B;URL**

**資料擷取** — 連線至各種資料來源，以擷取行為、異動、財務和營運資料。 即時或透過批次上傳擷取資料，以持續更新設定檔。 設定檔不會直接在[!DNL Journey Optimizer]介面中建立 — 系統會在擷取資料時，在Adobe Experience Platform中自動建立或更新設定檔。

>[!NOTE]
>
>擷取資料時，電子郵件區分大小寫。 這意味著可能會建立重複的輪廓 (例如，John.Greene@luma.com 是一個輪廓、john.greene@luma.com 是另一個輪廓)，並在您的 [!DNL Journey Optimizer] 歷程和行銷活動中定位對應的收件者時使用。

**身分圖表** — 使用客戶身分結合來自不同來源的資料，例如忠誠度識別碼或CRM系統ID。透過&#x200B;對應品牌資料集中不同身分之間的關聯性，建立客戶的完整檢視。&#x200B;URL

**客戶參與度** — 使用即時客戶設定檔來提供情境式個人化體驗，例如鎖定目標的選件和訊息。透過各種管道與客&#x200B;戶互動，包括行銷活動、客戶支援和交易更新。&#x200B;URL

**資料共用** — 與Amazon Web Services、Microsoft Azure和Google Cloud等頂級雲端儲存提供者共用客戶設定檔。 使用共用的設定檔，透過商業智慧工具進行報告、資料封存或更深入的分析。

>[!MORELIKETHIS]
>
>* [開始使用 Journey Optimizer 的資料管理](../data/gs-data.md)
>* [即時客戶輪廓文件](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=zh-Hant){target="_blank"}
>* [即時客戶個人檔案資料和細分的預設護欄](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/guardrails){target="_blank"}
>* {&#x200B;0}資料擷取檔案](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/home){target="_blank"}[

## 設定檔儀表板

若要存取設定檔，請導覽至左側導覽窗格中的&#x200B;**[!UICONTROL 客戶]** / **[!UICONTROL 設定檔]**&#x200B;功能表。

>[!NOTE]
>
>如果貴組織是初次使用 [!DNL Adobe Journey Optimizer]，且尚未建立作用中的輪廓資料集或合併原則，則&#x200B;**輪廓**&#x200B;儀表板不可見。 **總覽**&#x200B;標籤會顯示Adobe Experience Platform檔案的連結，以協助您開始使用即時客戶個人檔案。 若要瞭解如何使用&#x200B;**設定檔儀表板**，以及有關儀表板中顯示之量度的詳細資訊，請參閱[本節](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hant){target="_blank"}。

您可以將多個來源的資料片段放在一起，然後組合這些片段，即可檢視每個個別客戶的完整檢視。 彙總此資料時，合併原則是用來判斷資料優先順序的方式以及合併哪些資料以建立統一檢視的規則。 在此[檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hant){target="_blank"}中進一步瞭解&#x200B;**合併原則**。

![](assets/profiles-home.png)

## 作法影片 {#video}

瞭解Adobe Experience Platform如何組合和更新即時客戶設定檔，以及如何存取和使用這些設定檔。

>[!VIDEO](https://video.tv.adobe.com/v/27251?quality=12)
