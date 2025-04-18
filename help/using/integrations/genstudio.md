---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用GenStudio與Journey Optimizer的整合
description: 瞭解如何在Journey Optimizer中使用GenStudio
feature: Content Assistant, Integrations
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
exl-id: c22a44a8-e4e2-453a-9ca2-b80f7c0edc19
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 8%

---

# 開始使用 GenStudio 整合 {#gs-genstudio}

>[!CONTEXTUALHELP]
>id="ajo_genstudio_button"
>title="使用以 GenStudio 建置的範本"
>abstract="由於與 Adobe GenStudio for Performance Marketing 緊密整合，您可以輕鬆匯入透過 Adobe AI 技術增強的 GenStudio 範本。"

>[!AVAILABILITY]
>
>[!DNL Adobe Journey Optimizer]中的GenStudio整合目前無法搭配&#x200B;**Healthcare Shield**&#x200B;或&#x200B;**Privacy and Security Shield**&#x200B;附加元件方案使用。
>
>此功能僅適用於電子郵件通道。

[Adobe GenStudio for Performance Marketing](https://business.adobe.com/products/genstudio-for-performance-marketing.html){target="_blank"}是創作AI優先的應用程式，可讓行銷團隊建立自己的廣告和電子郵件，以推動符合您品牌標準並符合您企業政策的、具影響力的個人化行銷活動。 透過運用Adobe AI技術，提供一套完整的工具，可簡化內容建立及管理的複雜性，讓創意人員可專注在創新上。

在專屬的[檔案](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/home){target="_blank"}中進一步瞭解[!DNL GenStudio for Performance Marketing]。

>[!INFO]
>
>若要更進一步，請查閱此[總覽](https://business.adobe.com/products/genstudio-for-performance-marketing.html#watch-overview){target="_blank"}和[!DNL Adobe GenStudio for Performance Marketing]的[示範](https://business.adobe.com/products/genstudio-for-performance-marketing.html#demo){target="_blank"}。

<!--To access the GenStudio integration in [!DNL Adobe Journey Optimizer] feature, users need to be granted the **xxx** permission. [Learn more](../administration/permissions.md)

>[!IMPORTANT]
>
>* Before starting using this capability, read out related [Guardrails and Limitations](#generative-guardrails).-->

若要提升行銷效率並維持品牌一致性，您可以將&#x200B;[!DNL **GenStudio for Performance Marketing**]&#x200B;體驗與&#x200B;[!DNL **Adobe Journey Optimizer**]&#x200B;緊密整合。 這可讓您運用[!DNL GenStudio]的AI支援內容建立以及[!DNL Journey Optimizer]的進階協調功能。

<!--![](../rn/assets/do-not-localize/genstudio.gif)-->

<!--Guardrails and limitations {#genstudio-guardrails}

General guidelines for using the GenStudio integration in [!DNL Adobe Journey Optimizer] for email generation are listed below:

See if guidelines/limitations such as the ones listed [here](gs-generative.md#generative-guardrails) for the AI Assistant can apply.

The following limitations apply to GenStudio integration in [!DNL Adobe Journey Optimizer]:-->

## 利用Journey Optimizer中的GenStudio功能 {#use-genstudio}

[!DNL GenStudio for Performance Marketing]與[!DNL Journey Optimizer]整合可讓您公司的行銷人員更有效地合作，以簡化程式。

例如，使用[!DNL Journey Optimizer]開發和自動化電子郵件行銷活動的技術行銷人員，可以與使用[!DNL GenStudio]建立內容的效能行銷人員共同作業。

透過這項整合，兩者可以共同作業，輕鬆地將[!DNL GenStudio]中的品牌上內容整合到[!DNL Journey Optimizer]中，傳遞吸引人的電子郵件，以鎖定特定客戶細分並提升銷售量。

### 將HTML範本從Journey Optimizer匯出至GenStudio {#export-from-ajo-to-genstudio}

首先，您可以將包含品牌指引的[!DNL Journey Optimizer] HTML範本匯出至[!DNL GenStudio for Performance Marketing]。 請遵循下列步驟。

1. 在[!DNL Journey Optimizer]中，存取歷程或行銷活動中的電子郵件內容。 [了解作法](../email/get-started-email-design.md#key-steps)

1. 在電子郵件Designer中，從&#x200B;**[!UICONTROL 更多]**&#x200B;按鈕中選取&#x200B;**[!UICONTROL 匯出HTML]**。

   ![](assets/genstudio-export-template.png){zoomable="yes"}

1. 將此HTML匯出的範本上傳至[!DNL GenStudio for Performance Marketing]。<!--Make sure you detect the fields that the generative AI uses to insert content in order to create an actionable template.-->

   >[!NOTE]
   >
   >在[HTML使用手冊](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#templates-from-ajo-and-marketo){target="_blank"}專屬區段中，瞭解如何將Adobe GenStudio for Performance Marketing範本上傳至[!DNL GenStudio]。

1. 在GenStudio中，使用此範本建立具有AI提示的多個電子郵件變體並儲存。

   >[!NOTE]
   >
   >瞭解如何在GenStudio專屬的[區段](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience){target="_blank"}中建立電子郵件體驗。

### 在Journey Optimizer中善用GenStudio體驗 {#leverage-genstudio-experiences}

若要運用您剛才建立的[!DNL GenStudio]電子郵件變數（透過將其匯入[!DNL Journey Optimizer]中），請遵循下列步驟。

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
   >從 [!DNL Journey Optimizer] 範本](#export-from-ajo-to-genstudio)建立的GenStudio體驗[會直接匯入電子郵件Designer。 未使用[!DNL Journey Optimizer]範本建立的GenStudio體驗已匯入至[相容性模式](../email/existing-content.md)。

   使用[電子郵件內容編輯工具](../email/content-from-scratch.md)和[個人化欄位](../personalization/personalize.md)，依需要編輯您的電子郵件。 儲存您的內容。

1. 返回行銷活動摘要頁面，然後按一下&#x200B;**[!UICONTROL 建立實驗]**&#x200B;以使用實驗。 [瞭解如何建立內容實驗](../content-management/content-experiment.md)

   <!--![](assets/genstudio-create-experiment.png){zoomable="yes"}-->

1. 建立數個處理並重複上述步驟，以匯入並快速運用您在[!DNL GenStudio]中建立的其他電子郵件體驗變數。

   ![](assets/genstudio-define-treatments.png){zoomable="yes"}

1. 儲存您的變更並[啟動](../campaigns/review-activate-campaign.md)行銷活動。

執行實驗後，透過[實驗行銷活動報告](../reports/campaign-global-report-cja-experimentation.md)追蹤行銷活動處理的成效。 然後，您可以解譯實驗的結果。 [了解作法](../content-management/get-started-experiment.md#interpret-results)
