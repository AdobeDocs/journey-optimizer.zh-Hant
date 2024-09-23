---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform 資料來源
description: 瞭解如何設定Adobe Experience Platform資料來源
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: 內建，來源，資料，平台，整合
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: e45ec5f0e1bbcc73892f9cde5923627886f44ef6
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 31%

---

# Adobe Experience Platform 資料來源 {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Adobe Experience Platform 資料來源"
>abstract="Adobe Experience Platform 資料來源會定義和 Adobe 即時客戶輪廓的連線。此資料來源是內建和預先設定的，並無法刪除。它旨在從即時客戶輪廓服務中擷取和使用資料 (例如，檢查進入歷程的人是否為女性)。它可讓您使用輪廓資料和體驗事件資料。"

Adobe Experience Platform 資料來源會定義和 Adobe 即時客戶輪廓的連線。此資料來源是內建和預先設定的，並無法刪除。此資料來源旨在擷取及使用即時客戶個人檔案服務的資料（例如，檢查進入歷程的人員是否為女性）。 其可讓您使用個人檔資料與體驗事件資料。 如需Adobe即時客戶個人檔案的詳細資訊，請參閱[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}。

若要允許連線到即時客戶個人檔案服務，我們必須使用金鑰來識別人員，並使用名稱空間將金鑰內容化。 因此，如果您的歷程以包含索引鍵和名稱空間的事件開始，您只能使用此資料來源。 [了解更多](../building-journeys/journey.md)。

您可以編輯名為「ProfileFieldGroup」的預先設定欄位群組、新增欄位群組，以及移除未用於任何草稿或即時歷程的欄位群組。 [了解更多](../datasource/configure-data-sources.md#define-field-groups)。

>[!NOTE]
>
>您可以擷取不到一年前建立的1000個最新體驗事件。

以下是新增欄位群組至內建資料來源的主要步驟。

1. 從資料來源清單中，選取內建的Adobe Experience Platform資料來源。

   這會開啟畫面右側的資料來源設定窗格。

   ![](assets/journey23.png)

1. 按一下&#x200B;**[!UICONTROL 新增欄位群組]**&#x200B;以定義要擷取的新欄位系列。 [了解更多](../datasource/configure-data-sources.md#define-field-groups)。

   ![](assets/journey24.png)

1. 從&#x200B;**[!UICONTROL 結構描述]**&#x200B;下拉式清單中選取結構描述。 此欄位列出Adobe Experience Platform中可用的設定檔和體驗事件結構。 未在[!DNL Journey Optimizer]中執行結構描述建立。 在Adobe Experience Platform中執行。
1. 選取您要使用的欄位。
1. 按一下&#x200B;**[!UICONTROL 儲存]**。

將游標放在欄位群組的名稱上時，您會在右側看到兩個圖示。 它們可讓您刪除和複製欄位群組。 請注意，欄位群組未用於任何即時或草稿歷程時（**[!UICONTROL 用於]**&#x200B;欄位中顯示的資訊），才可使用&#x200B;**[!UICONTROL 刪除]**&#x200B;圖示。
