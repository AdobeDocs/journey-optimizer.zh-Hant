---
solution: Journey Optimizer
product: journey optimizer
title: 與 Intelligent Services 整合
description: 瞭解如何在Journey Optimizer中善用Adobe Intelligent Services和Customer AI預測
feature: Journeys, Integrations
topic: Artificial Intelligence
role: User
level: Intermediate
keywords: 人工， AI，智慧，歷程，服務
exl-id: 20da09e1-0611-4d27-a589-30552011e06c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/rTKcWHwfwleQtD68fcdeqYK2AMQHVaknKtsNDFsOldI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eb30f47f-d87a-400f-8f78-63ce7979ff56
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 669
ht-degree: 0%

---

# 與智慧型服務整合 {#ai-overview}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何將Adobe Intelligent Services和Customer AI預測與Journey Optimizer整合，以將流失和轉換分數作為個人資料屬性用於決策、動作和區段建置。

>[!ENDSHADEBOX]

與&#x200B;**[!DNL Adobe Intelligent Services]**&#x200B;的整合可讓您針對客戶體驗使用案例運用人工智慧和機器學習。 這可讓行銷分析人員使用商業層級設定，針對公司需求設定量身打造的預測，而不需要資料科學的專業知識。

以[!DNL Adobe Experience Platform]為基礎的[!DNL Intelligent Services]可提供客戶體驗團隊的AI-as-a-service。 它有助於預測客戶行為、衡量行銷活動影響以及改善投資報酬率。 如需詳細資訊，請參閱[[!DNL Adobe Experience Platform] 檔案](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/home.html){target="_blank"}。

[!DNL Journey Optimizer]與[!DNL Intelligent Services]之間的整合可讓您運用客戶預測。

[!DNL Adobe Intelligent Services]的元件Customer AI會預測可能的客戶動作。 請參閱[[!DNL Adobe Experience Platform] 檔案](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/customer-ai/overview.html){target="_blank"}。

Customer AI可讓品牌建立流失率或轉換機器學習型分數。 這些分數可在[!DNL Adobe Experience Platform]個設定檔（即時客戶設定檔）中作為設定檔屬性使用。

因此，這些屬性可以像在Journey Optimizer中的任何其他設定檔屬性一樣使用。 在用於決策、動作或建立區段的條件中使用它們。

![顯示傾向分數和預測的Customer AI整合](assets/customer-ai.png)

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

- **TL；DR：**&#x200B;本頁說明Journey Optimizer如何與Adobe Intelligent Services （尤其是Customer AI）整合，以將機器學習型傾向分數作為歷程中的設定檔屬性。

**意圖：**
- 瞭解Adobe Intelligent Services如何與Journey Optimizer整合
- 使用Customer AI傾向分數作為歷程條件或動作中的個人檔案屬性
- 啟用AI驅動的流失或轉換預測，而不需要資料科學的專業知識
- 套用機器學習分數至Journey Optimizer中的區段建置

**字彙表：**
- **Adobe Intelligent Services**：以Adobe Experience Platform為基礎的AI/ML服務套裝，可提供客戶體驗預測，而不需要資料科學專業知識&#x200B;*（產品專屬）*
- **Customer AI**： Adobe Intelligent Services的元件，可針對客戶設定檔&#x200B;*（產品特定）*&#x200B;產生機器學習型流失或轉換傾向分數
- **傾向分數**：機器學習型分數，代表客戶執行特定動作（例如，流失或轉換）的可能性，儲存為設定檔屬性&#x200B;*（產品特定）*

**護欄：**
- 不需要資料科學專業知識，但業務層級設定必須由行銷分析師完成
- Customer AI分數必須先在Adobe Experience Platform中設定，才能在Journey Optimizer中作為設定檔屬性使用

**術語：**
- 正式名稱：Adobe Intelligent Services — 縮寫：none — 變體：Intelligent Services、AI服務
- 正式名稱：Customer AI — 首字母縮寫：none — 變體：Customer AI分數、傾向分數
- 同義字：「流失分數」=「流失傾向」；「轉換分數」=「轉換傾向」
- 請勿混淆：「Adobe Intelligent Services」≠「AI Assistant」（Intelligent Services是預測性ML平台；AI Assistant是對話介面）

**常見問題集：**
- **問：什麼是Journey Optimizer內容中的Customer AI？** — Customer AI是Adobe Intelligent Services元件，可建立機器學習型流失或轉換分數，這些分數可用作Journey Optimizer條件、動作和區段建立中的設定檔屬性。
- **問：要使用Adobe Intelligent Services，是否需要資料科學技能？**  — 不行，行銷分析人員可使用業務層級設定來設定預測，而不需要資料科學的專業知識。
- **問：Customer AI分數會儲存在哪裡？**  — 它們會儲存為Adobe Experience Platform即時客戶設定檔中的設定檔屬性，可供Journey Optimizer中的任何其他設定檔屬性一樣存取。
- **問：如何在歷程中使用Customer AI分數？**  — 一旦可作為設定檔屬性使用，該分數即可用於決策、動作設定或建立受眾區段的條件。

+++
