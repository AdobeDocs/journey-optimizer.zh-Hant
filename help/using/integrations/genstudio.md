---
solution: Journey Optimizer
product: journey optimizer
title: 在Journey Optimizer中使用GenStudio for Performance Marketing
description: 瞭解如何在Journey Optimizer中使用GenStudio for Performance Marketing
feature: Content Assistant, Integrations
topic: Content Management, Artificial Intelligence
badge: label="有限可用性" type="Informative"
role: User
level: Beginner, Intermediate
exl-id: c22a44a8-e4e2-453a-9ca2-b80f7c0edc19
source-git-commit: 784f1fbfbf2cfa73666bdc943fc30028c9dc913c
workflow-type: tm+mt
source-wordcount: '1254'
ht-degree: 9%

---

# 使用 GenStudio for Performance Marketing {#ajo-genstudio}

>[!CONTEXTUALHELP]
>id="ajo_genstudio_button"
>title="使用以 GenStudio 建置的範本"
>abstract="由於與 Adobe GenStudio for Performance Marketing 緊密整合，您可以輕鬆匯入透過 Adobe AI 技術增強的 GenStudio 範本。"

## 開始使用GenStudio {#gs-genstudio}

[Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/home){target="_blank"}是創作AI優先的應用程式，可讓行銷團隊建立自己的廣告和電子郵件，以推動具影響力、個人化的行銷活動，符合您的品牌標準並遵守您的企業政策。 透過運用Adobe AI技術，提供一套完整的工具，可簡化內容建立及管理的複雜性，讓創意人員可專注在創新上。

>[!AVAILABILITY]
>
>* [!DNL Adobe Journey Optimizer] 的 GenStudio 整合目前無法搭配 **Healthcare Shield** 或 **Privacy and Security Shield** 附加元件方案使用。
>
>* 此功能僅適用於電子郵件頻道。

若要提升行銷效率並維持品牌一致性，您可以將&#x200B;[!DNL **GenStudio for Performance Marketing**]&#x200B;體驗與&#x200B;[!DNL **Adobe Journey Optimizer**]&#x200B;緊密整合。 這可讓您運用[!DNL GenStudio]的AI支援內容建立以及[!DNL Journey Optimizer]的進階協調功能。

![將GenStudio內容匯入Adobe Journey Optimizer](../rn/assets/do-not-localize/genstudio.gif)

>[!INFO]
>
>若要更進一步，請檢視此[總覽](https://business.adobe.com/tw/products/genstudio-for-performance-marketing.html#watch-overview){target="_blank"}以及[的](https://business.adobe.com/tw/products/genstudio-for-performance-marketing.html#demo){target="_blank"}示範[!DNL Adobe GenStudio for Performance Marketing]。

➡️ [在影片中探索此功能](#video)

## 先決條件 {#genstudio-prerequisites}

若要使用[!DNL GenStudio for Performance Marketing]與[!DNL Journey Optimizer]的整合，請確定符合下列需求：

* 您的組織必須有[!DNL GenStudio for Performance Marketing]的有效授權。

* [!DNL GenStudio for Performance Marketing]和[!DNL Adobe Journey Optimizer]都必須屬於相同的IMS組織。

* 使用者必須在&#x200B;**中至少擁有** Collaborator[!DNL GenStudio for Performance Marketing]角色或以上角色，才能使用整合功能。 [進一步瞭解GenStudio中的使用者角色](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/intro/user-roles){target="_blank"}

<!--To access the GenStudio integration in [!DNL Adobe Journey Optimizer] feature, users need to be granted the **xxx** permission. [Learn more](../administration/permissions.md)

>[!IMPORTANT]
>
>* Before starting using this capability, read out related [Guardrails and Limitations](#generative-guardrails).-->

<!--Guardrails and limitations {#genstudio-guardrails}

General guidelines for using the GenStudio integration in [!DNL Adobe Journey Optimizer] for email generation are listed below:

See if guidelines/limitations such as the ones listed [here](../content-management/gs-generative.md#generative-guardrails) for AI Assistant can apply.

The following limitations apply to GenStudio integration in [!DNL Adobe Journey Optimizer]:-->

## 在Journey Optimizer中運用GenStudio功能 {#use-genstudio}

[!DNL GenStudio for Performance Marketing]與[!DNL Journey Optimizer]整合可讓您公司的行銷人員更有效地合作，以簡化程式。

例如，使用[!DNL Journey Optimizer]開發和自動化電子郵件行銷活動的技術行銷人員，可以與使用[!DNL GenStudio]建立內容的效能行銷人員共同作業。

透過這項整合，兩者可以共同作業，輕鬆地將[!DNL GenStudio]中的品牌上內容整合到[!DNL Journey Optimizer]中，傳遞吸引人的電子郵件，以鎖定特定客戶細分並提升銷售量。

### 主要功能 {#genstudio-capabilities}

這項整合為您的行銷組織開啟了強大的功能：

* **由AI支援的內容產生**：運用Adobe的創作AI，以智慧型複製建議和設計元素有效率地建立多個品牌內電子郵件變體。

* **順暢的工作流程整合**：將Journey Optimizer電子郵件範本匯出至GenStudio、建立具有AI提示的變體，並以簡化的程式將其匯入回Journey Optimizer。

* **集中式資產管理**：存取GenStudio的ContentHub (由Adobe Experience Manager Assets提供技術支援)，在一個集中式位置組織、儲存和擷取所有數位資產。

* **內容實驗**：將多個GenStudio電子郵件變數匯入至Journey Optimizer，並利用實驗功能來測試及識別表現最佳的內容。

* **效能導向型深入分析**：使用AI支援的分析追蹤行銷活動績效，以瞭解哪些創意元素會與您的對象產生共鳴，並最佳化未來的行銷活動。

### 常見使用實例 {#genstudio-use-cases}

[!DNL GenStudio for Performance Marketing]與之間的整合
Journey Optimizer&rbrack;支援各種行銷情境：

* **產品上市行銷活動**：快速產生產品公告的多個電子郵件變體，以不同的對象區段進行測試，並在您的客戶群中擴充成功版本。

* **節日和季節性促銷活動**：使用GenStudio範本大規模產生時效性強的促銷活動內容，確保在緊迫期限內保持品牌一致性。

* **大規模A/B測試**：在GenStudio中建立許多內容變異，並在Journey Optimizer中系統地測試這些變異，以持續改善電子郵件效能。

* **多區段個人化**：在GenStudio中產生不同客戶角色的量身打造內容，然後將每個變數部署至Journey Optimizer中的對應區段，以發揮最大關聯性。

## 使用GenStudio整合 {#how-to-use}

整合工作流程包含兩個主要步驟：將範本從Journey Optimizer匯出至GenStudio，以及將GenStudio體驗匯入回Journey Optimizer。

### 將HTML範本從Journey Optimizer匯出至GenStudio {#export-from-ajo-to-genstudio}

首先，將包含您品牌指引的[!DNL Journey Optimizer] HTML範本匯出至[!DNL GenStudio for Performance Marketing]。 請遵循下列步驟。

1. 在[!DNL Journey Optimizer]中，存取歷程或行銷活動中的電子郵件內容。 [了解作法](../email/get-started-email-design.md#key-steps)

1. 在電子郵件Designer中，從&#x200B;**[!UICONTROL 更多]**&#x200B;按鈕中選取&#x200B;**[!UICONTROL 匯出HTML]**。

   ![](assets/genstudio-export-template.png){zoomable="yes"}

1. 將此HTML匯出的範本上傳至[!DNL GenStudio for Performance Marketing]。<!--Make sure you detect the fields that the generative AI uses to insert content in order to create an actionable template.-->

   >[!NOTE]
   >
   >在[!DNL GenStudio]HTML使用手冊[專屬區段中，瞭解如何將Adobe GenStudio for Performance Marketing範本上傳至](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#templates-from-ajo-and-marketo){target="_blank"}。

1. 在GenStudio中，使用此範本建立具有AI提示的多個電子郵件變體並儲存。

   >[!NOTE]
   >
   >瞭解如何在GenStudio專屬的[區段](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience){target="_blank"}中建立電子郵件體驗。

### 在Journey Optimizer中善用GenStudio體驗 {#leverage-genstudio-experiences}

在GenStudio中建立電子郵件變數後，請將它們匯入回[!DNL Journey Optimizer]以用於您的行銷活動。 請遵循下列步驟。

1. 在[!DNL Journey Optimizer]中，[新增電子郵件](../email/create-email.md)至行銷活動。

1. 從行銷活動設定畫面，瀏覽[編輯內容畫面](../email/create-email.md#define-email-content)，然後按一下&#x200B;**[!UICONTROL 編輯電子郵件內文]**&#x200B;以開啟電子郵件Designer。 [了解作法](../email/get-started-email-design.md#key-steps)

1. 在電子郵件Designer首頁上，選取&#x200B;**[!UICONTROL 匯入HTML]**，然後按一下&#x200B;**[!UICONTROL Adobe GenStudio for Performance Marketing]**&#x200B;按鈕。

   ![](assets/genstudio-pem-import-email.png){zoomable="yes"}

1. 瀏覽GenStudio體驗以開始建立您的內容。 您可以根據數個條件篩選體驗，例如產品、角色、品牌或甚至顏色。

   <!--![](assets/genstudio-filter-experiences.png){zoomable="yes"}-->

1. 選取體驗並按一下&#x200B;**[!UICONTROL 使用]**。

   ![](assets/genstudio-use-experience.png){zoomable="yes"}

1. 選取您要匯入GenStudio體驗的資料夾。

   ![](assets/genstudio-choose-destination.png){zoomable="yes"}

1. 選取的內容會顯示在電子郵件Designer中。

   ![](assets/genstudio-email-content.png){zoomable="yes"}

   >[!NOTE]
   >
   >從[範本 [!DNL Journey Optimizer] 建立的GenStudio體驗](#export-from-ajo-to-genstudio)會直接匯入具有完整編輯功能的電子郵件Designer。 未使用[!DNL Journey Optimizer]範本建立的GenStudio體驗已匯入至[相容性模式](../email/existing-content.md)，其編輯功能可能受限。

1. 使用[電子郵件內容編輯工具](../email/content-from-scratch.md)和[個人化欄位](../personalization/personalize.md)，視需要編輯您的電子郵件。 儲存您的內容。

1. 返回行銷活動摘要頁面，然後按一下&#x200B;**[!UICONTROL 建立實驗]**&#x200B;以使用實驗。 [瞭解如何建立內容實驗](../content-management/content-experiment.md)

   <!--![](assets/genstudio-create-experiment.png){zoomable="yes"}-->

1. 建立數個處理並重複上述步驟，以匯入並快速運用您在[!DNL GenStudio]中建立的其他電子郵件體驗變數。

   ![](assets/genstudio-define-treatments.png){zoomable="yes"}

1. 儲存您的變更並[啟動](../campaigns/review-activate-campaign.md)行銷活動。

1. 執行實驗後，透過[實驗行銷活動報告](../reports/campaign-global-report-cja-experimentation.md)追蹤行銷活動處理的成效。 然後，您可以解譯實驗的結果。 [了解作法](../content-management/get-started-experiment.md#interpret-results)

## 常見問題 {#genstudio-faq}

尋找有關[!DNL GenStudio for Performance Marketing]與[!DNL Journey Optimizer]整合的常見問題解答。

+++我可以將GenStudio整合用於電子郵件以外的管道嗎？

目前，[!DNL GenStudio for Performance Marketing]整合僅適用於電子郵件頻道。 未來版本可能會新增對其他頻道的支援。
+++

+++GenStudio整合是否適用於所有Journey Optimizer客戶？

使用&#x200B;**Healthcare Shield**&#x200B;或&#x200B;**Privacy and Security Shield**&#x200B;附加元件產品的組織目前無法進行整合。
+++

+++我可以在將GenStudio內容匯入Journey Optimizer後對其進行編輯嗎？

可以，將GenStudio體驗匯入[!DNL Journey Optimizer]之後，您可以使用電子郵件Designer的[內容編輯工具](../email/content-from-scratch.md)並新增[個人化欄位](../personalization/personalize.md)，以進一步自訂您的電子郵件內容。
+++

+++在沒有GenStudio範本的情況下建立的Journey Optimizer體驗有什麼改變？

從[!DNL Journey Optimizer]範本建立的GenStudio體驗會直接匯入電子郵件Designer。 未使用[!DNL Journey Optimizer]範本建立的GenStudio體驗已匯入至[相容性模式](../email/existing-content.md)。
+++

+++我可以在Journey Optimizer中測試多個GenStudio電子郵件變數嗎？

是的，您可以匯入不同的GenStudio電子郵件變數來建立數個內容處理，並使用Journey Optimizer的[內容實驗](../content-management/content-experiment.md)功能來測試哪些變數對您的對象執行時效果最佳。
+++

+++GenStudio如何確保品牌一致性？

GenStudio使用AI支援的品牌檢查，確保所有產生的內容都符合您的品牌標準和准則。 上傳包含您品牌元素的範本時，GenStudio會將這些標準套用至平台內建立的所有內容變數。
+++

+++我可以與其他團隊成員在GenStudio體驗上共同作業嗎？

是，GenStudio是專為共同作業所設計。 具有適當許可權的多個團隊成員可以一起建立和修訂電子郵件體驗，然後再將其匯入[!DNL Journey Optimizer]。
+++

## 作法影片 {#video}

了解將電子郵件範本從 Journey Optimizer 匯出至 GenStudio 進行績效行銷的過程、使用GenStudio 範本製作符合品牌要求的電子郵件，然後順暢地將其匯回 Journey Optimizer。

>[!VIDEO](https://video.tv.adobe.com/v/3456060/?captions=chi_hant&quality=12)